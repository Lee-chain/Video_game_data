```python
import pandas as pd
```


```python
data = pd.read_csv("Video_Games_Sales.csv")
```


```python
data.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Platform</th>
      <th>Year_of_Release</th>
      <th>Genre</th>
      <th>Publisher</th>
      <th>NA_Sales</th>
      <th>EU_Sales</th>
      <th>JP_Sales</th>
      <th>Other_Sales</th>
      <th>Global_Sales</th>
      <th>Critic_Score</th>
      <th>Critic_Count</th>
      <th>User_Score</th>
      <th>User_Count</th>
      <th>Developer</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>Wii Sports</td>
      <td>Wii</td>
      <td>2006.0</td>
      <td>Sports</td>
      <td>Nintendo</td>
      <td>41.36</td>
      <td>28.96</td>
      <td>3.77</td>
      <td>8.45</td>
      <td>82.53</td>
      <td>76.0</td>
      <td>51.0</td>
      <td>8</td>
      <td>322.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>1</td>
      <td>Super Mario Bros.</td>
      <td>NES</td>
      <td>1985.0</td>
      <td>Platform</td>
      <td>Nintendo</td>
      <td>29.08</td>
      <td>3.58</td>
      <td>6.81</td>
      <td>0.77</td>
      <td>40.24</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Mario Kart Wii</td>
      <td>Wii</td>
      <td>2008.0</td>
      <td>Racing</td>
      <td>Nintendo</td>
      <td>15.68</td>
      <td>12.76</td>
      <td>3.79</td>
      <td>3.29</td>
      <td>35.52</td>
      <td>82.0</td>
      <td>73.0</td>
      <td>8.3</td>
      <td>709.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Wii Sports Resort</td>
      <td>Wii</td>
      <td>2009.0</td>
      <td>Sports</td>
      <td>Nintendo</td>
      <td>15.61</td>
      <td>10.93</td>
      <td>3.28</td>
      <td>2.95</td>
      <td>32.77</td>
      <td>80.0</td>
      <td>73.0</td>
      <td>8</td>
      <td>192.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Pokemon Red/Pokemon Blue</td>
      <td>GB</td>
      <td>1996.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>11.27</td>
      <td>8.89</td>
      <td>10.22</td>
      <td>1.00</td>
      <td>31.37</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
# pandas way of filtering
not_nin = data[data["Publisher"] != "Nintendo"]
```


