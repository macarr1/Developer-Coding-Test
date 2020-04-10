1.	
I spent around 3 hours on this coding test. The bulk of my time was spent trying to figure out the logic behind printing all results 
from every possible page. If I were to put more time into the test I would focus on improving a few things. First of all, I would 
create a CSS stylesheet or just manually add some styling into the HTML file to improve the look of the application. In its current 
state, the layout is extremely basic without much appeal to it. Secondly, I tried putting the restaurant update code and HTML table 
entries in another function but found that this slowed down performance and caused other issues, such as improper ordering of results. 
I would work harder to find a way to not use this code repeatedly in the program as that is generally considered bad practice. Another 
thing I would improve would be the way the HTTP request is handled when it is returned. Currently, the fetch requests are loaded 
dynamically and while they all are eventually accepted and read by the application, if a city has a high number of pages of the API to 
be returned the order that it reads these pages becomes jumbled. I am aware of what an async function and corresponding await calls 
are, but after spending around 15-20 minutes trying to implement this I was unable to return the pages in order. With more time, I 
would research how to do this properly so that results in the application would appear in the same order as in the API.

2.	
After first using a HTTP GET response, I realized that I could use a fetch call to return the API JSON as an object. Fetch was used a 
couple times in the program and was extremely useful. 
fetch(api_url).then((response) => {
      return response.json();
    })
            .then((data) => {
				// return and handle data
			});
It allowed me to easily access any data point from each restaurant in the for loops, which meant I did not have to parse large 
strings of text for certain keywords.

3.	
I would track down a performance issue by first fully acquainting myself with an application by running it in its entirety. If 
available, I would open up an application on the side like Task Manager, or some sort of resource monitoring tool. I would then make 
note of the areas of the application that took a significant time to load or which created spikes in CPU, GPU, memory, or disk drive 
usage. I would find the points in the code that are causing these slowdowns or resource usage spikes, and begin debugging the code 
line by line to find out if there are unnecessary loops or unnecessary code in general that would be causing issues. I would use 
console.log to print out variables that I needed to learn more about to diagnose the performance issue. In my recent degree project, 
there was a major performance issue where the queries made to the Firebase would quite often exceed the daily quota since we were 
inefficiently calling for data from the Firebase. Tracking down this performance issue was done in the same fashion mentioned above. 
Since the load times in the application were clearly longer than they needed to be and we would eventually receive an error message 
that our free Firebase account had reached its maximum query number for the day, we eventually narrowed the issue down to some 
inefficient for loops which were reading too much data unnecessarily. 

4.	
I would improve the API by not having the restaurant information split across multiple pages. This way, I would only need one for loop 
to print all information returned from the API. However, I am sure solving this issue was one focus point of this test. When the API was used with 
fetch, I found that there were no glaring issues. The data was organized neatly in the objects and if I were to combine this API with another API such 
as Google Maps, I could very easily pull the latitude and longitude information to plot markers of the restaurants, while also having an abundance of 
information to fill the marker's information tab with.

5.	
{
	program: “software engineering”, 
	eager_to_learn: true, 
	favourite_sports: [basketball, baseball], 
	favourite_website: http://nationalgeographic.com, 
	motto: “treat others the way you want to be treated” 
}
