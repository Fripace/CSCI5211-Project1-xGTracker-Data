# CSCI 5211 Project 1 – xGTracker Dataset

This repository contains the organized and labeled xGTracker dataset for 18 selected sessions across four scenarios:

- Home / Stationary
- Home / Walking
- Alumni / Stationary
- Alumni / Walking

## Dataset file

- `CSCI5211_Project1_Labeled_18Sessions_H264_2026-11-06.zip`

The ZIP contains the copied raw session data, descriptive test-folder names, and the mapping manifest. The original source data was not modified.

## Known limitations

### File Download

All 96 File Download records in the selected 18 sessions use `100M.bin` (100 MB / 104,857,600 bytes): 48 runs use 1 connection and 48 runs use 4 connections. Other available file sizes were not collected, so this part does not yet satisfy the project requirement to download every available file size multiple times.

xGTracker displayed: `cannot connect to custom server; check its address, installation and service port`. The missing file-size options are therefore likely caused by the custom-server capability/service being unavailable.

### Video Uplink

All available `VideoUpLink_log.csv` records report `Codec=H264`. H265 collection is still pending because the custom server capability/service was unavailable.
