# Part 1 Dataset and Data Wrangling:

### 1. Definition of Dataset:
The dataset used in this project consists of Software Requirement Specifications (SRS) that detail the functionalities and capabilities of a software system. Each row in the dataset represents a single requirement, focusing on a specific capability or feature that the software should possess. The primary objective of this dataset is to provide a structured and comprehensive list of requirements that guide the development and functionality of the software.

### 2. Data Cleaning:
Data cleaning is a crucial step in preparing the dataset for further analysis and processing. The SRS datasets obtained initially contained a mix of relevant and irrelevant information, necessitating a thorough cleaning process to ensure that only the essential data is retained.

#### 2.1. Initial Data Collection:
The initial datasets were collected from various sources, each containing multiple columns, some of which were not pertinent to the SRS text. These non-sense columns included metadata and other extraneous information that did not contribute to the understanding or extraction of software requirements.

#### 2.2. Restructuring and Storing Data:
To streamline the dataset, the following steps were undertaken:

- **Removing Unnecessary Columns:** The first step involved identifying and removing columns that did not contain relevant SRS information. This helped in reducing the dataset to only those columns that were essential for the analysis.
  
- **Standardizing Texts:** The remaining SRS texts were then standardized to ensure consistency across the dataset. This involved converting all text to a uniform case (e.g., all lowercase) and ensuring that similar terms and phrases were represented consistently.

- **Removing Unnecessary Characters:** Using regular expressions (regex), unnecessary characters such as special symbols, extra spaces, and punctuation marks that did not contribute to the meaning of the requirements were removed. This step was crucial in ensuring that the text was clean and ready for further processing.

- **Saving the Cleaned Data:** After cleaning, the restructured and standardized data was saved in a new format, typically a CSV or a similar structured file, to facilitate easy access and further analysis. This cleaned dataset now contained only the relevant SRS text, making it ready for subsequent steps such as information extraction and workflow graph generation.

By meticulously cleaning and restructuring the dataset, we ensured that the data was in an optimal state for the next phases of the project, thereby enhancing the accuracy and efficiency of the information extraction and workflow graph generation processes.

### 3. Exploring the Cleaned Data:
After the initial data cleaning steps, the dataset was further explored to understand its structure and content better. At this stage, the dataset was reduced to a single column named `RequirementText`, which contained the SRS statements for each project. This column was the focal point for all subsequent analysis and processing.

#### Project Requirements Data:
To gain insights into the dataset, the number of requirements for each project was examined. This step involved counting the rows in the `RequirementText` column for each project file. The results of this exploration are summarized below:

| Project Title   | Number of Requirements |
|-----------------|-------------------------|
| dronology.csv   | 97                      |
| leeds.csv       | 87                      |
| rds8.csv        | 291                     |
| wasp.csv        | 67                      |

This table highlights the variability in the number of requirements across different projects. Each project has a unique set of requirements, with the number of requirements ranging from 67 to 291. This variability is expected, as different software projects have varying scopes and complexities, which are reflected in the number of requirements specified.

By exploring the cleaned data, we were able to:

- **Understand the Scope of Each Project:** The number of requirements gives an indication of the project's scope and complexity. For instance, `rds8.csv` with 291 requirements likely represents a more complex and feature-rich project compared to `wasp.csv` with 67 requirements.
  
- **Prepare for Further Analysis:** Knowing the number of requirements per project helps in planning the subsequent steps of information extraction and workflow graph generation. It also aids in resource allocation and time estimation for processing each project's requirements.

This exploration step was essential in setting the stage for the next phases of the project, ensuring that we had a clear understanding of the dataset's structure and the scope of each project.

# Part 2 Workflow Suggestion using LLMs

### Utilizing LLMs to Automate Drawing Workflow Process

The second part of the project involves leveraging Large Language Models (LLMs) to automate the creation of workflow graphs from Software Requirement Specifications (SRS). This step is crucial as it transforms textual requirements into a visual representation of the software's functionality, making it easier to understand and analyze.

#### Understanding SRS Statements:
Each SRS statement contains specific information about the functionality of the software. To create a workflow graph, we need to extract the following components from each statement:

