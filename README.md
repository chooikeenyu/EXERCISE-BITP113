# EXERCISE-BITP113
Programming technique exercises

{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Coding Exercises (Part 2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Full Data Workflow A-Z: Importing Data"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Exercise 10: Importing Data from messy csv-files"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Now, you will have the opportunity to analyze your own dataset. <br>\n",
    "__Follow the instructions__ and insert your code! You are either requested to \n",
    "- Complete the Code and __Fill in the gaps__. Gaps are marked with \"__---__\" and are __placeholders__ for your code fragment. \n",
    "- Write Code completely __on your own__ "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In some exercises, you will find questions that can only be answered, if your code is correct and returns the right output! The correct answer is provided below your coding cell. There you can check whether your code is correct."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "If you need a hint, check the __Hints Section__ at the end of this Notebook. Exercises and Hints are numerated accordingly."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "If you need some further help or if you want to check your code, you can also check the __solutions notebook__."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Have Fun!"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "--------------------------------------------------------------------------------------------------------------"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Option 1: Self_guided"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "__Import__ the cars Dataset from the messy csv-file __cars_raw.csv__ into a Pandas DataFrame. Use appropriate __parameters__ in the __pd.read_csv()__ method to bring the DataFrame into a clean format. __Columns__ should have the following __labels__:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "labels = ['mpg',\n",
    " 'cylinders',\n",
    " 'displacement',\n",
    " 'horsepower',\n",
    " 'weight',\n",
    " 'acceleration',\n",
    " 'model year',\n",
    " 'origin',\n",
    " 'name']"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Finally, __save__ and __export__ the dataset as new csv-file (__cars_imp.csv__)."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "--------------------------------"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Option 2: Guided and Instructed"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# STOP HERE, IF YOU WANT TO DO THE EXERCISE ON YOUR OWN!"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "77. __Import__ Pandas (pd)!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 1,
   "metadata": {},
   "outputs": [],
   "source": [
    "import pandas as pd"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "78. __Import__ the csv-file __cars_raw.csv__ with the appropriate pandas method and __inspect__ the data!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th></th>\n",
       "      <th>Welcome</th>\n",
       "      <th>to</th>\n",
       "      <th>the</th>\n",
       "      <th>cars</th>\n",
       "      <th>Dataset!</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>Feel</th>\n",
       "      <th>free</th>\n",
       "      <th>to</th>\n",
       "      <th>analyze</th>\n",
       "      <th>and</th>\n",
       "      <td>clean</td>\n",
       "      <td>the</td>\n",
       "      <td>messy</td>\n",
       "      <td>Dataset</td>\n",
       "      <td>!</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>18.0</th>\n",
       "      <th>8</th>\n",
       "      <th>307.0</th>\n",
       "      <th>130.0 hp</th>\n",
       "      <th>3504</th>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>15.0</th>\n",
       "      <th>8</th>\n",
       "      <th>350.0</th>\n",
       "      <th>165.0 hp</th>\n",
       "      <th>3693</th>\n",
       "      <td>11.5</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>buick skylark 320</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>18.0</th>\n",
       "      <th>8</th>\n",
       "      <th>318.0</th>\n",
       "      <th>150.0 hp</th>\n",
       "      <th>3436</th>\n",
       "      <td>11.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>plymouth satellite</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>16.0</th>\n",
       "      <th>8</th>\n",
       "      <th>304.0</th>\n",
       "      <th>150.0 hp</th>\n",
       "      <th>3433</th>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>amc rebel sst</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <th>...</th>\n",
       "      <th>...</th>\n",
       "      <th>...</th>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>27.0</th>\n",
       "      <th>4</th>\n",
       "      <th>101.0</th>\n",
       "      <th>83.0 hp</th>\n",
       "      <th>2202</th>\n",
       "      <td>15.3</td>\n",
       "      <td>76</td>\n",
       "      <td>europe</td>\n",
       "      <td>renault 12tl</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>17.0</th>\n",
       "      <th>6</th>\n",
       "      <th>250.0</th>\n",
       "      <th>100.0 hp</th>\n",
       "      <th>3329</th>\n",
       "      <td>15.5</td>\n",
       "      <td>71</td>\n",
       "      <td>usa</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>14.5</th>\n",
       "      <th>8</th>\n",
       "      <th>351.0</th>\n",
       "      <th>152.0 hp</th>\n",
       "      <th>4215</th>\n",
       "      <td>12.8</td>\n",
       "      <td>76</td>\n",
       "      <td>usa</td>\n",
       "      <td>ford gran torino</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>25.0</th>\n",
       "      <th>6</th>\n",
       "      <th>181.0</th>\n",
       "      <th>110.0 hp</th>\n",
       "      <th>2945</th>\n",
       "      <td>16.4</td>\n",
       "      <td>82</td>\n",
       "      <td>usa</td>\n",
       "      <td>buick century limited</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>Thanks</th>\n",
       "      <th>for</th>\n",
       "      <th>analyzing</th>\n",
       "      <th>this</th>\n",
       "      <th>Dataset</th>\n",
       "      <td>!</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "      <td>NaN</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>331 rows × 5 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "                                          Welcome    to            the  \\\n",
       "Feel    free  to         analyze  and       clean   the          messy   \n",
       "18.0   8     307.0      130.0 hp 3504        12.0    70  United States   \n",
       "15.0   8     350.0      165.0 hp 3693        11.5    70  United States   \n",
       "18.0   8     318.0      150.0 hp 3436        11.0    70  United States   \n",
       "16.0   8     304.0      150.0 hp 3433        12.0    70            usa   \n",
       "...                                           ...   ...            ...   \n",
       "27.0   4     101.0      83.0 hp  2202        15.3    76         europe   \n",
       "17.0   6     250.0      100.0 hp 3329        15.5    71            usa   \n",
       "14.5   8     351.0      152.0 hp 4215        12.8    76            usa   \n",
       "25.0   6     181.0      110.0 hp 2945        16.4    82            usa   \n",
       "Thanks  for   analyzing  this     Dataset       !   NaN            NaN   \n",
       "\n",
       "                                                                   cars  \\\n",
       "Feel    free  to         analyze  and                           Dataset   \n",
       "18.0   8     307.0      130.0 hp 3504        chevrolet chevelle malibu    \n",
       "15.0   8     350.0      165.0 hp 3693                buick skylark 320    \n",
       "18.0   8     318.0      150.0 hp 3436               plymouth satellite    \n",
       "16.0   8     304.0      150.0 hp 3433                    amc rebel sst    \n",
       "...                                                                 ...   \n",
       "27.0   4     101.0      83.0 hp  2202                     renault 12tl    \n",
       "17.0   6     250.0      100.0 hp 3329        chevrolet chevelle malibu    \n",
       "14.5   8     351.0      152.0 hp 4215                 ford gran torino    \n",
       "25.0   6     181.0      110.0 hp 2945            buick century limited    \n",
       "Thanks  for   analyzing  this     Dataset                           NaN   \n",
       "\n",
       "                                           Dataset!  \n",
       "Feel    free  to         analyze  and             !  \n",
       "18.0   8     307.0      130.0 hp 3504           NaN  \n",
       "15.0   8     350.0      165.0 hp 3693           NaN  \n",
       "18.0   8     318.0      150.0 hp 3436           NaN  \n",
       "16.0   8     304.0      150.0 hp 3433           NaN  \n",
       "...                                             ...  \n",
       "27.0   4     101.0      83.0 hp  2202           NaN  \n",
       "17.0   6     250.0      100.0 hp 3329           NaN  \n",
       "14.5   8     351.0      152.0 hp 4215           NaN  \n",
       "25.0   6     181.0      110.0 hp 2945           NaN  \n",
       "Thanks  for   analyzing  this     Dataset       NaN  \n",
       "\n",
       "[331 rows x 5 columns]"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "pd.read_csv(\"cars_raw.csv\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Use appropriate __parameters__ in the __pd.read_csv()__ method to clean the format. The following issues need to be solved:"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "79. __Remove__ the __first row(s)__ containing nonsense content."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "80. __Remove__ the __last row(s)__ containing nonsense content."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "81. Define that there are __no appropriate column labels/headers__ in the data. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "82. __Set__ the following __column labels/headers__:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "metadata": {},
   "outputs": [],
   "source": [
    "labels = ['mpg',\n",
    " 'cylinders',\n",
    " 'displacement',\n",
    " 'horsepower',\n",
    " 'weight',\n",
    " 'acceleration',\n",
    " 'model year',\n",
    " 'origin',\n",
    " 'name']"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 6,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "<ipython-input-6-45c45b65d742>:2: ParserWarning: Falling back to the 'python' engine because the 'c' engine does not support skipfooter; you can avoid this warning by specifying engine='python'.\n",
      "  pd.read_csv(\"cars_raw.csv\", skiprows= 2, skipfooter= 1, header = None, names = labels)\n"
     ]
    },
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>mpg</th>\n",
       "      <th>cylinders</th>\n",
       "      <th>displacement</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>weight</th>\n",
       "      <th>acceleration</th>\n",
       "      <th>model year</th>\n",
       "      <th>origin</th>\n",
       "      <th>name</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>307.0</td>\n",
       "      <td>130.0 hp</td>\n",
       "      <td>3504</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>15.0</td>\n",
       "      <td>8</td>\n",
       "      <td>350.0</td>\n",
       "      <td>165.0 hp</td>\n",
       "      <td>3693</td>\n",
       "      <td>11.5</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>buick skylark 320</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>318.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3436</td>\n",
       "      <td>11.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>plymouth satellite</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>16.0</td>\n",
       "      <td>8</td>\n",
       "      <td>304.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3433</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>amc rebel sst</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>17.0</td>\n",
       "      <td>8</td>\n",
       "      <td>302.0</td>\n",
       "      <td>140.0 hp</td>\n",
       "      <td>3449</td>\n",
       "      <td>10.5</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>FORD TORINO</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>324</th>\n",
       "      <td>12.0</td>\n",
       "      <td>8</td>\n",
       "      <td>429.0</td>\n",
       "      <td>198.0 hp</td>\n",
       "      <td>4952</td>\n",
       "      <td>11.5</td>\n",
       "      <td>73</td>\n",
       "      <td>usa</td>\n",
       "      <td>mercury marquis brougham</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>325</th>\n",
       "      <td>27.0</td>\n",
       "      <td>4</td>\n",
       "      <td>101.0</td>\n",
       "      <td>83.0 hp</td>\n",
       "      <td>2202</td>\n",
       "      <td>15.3</td>\n",
       "      <td>76</td>\n",
       "      <td>europe</td>\n",
       "      <td>renault 12tl</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>326</th>\n",
       "      <td>17.0</td>\n",
       "      <td>6</td>\n",
       "      <td>250.0</td>\n",
       "      <td>100.0 hp</td>\n",
       "      <td>3329</td>\n",
       "      <td>15.5</td>\n",
       "      <td>71</td>\n",
       "      <td>usa</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>327</th>\n",
       "      <td>14.5</td>\n",
       "      <td>8</td>\n",
       "      <td>351.0</td>\n",
       "      <td>152.0 hp</td>\n",
       "      <td>4215</td>\n",
       "      <td>12.8</td>\n",
       "      <td>76</td>\n",
       "      <td>usa</td>\n",
       "      <td>ford gran torino</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>328</th>\n",
       "      <td>25.0</td>\n",
       "      <td>6</td>\n",
       "      <td>181.0</td>\n",
       "      <td>110.0 hp</td>\n",
       "      <td>2945</td>\n",
       "      <td>16.4</td>\n",
       "      <td>82</td>\n",
       "      <td>usa</td>\n",
       "      <td>buick century limited</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>329 rows × 9 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "      mpg  cylinders  displacement horsepower  weight  acceleration  \\\n",
       "0    18.0          8         307.0   130.0 hp    3504          12.0   \n",
       "1    15.0          8         350.0   165.0 hp    3693          11.5   \n",
       "2    18.0          8         318.0   150.0 hp    3436          11.0   \n",
       "3    16.0          8         304.0   150.0 hp    3433          12.0   \n",
       "4    17.0          8         302.0   140.0 hp    3449          10.5   \n",
       "..    ...        ...           ...        ...     ...           ...   \n",
       "324  12.0          8         429.0   198.0 hp    4952          11.5   \n",
       "325  27.0          4         101.0    83.0 hp    2202          15.3   \n",
       "326  17.0          6         250.0   100.0 hp    3329          15.5   \n",
       "327  14.5          8         351.0   152.0 hp    4215          12.8   \n",
       "328  25.0          6         181.0   110.0 hp    2945          16.4   \n",
       "\n",
       "     model year         origin                          name  \n",
       "0            70  United States    chevrolet chevelle malibu   \n",
       "1            70  United States            buick skylark 320   \n",
       "2            70  United States           plymouth satellite   \n",
       "3            70            usa                amc rebel sst   \n",
       "4            70            usa                  FORD TORINO   \n",
       "..          ...            ...                           ...  \n",
       "324          73            usa     mercury marquis brougham   \n",
       "325          76         europe                 renault 12tl   \n",
       "326          71            usa    chevrolet chevelle malibu   \n",
       "327          76            usa             ford gran torino   \n",
       "328          82            usa        buick century limited   \n",
       "\n",
       "[329 rows x 9 columns]"
      ]
     },
     "execution_count": 6,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#complete the code and run the cell!\n",
    "pd.read_csv(\"cars_raw.csv\", skiprows= 2, skipfooter= 1, header = None, names = labels)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "83. Once you are happy with the import, __save__ the DataFrame in the variable __cars__!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 7,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "<ipython-input-7-750bd20fbbf4>:2: ParserWarning: Falling back to the 'python' engine because the 'c' engine does not support skipfooter; you can avoid this warning by specifying engine='python'.\n",
      "  cars = pd.read_csv(\"cars_raw.csv\", skiprows= 2, skipfooter= 1, header = None, names = labels)\n"
     ]
    }
   ],
   "source": [
    "#complete the code and run the cell!\n",
    "cars = pd.read_csv(\"cars_raw.csv\", skiprows= 2, skipfooter= 1, header = None, names = labels)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 8,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>mpg</th>\n",
       "      <th>cylinders</th>\n",
       "      <th>displacement</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>weight</th>\n",
       "      <th>acceleration</th>\n",
       "      <th>model year</th>\n",
       "      <th>origin</th>\n",
       "      <th>name</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>307.0</td>\n",
       "      <td>130.0 hp</td>\n",
       "      <td>3504</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>15.0</td>\n",
       "      <td>8</td>\n",
       "      <td>350.0</td>\n",
       "      <td>165.0 hp</td>\n",
       "      <td>3693</td>\n",
       "      <td>11.5</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>buick skylark 320</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>318.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3436</td>\n",
       "      <td>11.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>plymouth satellite</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>16.0</td>\n",
       "      <td>8</td>\n",
       "      <td>304.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3433</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>amc rebel sst</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>17.0</td>\n",
       "      <td>8</td>\n",
       "      <td>302.0</td>\n",
       "      <td>140.0 hp</td>\n",
       "      <td>3449</td>\n",
       "      <td>10.5</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>FORD TORINO</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "    mpg  cylinders  displacement horsepower  weight  acceleration  model year  \\\n",
       "0  18.0          8         307.0   130.0 hp    3504          12.0          70   \n",
       "1  15.0          8         350.0   165.0 hp    3693          11.5          70   \n",
       "2  18.0          8         318.0   150.0 hp    3436          11.0          70   \n",
       "3  16.0          8         304.0   150.0 hp    3433          12.0          70   \n",
       "4  17.0          8         302.0   140.0 hp    3449          10.5          70   \n",
       "\n",
       "          origin                          name  \n",
       "0  United States    chevrolet chevelle malibu   \n",
       "1  United States            buick skylark 320   \n",
       "2  United States           plymouth satellite   \n",
       "3            usa                amc rebel sst   \n",
       "4            usa                  FORD TORINO   "
      ]
     },
     "execution_count": 8,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# run the cell!\n",
    "cars.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 9,
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>mpg</th>\n",
       "      <th>cylinders</th>\n",
       "      <th>displacement</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>weight</th>\n",
       "      <th>acceleration</th>\n",
       "      <th>model year</th>\n",
       "      <th>origin</th>\n",
       "      <th>name</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>324</th>\n",
       "      <td>12.0</td>\n",
       "      <td>8</td>\n",
       "      <td>429.0</td>\n",
       "      <td>198.0 hp</td>\n",
       "      <td>4952</td>\n",
       "      <td>11.5</td>\n",
       "      <td>73</td>\n",
       "      <td>usa</td>\n",
       "      <td>mercury marquis brougham</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>325</th>\n",
       "      <td>27.0</td>\n",
       "      <td>4</td>\n",
       "      <td>101.0</td>\n",
       "      <td>83.0 hp</td>\n",
       "      <td>2202</td>\n",
       "      <td>15.3</td>\n",
       "      <td>76</td>\n",
       "      <td>europe</td>\n",
       "      <td>renault 12tl</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>326</th>\n",
       "      <td>17.0</td>\n",
       "      <td>6</td>\n",
       "      <td>250.0</td>\n",
       "      <td>100.0 hp</td>\n",
       "      <td>3329</td>\n",
       "      <td>15.5</td>\n",
       "      <td>71</td>\n",
       "      <td>usa</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>327</th>\n",
       "      <td>14.5</td>\n",
       "      <td>8</td>\n",
       "      <td>351.0</td>\n",
       "      <td>152.0 hp</td>\n",
       "      <td>4215</td>\n",
       "      <td>12.8</td>\n",
       "      <td>76</td>\n",
       "      <td>usa</td>\n",
       "      <td>ford gran torino</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>328</th>\n",
       "      <td>25.0</td>\n",
       "      <td>6</td>\n",
       "      <td>181.0</td>\n",
       "      <td>110.0 hp</td>\n",
       "      <td>2945</td>\n",
       "      <td>16.4</td>\n",
       "      <td>82</td>\n",
       "      <td>usa</td>\n",
       "      <td>buick century limited</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "</div>"
      ],
      "text/plain": [
       "      mpg  cylinders  displacement horsepower  weight  acceleration  \\\n",
       "324  12.0          8         429.0   198.0 hp    4952          11.5   \n",
       "325  27.0          4         101.0    83.0 hp    2202          15.3   \n",
       "326  17.0          6         250.0   100.0 hp    3329          15.5   \n",
       "327  14.5          8         351.0   152.0 hp    4215          12.8   \n",
       "328  25.0          6         181.0   110.0 hp    2945          16.4   \n",
       "\n",
       "     model year  origin                          name  \n",
       "324          73     usa     mercury marquis brougham   \n",
       "325          76  europe                 renault 12tl   \n",
       "326          71     usa    chevrolet chevelle malibu   \n",
       "327          76     usa             ford gran torino   \n",
       "328          82     usa        buick century limited   "
      ]
     },
     "execution_count": 9,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "# run the cell!\n",
    "cars.tail()"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "84. __Export__ and __save__ cars as new csv-file (__cars_imp.csv__). Do __not__ export any __RangeIndex__!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 10,
   "metadata": {},
   "outputs": [],
   "source": [
    "cars.to_csv(\"cars_imp.csv\", index= False)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "__Reimport__ cars_imp.csv and check!"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 11,
   "metadata": {
    "scrolled": true
   },
   "outputs": [
    {
     "data": {
      "text/html": [
       "<div>\n",
       "<style scoped>\n",
       "    .dataframe tbody tr th:only-of-type {\n",
       "        vertical-align: middle;\n",
       "    }\n",
       "\n",
       "    .dataframe tbody tr th {\n",
       "        vertical-align: top;\n",
       "    }\n",
       "\n",
       "    .dataframe thead th {\n",
       "        text-align: right;\n",
       "    }\n",
       "</style>\n",
       "<table border=\"1\" class=\"dataframe\">\n",
       "  <thead>\n",
       "    <tr style=\"text-align: right;\">\n",
       "      <th></th>\n",
       "      <th>mpg</th>\n",
       "      <th>cylinders</th>\n",
       "      <th>displacement</th>\n",
       "      <th>horsepower</th>\n",
       "      <th>weight</th>\n",
       "      <th>acceleration</th>\n",
       "      <th>model year</th>\n",
       "      <th>origin</th>\n",
       "      <th>name</th>\n",
       "    </tr>\n",
       "  </thead>\n",
       "  <tbody>\n",
       "    <tr>\n",
       "      <th>0</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>307.0</td>\n",
       "      <td>130.0 hp</td>\n",
       "      <td>3504</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>1</th>\n",
       "      <td>15.0</td>\n",
       "      <td>8</td>\n",
       "      <td>350.0</td>\n",
       "      <td>165.0 hp</td>\n",
       "      <td>3693</td>\n",
       "      <td>11.5</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>buick skylark 320</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>2</th>\n",
       "      <td>18.0</td>\n",
       "      <td>8</td>\n",
       "      <td>318.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3436</td>\n",
       "      <td>11.0</td>\n",
       "      <td>70</td>\n",
       "      <td>United States</td>\n",
       "      <td>plymouth satellite</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>3</th>\n",
       "      <td>16.0</td>\n",
       "      <td>8</td>\n",
       "      <td>304.0</td>\n",
       "      <td>150.0 hp</td>\n",
       "      <td>3433</td>\n",
       "      <td>12.0</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>amc rebel sst</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>4</th>\n",
       "      <td>17.0</td>\n",
       "      <td>8</td>\n",
       "      <td>302.0</td>\n",
       "      <td>140.0 hp</td>\n",
       "      <td>3449</td>\n",
       "      <td>10.5</td>\n",
       "      <td>70</td>\n",
       "      <td>usa</td>\n",
       "      <td>FORD TORINO</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>...</th>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "      <td>...</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>324</th>\n",
       "      <td>12.0</td>\n",
       "      <td>8</td>\n",
       "      <td>429.0</td>\n",
       "      <td>198.0 hp</td>\n",
       "      <td>4952</td>\n",
       "      <td>11.5</td>\n",
       "      <td>73</td>\n",
       "      <td>usa</td>\n",
       "      <td>mercury marquis brougham</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>325</th>\n",
       "      <td>27.0</td>\n",
       "      <td>4</td>\n",
       "      <td>101.0</td>\n",
       "      <td>83.0 hp</td>\n",
       "      <td>2202</td>\n",
       "      <td>15.3</td>\n",
       "      <td>76</td>\n",
       "      <td>europe</td>\n",
       "      <td>renault 12tl</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>326</th>\n",
       "      <td>17.0</td>\n",
       "      <td>6</td>\n",
       "      <td>250.0</td>\n",
       "      <td>100.0 hp</td>\n",
       "      <td>3329</td>\n",
       "      <td>15.5</td>\n",
       "      <td>71</td>\n",
       "      <td>usa</td>\n",
       "      <td>chevrolet chevelle malibu</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>327</th>\n",
       "      <td>14.5</td>\n",
       "      <td>8</td>\n",
       "      <td>351.0</td>\n",
       "      <td>152.0 hp</td>\n",
       "      <td>4215</td>\n",
       "      <td>12.8</td>\n",
       "      <td>76</td>\n",
       "      <td>usa</td>\n",
       "      <td>ford gran torino</td>\n",
       "    </tr>\n",
       "    <tr>\n",
       "      <th>328</th>\n",
       "      <td>25.0</td>\n",
       "      <td>6</td>\n",
       "      <td>181.0</td>\n",
       "      <td>110.0 hp</td>\n",
       "      <td>2945</td>\n",
       "      <td>16.4</td>\n",
       "      <td>82</td>\n",
       "      <td>usa</td>\n",
       "      <td>buick century limited</td>\n",
       "    </tr>\n",
       "  </tbody>\n",
       "</table>\n",
       "<p>329 rows × 9 columns</p>\n",
       "</div>"
      ],
      "text/plain": [
       "      mpg  cylinders  displacement horsepower  weight  acceleration  \\\n",
       "0    18.0          8         307.0   130.0 hp    3504          12.0   \n",
       "1    15.0          8         350.0   165.0 hp    3693          11.5   \n",
       "2    18.0          8         318.0   150.0 hp    3436          11.0   \n",
       "3    16.0          8         304.0   150.0 hp    3433          12.0   \n",
       "4    17.0          8         302.0   140.0 hp    3449          10.5   \n",
       "..    ...        ...           ...        ...     ...           ...   \n",
       "324  12.0          8         429.0   198.0 hp    4952          11.5   \n",
       "325  27.0          4         101.0    83.0 hp    2202          15.3   \n",
       "326  17.0          6         250.0   100.0 hp    3329          15.5   \n",
       "327  14.5          8         351.0   152.0 hp    4215          12.8   \n",
       "328  25.0          6         181.0   110.0 hp    2945          16.4   \n",
       "\n",
       "     model year         origin                          name  \n",
       "0            70  United States    chevrolet chevelle malibu   \n",
       "1            70  United States            buick skylark 320   \n",
       "2            70  United States           plymouth satellite   \n",
       "3            70            usa                amc rebel sst   \n",
       "4            70            usa                  FORD TORINO   \n",
       "..          ...            ...                           ...  \n",
       "324          73            usa     mercury marquis brougham   \n",
       "325          76         europe                 renault 12tl   \n",
       "326          71            usa    chevrolet chevelle malibu   \n",
       "327          76            usa             ford gran torino   \n",
       "328          82            usa        buick century limited   \n",
       "\n",
       "[329 rows x 9 columns]"
      ]
     },
     "execution_count": 11,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "#run the cell!\n",
    "pd.read_csv(\"cars_imp.csv\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Well Done!"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "----------------------------"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Hints (Spoiler!)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "77. at this point, you should know this ;-) !"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "78. pd.read_csv(\"filename\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "79. parameter skiprows"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "80. parameter skipfooter"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "81. header = N---"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "82. parameter names"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "83. see hints 79-82"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "84. to_csv() method"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
