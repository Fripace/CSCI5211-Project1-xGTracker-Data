# CSCI 5211 Project 1 – xGTracker Dataset

This repository contains the organized xGTracker data collected for four scenarios:

- Home / Stationary
- Home / Walking
- Alumni / Stationary
- Alumni / Walking

## Dataset files

### Original selected dataset – November 6

- `CSCI5211_Project1_Labeled_18Sessions_H264_2026-11-06.zip`

This ZIP contains the original organized and labeled 18-session dataset. Its Video Uplink logs are H264, and its File Download tests use only the 100 MB file size.

### File Download and H265 retests – November 10

- `CSCI5211_Project1_Retests_12Sessions_FileDownload_AllSizes_H265_2026-11-10.zip`

This ZIP contains 12 complete retest sessions: three loops for each of the four scenarios. Every included loop contains:

- Eight completed File Download tests:
  - 100 MB with 1 and 4 connections
  - 512 MB with 1 and 4 connections
  - 1 GB with 1 and 4 connections
  - 2 GB with 1 and 4 connections
- One completed H265 Video Uplink test

## Retest validation

- All 96 File Download logs end with `Status=COMPLETED`.
- For every download, `bytesDownloaded` exactly equals the requested `FileSize`.
- All 12 H265 Video Uplink logs reach `Progress=100` and `Status=COMPLETED` with nonzero bytes sent.
- Location speed data agrees with the Stationary/Walking labels.
- Three failed, restarted, or partial sessions were excluded. They are listed in the exclusion manifest inside the retest ZIP.
- Every copied session was verified against its source by file count, byte count, and file hashes.

## Contents of the retest ZIP

- Four scenario folders, each containing three labeled loops
- `Session_Selection_and_Validation.csv`
- `Test_Configuration_Map.csv`
- `Excluded_Failed_or_Partial_Sessions.csv`
- `Copy_Verification.csv`
- `README.txt`

The source export was not modified. The repository contains copied and reorganized data only.

## Checksums

SHA-256 checksums are provided in `SHA256SUMS.txt`.