1. **Actor1:** This is the subject of the statement that initiates an action. In the context of a workflow graph, Actor1 represents a node that can perform certain actions.

2. **Actor2:** This is the object that is affected by the action of Actor1. Actor2 is another node in the workflow graph, representing the entity that receives or is impacted by the action.

3. **Interaction:** This is the action taken by Actor1. In the workflow graph, the interaction is represented as an edge connecting Actor1 and Actor2, illustrating the relationship and action flow between these two nodes.

4. **Information:** This refers to any data or additional information linked to the interaction. In the workflow graph, information is also represented as an edge, providing context or details about the interaction between Actor1 and Actor2.

5. **Decision:** This is the final node that extends the interaction initiated by Actor2. The decision node represents a point in the workflow where a choice or outcome is determined, further extending the interaction flow.


<div>
<img src="[attachment:image.png](https://github.com/user-attachments/assets/b156be83-7a75-40cc-9bd8-6835f0b526c2)" width=800 />
</div>


#### Aim:
The primary aim is to take each SRS statement and systematically create these nodes and edges to construct a comprehensive workflow graph. This step is essential as it forms the foundation for visualizing the software's functionality and interactions.

#### Process:
1. **Extracting Components Using LLMs:**
   - **Actor1 Identification:** The LLM is used to parse the SRS statement and identify the subject (Actor1) that initiates the action.
   - **Actor2 Identification:** The LLM then identifies the object (Actor2) that is affected by the action of Actor1.
   - **Interaction Extraction:** The LLM extracts the verb or action phrase that describes the interaction between Actor1 and Actor2.
   - **Information Extraction:** Any additional data or context related to the interaction is identified and extracted by the LLM.
   - **Decision Identification:** Finally, the LLM identifies any decision points or outcomes that extend from the interaction involving Actor2.

2. **Creating Nodes and Edges:**
   - **Nodes Creation:** Based on the extracted components, nodes are created for Actor1, Actor2, and Decision.
   - **Edges Creation:** Edges are created to represent the interactions and information flow between the nodes. The interaction edge connects Actor1 and Actor2, while the information edge provides additional context to the interaction.

3. **Constructing the Workflow Graph:**
   - Using the nodes and edges created from each SRS statement, a workflow graph is constructed. This graph visually represents the sequence of actions, interactions, and decisions, providing a clear and structured view of the software's functionality.

By automating this process with LLMs, we can efficiently and accurately transform textual SRS statements into detailed workflow graphs. This not only enhances the understanding of the software requirements but also aids in identifying potential issues, dependencies, and areas for improvement in the software design.

# Part 1 Dataset and Data Wrangling:

### 1. Definition of Dataset:
The dataset used in this project consists of Software Requirement Specifications (SRS) that detail the functionalities and capabilities of a software system. Each row in the dataset represents a single requirement, focusing on a specific capability or feature that the software should possess. The primary objective of this dataset is to provide a structured and comprehensive list of requirements that guide the development and functionality of the software.

### 2. Data Cleaning:
Data cleaning is a crucial step in preparing the dataset for further analysis and processing. The SRS datasets obtained initially contained a mix of relevant and irrelevant information, necessitating a thorough cleaning process to ensure that only the essential data is retained.

#### 2.1. Initial Data Collection:
The initial datasets were collected from various sources, each containing multiple columns, some of which were not pertinent to the SRS text. These non-sense columns included metadata and other extraneous information that did not contribute to the understanding or extraction of software requirements.

#### 2.2. Restructuring and Storing Data:
To streamline the dataset, the following steps were undertaken:

- **Removing Unnecessary Columns:** The first step involved identifying and removing columns that did not contain relevant SRS information. This helped in reducing the dataset to only those columns that were essential for the analysis.
  
- **Standardizing Texts:** The remaining SRS texts were then standardized to ensure consistency across the dataset. This involved converting all text to a uniform case (e.g., all lowercase) and ensuring that similar terms and phrases were represented consistently.

- **Removing Unnecessary Characters:** Using regular expressions (regex), unnecessary characters such as special symbols, extra spaces, and punctuation marks that did not contribute to the meaning of the requirements were removed. This step was crucial in ensuring that the text was clean and ready for further processing.

