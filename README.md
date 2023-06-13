# Your basic Node.js web application built on MongoDB

Here is a very simple web "application" (just a form, really) that illustrates one of the key benefits of using MongoDB: the ability to iterate rapidly and build great apps faster. The scneario is immaterial, but if you want one, let's say you're collecting data from a variety of sources and you want to then make it available to anyone who wants it. But before you do that, you want a data steward to take a look at it and sign off on it, verifying that it's suitable (or not) for public consumption. It's a very simple (but not unreasonable) requirement, and your lead developer decides to implement this as a simple HTML/JavaScript web form and Node.js on the back end (also immaterial, as MongoDB supports a dozen different languages). The point of the demo is to show how your developers can build their apps immediately, without first designing a database schema in advance, and can then make iterative changes to their application without constantly going back to the database or their DBAs to make schema modifications (as would be required by any relational database). 

<img src="images/MongoDB-easy-to-innovate.png" alt="No Backend Changes" width="800"/>

**Step 1:** Just launch this simple web form and submit a record to the database. Note how the record looks in MongoDB (I use MongoDB Compass side-by-side with the web form).

<img src="images/simpleApp-first-iteration.png" alt="First Iteration" width="800"/>

**Step 2:** Modify the web form to accomodate separate first and last names, then reload the web form. Resubmit. Presto! Show the data in MongoDB using Compass. Show how all fields are instantly queryable (e.g. query on approvedBy.lastName), drawing a distinction between MongoDB and a simple key-value store. You can create secondary indexes, build data pipelines, run analytics, etc. With Compass open, you could show JSON Schema validation at this point, to alleviate any concerns about inconsistent/erroneous data models (e.g. require approvedBy.lastName).

<img src="images/simpleApp-second-iteration.png" alt="Second Iteration" width="800"/>

**Setup:** Node.js and NPM have to be installed. Then, from the <em>code</em> directory, run "npm install" to install the dependencies defined in <em>package.json</em>. In <em>index.js</em>, modify the MongoDB connect string to connect to your database. Passwords can be put in the key.json file. Run the app with "node index.js". The web form is in <em>index.html</em>. The 2 required code changes to get from v1 of the form to v2 are clearly commented in the code - just make these changes on-the-fly in the demo using your favorite code editor, save the changes, and then reload the form in your web browser. Backup versions of both v1 and v2 forms are only there in case you ever forget to undo your work at the end of the demo.

**Credits:** This demo is a stripped-down version of a demo developed by Matt Groghan ([here](https://github.com/mdg-2018/30-min-data-web-form)), which itself was a node.js adaptation of a MongoDB Atlas demo created by Michael Lynn ([here](https://github.com/mrlynn/30-min-data-web-form)).
