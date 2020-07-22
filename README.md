# testSearchKeyword
These scripts do a simple functional test and load test to duckduckgo search box, with pytest,selenium and locust.



# environment and prerequisites:
	
	Ubuntu 20.04 
	pytest 5.4.3
	pytest-html-2.1.1
	geckodriver 0.26.0
	Selenium server 3.141.59
	locust 1.1.1
 	fake-headers 1.0.2


# description and usage:

    By run_jmeter.sh, you can run a non-GUI mode jmeter script(allwebtest.jmx).
	$sh ./run_allwebtest.sh


    The whole test list :

![](https://github.com/k-eeer/jmetertest/blob/master/illustration/testStructure.png)

and detail description of those tests are in ./illustration folder.


    It'll generate a result as .jtl file. You  can view it in  chart or graph  with jmeter  GUI listeners.

![](https://github.com/k-eeer/jmetertest/blob/master/illustration/sumReport.png)

![](https://github.com/k-eeer/jmetertest/blob/master/illustration/resultGraph.png)



    You also can have a quick check those tests (stress test is not included)  are success or not.

    $less quickChecResult.txt

![](https://github.com/k-eeer/jmetertest/blob/master/illustration/quickCheckResult.png)
