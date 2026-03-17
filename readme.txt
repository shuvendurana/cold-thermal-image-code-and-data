**For without dew point: cold object detection codes\cold object detection dataset500\code.ipynb

**For with dew point: cold object detection codes\cold object detection dataset500 with due point\code.ipynb

‎Title – A Novel Thermal Image Based Approach for Cold Object Detection and Classification Using Machine Learning

‎Description – An overview of the code/dataset.

Dataset Overview (Cold Object Thermal Dataset)

1. Dataset Purpose: The dataset is specifically designed for: Cold object detection and classification, Capturing time-dependent thermal behavior of objects, Enabling machine learning models to learn temperature variation patterns. Unlike traditional thermal datasets (focused on hot objects), this dataset targets low-temperature objects, which are harder to distinguish due to low thermal contrast .

2. Object Categories: The dataset includes multiple types of cold objects:

Categories:

Liquids: Water, Cool Drink, Fruit Juice

Food items: Ice cream, Frozen fruit (apple), Meat (chicken)

Medical products: Medicine

Metals: Iron, Aluminium, Copper

These objects were selected because they exhibit distinct thermal warming patterns over time .

3. Data Collection Process:

Thermal Image Acquisition: Objects stored in refrigerator for 12 hours, Thermal images captured using FLIR C5 camera, Images taken every 10 seconds, Recording continues until object reaches ambient temperature, Controlled environment to reduce noise

4. Feature Extraction(Temperature Data Extraction):

For each thermal image: Pixel-wise temperature map extracted, Cold region detected (lower temperature than background), Mean temperature of object computed, Stored as (time, temperature) pair. This creates a time–temperature sequence per object

5. Dataset Size

Total dataset size: ~7,000 samples, Each sample represents a short thermal sequence (12 zip files and 2 csv files)
**The CSV files are generated using the thermal images : dataset 1 and dataset 2

6. Dataset-1: Each record contains:

Starting Time, Time Gap 1, Time Gap 2, Time Gap 3, Start temp, Gap 1 temp, Gap 2 temp, Gap 3 temp, Class label (Cold Object)

7. Dataset-2: (Enhanced Dataset with Dew Point)

Includes all Dataset-1 features plus: Dew Point Temperature Gap

‎Code Information: After creating the datasets, we have used the basic Machine Learning classification models.

‎Usage Instructions – How to use or load the dataset and code.

the dataset is stored in a file combined_shuffled.csv which is having data of all cold objects. You can load the dataset using the following line of code.

df = pd.read_csv("combined_shuffled.csv")

‎Requirements – pandas, sklearn, matplotlib

‎Methodology (if applicable) – Steps taken for data processing or modeling.

The methodology begins with thermal image acquisition of cold objects under controlled conditions. The captured images are processed to extract temperature values over time, forming time–temperature sequences. A structured dataset is then created using time gaps and corresponding temperature readings. In addition, dew point temperature gap is included to capture environmental effects. The dataset is used to train various machine learning models such as Random Forest, Decision Tree, and XGBoost. Finally, the models are evaluated using performance metrics like accuracy, precision, recall, and F1-score.

‎Citations (if applicable) – This is our own dataset.

‎License & Contribution Guidelines (if applicable). NA


