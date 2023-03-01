# PET-Diagnostic-Clip
This is a modern remake of the two Commodore Diagnostic Clips

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3934_-_diagnostic_clip_set.JPG" width="300" alt="Diagnostic Clip (complete)"><br>Complete Diagnostic Clip Set

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3933_-_test_in_3016.JPG" width="300" alt="Diagnostic Clip in CBM3016"><br>Diagnostic Clip installed in a CBM3016 (non CRTC machine)

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3827_-_test_clipv2_8032.JPG" width="300" alt="Diagnostic Clip in CBM8032"><br>Diagnostic Clip installed in a CBM8032 (CRTC machine)

# PET Diagnostic Software (40 column, non CRTC):<br>
<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3815_-_diag320350g_start.JPG" width="300" alt="40col non CRTC Start"><br>Opening Screen

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3816_-_diag_320350g_loop1.JPG" width="300" alt="40col non CRTC Tests"><br>Actual tests

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3817_-_diag_320350g_loop2.JPG" width="300" alt="40col non CRTC Tests"><br>Actual tests (continued)



# PET Diagnostic Software (80 column, CRTC):<br>
<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3824_-_80col_diag_v1.1_start.JPG" width="300" alt="80col CRTC Start"><br>Opening Screen

<img src="https://github.com/svenpetersen1965/PET-Diagnostic-Clip/blob/main/PET_Diagnostic_Clip/Rev.%202/Pictures/3826_-_80col_diag_v1.1_loop.JPG" width="300" alt="80col CRTC Tests"><br>Actual tests

# Binaries for the EPROM
The name of the combined file is "80colCRCTv1.1_40colCRCTv2.0_diag3202350g_diag320350g.bin"
it contains:
$0000: 80_col_diagnostic_v1.1.bin                 A[15..12]: 0000 =  ON  ON  ON  ON
$1000: 40_col_diagnostic_v2.0.bin                 A[15..12]: 0000 =  ON  ON  ON  OFF
$2000: 901447-30_diagnostic_320350g_$9000.bin     A[15..12]: 0000 =  ON  ON  OFF ON
$3000: 901447-30_diagnostic_320350g_$9000.bin     A[15..12]: 0000 =  ON  ON  OFF OFF

The Diagnistic 320350g is double. The reason is, the computer would crash if an empty slot is selected. So all slots that are selected with the two low switches of the dip switch. 
