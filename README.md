# strava-smooth

INTRODUCTION

Export data from the last Strava activity to a gpx file, smoothen the GPS data, and re-upload the activity.

Functionality of the scripts:

-- strava-smooth.py  
Runs the job as described above.

-- exportgpx.py
Retrieves data from the last Strava activity and writes it to a gpx file.
Warning:  This code has only been tested on activities recorded with the Strava Android App.
          Currently only position, time and elevation data are extracted.

-- smoothen.py
Smoothens the data in the gpx file. Currently it uses a simple algorithm written by myself that interpolates between sets of 9 points. More advanced algorithms may be implemented in the future, but it's already a significant improvement over untreated data.

-- stravaup.py
Uploads the the activity.


DEPENDENCIES

The code requires libraries from  
https://github.com/hozn/stravalib  
https://github.com/tkrajina/gpxpy  
For installation directions I refer to the respective repositories.

You need an access token. You can generate it on https://stravacli-dlenski.rhcloud.com/. The code expects the token to be saved according to the instructions on that page.

Stravalib is used to communicate with the Strava API.
Gpxpy is used to play with gpx coordinates

Code has been shamelessly copied from  
https://github.com/dlenski/stravacli  
in order to download and upload Strava activities. Because of relatively large modifications I copied the code. I might prepare a pull request, and if accepted I'll refer to it as a true dependency.

http://andykee.com/visualizing-strava-tracks-with-python.html
The macro presented in this blog posting is used to read and plot gpx files.



