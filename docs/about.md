
---------------------------
## Data Collection and Annotation
---------------------------

One possible approach for data annotation after raw data collection from sensors:

- __Label Studio__
<a href="https://labelstud.io/" target="_blank">Visit Label Studio</a>

![img width="100"](images/pipeline_annotated_TS_TCD.png)

An example of how configuration can be done in label-studio to represent different classes:
```xml
<View>

<Header value="Time Series classification" style="font-weight: normal"/>
        
<Choices name="pattern" toName="ts">
    <Choice value="Left_Prox"/>
</Choices>

<TimeSeriesLabels name="label" toName="ts">
    <Label value="phase_1" background="red"/>
    <Label value="phase_2" background="green"/>
    <Label value="phase_3" background="yellow"/>
    <Label value="phase_4" background="blue"/>
</TimeSeriesLabels>

<TimeSeries name="ts" value="$Left_Prox" valueType="url">
    <Channel column="Left_Prox"/>
</TimeSeries>
   
</View>
```
---------------------------
__How the data looks like after annotation of each phase of a chewing sequence:__

![img width="100"](images/annotated_TS_TCD.png)


---------------------------

---------------------------
# Feature Engineering 
---------------------------

__1. Transforming raw data into features.__

__2. The performance of ML models heavily depends on the relevance of the features used to train them.__

__3. Five processes in feature engineering:__

-->Feature Creation

-->Feature Transformation

-->Feature Extraction

-->Feature Selection

-->Feature Scaling

