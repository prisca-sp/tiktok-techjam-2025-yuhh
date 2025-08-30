# tiktok-techjam-2025-yuhh

*Project Overview*

This project focuses on filtering and classifying Google Local Reviews into three categories:
1. Advertisements (e.g. reviews containing URLs such as www or http)
2. Spam (e.g. reviews with patterns like "never been here")
3. Normal reviews (genuine customer feedback)

Online review datasets are often noisy, with irrelevant or misleading content. Cleaning these datasets improves the reliability of downstream tasks such as sentiment analysis, trend detection, and recommendation systems. We used pseudo-labelling rules to generate initial labels, followed by class balancing and fine-tuning of a BERT-based model (bert-base-uncased) with a custom classification head.
Our pipeline includes:
1. Data preprocessing (cleaning data, sentiment analysis, pseudo-labelling, oversampling minority classes)
2. Policy enforcement (filtering out ads/spam before further use)
3. Modeling (fine-tuned BERT with additional numeric features)
4. Evaluation (manual ground truthing + external dataset testing)

The model was evaluated on Google reviews from Hawaii and New York, successfully filtering out ads and spam, demonstrating generalization across datasets.

*Setup Instructions*

git clone https://github.com/prisca-sp/tiktok-techjam-2025-yuhh.git
cd tiktok-techjam-2025-yuhh
Get the Google Local Reviews dataset from McAuley Lab – Google Local Dataset (https://mcauleylab.ucsd.edu/public_datasets/gdrive/googlelocal/) or download from /data

*How To Reproduce Results*

Run the jupyter notebook - however, take note that running the code in batches is preferred to avoid crashing.

