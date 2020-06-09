# Company-Email-Network-Analysis

A company's email network is analyzed to predict whether an employee, based on their attributes, is receiving management level salary. 
The communication each employee has with one another is also analyzed. In NetworkX, each node is an employee, and each edge indicaties that at least one email has
been sent between the two people. The node attributes are Department and ManagementSalary (the target variable). 

Some feature engineering is performed, mostly in NetworkX, to determine important indicative factors of the salary received. The department data was found to detract from the AUC score, even
after one-hot encoding. The nodal clustering, degree, closeness centrality, and HITS scores are added to improve the AUC score from a baseline of ~0.5 to 0.93. Among these, the most important are clustering and closeness centrality. 
This can make sense when managers tend to be the ones sending emails to other people that are well connected. Closeness centrality can make sense when managers tend to be the ones disseminating information. It is conceivable
that degree would be less influential, because it depends on the organizational structure of the company. The importance of the nodal clustering and closeness centrality seems to suggest managers at this company communicate in a hierarchical manner. 
By the same tokens, it is somewhat surprising to see that HITS scores are not of the same order of magnitude of importance as the former two. 

This model achieves an AUC of 0.93. 
