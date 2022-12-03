# Simply load, slice, cache, and analyze.
A Fast feature-packed multi-dimensional labeled vector matrix for market data.

Powered by C, Numba, Numpy. Target use is Freqtrade and FreqAI.

The main class of this package, numla, is a LAbeled numpy aRRaY, larry. A larry consists of raw OHLCV data, cascading time series features, and labels. All the data is stored as a NumPy array, the labels as a list of lists (one list per dimension).

# Install & use

pip3 install numla

from numla import larry 

or

import numla as la

>>>>ohlcv = np.array([[1, 2, 3, 4, 5], [6, 7, 8, 9, 10]])

>>>>label = [['open', 'high', 'low', 'close', 'volume'], ['2022-01-17 00:00:00', '2022-01-18 00:00:00']]

>>>>dk = larry(ohlcv, label, dtype=float)

>>>or

>>>>dk = larry(dataframe)

Slice with index values or with labels:

>>>>dk.loc[['close']:4]

Acts like a numpy:

>>>>dk.myta = myta(dk.close)

Methods for built-in fast-ta signals with rolling window statistics:

>>>>dk.SMA(dk.close, timeperiod=50, label="sma")

>>>or for a list of timeperiods

>>>>dk.SMA(dk.close, timeperiod=[50, 100, 200], label="sma")

>>>or for a range of timeperiods

>>>>dk.SMA(dk.close, timeperiod=[10:200], label="sma")

Create train and test numpy arrays with NaN clean data:

>>>>idx_train, idx_test = cross_validation(n, kfold)

>>>>dktrain, dktest = split(dk, idx_train, idx_test)


![8e243b96-c882-441b-9a58-e869ff896b0d_original (2)](https://user-images.githubusercontent.com/13509246/205417536-b5b3798e-02f7-4eb1-8ff7-7c7b8a878e4c.png)

Making life surfable. Surfable Inc.

We are supportive, we don't take things too seriously, and we have a single-minded focus to be "Fast".
