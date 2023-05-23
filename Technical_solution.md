## Technical Solution Description

The purpose of this technical solution is to serve as a middleware between OpenAI and the user interface. Its main objective is to provide users with up-to-date information about centers that offer free assistance in challenging life situations.

To achieve this, a database has been created to store data on the operations and locations of these centers.

For each entry in the existing database, a pool of questions is generated to accurately capture the essence of the entry. These questions are then converted into vector representations and stored in the database. When a user makes a query, their question is also transformed into a vector representation and compared to the existing vectors. If similar vectors are found, the corresponding information from the related table is added to the query context for OpenAI.

Word embeddings, a technique widely used in natural language processing, are employed to convert questions and responses into vector representations. As stated in the OpenAI documentation, "Word embeddings give us a way to use an efficient, dense representation in which similar words have a similar encoding." This allows for efficient comparison and retrieval of relevant information.

To configure OpenAI's role as a supportive psychologist, prompts are utilized. OpenAI aims to provide assistance to the user and inform them about the nearest specialized location where they can receive qualified help and support.

The technologies used in this solution include OpenAI, Supabase (with the possibility of transitioning to a different database), and Python.
