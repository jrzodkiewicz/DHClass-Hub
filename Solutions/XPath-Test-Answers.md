## XPath Exam Solutions ##

**Q1.** //div[@type='book'][2]//p[persName][placeName] 127 Results

**Q2.** distinct-values(//div[@type='book'][2]//placeName) 293 Results

**Q3.** string-join(distinct-values(//div[@type='book'][2]//placeName), ";")

**Q4.** //p/placeName[contains(.,"Taheitee")] 198 Results

**BONUS**

Shortest:  
(distinct-values(//p/placeName[contains(.,"Taheitee")]/string-length()))
*You get 5 results: 8, 10, 16, 15, 14*

min(//p/placeName[contains(.,"Taheitee")]/string-length())  
*You get Taheitee with 8 characters*

//p/placeName[contains(.,"Taheitee")][string-length()= min(//p/placeName[contains(.,"Taheitee")]/string-length())]   
*If you wanted to take it further and get the XPath location of all the shortest you would do this expression with 173 Results, all spelled Taheitee*

Longest:  
(distinct-values(//p/placeName[contains(.,"Taheitee")]/string-length()))   
*You get 5 results: 8, 10, 16, 15, 14*

max(//p/placeName[contains(.,"Taheitee")]/string-length())   
*You get a result with 16 characters*

//p/placeName[contains(.,"Taheitee")][string-length()= min(//p/placeName[contains(.,"Taheitee")]/string-length())]   
*If you wanted to take it further and get the XPath location of all the longest, you would do this expression with 1 Result: spelled O-Taheitee-eetee*