- **Saving the Cleaned Data:** After cleaning, the restructured and standardized data was saved in a new format, typically a CSV or a similar structured file, to facilitate easy access and further analysis. This cleaned dataset now contained only the relevant SRS text, making it ready for subsequent steps such as information extraction and workflow graph generation.

By meticulously cleaning and restructuring the dataset, we ensured that the data was in an optimal state for the next phases of the project, thereby enhancing the accuracy and efficiency of the information extraction and workflow graph generation processes.

### 3. Exploring the Cleaned Data:
After the initial data cleaning steps, the dataset was further explored to understand its structure and content better. At this stage, the dataset was reduced to a single column named `RequirementText`, which contained the SRS statements for each project. This column was the focal point for all subsequent analysis and processing.

#### Project Requirements Data:
To gain insights into the dataset, the number of requirements for each project was examined. This step involved counting the rows in the `RequirementText` column for each project file. The results of this exploration are summarized below:

| Project Title   | Number of Requirements |
|-----------------|-------------------------|
| dronology.csv   | 97                      |
| leeds.csv       | 87                      |
| rds8.csv        | 291                     |
| wasp.csv        | 67                      |

This table highlights the variability in the number of requirements across different projects. Each project has a unique set of requirements, with the number of requirements ranging from 67 to 291. This variability is expected, as different software projects have varying scopes and complexities, which are reflected in the number of requirements specified.

By exploring the cleaned data, we were able to:

- **Understand the Scope of Each Project:** The number of requirements gives an indication of the project's scope and complexity. For instance, `rds8.csv` with 291 requirements likely represents a more complex and feature-rich project compared to `wasp.csv` with 67 requirements.
  
- **Prepare for Further Analysis:** Knowing the number of requirements per project helps in planning the subsequent steps of information extraction and workflow graph generation. It also aids in resource allocation and time estimation for processing each project's requirements.

This exploration step was essential in setting the stage for the next phases of the project, ensuring that we had a clear understanding of the dataset's structure and the scope of each project.



---

# Part 2 Workflow Suggestion using LLMs

### Utilizing LLMs to Automate Drawing Workflow Process

The second part of the project involves leveraging Large Language Models (LLMs) to automate the creation of workflow graphs from Software Requirement Specifications (SRS). This step is crucial as it transforms textual requirements into a visual representation of the software's functionality, making it easier to understand and analyze.

#### Understanding SRS Statements:
Each SRS statement contains specific information about the functionality of the software. To create a workflow graph, we need to extract the following components from each statement:

1. **Actor1:** This is the subject of the statement that initiates an action. In the context of a workflow graph, Actor1 represents a node that can perform certain actions.

2. **Actor2:** This is the object that is affected by the action of Actor1. Actor2 is another node in the workflow graph, representing the entity that receives or is impacted by the action.

3. **Interaction:** This is the action taken by Actor1. In the workflow graph, the interaction is represented as an edge connecting Actor1 and Actor2, illustrating the relationship and action flow between these two nodes.

4. **Information:** This refers to any data or additional information linked to the interaction. In the workflow graph, information is also represented as an edge, providing context or details about the interaction between Actor1 and Actor2.

5. **Decision:** This is the final node that extends the interaction initiated by Actor2. The decision node represents a point in the workflow where a choice or outcome is determined, further extending the interaction flow.

<div>
<img src="attachment:image.png" width=800 />
</div>


#### Aim:
The primary aim is to take each SRS statement and systematically create these nodes and edges to construct a comprehensive workflow graph. This step is essential as it forms the foundation for visualizing the software's functionality and interactions.

#### Process:
1. **Extracting Components Using LLMs:**
   - **Actor1 Identification:** The LLM is used to parse the SRS statement and identify the subject (Actor1) that initiates the action.
   - **Actor2 Identification:** The LLM then identifies the object (Actor2) that is affected by the action of Actor1.
   - **Interaction Extraction:** The LLM extracts the verb or action phrase that describes the interaction between Actor1 and Actor2.
   - **Information Extraction:** Any additional data or context related to the interaction is identified and extracted by the LLM.
   - **Decision Identification:** Finally, the LLM identifies any decision points or outcomes that extend from the interaction involving Actor2.

