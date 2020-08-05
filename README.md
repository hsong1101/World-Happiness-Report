
## Data Plots

Data used here is from [this Kaggle page](https://www.kaggle.com/PromptCloudHQ/world-happiness-report-2019) which has been released by SDSN and extracted by PromptCloud's custom web crawling solution.


```python
data.head(10)
```




<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country (region)</th>
      <th>Ladder</th>
      <th>SD of Ladder</th>
      <th>Positive affect</th>
      <th>Negative affect</th>
      <th>Social support</th>
      <th>Freedom</th>
      <th>Corruption</th>
      <th>Generosity</th>
      <th>Log of GDP
per capita</th>
      <th>Healthy life
expectancy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Finland</td>
      <td>1</td>
      <td>4</td>
      <td>41.0</td>
      <td>10.0</td>
      <td>2.0</td>
      <td>5.0</td>
      <td>4.0</td>
      <td>47.0</td>
      <td>22.0</td>
      <td>27.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Denmark</td>
      <td>2</td>
      <td>13</td>
      <td>24.0</td>
      <td>26.0</td>
      <td>4.0</td>
      <td>6.0</td>
      <td>3.0</td>
      <td>22.0</td>
      <td>14.0</td>
      <td>23.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Norway</td>
      <td>3</td>
      <td>8</td>
      <td>16.0</td>
      <td>29.0</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>8.0</td>
      <td>11.0</td>
      <td>7.0</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Iceland</td>
      <td>4</td>
      <td>9</td>
      <td>3.0</td>
      <td>3.0</td>
      <td>1.0</td>
      <td>7.0</td>
      <td>45.0</td>
      <td>3.0</td>
      <td>15.0</td>
      <td>13.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Netherlands</td>
      <td>5</td>
      <td>1</td>
      <td>12.0</td>
      <td>25.0</td>
      <td>15.0</td>
      <td>19.0</td>
      <td>12.0</td>
      <td>7.0</td>
      <td>12.0</td>
      <td>18.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Switzerland</td>
      <td>6</td>
      <td>11</td>
      <td>44.0</td>
      <td>21.0</td>
      <td>13.0</td>
      <td>11.0</td>
      <td>7.0</td>
      <td>16.0</td>
      <td>8.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Sweden</td>
      <td>7</td>
      <td>18</td>
      <td>34.0</td>
      <td>8.0</td>
      <td>25.0</td>
      <td>10.0</td>
      <td>6.0</td>
      <td>17.0</td>
      <td>13.0</td>
      <td>17.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>New Zealand</td>
      <td>8</td>
      <td>15</td>
      <td>22.0</td>
      <td>12.0</td>
      <td>5.0</td>
      <td>8.0</td>
      <td>5.0</td>
      <td>8.0</td>
      <td>26.0</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Canada</td>
      <td>9</td>
      <td>23</td>
      <td>18.0</td>
      <td>49.0</td>
      <td>20.0</td>
      <td>9.0</td>
      <td>11.0</td>
      <td>14.0</td>
      <td>19.0</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Austria</td>
      <td>10</td>
      <td>10</td>
      <td>64.0</td>
      <td>24.0</td>
      <td>31.0</td>
      <td>26.0</td>
      <td>19.0</td>
      <td>25.0</td>
      <td>16.0</td>
      <td>15.0</td>
    </tr>
  </tbody>
</table>
</div>



1. <b>Country (region)</b> Name of the country.
2. <b>Ladder</b> is a measure of life satisfaction.
3. <b>SD of Ladder</b> Standard deviation of the ladder.
4. <b>Positive affect</b> Measure of positive emotion.
5. <b>Negative affect</b> Measure of negative emotion.
6. <b>Social support</b> The extent to which Social support contributed to the calculation of the Happiness Score.
7. <b>Freedom</b> The extent to which Freedom contributed to the calculation of the Happiness Score.
8. <b>Corruption</b> The extent to which Perception of Corruption contributes to Happiness Score.
9. <b>Generosity</b> The extent to which Generosity contributed to the calculation of the Happiness Score.
10. <b>Log of GDP per capita</b> The extent to which GDP contributes to the calculation of the Happiness Score.
11. <b>Healthy life expectancy</b> The extent to which Life expectancy contributed to the calculation of the Happiness Score.

Data is sorted in a way the country on top of the dataframe is the happiest while the last is the opposite.


```python
data.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Pos</th>
      <th>Neg</th>
      <th>Social support</th>
      <th>Freedom</th>
      <th>Corruption</th>
      <th>Generosity</th>
      <th>GDP</th>
      <th>Life expectancy</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
      <td>140.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>78.242857</td>
      <td>79.157143</td>
      <td>77.500000</td>
      <td>78.828571</td>
      <td>75.700000</td>
      <td>78.850000</td>
      <td>79.014286</td>
      <td>75.478571</td>
    </tr>
    <tr>
      <th>std</th>
      <td>44.331627</td>
      <td>44.506126</td>
      <td>45.815787</td>
      <td>45.108972</td>
      <td>42.656011</td>
      <td>44.727782</td>
      <td>43.356310</td>
      <td>43.979961</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>40.750000</td>
      <td>40.750000</td>
      <td>36.750000</td>
      <td>39.750000</td>
      <td>39.750000</td>
      <td>40.750000</td>
      <td>41.750000</td>
      <td>36.750000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>78.500000</td>
      <td>78.500000</td>
      <td>77.500000</td>
      <td>79.500000</td>
      <td>76.500000</td>
      <td>79.500000</td>
      <td>78.500000</td>
      <td>77.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>116.250000</td>
      <td>117.250000</td>
      <td>118.250000</td>
      <td>118.250000</td>
      <td>112.250000</td>
      <td>116.250000</td>
      <td>117.250000</td>
      <td>113.250000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>154.000000</td>
      <td>154.000000</td>
      <td>155.000000</td>
      <td>155.000000</td>
      <td>148.000000</td>
      <td>155.000000</td>
      <td>152.000000</td>
      <td>150.000000</td>
    </tr>
  </tbody>
</table>
</div>



[Full Report](https://github.com/hsong1101/Data-Analysis/blob/master/World%20Happiness%20Report/World%20Happiness%20Record.ipynb)
