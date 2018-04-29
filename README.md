# ECG Process
Quick shell script to preprocess Atrial Fibrillation Database.

## Usage
* Create raw folder
* Download [afdb](https://physionet.org/physiobank/database/afdb/) and [nsrdb](https://physionet.org/physiobank/database/nsrdb/)
and them move them all to raw folder
* To generate image from csv:
```
./gnuplot -e "fileIn='<input csv>'; fileOut='<output image>'" csv2img.gnuplot
Eg: gnuplot -e "fileIn='csv/04015.csv'; fileOut='uploads/04015.png'" csv2img.gnuplot
```
* To convert all raw data to csv and image (include above step already):
```
./raws2img
```

* To convert single file to csv and image:
```
./raw2img <filename without extension>
Eg: ./raw2img 04015
```

* To convert image to csv:
```
python img2csv.py '<full path to file>'
Eg: python img2csv.py '/Users/nhict/Desktop/ecg-process/uploads/04015.png'
```
