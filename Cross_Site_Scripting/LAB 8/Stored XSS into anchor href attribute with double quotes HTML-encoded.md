![Solved](image.png)

Lab: Stored XSS into anchor href attribute with double quotes HTML-encoded

Solution: 

    1. Post a comment with a random alphanumeric string in the "Website" input, then use Burp Suite to intercept the request and send it to Burp Repeater.
    
    2. Make a second request in the browser to view the post and use Burp Suite to intercept the request and send it to Burp Repeater.
    
    3. Observe that the random string in the second Repeater tab has been reflected inside an anchor href attribute.

    4. Repeat the process again but this time replace your input with the following payload to inject a JavaScript URL that calls alert:
    javascript:alert(1)
    
    5. Verify the technique worked by right-clicking, selecting "Copy URL", and pasting the URL in the browser. Clicking the name above your comment should trigger an alert.

![Solved](image-1.png)