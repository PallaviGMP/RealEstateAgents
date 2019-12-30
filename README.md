# RealEstateAgents
mvc solution to get real estate agent names

Manual:
1. Clone this https://github.com/PallaviGMP/RealEstateAgents.git to your local machine
2. Clone https://github.com/PallaviGMP/RealEstateAgents.UnitTests.git to your local
machine
3. Open the solution and run, you will get the top 10 makelaar's in Amsterdam have the
most object listed for sale- https://localhost:xxxxx/Home/GetRealEstateAgents/
4. Browse https://localhost:xxxxx/Home/GetRealEstateAgents/tuin/, you will get the top 10
makelaar's in Amsterdam have the most object with the tuin listed for sale
5. Handling too many API requests in a short period of time
I have implemented Asp.net MVC Throttling with 5 seconds duration per API request(see file
ThrottleAttribute.cs). With this implementation, the API request per user will be limited to 5
seconds(configurable) and thereby limiting the API load at the application end. However, my
proposal would be to implement resource throttling in the web API code with configurable counter
(or by implementing web api Throttling framework) if we want to limit the API request <100 per
minute.