```python
not_nin.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Platform</th>
      <th>Year_of_Release</th>
      <th>Genre</th>
      <th>Publisher</th>
      <th>NA_Sales</th>
      <th>EU_Sales</th>
      <th>JP_Sales</th>
      <th>Other_Sales</th>
      <th>Global_Sales</th>
      <th>Critic_Score</th>
      <th>Critic_Count</th>
      <th>User_Score</th>
      <th>User_Count</th>
      <th>Developer</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>14</td>
      <td>Kinect Adventures!</td>
      <td>X360</td>
      <td>2010.0</td>
      <td>Misc</td>
      <td>Microsoft Game Studios</td>
      <td>15.00</td>
      <td>4.89</td>
      <td>0.24</td>
      <td>1.69</td>
      <td>21.81</td>
      <td>61.0</td>
      <td>45.0</td>
      <td>6.3</td>
      <td>106.0</td>
      <td>Good Science Studio</td>
      <td>E</td>
    </tr>
    <tr>
      <td>16</td>
      <td>Grand Theft Auto V</td>
      <td>PS3</td>
      <td>2013.0</td>
      <td>Action</td>
      <td>Take-Two Interactive</td>
      <td>7.02</td>
      <td>9.09</td>
      <td>0.98</td>
      <td>3.96</td>
      <td>21.04</td>
      <td>97.0</td>
      <td>50.0</td>
      <td>8.2</td>
      <td>3994.0</td>
      <td>Rockstar North</td>
      <td>M</td>
    </tr>
    <tr>
      <td>17</td>
      <td>Grand Theft Auto: San Andreas</td>
      <td>PS2</td>
      <td>2004.0</td>
      <td>Action</td>
      <td>Take-Two Interactive</td>
      <td>9.43</td>
      <td>0.40</td>
      <td>0.41</td>
      <td>10.57</td>
      <td>20.81</td>
      <td>95.0</td>
      <td>80.0</td>
      <td>9</td>
      <td>1588.0</td>
      <td>Rockstar North</td>
      <td>M</td>
    </tr>
    <tr>
      <td>23</td>
      <td>Grand Theft Auto V</td>
      <td>X360</td>
      <td>2013.0</td>
      <td>Action</td>
      <td>Take-Two Interactive</td>
      <td>9.66</td>
      <td>5.14</td>
      <td>0.06</td>
      <td>1.41</td>
      <td>16.27</td>
      <td>97.0</td>
      <td>58.0</td>
      <td>8.1</td>
      <td>3711.0</td>
      <td>Rockstar North</td>
      <td>M</td>
    </tr>
    <tr>
      <td>24</td>
      <td>Grand Theft Auto: Vice City</td>
      <td>PS2</td>
      <td>2002.0</td>
      <td>Action</td>
      <td>Take-Two Interactive</td>
      <td>8.41</td>
      <td>5.49</td>
      <td>0.47</td>
      <td>1.78</td>
      <td>16.15</td>
      <td>95.0</td>
      <td>62.0</td>
      <td>8.7</td>
      <td>730.0</td>
      <td>Rockstar North</td>
      <td>M</td>
    </tr>
  </tbody>
</table>
</div>




```python
data["Platform"].unique()
```




    array(['Wii', 'NES', 'GB', 'DS', 'X360', 'PS3', 'PS2', 'SNES', 'GBA',
           'PS4', '3DS', 'N64', 'PS', 'XB', 'PC', '2600', 'PSP', 'XOne',
           'WiiU', 'GC', 'GEN', 'DC', 'PSV', 'SAT', 'SCD', 'WS', 'NG', 'TG16',
           '3DO', 'GG', 'PCFX'], dtype=object)




```python
set(data["Platform"])
```




    {'2600',
     '3DO',
     '3DS',
     'DC',
     'DS',
     'GB',
     'GBA',
     'GC',
     'GEN',
     'GG',
     'N64',
     'NES',
     'NG',
     'PC',
     'PCFX',
     'PS',
     'PS2',
     'PS3',
     'PS4',
     'PSP',
     'PSV',
     'SAT',
     'SCD',
     'SNES',
     'TG16',
     'WS',
     'Wii',
     'WiiU',
     'X360',
     'XB',
     'XOne'}




```python
fil = data[data["Platform"].isin(["GB", "PSP", "DS", "3DS"])]
```


```python
fil.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Platform</th>
      <th>Year_of_Release</th>
      <th>Genre</th>
      <th>Publisher</th>
      <th>NA_Sales</th>
      <th>EU_Sales</th>
      <th>JP_Sales</th>
      <th>Other_Sales</th>
      <th>Global_Sales</th>
      <th>Critic_Score</th>
      <th>Critic_Count</th>
      <th>User_Score</th>
      <th>User_Count</th>
      <th>Developer</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Pokemon Red/Pokemon Blue</td>
      <td>GB</td>
      <td>1996.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>11.27</td>
      <td>8.89</td>
      <td>10.22</td>
      <td>1.00</td>
      <td>31.37</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Tetris</td>
      <td>GB</td>
      <td>1989.0</td>
      <td>Puzzle</td>
      <td>Nintendo</td>
      <td>23.20</td>
      <td>2.26</td>
      <td>4.22</td>
      <td>0.58</td>
      <td>30.26</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>6</td>
      <td>New Super Mario Bros.</td>
      <td>DS</td>
      <td>2006.0</td>
      <td>Platform</td>
      <td>Nintendo</td>
      <td>11.28</td>
      <td>9.14</td>
      <td>6.50</td>
      <td>2.88</td>
      <td>29.80</td>
      <td>89.0</td>
      <td>65.0</td>
      <td>8.5</td>
      <td>431.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Nintendogs</td>
      <td>DS</td>
      <td>2005.0</td>
      <td>Simulation</td>
      <td>Nintendo</td>
      <td>9.05</td>
      <td>10.95</td>
      <td>1.93</td>
      <td>2.74</td>
      <td>24.67</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Mario Kart DS</td>
      <td>DS</td>
      <td>2005.0</td>
      <td>Racing</td>
      <td>Nintendo</td>
      <td>9.71</td>
      <td>7.47</td>
      <td>4.13</td>
      <td>1.90</td>
      <td>23.21</td>
      <td>91.0</td>
      <td>64.0</td>
      <td>8.6</td>
      <td>464.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Pokemon Gold/Pokemon Silver</td>
      <td>GB</td>
      <td>1999.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>9.00</td>
      <td>6.18</td>
      <td>7.20</td>
      <td>0.71</td>
      <td>23.10</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>19</td>
      <td>Brain Age: Train Your Brain in Minutes a Day</td>
      <td>DS</td>
      <td>2005.0</td>
      <td>Misc</td>
      <td>Nintendo</td>
      <td>4.74</td>
      <td>9.20</td>
      <td>4.16</td>
      <td>2.04</td>
      <td>20.15</td>
      <td>77.0</td>
      <td>58.0</td>
      <td>7.9</td>
      <td>50.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
    <tr>
      <td>20</td>
      <td>Pokemon Diamond/Pokemon Pearl</td>
      <td>DS</td>
      <td>2006.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>6.38</td>
      <td>4.46</td>
      <td>6.04</td>
      <td>1.36</td>
      <td>18.25</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>21</td>
      <td>Super Mario Land</td>
      <td>GB</td>
      <td>1989.0</td>
      <td>Platform</td>
      <td>Nintendo</td>
      <td>10.83</td>
      <td>2.71</td>
      <td>4.18</td>
      <td>0.42</td>
      <td>18.14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>26</td>
      <td>Brain Age 2: More Training in Minutes a Day</td>
      <td>DS</td>
      <td>2005.0</td>
      <td>Puzzle</td>
      <td>Nintendo</td>
      <td>3.43</td>
      <td>5.35</td>
      <td>5.32</td>
      <td>1.18</td>
      <td>15.29</td>
      <td>77.0</td>
      <td>37.0</td>
      <td>7.1</td>
      <td>19.0</td>
      <td>Nintendo</td>
      <td>E</td>
    </tr>
  </tbody>
