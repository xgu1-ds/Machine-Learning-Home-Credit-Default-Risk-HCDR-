The data consists of a mix of numerical features and categorical features. 
However, there are no columns with ‘text’ data. Based on an initial 
inspection of the data, we can see that there are missing values in a 
significant number of columns and will require imputing. Also, combining 
features from different datasets will require custom transformations.

Following pipelines will be used in the workflow:

* **Numerical pipeline** - This pipeline will include but not limited to 
  scaling of numerical features using StandardScaler() and imputing 
  missing values using SimpleImputer().
* **Categorial pipeline** - This pipeline will inlcude but not limited to 
  encoding categorical features using OneHotEncoding() and imputing 
  missing values using SimpleImputer().
* **Pre-Processing pipeline** - A prep-processing step will combine the 
  numerical and categorical pipeline and also include steps to 
  transform different columns, feature engineering wo add new features 
  from different datastes. The pipeline will be built using 
  ColumnTransformer() and will include custom transformation steps which 
  can be fed into the pipeline directly.
* **Model pipeline** - Finally the model pipeline will combine above 
  created pre-processing pipeline and the actual algorithm being 
  used for classification. 
  
Data will be fitted into the final model pipeline and transformed 
accordingly and used for evaluating the different models.

