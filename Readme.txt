Find this repository at: https://github.com/Baxby-UM/PRA3006

This code shows an interactive phylogenetic tree of species across all marine regions that classify as vulnerable or worse based on data and species from the IUCN Redlist.
Follow these steps to get it operational.


Installing nescesarry software:
	1. Google Chrome : https://www.google.com/chrome/?brand=JJTC&ds_kid=43700052282304883&gad_source=1&gclid=CjwKCAiA9IC6BhA3EiwAsbltOEw2CM_BdX4WJ9zMpAKAwnwSWUpEw6BL2hp8SfosWEL2h10qO1IBAhoCQ_sQAvD_BwE&gclsrc=aw.ds
	2. Java : https://www.java.com/download/ie_manual.jsp
	3. Node.js : https://nodejs.org/en
	4. Blazegraph.jar : https://blazegraph.com/

Running the blazegraph server:
	1. Press Windows + R
	2. Type in "cmd"
	3. Press Enter
	4. Copy the path to the folder where you have blazegraph.jar saved
	5. Use this command in cmd with your filepath : cd "filepath"
	6. Use this command : java -server -Xmx1g -jar blazegraph.jar
	7. Go to : http://localhost:9999/blazegraph/

Uploading data to the server:
	1. Go to the "Update" window
	2. Upload "data.ttl" and execute the update
	3. Go to the "Query" window
	4. Test the database with this query : 
SELECT ?s ?p ?o
WHERE {
  ?s ?p ?o .
}
LIMIT 10

Running the http server:
	1. Run a new instance of command prompt (cmd)
	2. Use this command : npm install http-server -g
	3. Copy the filepath to where you have index.html saved
	4. Edit and use this command : cd "filepath"
	5. Use this command : http-server
	6. Go to : localhost:8080
		a. If the page opens the server is working

Running a CORS free web instance:
	1. Open Task Manager (Ctrl + Shift + Escape)
	2. Close any instances of chrome you have running
	3. Copy the filepath to where "chrome.exe" is installed
	4. Run a new instance of command prompt (cmd)
	5. Edit the filepath and username and then use this command : "filepath" --disable-web-security --user-data-dir=C:\Users\username

!!!CAUTION!!! 
	Do not open any public websites on this browser instance and after you're done testing, restart your computer for safety.
	
Now you can open the website and experiment with the phylogenetic tree.
	1. Go to localhost:8080 to open the website
