![Lab title](image.png) 

Lab: DOM XSS in innerHTML sink using source location.search

Solution: 
    

    1. Enter the following into the into the search box:
    <img src=1 onerror=alert(1)>
    
    2. Click "Search".

    The value of the src attribute is invalid and throws an error. This triggers the onerror event handler, which then calls the alert() function. As a result, the payload is executed whenever the user's browser attempts to load the page containing your malicious post.

![Solved](image-1.png)  
