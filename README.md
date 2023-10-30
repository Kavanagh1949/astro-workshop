Using Python and Astropy for Astronomical Data Analysis
=======================================================
*Workshop at the 112th Annual Meeting of the American Association of Variable Star Observers, Boston, MA*

* **DATE:** Fri, Nov 2, 2023
* **TIME:** 9AM to 4PM Eastern Daylight Time
* **LOCATION:** The Row Hotel/zoom

## PRE-WORKSHOP SETUP
Please be sure your laptop is properly configured before the workshop by following the
[installation and setup instructions](00-Install_and_Setup).

This could take as long as *one hour* depending on your current configuration and internet speeds.
DO NOT WAIT UNTIL THE DAY OF THE WORKSHOP.

If your setup is not working at the workshop, we will have a cloud option for you.

## Schedule (workshop begins at 9:00AM EDT; all times below are EDT)

1. (0:00) Python overview and installation options
2. (0:10) Getting your data into Python
    1. Astropy tables (25 min)
    2. Pandas dataframes → Astropy table (5 min)
3. (0:30) Fundamental concepts
    1. Times and Coordinates (20 min)
    1. Time series (10 min)
4. (1:00) Break -- 5 min
5. (1:05) Getting images into Python
    1. CCDData to read images (10 min)
    1. astrowidgets to display images interactively (10 min) (**)
6. (1:30) Plotting time series data
    1. Intro (10 min) (****)
    2. More complicated plots (20 min)
7. (2:00) Break -- 10 min
8. (2:10) More time series -- lightkurve
9. (2:30) Using external catalogs/web services (***)
    1. Intro to astroquery (10 min)
    2. Retrieving data from Vizier (15 min)
    3. astrometry.net (5 min)
10. (3:00) Lunch
11. (4:00) Other catalogs/web services
    1. Gaia/TESS/Kepler (15 min)
12. (4:15) Photometry with photutils (****)
    1. Detecting/centering sources (15 min)
    1. Aperture photometry (20 min)
    1. PSF photometry (10 min)
13. (5:00) Break -- 5 min
14. (5:05) Light curve analysis (***)
    1. Periodograms with Astropy (20 min)
    2. Periodograms with Pyriod (15 min) (maybe????)
    3. Exoplanet light cures with EXOTIC (5 min)
15. (5:45) Break -- 10 min
16. (5:55) Higher-level options
    1. ccdproc or reducer for calibrating data (15 min) (**)
    2. stellarphot for photometry and some analysis (25 min)
    3. Planning observations with astroplan (10 min)
1. (6:45) Open time/questions

### Presenter

Matt Craig, Professor, Department of Physics and Astronomy, Minnesota State University Moorhead

### Additional Helpers

* Bert Pablo, AAVSO Staff Astronomer
* Moritz Günther, Research Scientist, Chandra X-ray Center
* Mara DeRung, student, Minnesota State University Moorhead
* Abigail Moen, student, Minnesota State University Moorhead
* Emily Watson, student, Minnesota State University Moorhead
* Tanner Weyer, student, Minnesota State University Moorhead

## Description
This workshop covers the use of Python tools for astronomical data analysis and visualization, with the focus primarily
on UV, Optical, and IR data. Data analysis tools for JWST are being written in Python and distributed as part of Astropy,
a community developed Python library for astronomy, and its affiliated packages.

The workshop goals introduce you to the variety of tools which are already available inside the Astropy library as
well as provide ample hands-on time during which you’ll be able to explore the science analysis capabilities which the
greater Python environment and community provide.

Some basic Python experience is highly recommended to be able to effectively participate in the exercises,
but those without Python experience will still get much useful information about the capabilities for data analysis in
Python and perhaps pick up some pointers on where they can get started learning more scientific Python and integrating
it into their work flow.

If you would like to get a head start with the tools we will be concentrating on you can check out their documentation on readthedocs:

* [Physical Units and Quantities](https://docs.astropy.org/en/stable/units/index.html)
* [Constants](https://docs.astropy.org/en/stable/constants/index.html)
* [Coordinate utilities](https://docs.astropy.org/en/stable/coordinates/index.html)
* [Basics on accessing data files, both FITS and ASCII tables](https://docs.astropy.org/en/stable/io/unified.html)
* [Modeling and Fitting](https://docs.astropy.org/en/stable/modeling/index.html)
* [Astropy WCS](https://docs.astropy.org/en/stable/wcs/index.html)
* [photutils](https://photutils.readthedocs.io/)
* [specutils](https://specutils.readthedocs.io/)
* [ccdproc package documentation](https://ccdproc.readthedocs.io/en/latest/) and a more [extended guide to image reduction with ccdproc](https://github.com/astropy/ccd-reduction-and-photometry-guide)
* [Contributing to Astropy](https://docs.astropy.org/en/stable/development/workflow/development_workflow.html)
* [Affiliated Packages](https://www.astropy.org/affiliated/)

* Other tools we can answer questions about but probably won't discuss explicitly:
  * [Numpy](https://numpy.org/)
  * [Scipy](https://www.scipy.org/)
  * [Jupyter](https://jupyter.org/)
  * [Git and Github](https://guides.github.com/activities/hello-world/)
  * [Git branching](https://learngitbranching.js.org/)

## Problems or Questions?

We encourage you to submit any problems or questions you have to this
repository [issue tracker](https://github.com/astropy/astropy-workshop/issues)
by choosing the "Question from workshop participant" issue template.

## Past Workshops

Materials from past workshops can be found in other branches on this repo and in the [past-astropy-workshops repo](https://github.com/astropy/past-astropy-workshops).
