# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Added
- `CHANGELOG.md` (this file) to help track changes
- In `examples/soccer` added progress view when processing mp4 using `tqdm(..)`, shows a progress bar, the current frame, total frames, and ETA.
### Changed
- After typing the full line in many times, I wanted a quicker way to start `examples/soccer/main.py` and provide just the minimal command line arguments (the input mp4 and mode to run in). `--<ARGUMENT NAME>` is optional now, the output video name is derived from the input name + the mode name, and the `--device` option comes last so it can be omitted for brevity. (The Windows machine I'm using does not suppor `cuda` so I always use the default `cpu` option).
- window showing latest frame result has title matching output file name instead of 'frame'. If running two or more main.py processes it makes it clear which is which.
### Fixed
- latest version of supervision (0.26.1) does not support `overlap_filter_strategy=sv.OverlapFilter.NONE`. Commented out that argument for the moment as there doesn't seem to be an obvious replacement. Will have to see how it performs.

## Oct 27, 2025 version of [roboflow/sports](https://github.com/roboflow/sports/tree/13fd1e67b54ffab06cee82f26c0148b1197d527c)