2. **Creating Nodes and Edges:**
   - **Nodes Creation:** Based on the extracted components, nodes are created for Actor1, Actor2, and Decision.
   - **Edges Creation:** Edges are created to represent the interactions and information flow between the nodes. The interaction edge connects Actor1 and Actor2, while the information edge provides additional context to the interaction.

3. **Constructing the Workflow Graph:**
   - Using the nodes and edges created from each SRS statement, a workflow graph is constructed. This graph visually represents the sequence of actions, interactions, and decisions, providing a clear and structured view of the software's functionality.

By automating this process with LLMs, we can efficiently and accurately transform textual SRS statements into detailed workflow graphs. This not only enhances the understanding of the software requirements but also aids in identifying potential issues, dependencies, and areas for improvement in the software design.

### Implementing the Workflow Automation with GPT-4

To achieve the task of automating the drawing of workflow processes from SRS statements, I utilized the HuggingFace transformers library initially. However, after experimenting with several open-source models and finding them inadequate for the specific requirements of this project, I opted to use the advanced GPT-4 model from OpenAI. Given the time constraints and the proof-of-concept nature of this work, GPT-4 provided a more reliable and efficient solution.

#### Implementation Steps:

1. **Using GPT-4 for Information Extraction:**
   - **Model Selection:** Due to the limitations of open-source models, GPT-4 was chosen for its advanced capabilities in natural language understanding and generation.
   - **API Integration:** The OpenAI API was integrated into the project to leverage GPT-4 for extracting the necessary components (Actor1, Actor2, Interaction, Information, Decision) from each SRS statement.

2. **Helper Functions:**
   - Several helper functions were constructed to streamline the process of running the LLM model, validating the outputs, and saving the results. These functions ensure that the workflow is efficient and the results are accurate.

3. **Running the Code:**
   - The following code snippet demonstrates how to run the process for any file in the dataset by providing an OpenAI API key. This code extracts the required information from each SRS statement and constructs the workflow graph.


#### Explanation of the Code:

1. **API Key Setup:**
   - The OpenAI API key is set to authenticate requests to the GPT-4 model.

2. **`OpenAIChatHelper` Object:**
   - This class sends a prompt to GPT-4 to extract the required components (Actor1, Actor2, Interaction, Information, Decision) from an SRS statement.
   - The response from GPT-4 is parsed to retrieve the extracted components.

3. **`read_string_to_json and list_to_str` Functions:**
   - These functions perform basic validation on the extracted output to ensure all necessary components are in JSON format.
   - The validation logic can be expanded based on specific requirements.

4. **`save_nodes` Function:**
   - This function saves the extracted and validated results to a local CSV file for further analysis and visualization.


By using GPT-4 and the helper functions, the process of extracting workflow components from SRS statements and constructing workflow graphs is automated efficiently. This approach demonstrates the feasibility of the concept and provides a solid foundation for further development and refinement.

### Results Overview

After processing the SRS statements using GPT-4, the extracted components are structured into a tabular format. Each row corresponds to an SRS statement, with columns representing the extracted workflow components: `Actor1`, `Actor2`, `Interaction`, `Information`, and `Decision`. Below is an example of how the results look:

| index | Statement                                                                 | Actor1         | Actor2           | Interaction       | Information         | Decision  |
|-------|---------------------------------------------------------------------------|----------------|------------------|-------------------|---------------------|-----------|
| 0     | There should be an application that provides f...                         | mobile users   | meetings         | propose schedule  | None                | None      |
| 1     | The WASP platform must provide services that m...                         | wasp platforms | wasp applications| personalize       | content user profile| None      |
| 2     | The WASP platform should provide services that...                         | wasp platforms | wasp applications| personalize       | content user profiles| end-users |

### Explanation of the Results:

1. **Index:** This column is an identifier for each SRS statement, allowing easy reference and tracking.

2. **Statement:** This column contains the original SRS statement from which the workflow components were extracted.

3. **Actor1:** Represents the subject of the statement that initiates an action. For example, "mobile users" in the first statement.

