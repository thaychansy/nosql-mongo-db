<h1  align="center">NoSQL Challenge</h1>
<a name="readme-top"></a>


<!-- TABLE OF CONTENTS -->



Table of Contents
<ol>
<li><a href="#about-the-project">About The Project</a></li>
<li><a href="#built-with-nosql-and-mongodb-framework">Build With NoSQL and MongoDB Framework</a></li>
<li><a href="#contributing">Contributing (UC Berkeley Bootcamp Students Only) </a></li>
<li><a href="#contact">Contact</a></li>
<li><a href="#acknowledgments">Acknowledgments</a></li>
</ol>


<!-- ABOUT THE PROJECT -->

## About The Project

### Instructions

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up

Use `NoSQL_setup_starter.ipynb` for this section of the challenge.

1. Import the data provided in the `establishments.json` file from your Terminal. Name the database uk_food and the collection `establishments`. Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

2. Within your notebook, import the libraries you need: PyMongo and Pretty Print `(pprint)`.

3. Create an instance of the Mongo Client.

4. Confirm that you created the database and loaded the data properly:

- List the databases you have in MongoDB. Confirm that `uk_food` is listed.
- List the collection(s) in the database to ensure that `establishments` is there.
- Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.

5. Assign the `establishments` collection to a variable to prepare the collection for use.

## Part 2: Update the Database

Use `NoSQL_setup_starter.ipynb` for this section of the challenge.

The magazine editors have some requested modifications for the database before you can perform any queries or analysis for them. Make the following changes to the `establishments` collection:

1. An exciting new halal restaurant just opened in Greenwich, but hasn't been rated yet. The magazine has asked you to include it in your analysis. Add the following information to the database:

   <img width="560" alt="image" src="https://github.com/user-attachments/assets/18987a7a-e36e-47b5-9d08-207183731cfa">


3. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.

4. Update the new restaurant with the `BusinessTypeID` you found.

5. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.

6. Some of the number values are stored as strings, when they should be stored as numbers.

- Use `update_many` to convert `latitude` and `longitude` to decimal numbers.
- Use `update_many` to convert `RatingValue` to integer numbers.

## Part 3: Exploratory Analysis

Eat Safe, Love has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

Use `NoSQL_analysis_starter.ipynb` for this section of the challenge.

Some notes to be aware of while you are exploring the dataset:

- `RatingValue` refers to the overall rating decided by the Food Authority and ranges from 1-5. The higher the value, the better the rating.
    -   Note: This field also includes non-numeric values such as 'Pass', where 'Pass' means that the establishment passed their inspection but isn't given a number rating. We will coerce non-numeric values to nulls during the database setup before converting ratings to integers.
- The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse. This means, the higher the value, the worse the establishment is in these areas.

Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.

Unless otherwise stated, for each question:

- Use `count_documents` to display the number of documents contained in the result.

- Display the first document in the results using `pprint`.

- Convert the result to a Pandas DataFrame, print the number of rows in the DataFrame, and display the first 10 rows.

1. Which establishments have a hygiene score equal to 20?

2. Which establishments in London have a `RatingValue` greater than or equal to 4?

3. What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

The first 5 rows of your resulting DataFrame should look something like this:

![Uploading image.png…]()

  
<!-- BUILT-WITH-NOSQL-AND-MONGODB -->
## Built with NoSQL and MongoDB Framework 

- NoSQL (Not Only SQL) is a broad class of database management systems that are designed to handle large volumes of data with more flexibility than traditional relational databases. They often use key-value stores, document stores, wide-column stores, or graph databases to store and manage data.

- MongoDB is a popular NoSQL database that uses a document-oriented data model. This means that data is stored in flexible, JSON-like documents, allowing for easier schema evolution and handling of complex data structures.

By using MongoDB, a system can benefit from its ability to scale horizontally, handle unstructured data, and provide high performance for read and write operations. This makes it a suitable choice for applications that deal with large amounts of data, such as big data analytics, content management systems, and real-time applications.
  
  <p  align="right">(<a  href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->

## Contributing 

(UC Berkeley Bootcamp Students Only)  

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

  

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!

1. Fork the Project

2. Create your Feature Branch (`git checkout -b new-branch-name`)

3. Commit your Changes (`git commit -m 'Add some message'`)

4. Push to the Branch (`git push origin new-branch-name`)

5. Create a pull request. 

Forking a repository and creating a pull request on GitHub is a great way to contribute to open-source projects. Here's a breakdown of the process:

1. Forking the Repository:

Find the repository you want to contribute to on GitHub.
Click on the "Fork" button in the top right corner. This creates a copy of the repository in your own account.

2. Clone the Forked Repository to Your Local Machine

You'll need Git installed on your system.
Use Git commands to clone your forked repository to your local machine. There will be instructions on the GitHub repository page for cloning.

3. Making Changes (Local Work):

Make your changes to the code in your local copy.
Use Git commands to track your changes (adding, committing).

4. Pushing Changes to Your Fork:

Once you're happy with your changes, use Git commands to push your local commits to your forked repository on GitHub.

5. Creating a Pull Request:

Go to your forked repository on GitHub.
Click the "Compare & pull request" button (might appear as a yellow banner).
Here, you'll see a comparison between your changes and the original repository.
Write a clear title and description for your pull request explaining the changes you made.
Click "Create Pull Request" to submit it for review.

<p  align="right">(<a  href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under  GNU General Public License. See `LICENSE.txt` for more information.

<p  align="right">(<a  href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Thay Chansy - [@thaychansy](https://twitter.com/thaychansy) - or thay.chansy@gmail.com


Please visit my Portfolio Page: thaychansy.github.io (https://thaychansy.github.io/)



Project Link: [thaychansy/nosql-challenge (github.com)](https://github.com/thaychansy/nosql-challenge)
  

<p  align="right">(<a  href="#readme-top">back to top</a>)</p>

   
  

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments


Here's a list of resources we found helpful and would like to give credit to. 

  
* [Chat GPT] [ChatGPT](https://chatgpt.com/)
* [Google Gemini] [Gemini Generative AI](https://gemini.google.com/app)
  

<p  align="right">(<a  href="#readme-top">back to top</a>)</p>

