
## Project Title: Esports Graph Database

### Description

This project involves the design and implementation of a graph database utilizing an esports dataset in CSV format. The database connects over 1500 nodes, incorporating a manually defined structure that includes specialized nodes such as "locations" and "tournaments". This setup enables the exploration of the technical ecosystem within the esports industry, providing a unique insight into how different entities such as players, games, and events interconnect.

### Features

- **Comprehensive Graph Structure**: Includes over 1500 nodes and defines relationships that mirror the real-world interactions within the esports ecosystem.
- **Custom Nodes and Relationships**: Features custom-defined nodes and relationships that enhance the understanding of the esports landscape.
- **Data Analysis**: Allows for complex queries and analysis, facilitating insights into trends and patterns in esports data.

### Technologies Used

- **Neo4j**: Graph database platform used for storing and managing the network of nodes and relationships.
- **Cypher Query Language**: Utilized for querying the Neo4j database.
- **Python**: Scripts for data processing and integration into Neo4j.

### Installation

1. **Clone the repository:**
   ```
   git clone https://github.com/somilsaparia/Neo4j-Esports-Event-Management-Project.git
   ```
2. **Install Neo4j:**
   Follow the instructions at [Neo4j Installation Guide](https://neo4j.com/docs/installation/) to set up Neo4j on your local machine.

3. **Set up Python environment:**
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

### Usage

1. **Load the Dataset:**
   ```
   python load_data.py
   ```
   This script will parse the CSV files and load the data into the Neo4j database.

2. **Start Neo4j Server:**
   ```
   neo4j start
   ```
   Access the Neo4j browser at `http://localhost:7474` and explore the graph.

3. **Query the Database:**
   Utilize the Cypher query language to perform queries. Example:
   ```cypher
   MATCH (p:Player)-[r:PLAYS]->(g:Game)
   RETURN p, g
   ```

### Contributing

Contributions to the project are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b new-feature`
3. Make your changes and commit them: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin new-feature`
5. Submit a pull request.

### License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