4. **Actor2:** Represents the object affected by the action of Actor1. For example, "meetings" in the first statement.

5. **Interaction:** Describes the action taken by Actor1. For example, "propose schedule" in the first statement.

6. **Information:** Contains any additional data or context related to the interaction. For example, "content user profile" in the second statement.

7. **Decision:** Represents any decision points or outcomes that extend from the interaction involving Actor2. For example, "end-users" in the third statement.

### Summary:

The results table provides a clear and structured view of the extracted workflow components from each SRS statement. This structured data can be used to construct workflow graphs, visually representing the interactions and decisions within the software system. The table highlights the relationships between different actors, their interactions, and any associated information or decisions, making it easier to understand and analyze the software requirements.

By automating the extraction process using GPT-4 and organizing the results in this format, we demonstrate the feasibility of the approach and provide a solid foundation for further development and refinement. This proof-of-concept work shows that the methodology can effectively transform textual SRS statements into actionable workflow components, paving the way for more advanced and production-grade implementations in the future.

### Visualizing Workflow Graphs

In this part of the project, the focus was on visualizing the extracted workflow components to provide a clear understanding of the software's functionality. To achieve this, I used the NetworkX library, which is well-suited for creating and visualizing complex networks and graphs.

#### Functions for Visualization:

1. **`workflow_springlayout()` Function:**
   - This function uses the spring layout algorithm provided by NetworkX to visualize the workflow graph.
   - The spring layout algorithm positions nodes using a force-directed layout, which attempts to position nodes such that all the edges are of more or less equal length and there are as few crossing edges as possible.
   - **Strengths:** This layout is useful for presenting more connections between nodes, giving a comprehensive view of the relationships and interactions within the software.
   - **Limitations:** While it shows more connections, it can become cluttered and less clear, especially for larger datasets, making it difficult to discern a clear workflow.

2. **`workflow_graph()` Function:**
   - This function provides a more straightforward visualization of the workflow graph, focusing on clarity and simplicity.
   - It is particularly effective for datasets with up to 20 connections, where it can clearly depict the interactions and decisions without becoming too messy.
   - **Strengths:** This layout is very handy for smaller datasets, providing a clear and concise view of the workflow.
   - **Limitations:** As the number of nodes and connections increases beyond 20, the graph can become cluttered and difficult to interpret, reducing its effectiveness.

#### Implementation and Visualization:

The following code snippets demonstrate how these functions are implemented and used to visualize the workflow graphs:

#### Explanation of the Code:

1. **Creating the Graph:**
   - Both functions create a directed graph (`DiGraph`) using NetworkX.
   - Nodes and edges are added to the graph based on the extracted workflow components from the dataframe.

2. **Spring Layout Visualization (`workflow_springlayout`):**
   - The spring layout algorithm is used to position the nodes.
   - The graph is drawn with nodes, edges, and edge labels, providing a comprehensive view of the interactions.
   - This layout is useful for visualizing more connections but can become cluttered for larger datasets.
   
<div>
<img src="attachment:image.png" width=800 />
</div>

3. **Simple Layout Visualization (`workflow_graph`):**
   - A simpler circular layout is used to position the nodes.
   - This layout is effective for smaller datasets, providing a clear and concise view of the workflow.
   - As the number of nodes and connections increases, the graph can become cluttered.
   
<div>
<img src="attachment:image-2.png" width=800 />
</div>

### Summary:

The visualization of workflow graphs using NetworkX demonstrates the feasibility of the concept. The `workflow_springlayout` function provides a comprehensive view of the interactions, while the `workflow_graph` function offers a clearer view for smaller datasets. Both functions have their strengths and limitations, highlighting the need for further refinement and better infrastructure for production-grade implementations.

This proof-of-concept work successfully shows that the approach can transform textual SRS statements into meaningful workflow graphs, providing valuable insights into the software's functionality and interactions.

---

# Part 3: Evaluation

To evaluate the performance of the LLM in extracting workflow components from SRS statements, I created a ground truth dataset by manually classifying each statement. This ground truth dataset serves as a benchmark to assess the accuracy of the LLM-generated labels. The evaluation process involves comparing the LLM-generated labels with the ground truth labels for each node and edge column in the dataset.

