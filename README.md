# friends

test output:
```bash
find . -type f -name 'friends*.srt' -exec \
  bash -c 'a={}; b=${a##*s_}; c=${b%_720p*}; \
  d="friends_${c}_720p_bluray_x264-sujaidr.srt"; \
  echo ${d}' \;
```

rename srt files:
```bash
find . -type f -name 'friends.*' -exec \
  bash -c 'a={}; b=${a##*s.}; c=${b%.720p.bluray.x264-psychd.srt}; \
  d="friends_${c}_720p_bluray_x264-sujaidr.srt"; \
  mv {} ${d}' \;
```


fix up:
```bash
find . -type f -name 'friends*.srt' -exec \
  bash -c 'a={}; b=${a##*s_}; c=${b%_720p*}; \
  d="friends_${c}_720p_bluray_x264-sujaidr.srt"; \
  mv {} ${d}' \;
```

