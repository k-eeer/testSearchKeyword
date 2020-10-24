# testSearchKeyword
These scripts do a simple functional test and load test to duckduckgo search box, with pytest, Selenium and Locust.



# environment and prerequisites:
	
	Ubuntu 20.04 
	pytest 5.4.3
	pytest-html-2.1.1
	geckodriver 0.26.0
	Selenium server 3.141.59
	locust 1.1.1
 	fake-headers 1.0.2


# description and usage:

    By test_web.py, you can test search box in duckduckgo.com with "panda" keyword, and gererate a html repot.
    	
	    $pytest --html=functionalTest.html
 **[the html report](https://github.com/k-eeer/testSearchKeyword/blob/master/output/functionalTest.html)**
 ![](https://github.com/k-eeer/testSearchKeyword/blob/master/output/functionalTest.png)
	
	
</br></br></br>
    
     By locustFile.py, you can do a load test on loading search result page.
    
    	$locust -f locustFile.py
		#open http://127.0.0.1:8089 and setting total number and increment per secsond of simulated users.
		
		
    It's the result of 100 users(increaseing 2 users/second).
    According to the first figure below,the server is able to handle 9 requests per second, 
    when load tested with 60 current users. In the final figure below,the median response time(yellow line) 
    is 300ms to 400ms, and 95% response time(green line) is 100ms to 200ms then. 
    
    In the first figure below,some request fails(red line) and bocome dominant when total requests per second around 60 due to Http Error 418.
    The error might be solved by providing proxy list.
    
![](https://github.com/k-eeer/testSearchKeyword/blob/master/output/totalRequestsPerSecond.png)
![](https://github.com/k-eeer/testSearchKeyword/blob/master/output/numberOfUsers.png)
![](https://github.com/k-eeer/testSearchKeyword/blob/master/output/responseTimes(ms).png)


   