</table>
</div>




```python
fil1 = data[data["Genre"] == "Role-Playing"]
```


```python
fil1.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Platform</th>
      <th>Year_of_Release</th>
      <th>Genre</th>
      <th>Publisher</th>
      <th>NA_Sales</th>
      <th>EU_Sales</th>
      <th>JP_Sales</th>
      <th>Other_Sales</th>
      <th>Global_Sales</th>
      <th>Critic_Score</th>
      <th>Critic_Count</th>
      <th>User_Score</th>
      <th>User_Count</th>
      <th>Developer</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Pokemon Red/Pokemon Blue</td>
      <td>GB</td>
      <td>1996.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>11.27</td>
      <td>8.89</td>
      <td>10.22</td>
      <td>1.00</td>
      <td>31.37</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Pokemon Gold/Pokemon Silver</td>
      <td>GB</td>
      <td>1999.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>9.00</td>
      <td>6.18</td>
      <td>7.20</td>
      <td>0.71</td>
      <td>23.10</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>20</td>
      <td>Pokemon Diamond/Pokemon Pearl</td>
      <td>DS</td>
      <td>2006.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>6.38</td>
      <td>4.46</td>
      <td>6.04</td>
      <td>1.36</td>
      <td>18.25</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>25</td>
      <td>Pokemon Ruby/Pokemon Sapphire</td>
      <td>GBA</td>
      <td>2002.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>6.06</td>
      <td>3.90</td>
      <td>5.38</td>
      <td>0.50</td>
      <td>15.85</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>27</td>
      <td>Pokemon Black/Pokemon White</td>
      <td>DS</td>
      <td>2010.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>5.51</td>
      <td>3.17</td>
      <td>5.65</td>
      <td>0.80</td>
      <td>15.14</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>30</td>
      <td>Pokémon Yellow: Special Pikachu Edition</td>
      <td>GB</td>
      <td>1998.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>5.89</td>
      <td>5.04</td>
      <td>3.12</td>
      <td>0.59</td>
      <td>14.64</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>33</td>
      <td>Pokemon X/Pokemon Y</td>
      <td>3DS</td>
      <td>2013.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>5.28</td>
      <td>4.19</td>
      <td>4.35</td>
      <td>0.78</td>
      <td>14.60</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>47</td>
      <td>Pokemon Omega Ruby/Pokemon Alpha Sapphire</td>
      <td>3DS</td>
      <td>2014.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>4.35</td>
      <td>3.49</td>
      <td>3.10</td>
      <td>0.74</td>
      <td>11.68</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>58</td>
      <td>Pokemon FireRed/Pokemon LeafGreen</td>
      <td>GBA</td>
      <td>2004.0</td>
      <td>Role-Playing</td>
      <td>Nintendo</td>
      <td>4.34</td>
      <td>2.65</td>
      <td>3.15</td>
      <td>0.35</td>
      <td>10.49</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>65</td>
      <td>Final Fantasy VII</td>
      <td>PS</td>
      <td>1997.0</td>
      <td>Role-Playing</td>
      <td>Sony Computer Entertainment</td>
      <td>3.01</td>
      <td>2.47</td>
      <td>3.28</td>
      <td>0.96</td>
      <td>9.72</td>
      <td>92.0</td>
      <td>20.0</td>
      <td>9.2</td>
      <td>1282.0</td>
      <td>SquareSoft</td>
      <td>T</td>
    </tr>
  </tbody>
</table>
</div>




```python
boo = data["Publisher"].unique()
```


```python
boo
```




    array(['Nintendo', 'Microsoft Game Studios', 'Take-Two Interactive',
           'Sony Computer Entertainment', 'Activision', 'Ubisoft',
           'Bethesda Softworks', 'Electronic Arts', 'Sega', 'SquareSoft',
           'Atari', '505 Games', 'Capcom', 'GT Interactive',
           'Konami Digital Entertainment', 'Square Enix',
           'Sony Computer Entertainment Europe', 'Virgin Interactive',
           'LucasArts', 'Warner Bros. Interactive Entertainment',
           'Universal Interactive', 'Eidos Interactive', 'RedOctane',
           'Vivendi Games', 'Enix Corporation', 'Namco Bandai Games',
           'Palcom', 'Hasbro Interactive', 'THQ', 'Fox Interactive',
           'Acclaim Entertainment', 'MTV Games', 'Disney Interactive Studios',
           nan, 'Codemasters', 'Majesco Entertainment', 'Red Orb', 'Level 5',
           'Arena Entertainment', 'Midway Games', 'JVC', 'Deep Silver',
           'NCSoft', '989 Studios', 'UEP Systems', 'Parker Bros.', 'Maxis',
           'Imagic', 'Tecmo Koei', 'ASCII Entertainment', 'Valve Software',
           'Mindscape', 'Infogrames', 'Unknown', 'Square', 'Valve',
           'Banpresto', 'Hello Games', 'D3Publisher', 'Activision Value',
           'Oxygen Interactive', 'Red Storm Entertainment', 'Video System',
           'Global Star', 'Gotham Games', 'Westwood Studios', 'GungHo',
           'Crave Entertainment', 'Hudson Soft', 'Coleco',
           'Rising Star Games', 'TDK Mediactive', 'ASC Games', 'Accolade',
           'Zoo Games', 'Sony Online Entertainment', '3DO', 'Natsume', 'RTL',
           'Alchemist', 'Black Label Games', 'SouthPeak Games',
           'Focus Home Interactive', 'Ocean', 'Zoo Digital Publishing',
           'Psygnosis', 'City Interactive', 'Empire Interactive', 'Success',
           'Compile', 'Russel', 'Atlus', 'Mastertronic',
           'Slightly Mad Studios', 'Taito', 'Agetec', 'Microprose', 'Play It',
           'GSP', 'Tomy Corporation', 'Sammy Corporation', 'Koch Media',
           'Game Factory', 'Titus', 'Marvelous Entertainment', 'Genki',
           'Mojang', 'CTO SpA', 'TalonSoft', 'Crystal Dynamics',
           'Square Enix ', 'mixi, Inc', 'Pinnacle', 'SCi', 'Quelle',
           'Rage Software', 'Ubisoft Annecy', 'Interplay', 'Scholastic Inc.',
           'Mystique', 'ChunSoft', 'Square EA',
           '20th Century Fox Video Games', 'Hudson Entertainment',
           'Men-A-Vision', 'Nobilis', 'Avanquest Software',
           'Big Ben Interactive', 'Nordic Games', 'Touchstone', 'Spike',
           'Nippon Ichi Software', 'Sony Computer Entertainment America',
           'Jester Interactive', 'LEGO Media', 'Quest', 'Illusion Softworks',
           'Tigervision', 'Rocket Company', 'Metro 3D', 'Mattel Interactive',
           'IE Institute', 'Funbox Media', 'Rondomedia', 'Universal Gamex',
           'Ghostlight', 'Wizard Video Games',
           'BMG Interactive Entertainment', 'PQube', 'Trion Worlds',
           'Xseed Games', 'Laguna', 'Takara', 'Ignition Entertainment',
           'Kadokawa Shoten', 'Enterbrain', 'Imagineer', 'CPG Products',
           'System 3 Arcade Software', 'Aruze Corp', 'Destineer',
           'Gamebridge', 'Midas Interactive Entertainment', 'Jaleco',
           'Answer Software', 'Pack In Soft', 'XS Games', 'Rebellion',
           'Ultravision', 'Harmonix Music Systems', 'Activision Blizzard',
           'Xplosiv', 'Wanadoo', 'Telltale Games', 'NovaLogic', 'Epoch',
           'BAM! Entertainment', 'GameMill Entertainment',
           'Knowledge Adventure', 'Tetris Online', 'Mastiff', 'ESP', 'TYO',
           'Telegames', 'Mud Duck Productions', 'Screenlife', 'Pioneer LDC',
           'Magical Company', 'Kemco', 'Mentor Interactive',
           'Human Entertainment', 'Data Age', 'Electronic Arts Victor',
           'Jack of All Games', 'Avanquest', 'Black Bean Games', '989 Sports',
           'Takara Tomy', 'Media Rings', 'Elf', 'Starfish', 'Zushi Games',
           'Jorudan', 'Destination Software, Inc', 'New',
           'Brash Entertainment', 'Kalypso Media', 'ITT Family Games',
           'Ackkstudios', 'PopCap Games', 'Starpath Corp.', 'BPS',
           'Gathering of Developers', 'NewKidCo', 'Marvelous Interactive',
           'Storm City Games', 'CokeM Interactive', 'P2 Games',
           'CBS Electronics', 'Home Entertainment Suppliers', 'Magix',
           'Arc System Works', 'Angel Studios', 'Wargaming.net', 'Playmates',
           'SNK Playmore', 'Hamster Corporation', 'From Software',
           'Nippon Columbia', 'Nichibutsu', 'Conspiracy Entertainment',
           'Hect', 'Mumbo Jumbo', 'DTP Entertainment',
           'Pacific Century Cyber Works', 'Indie Games', 'Liquid Games',
           'NEC', 'Axela', 'ArtDink', 'Sunsoft', 'Little Orbit', 'FuRyu',
           'Gust', 'SNK', 'NEC Interchannel', 'Nihon Falcom Corporation',
           'Xing Entertainment', 'ValuSoft', 'Victor Interactive',
           'American Softworks', 'Falcom Corporation', 'Detn8 Games', 'Bomb',
           'Nordcurrent', 'Milestone S.r.l.', 'AQ Interactive', 'Sears',
           'Seta Corporation', 'On Demand', 'CCP', 'NCS',
           'Rebellion Developments', 'Agatsuma Entertainment',
           'Gremlin Interactive Ltd', 'Aspyr', 'Compile Heart',
           'Culture Brain', 'Mad Catz', 'Shogakukan', 'Merscom LLC',
           'JoWood Productions', 'Nippon Telenet', 'TDK Core',
           'Kadokawa Games', 'SSI', 'Foreign Media Games', 'Core Design Ltd.',
           'bitComposer Games', 'Astragon', 'Asylum Entertainment',
           'Performance Designed Products', 'UFO Interactive',
           'Essential Games', 'Adeline Software', 'Funcom', 'PlayV',
           'Panther Software', 'Blast! Entertainment Ltd',
           'Playlogic Game Factory', 'DSI Games', 'Avalon Interactive',
           'Game Life', 'Popcorn Arcade', 'Aques', 'System 3', 'Syscom',
           'Vir2L Studios', 'Vatical Entertainment', 'Neko Entertainment',
           'White Park Bay Software', 'Vic Tokai', 'Media Factory',
           'Daedalic', 'Game Arts', 'The Adventure Company', 'EA Games',
           'Acquire', 'Broccoli', 'General Entertainment',
           'Paradox Interactive', 'Yacht Club Games', 'Imadio',
           'Swing! Entertainment', 'Sony Music Entertainment', 'Aqua Plus',
           'Excalibur Publishing', 'Hip Interactive', 'Tripwire Interactive',
           'DreamCatcher Interactive', 'SCS Software', 'Havas Interactive',
           'Sting', 'Idea Factory', 'Telstar', 'U.S. Gold', 'Funsta',
           'DreamWorks Interactive', 'Slitherine Software', 'MTO', 'Graffiti',
           'Tru Blu Entertainment', 'DHM Interactive', 'Crytek', 'FunSoft',
           'Data Design Interactive', 'SPS', 'Moss', 'T&E Soft',
           'NDA Productions', 'Bigben Interactive', 'Data East',
           'Idea Factory International', 'Time Warner Interactive',
           'Gainax Network Systems', 'Daito', 'O3 Entertainment', 'O-Games',
           'Gameloft', 'Xicat Interactive', 'Simon & Schuster Interactive',
           'Valcon Games', 'PopTop Software', 'TOHO', 'PM Studios',
           'Bohemia Interactive', 'Reef Entertainment', '5pb',
           'HMH Interactive', 'inXile Entertainment', 'Cave', 'Microids',
           'Paon', 'CDV Software Entertainment', 'Micro Cabin', 'GameTek',
           'Benesse', 'Type-Moon', 'Enjoy Gaming ltd.', 'Asmik Corp',
           'Interplay Productions', 'Asmik Ace Entertainment', 'Image Epoch',
           'Phantom EFX', 'Evolved Games', 'responDESIGN',
           'Griffin International', 'Culture Publishers', 'Hackberry',
           'Hearty Robin', 'Nippon Amuse', 'Origin Systems', 'Seventh Chord',
           'Abylight', 'Mitsui', 'Insomniac Games', 'Flight-Plan',
           'Milestone', 'Glams', 'Aksys Games', 'Locus', 'Warp',
           'Irem Software Engineering', 'Myelin Media',
           'Global A Entertainment', 'Alternative Software', 'Mercury Games',
           'Sunrise Interactive', 'Elite', 'Evolution Games',
           'Daedalic Entertainment', 'Edia', 'Athena', 'Aria', 'Tivola',
           'Happinet', 'Tommo', 'Altron', 'Revolution Software',
           'Media Works', 'Fortyfive', 'Gamecock', 'Imax', '10TACLE Studios',
           'Groove Games', 'Pack-In-Video', 'Crimson Cow', 'iWin', 'Asgard',
           'Ecole', 'Yumedia', 'Ascaron Entertainment GmbH', 'HAL Laboratory',
           'Phenomedia', 'Grand Prix Games', 'DigiCube', 'Creative Core',
           'Kaga Create', 'WayForward Technologies', 'LSP Games',
           'ASCII Media Works', '1C Company', 'Coconuts Japan', 'Arika',
           'Marvel Entertainment', 'Ertain', 'Prototype', 'Phantagram',
           'The Learning Company', 'TechnoSoft', 'MLB.com', 'Vap', 'Misawa',
           'Yeti', 'Dusenberry Martin Racing', 'Navarre Corp', 'Pow',
           'MediaQuest', 'Team17 Software', 'Max Five', 'Tradewest',
           'Comfort', 'Milestone S.r.l', 'Pony Canyon', 'Riverhillsoft',
           'Summitsoft', 'Playmore', 'Kool Kizz', 'Monte Christo Multimedia',
           'TopWare Interactive', 'Legacy Interactive',
           'Cloud Imperium Games Corporation', 'Flashpoint Games',
           'CyberFront', 'Alawar Entertainment', 'Societa', 'Interchannel',
           'Experience Inc.', 'Sonnet', 'Virtual Play Games', 'Zenrin',
           'Iceberg Interactive', 'Ivolgamus', 'MC2 Entertainment', '2D Boy',
           'Games Workshop', 'Kando Games', 'Office Create',
           'Maximum Family Games', 'Fields', 'Gearbox Software',
           'Princess Soft', 'Extreme Entertainment Group', 'Big Fish Games',
           'Berkeley', 'Mamba Games', 'Fuji', 'FuRyu Corporation',
           'Her Interactive', 'imageepoch Inc.', 'Just Flight', 'Kamui',
           'ASK', 'Cygames', 'Introversion Software', '49Games', 'KSS',
           'dramatic create', 'TGL', 'KID', 'Quinrose', 'Sold Out', 'Encore',
           'G.Rev', 'Sunflowers', 'Headup Games', 'Sweets',
           'Kokopeli Digital Studios', 'id Software', 'Nexon', 'BushiRoad',
           'Devolver Digital', 'Number None', 'Tryfirst', 'GN Software',
           "Yuke's", 'Strategy First', 'Lexicon Entertainment',
           'Paon Corporation', 'Kids Station', 'Licensed 4U', 'GOA',
           '7G//AMES', 'King Records', 'Minato Station',
           'Graphsim Entertainment', 'Easy Interactive', 'Gaga',
           'Yamasa Entertainment', 'Plenty', 'Views', 'Blue Byte', 'fonfun',
           'NetRevo', 'Epic Games', 'Quintet', 'Focus Multimedia',
           'Phoenix Games', 'Marvelous Games', 'Dorart', 'Codemasters Online',
           'Stainless Games', 'Aerosoft', 'Imageworks', 'Karin Entertainment',
           'Technos Japan Corporation', 'Masque Publishing', 'Gakken',
           'New World Computing', 'Mirai Shounen', 'Datam Polystar', 'HuneX',
           'Visco', 'Saurus', 'Revolution (Japan)', 'Giza10', 'Alvion',
           'Giga', 'Mycom', 'Warashi', 'System Soft', 'RED Entertainment',
           'Lighthouse Interactive', 'Michaelsoft', 'Media Entertainment',
           'Genterprise', 'Interworks Unlimited, Inc.', 'Inti Creates',
           'Boost On', 'EON Digital Entertainment', 'Nitroplus', 'Naxat Soft',
           'Piacci', 'Paradox Development', 'Otomate',
           'Ascaron Entertainment', 'Ongakukan', 'Commseed',
           'UIG Entertainment', 'Takuyo', 'Interchannel-Holon',
           'Red Flagship'], dtype=object)




```python
fil2 = data[data["Publisher"].isin(boo[1:11])]
```


```python
fil2.head(2)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Platform</th>
      <th>Year_of_Release</th>
      <th>Genre</th>
      <th>Publisher</th>
      <th>NA_Sales</th>
      <th>EU_Sales</th>
      <th>JP_Sales</th>
      <th>Other_Sales</th>
      <th>Global_Sales</th>
      <th>Critic_Score</th>
      <th>Critic_Count</th>
      <th>User_Score</th>
      <th>User_Count</th>
      <th>Developer</th>
      <th>Rating</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>14</td>
      <td>Kinect Adventures!</td>
      <td>X360</td>
      <td>2010.0</td>
      <td>Misc</td>
      <td>Microsoft Game Studios</td>
      <td>15.00</td>
      <td>4.89</td>
      <td>0.24</td>
      <td>1.69</td>
      <td>21.81</td>
      <td>61.0</td>
      <td>45.0</td>
      <td>6.3</td>
      <td>106.0</td>
      <td>Good Science Studio</td>
      <td>E</td>
    </tr>
    <tr>
      <td>16</td>
      <td>Grand Theft Auto V</td>
      <td>PS3</td>
      <td>2013.0</td>
      <td>Action</td>
      <td>Take-Two Interactive</td>
      <td>7.02</td>
      <td>9.09</td>
      <td>0.98</td>
      <td>3.96</td>
      <td>21.04</td>
      <td>97.0</td>
      <td>50.0</td>
      <td>8.2</td>
      <td>3994.0</td>
      <td>Rockstar North</td>
      <td>M</td>
    </tr>
  </tbody>
