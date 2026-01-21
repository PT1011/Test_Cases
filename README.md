# TikTok Video Upload - Test Cases

---

## Test Case 1

**Test Case ID:** TTK_UPLOAD_001  
**Title:** Verify Successful Upload of MOV File  
**Requirement:** System must accept MOV format videos within size and length limits  
**Test Type:** Positive  

### Preconditions
- User has navigated to the upload screen  
- Valid test video file (MOV) is available on device  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 100 MB  
- **Length:** 1 minute  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "67"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Success message: *“Your video has been posted!”*  
- Video appears in user’s profile  
- Video is playable  
- Caption displays correctly  

**Priority:** High (core functionality)

---

## Test Case 2

**Test Case ID:** TTK_UPLOAD_002  
**Title:** Verify Successful Upload of AVI File  
**Requirement:** System must accept AVI format videos within size and length limits  
**Test Type:** Positive  

### Preconditions
- User has navigated to the upload screen  
- Valid test video file (AVI) is available on device  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_videoAVI.avi`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_videoAVI.avi  
- **Format:** AVI  
- **Size:** 67 MB  
- **Length:** 67 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "6767"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Success message: *“Your video has been posted!”*  
- Video appears in user’s profile  
- Video is playable  
- Caption displays correctly  

**Priority:** High (core functionality)

---

## Test Case 3

**Test Case ID:** TTK_UPLOAD_003  
**Title:** Video Length is Under Minimum  
**Requirement:** System must have a minimum video length limit of 3 seconds  
**Test Type:** Negative  

### Preconditions
- User is about to upload a video of correct file type but incorrect length  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 100 MB  
- **Length:** 2.32 seconds  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "67"  

### Expected Result
- Video does not upload successfully  
- System notifies user of video length requirements  
- System returns user to upload page  

**Priority:** Medium

---

## Test Case 4

**Test Case ID:** TTK_UPLOAD_004  
**Title:** Attempting to Upload a Video of Unsupported Format  
**Requirement:** System must not accept JPG file types when uploading a video  
**Test Type:** Negative  

### Preconditions
- User is about to upload a file of incorrect type  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test image file `test_image.jpg`  
4. Tap "Next"  
5. Add caption: `67`  
6. Tap "Post"  

### Test Data
- **File:** test_image.jpg  
- **Format:** JPG  
- **Size:** 100 MB  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "67"  

### Expected Result
- Upload fails  
- System notifies user of invalid file type  
- System provides directions for uploading images  
- User is returned to upload screen  

**Priority:** Medium

---

## Test Case 5

**Test Case ID:** TTK_UPLOAD_005  
**Title:** Verify That a Video of Acceptable Length is Successfully Uploaded  
**Requirement:** System allows videos from 3 seconds to 10 minutes  
**Test Type:** Boundary  

### Preconditions
- User is uploading a video of acceptable length  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 100 MB  
- **Length:** 2 minutes  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "67"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Success message displayed  
- Video is playable and visible on profile  

**Priority:** High

---

## Test Case 6

**Test Case ID:** TTK_UPLOAD_006  
**Title:** Verify That a Video of Acceptable File Size is Successfully Uploaded  
**Requirement:** System enforces file size limits  
**Test Type:** Boundary  

### Preconditions
- User is uploading a video of acceptable file size  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 192 MB  
- **Length:** 2 minutes  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** "67"  

### Expected Result
- Video uploads successfully  
- Processing screen appears  
- Video is visible and playable  

**Priority:** High

---

## Test Case 7

**Test Case ID:** TTK_UPLOAD_007  
**Title:** Verify That a Video with No Caption Can Be Successfully Posted  
**Requirement:** System allows empty captions  
**Test Type:** Edge Case  

### Preconditions
- User is uploading a video without a caption  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Leave caption empty  
7. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 192 MB  
- **Length:** 2 minutes  
- **Resolution:** 1080x1920  
- **Aspect Ratio:** 9:16  
- **Caption:** ""  

### Expected Result
- Video uploads successfully  
- Video appears in profile  
- No caption is displayed  

**Priority:** High

---

## Test Case 8

**Test Case ID:** TTK_UPLOAD_008  
**Title:** Verify That a Corrupted File is Not Accepted  
**Requirement:** System must reject corrupted files  
**Test Type:** Boundary  

### Preconditions
- User is uploading a corrupted video file  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select corrupted file `test_video.mov`  
4. Tap "Next"  
5. Add caption: `67`  
6. Tap "Post"  

### Test Data
- **File:** test_video.mov (corrupted)  
- **Format:** MOV  
- **Size:** 192 MB  
- **Length:** 2 minutes  

### Expected Result
- Upload fails  
- System notifies user that the file is corrupted  

**Priority:** High

---

## Test Case 9

**Test Case ID:** TTK_UPLOAD_009  
**Title:** Maximum Hashtags are Used and Successfully Uploaded  
**Requirement:** System allows a maximum of 30 hashtags  
**Test Type:** Black Box  

### Preconditions
- User is uploading a video with 30 hashtags  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.mov`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Add 30 hashtags  
8. Tap "Post"  

### Test Data
- **File:** test_video.mov  
- **Format:** MOV  
- **Size:** 192 MB  
- **Length:** 2 minutes  
- **Hashtags:** 30 total  

### Expected Result
- Video uploads successfully  
- Video appears in user profile  
- All hashtags are displayed  

**Priority:** High

---

## Test Case 10

**Test Case ID:** TTK_UPLOAD_010  
**Title:** Verify That a WebM File is Successfully Uploaded  
**Requirement:** System accepts WebM file types  
**Test Type:** Boundary  

### Preconditions
- User is uploading a WebM video  

### Test Steps
1. Tap "+" button to access upload screen  
2. Tap "Upload" to select from device storage  
3. Select test video file `test_video.webm`  
4. Verify video preview loads  
5. Tap "Next"  
6. Add caption: `67`  
7. Tap "Post"  

### Test Data
- **File:** test_video.webm  
- **Format:** WebM  
- **Size:** 192 MB  
- **Length:** 2 minutes  

### Expected Result
- Video uploads successfully  
- Video appears in user profile  

**Priority:** High
