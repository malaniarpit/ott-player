# ott-player

sudo ffmpeg -re -i B4UVI128773001.ts -loop 1 -pattern_type glob -i "B4UCLMOV9/*.tga" -filter_complex "[0:v][1:v] overlay=0:0:enable='between(t,0,200)'" -c:a libmp3lame -c:v libx264 -f flv -ar 44100 rtmp://127.0.0.1/live/test < /dev/null