</table>
</div>




```python
boo2 = data.groupby(["Platform"])["Platform","JP_Sales"]
```


```python
# get the average of JP_Sales
boo2.mean()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>JP_Sales</th>
    </tr>
    <tr>
      <th>Platform</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>2600</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <td>3DO</td>
      <td>0.033333</td>
    </tr>
    <tr>
      <td>3DS</td>
      <td>0.193596</td>
    </tr>
    <tr>
      <td>DC</td>
      <td>0.164615</td>
    </tr>
    <tr>
      <td>DS</td>
      <td>0.081585</td>
    </tr>
    <tr>
      <td>GB</td>
      <td>0.868571</td>
    </tr>
    <tr>
      <td>GBA</td>
      <td>0.057579</td>
    </tr>
    <tr>
      <td>GC</td>
      <td>0.038813</td>
    </tr>
    <tr>
      <td>GEN</td>
      <td>0.093103</td>
    </tr>
    <tr>
      <td>GG</td>
      <td>0.040000</td>
    </tr>
    <tr>
      <td>N64</td>
      <td>0.107273</td>
    </tr>
    <tr>
      <td>NES</td>
      <td>1.006633</td>
    </tr>
    <tr>
      <td>NG</td>
      <td>0.120000</td>
    </tr>
    <tr>
      <td>PC</td>
      <td>0.000175</td>
    </tr>
    <tr>
      <td>PCFX</td>
      <td>0.030000</td>
    </tr>
    <tr>
      <td>PS</td>
      <td>0.116809</td>
    </tr>
    <tr>
      <td>PS2</td>
      <td>0.064415</td>
    </tr>
    <tr>
      <td>PS3</td>
      <td>0.060248</td>
    </tr>
    <tr>
      <td>PS4</td>
      <td>0.040712</td>
    </tr>
    <tr>
      <td>PSP</td>
      <td>0.063507</td>
    </tr>
    <tr>
      <td>PSV</td>
      <td>0.050764</td>
    </tr>
    <tr>
      <td>SAT</td>
      <td>0.186474</td>
    </tr>
    <tr>
      <td>SCD</td>
      <td>0.075000</td>
    </tr>
    <tr>
      <td>SNES</td>
      <td>0.487657</td>
    </tr>
    <tr>
      <td>TG16</td>
      <td>0.080000</td>
    </tr>
    <tr>
      <td>WS</td>
      <td>0.236667</td>
    </tr>
    <tr>
      <td>Wii</td>
      <td>0.052523</td>
    </tr>
    <tr>
      <td>WiiU</td>
      <td>0.088503</td>
    </tr>
    <tr>
      <td>X360</td>
      <td>0.009849</td>
    </tr>
    <tr>
      <td>XB</td>
      <td>0.001675</td>
    </tr>
    <tr>
      <td>XOne</td>
      <td>0.001377</td>
    </tr>
  </tbody>
</table>
</div>




```python
fil4 = data[data["Platform"].isin(["Wii", "WiiU", "DS", "3DS","PS3", "PS4","X360","XOne"])]
```


```python
pl_jp = fil4.groupby(["Platform"])["Platform","JP_Sales"]
```


```python
ish = pl_jp.mean().reset_index()
```


```python
ish.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Platform</th>
      <th>JP_Sales</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>3DS</td>
      <td>0.193596</td>
    </tr>
    <tr>
      <td>1</td>
      <td>DS</td>
      <td>0.081585</td>
    </tr>
    <tr>
      <td>2</td>
      <td>PS3</td>
      <td>0.060248</td>
    </tr>
    <tr>
      <td>3</td>
      <td>PS4</td>
      <td>0.040712</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Wii</td>
      <td>0.052523</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib.pyplot as plt
```


```python
# makes the graph display within the notebook
%matplotlib inline 
```


```python
plt.style.use("ggplot")
```


```python
plt.figure()
```




    <Figure size 432x288 with 0 Axes>




    <Figure size 432x288 with 0 Axes>



```python
plt.plot(ish["Platform"], ish["JP_Sales"])
```




    [<matplotlib.lines.Line2D at 0x1183af588>]




![png](output_25_1.png)



```python

```
