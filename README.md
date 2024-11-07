All coordinates in J2000.
MW color-excess based on the Schlafly & Finkbeiner 2011 rescaling (0.86) of the Schlegel, Finkbeiner & Davis 1998 dust map at the coordinates of the target.
z_flag is an internal system used to distinguish between spectroscopic (sp), photometric (p), or unknown literature (l) redshifts. z_flags ending with 'u' have an uncertainty.
Tonry r-score for cross-correlation is defined as the ratio between the global maximum and the average of the local maxima in a given redshift domain (Tonry and Davis 1979). Our r-scores are based on the domain spanning 0 <= z < 0.1 sampled every 1e-5.
rchi2_data and fitprob_data describes the reduced chi-squared value or fit probability of the light curve fit based only on the data uncertainties.
rchi2_data_model and fitprob_data_model include data and model uncertainties.

The bandpasses used in this analysis are as follows:
- g: ASAS-SN g
- ztfg: ZTF g
- c: ATLAS cyan
- ztfr: ZTF r
- o: ATLAS orange
- J: WFCAM J

The variant of J photometry refers to the use of a late-time observation in the scene-modeling photometry.
- 2D: Late-time observation used
- 1D3: No late-time observation used
- 0D: No apparent host galaxy

Top level files:
- targets.dat - space-separated columns for TNS name, TNS classification, RA, Dec, MW_EBV, host galaxy RA, host galaxy Dec, host galaxy heliocentric z, host galaxy CMB redshift, z_flag.
- redshifts.dat - space-separated columns for galaxy's SN name, SNIFS/FOCAS, heliocentric z, plus error, minus, Tonry r-score, flag.
- {ebv, max, salt}\_fits.dat - header for model_name, average weighted H0, N, various measures of dispersion, intrinsic dispersion, reduced chi squared value for Hubble residuals. Space separated columns for TNS name, RA, Dec, host galaxy PGC number, host galaxy RA, host galaxy Dec, bandpasses used for fit, variant of J photometry used, calibration (if ebv_fits.dat), MW_EBV
- CSP_fits.dat - Fits to the CSP-I SNe with space-separated columns for SN name, bandpasses used (SNooPy bandpass codes), fit success status, reddening law, fitting parameters

Top level directories:
- Ia
- non_Ia
- unclassified
- non_transient

These directories contains subdirectories for each target, each of which contains
- J_{2D,1D3,0D}.phot - Result files from the scene-modeling photometry code.
- all.phot - all available photometry with space-separated columns for observation MJD, bandpass, flux, flux error, magnitude, magnitude error, zero point, and zero point system
- {ebv,max,salt}\_fits.dat file with columns for bandpasses used for fit, variant of J photometry used, fit success status, reddening law, calibration (if ebv_fits.dat), fitting parameters, reduced chi-squared, fit prob
