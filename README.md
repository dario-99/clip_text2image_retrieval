# clip-ViT-B-32 Text2Image retrieval performance testing with Flickr30k dataset
This python projects uses the clip-ViT-B-32 transformer model as a Text2Image retrieval system.
The system uses the model to create Image embeddings and indexes them with **hnsw**
on the SOLR search platform.
The textual query is then embedded with the model and using the cosine similarity metric the system
retrieves the most similiar embeddings indexed in SOLR.

## Evaluation metrics
The retrieval performance will be measured with Recall at K metric, precisily
R@1, R@5 and R@10 metrics.
Recall@K measures how many revelant items were returned against how 
many relevant items exist in the dataset

$$
R@K = \frac{\text{truePositives}}{truePositves + FalseNegatives}
$$