#### Evaluation Process:

1. **Ground Truth Dataset:**
   - A manually classified dataset was created, containing the same columns as the LLM-generated dataset (`Actor1`, `Actor2`, `Interaction`, `Information`, `Decision`).
   - This dataset serves as the reference for evaluating the LLM's performance.

2. **Evaluation Function:**
   - The `evaluation_scores()` function was developed to compare the LLM-generated labels with the ground truth labels.
   - The function calculates evaluation metrics such as accuracy, precision, recall, and F1-score for each node and edge column.

3. **Running the Evaluation:**
   - The evaluation process is run for each node and edge column in the dataset, providing a comprehensive assessment of the LLM's performance.

#### Implementation:

The following code snippet demonstrates the implementation of the `evaluation_scores()` function and the evaluation process:

### Evaluation Results and Interpretation

Given the evaluation results and the nature of your ground truth data, it's important to focus on the metrics that provide meaningful insights. As you correctly pointed out, the precision and F1 scores are not informative in this context due to the nature of your ground truth data containing only true values. Similarly, the accuracy score is misleading because it includes True Negatives (TN) and False Positives (FP) in its calculation, which are not relevant here.

<div>
<img src="attachment:image-2.png" width=500 />
</div>

Therefore, the most meaningful metrics for your evaluation are the recall score and the number of matched and missed labels. These metrics directly reflect the LLM's ability to correctly identify the workflow components.

#### Evaluation Results:

| Node_Edge   | Recall   | Num_Matched | Num_Missed | Accuracy  | Precision | F1       |
|-------------|----------|-------------|------------|-----------|-----------|----------|
| Actor1      | 0.850746 | 57          | 10         | 0.850746  | 1.0       | 0.919355 |
| Interaction | 0.761194 | 51          | 16         | 0.761194  | 1.0       | 0.864407 |
| Information | 0.402985 | 27          | 40         | 0.402985  | 1.0       | 0.574468 |
| Actor2      | 0.253731 | 17          | 50         | 0.253731  | 1.0       | 0.404762 |
| Decision    | 0.014925 | 1           | 66         | 0.014925  | 1.0       | 0.029412 |

---
<div>
<img src="attachment:image.png" width=800 />
</div>

Given the evaluation results and the nature of the data, it is reasonable to focus on the most informative components: `Actor1`, `Interaction`, and `Actor2`. The `Decision` node and `Information` edge can be ignored in this evaluation due to the high number of null values, which makes their comparison less valuable.

#### Interpretation:

1. **Actor1:**
   - **Recall:** 0.850746
   - **Num_Matched:** 57
   - **Num_Missed:** 10
   - **Interpretation:** The LLM performed well in identifying `Actor1`, with a high recall score of approximately 85%. This indicates that the majority of `Actor1` labels were correctly identified, demonstrating strong performance in this area.

2. **Interaction:**
   - **Recall:** 0.761194
   - **Num_Matched:** 51
   - **Num_Missed:** 16
   - **Interpretation:** The LLM also performed reasonably well in identifying `Interaction`, with a recall score of approximately 76%. This suggests that most interactions were correctly extracted, although there is room for improvement.

3. **Actor2:**
   - **Recall:** 0.253731
   - **Num_Matched:** 17
   - **Num_Missed:** 50
   - **Interpretation:** The LLM's performance in identifying `Actor2` is relatively low, with a recall score of approximately 25%. This suggests that the majority of `Actor2` labels were missed, indicating a need for substantial improvement in this area.

### Summary:

By focusing on the key components (`Actor1`, `Interaction`, and `Actor2`), we obtain a clearer and more meaningful assessment of the LLM's performance. The results indicate that while the LLM performs well in identifying `Actor1` and reasonably well in identifying `Interaction`, it struggles with identifying `Actor2`.

#### Recommendations for Improvement:

1. **Actor1:** The high recall score indicates strong performance, but further fine-tuning and additional training data could help achieve even higher accuracy.

2. **Interaction:** The LLM performs reasonably well, but there is room for improvement. Enhancing the training data with more diverse examples of interactions could help improve recall.

