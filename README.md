# **Project: Book Database Analysis**

This project focuses on the exploration and analysis of an application market for book lovers through complex SQL queries. The analysis covers user behavior, publishing trends, publishers, and highly-rated authors. It provides strategic insights to develop a value proposition focused on improving the user experience in interacting with digital and physical books.

**Objective**

The project is structured in the following main phases:

1. **Database Connection:** Establish a secure connection to the remote PostgreSQL database.
2. **Structure Exploration:** Document 5 main tables (books, authors, publishers, ratings, reviews) and their relationships.
3. **Temporal Trend Analysis:** Identify book publishing patterns post-2000.
4. **User Interaction Analysis:** Evaluate ratings and reviews to determine reader satisfaction.
5. **Identification of Leading Publishers:** Recognize publishers with the highest activity in substantial publications.
6. **Author Analysis:** Classify authors by user rating and engagement.
7. **Strategic Proposal:** Synthesize findings and recommend product strategies.

**🛠️ Technologies Used**

* **Python:** Main language for data analysis and processing.
* **SQL:** Query language with complex JOINs, subqueries, and aggregations.
* **PostgreSQL:** Remote relational database (Yandex Cloud).
* **SQLAlchemy:** ORM for secure database connection.
* **Pandas:** Manipulation and transformation of SQL results into DataFrames.
* **Jupyter Notebook:** Interactive environment for analysis development and documentation.

**Key Steps**

1. **Database Connection:**
   - Secure configuration of credentials and connection parameters.
   - Initialization of SQLAlchemy engine with PostgreSQL connection.
   - Access validation for all main tables.

2. **Structure Exploration (5 Tables):**
   - **books:** 1,000 records with metadata (ID, author, title, pages, date, publisher).
   - **authors:** 636 records with author information.
   - **publishers:** 340 records with publisher data.
   - **ratings:** 6,456 user numeric rating records.
   - **reviews:** 2,793 user text review records.

3. **Query 1 - Post-2000 Books:**
   - Filter books by publication date after 2000-01-01.
   - Identification of 819 books in this period (81.9% of the catalog).

4. **Query 2 - Review and Rating Analysis:**
   - Aggregation of reviews by book using LEFT JOINs.
   - Calculation of average rating (AVG rating) by title.
   - Evaluation of varied behavior between books in terms of interaction.

5. **Query 3 - Leading Publisher by Volume:**
   - JOIN between publishers and books filtered by pages > 50.
   - Identification of "Penguin Books" as the leader with 42 substantial books.

6. **Query 4 - Author with Highest Rating:**
   - Subquery with HAVING to filter books with ≥50 ratings.
   - Identification of J.K. Rowling with an average rating of 4.28 (maximum).

7. **Query 5 - Active Users and Reviews:**
   - Nested subquery to identify users with >50 ratings.
   - Calculation of text review average: 24.33 per active user.

**Results**

The analysis reveals that:

- **Data Coverage:** Intact database with 1,000 books, 636 authors, and 340 publishers.
- **Editorial Modernization:** 819 books (81.9%) published post-2000, indicating an updated catalog.
- **User Interaction:** 6,456 ratings and 2,793 reviews indicate an active and engaged community.
- **Dominant Publisher:** Penguin Books leads with 42 quality books (>50 pages).
- **Featured Author:** J.K. Rowling with a 4.28 rating, evidencing high reader satisfaction.
- **Highly Active Users:** 24.33 average reviews from users who rate frequently (>50 books).
- **Variability in Popularity:** Uneven behavior of books suggests the presence of bestseller titles and specialized niches.

**Strategic Recommendations**

1. **Focus on Premium Content:** Prioritize the promotion of books with ratings >4.0 and >100 reviews to attract high-value users.
2. **Editorial Alliances:** Establish agreements with Penguin Books and similar publishers to ensure a constant flow of substantial titles.
3. **Participation Gamification:** Incentivize users to write reviews (currently 2,793 out of 6,456 raters = 43.3% write reviews).
4. **Curation by Top Authors:** Create featured sections for authors like J.K. Rowling with proven satisfaction metrics.
5. **Community Management:** Integrate ultra-active users (>50 ratings) as brand ambassadors or editorial critics.

**How to Run the Project**

1. Clone this repository to your local machine.
   ```bash
   git clone <REPOSITORY_URL>
   ```
   *(Note: Make sure to replace the URL with your actual repository URL).*

2. Set up database connection credentials:
   - Open the `ProyectoSQL.ipynb` file
   - Locate the connection cell and update `db_config` with your credentials (user, password, host, port)

3. Install necessary dependencies:
   ```bash
   pip install pandas sqlalchemy psycopg2 jupyter
   ```

4. Run the notebook in Jupyter Notebook:
   ```bash
   jupyter notebook ProyectoSQL.ipynb
   ```

5. Run the code cells in sequential order to:
   - Connect to the database
   - Explore table structure
   - Execute the 5 main SQL queries
   - Analyze and visualize results

**Important Notes**

- The database is private and requires a secure connection (SSL).
- The queries are optimized to handle thousands of records efficiently.
- The results are reproducible and can serve as a basis for deeper segmentation and machine learning analysis.