3. **Actor2:**  The low recall score suggests that the LLM has difficulty identifying `Actor2`. This could be addressed by:
     - Providing more annotated examples of `Actor2` in the training data.
     - Refining the model's understanding of the context in which `Actor2` appears.
     - Implementing additional preprocessing steps to better highlight `Actor2` in the SRS statements.

By focusing on these key areas, we can make targeted improvements to the LLM's performance, ultimately enhancing its ability to accurately extract workflow components from SRS statements. This focused evaluation provides a solid foundation for further development and optimization, ensuring that the proof-of-concept work is both rigorous and informative.

---

# Bonus Task: Smart Evaluation and Multimodal Input Suggestions

To implement advanced evaluation techniques and provide suggestions for further improvements, we need to address several key points based on the current implementation and its limitations. Below, I explain each point in detail to fulfill the final task requirements.

#### 1. Lack of Domain Knowledge Results in Inadequate Ground Truth Data

**Challenge:**
- Finding corresponding node and edge data points for the dataset was challenging due to the lack of available resources.
- As a result, I manually classified the data to create a ground truth reference. While this is acceptable for a proof-of-concept, it is not ideal for a production-level solution.
- The lack of domain knowledge can significantly impact the quality of the ground truth data, leading to suboptimal results.

**Suggestion:**
- Collaborate with domain experts to create a more accurate and reliable ground truth dataset. Professionals with domain knowledge can provide precise labels, ensuring the ground truth data is of high quality.
- This collaboration will help mitigate the impact of inadequate domain knowledge and improve the overall accuracy of the evaluation.

#### 2. Fine-Tuning an LLM for the Task

**Challenge:**
- The current implementation uses a general-purpose LLM, which may not be optimized for extracting nodes and edges from SRS statements.
- SRS statements are typically structured in a specific way, and a general LLM may not capture these nuances effectively.

**Suggestion:**
- Fine-tune an LLM specifically for this task using a dataset of 200-300 correctly labeled SRS statements provided by professionals.
- Fine-tuning the model on domain-specific data will significantly enhance its ability to extract nodes and edges accurately.
- This targeted approach will improve the model's performance and ensure it is better suited for the task at hand.

#### 3. Multimodal Input for Enhanced Understanding

**Challenge:**
- The current implementation relies solely on textual input, which may limit the model's understanding of the task.
- Incorporating visual information, such as corresponding workflow graphs, can provide additional context and improve the model's performance.

**Suggestion:**
- Utilize multimodal capabilities by feeding the LLM with both SRS data and corresponding workflow graphs.
- This approach will enable the model to capture the task visually and verbally, leading to a more comprehensive understanding.
- Multimodal input can significantly enhance the model's ability to generate accurate workflow components and improve overall performance.

#### 4. Interactive Visualization Infrastructure

**Challenge:**
- The current implementation uses NetworkX for graph visualization, which is sufficient for a proof-of-concept but may not be ideal for production-level work.
- More interactive and user-friendly visualization tools can improve the quality and usability of the workflow graphs.

**Suggestion:**
- Explore more advanced and interactive visualization infrastructures, such as D3.js, Plotly, or Cytoscape.
- These tools offer enhanced interactivity and better user experiences, making it easier to analyze and interpret the workflow graphs.
- Implementing a more robust visualization infrastructure will improve the quality of the work and make it more accessible to end-users.

### Advanced Evaluation Techniques

To further enhance the evaluation process, we can implement advanced techniques such as semantic similarity and error analysis.

#### Semantic Similarity

**Implementation:**
- Use semantic similarity measures to compare the generated workflow steps with the ground truth.
- Tools like BERT embeddings or cosine similarity can be used to quantify the similarity between the generated and ground truth labels.

### Summary

By addressing the challenges and implementing the suggested improvements, we can significantly enhance the evaluation process and the overall quality of the workflow extraction task. Collaborating with domain experts, fine-tuning the LLM, utilizing multimodal input, and adopting advanced visualization tools will lead to more accurate and reliable results. Additionally, incorporating semantic similarity measures and performing thorough error analysis will provide deeper insights into the model's performance and guide further refinements.



