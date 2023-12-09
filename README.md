# mid2csv
MIDI to event-wise CSV conversion tool

- Beats and tempo events
- Markers
- Notes
- Texts

# Usage

```
python mid2csv.py -i /path/to/mid -o /path/to/output_dir
```

# Output data sample

- beats_and_tempo.csv

```
,拍子位置,時間(秒),拍子分子,拍子分母,1小節長さ,テンポ,調,長調/短調,絶対時間
0,1.1.0,0,4,4,1920,175.0,-6,major,0.0
1,2.1.0,1920,4,4,1920,175.0,-6,major,1.3714285714285714
2,3.1.0,3840,4,4,1920,175.0,-6,major,2.742857142857143
3,4.1.0,5760,4,4,1920,175.0,-6,major,4.114285714285714
4,5.1.0,7680,4,4,1920,175.0,-6,major,5.485714285714286
5,6.1.0,9600,4,4,1920,175.0,-6,major,6.857142857142858
6,7.1.0,11520,4,4,1920,175.0,-6,major,8.22857142857143
7,8.1.0,13440,4,4,1920,175.0,-6,major,9.600000000000001
8,9.1.0,15360,4,4,1920,175.0,-6,major,10.971428571428573
```

- markers.csv

```
,拍子位置,時間(秒),時間,拍子位置,マーカー
0,5760,4.114285714285714,0:04:11,4.1.0,I
1,13440,9.600000000000001,0:09:60,8.1.0,I-A1
2,28800,20.57142857142857,0:20:57,16.1.0,A1
3,59520,42.51428571428572,0:42:51,32.1.0,B1
4,74880,53.48571428571431,0:53:48,40.1.0,S1
5,117120,83.65714285714283,1:23:65,62.1.0,S1-A2
6,128640,91.88571428571423,1:31:88,68.1.0,A2
7,144000,102.85714285714276,1:42:85,76.1.0,B2
```
- notes.csv

```
,Note ON拍子位置,Note OFF拍子位置,Note ON時間(秒),Note OFF時間(秒),オクターブ,音階,音高,チャンネル
0,5760,6235,4.1.0,4.1.475,4.114285714285714,4.453571428571428,5,Bb,82,0
1,6240,6478,4.2.0,4.2.238,4.457142857142856,4.627142857142857,5,Eb,75,0
2,6720,7195,4.3.0,4.3.475,4.8,5.139285714285714,5,Ab,80,0
3,7200,7438,4.4.0,4.4.238,5.142857142857142,5.312857142857142,5,Db,73,0
4,7440,7915,4.4.240,5.1.235,5.314285714285714,5.6535714285714285,5,Ab,80,0
5,7920,8158,5.1.240,5.1.478,5.6571428571428575,5.827142857142857,5,Db,73,0
```

- texts.csv

```
,拍子位置,時間(秒),時間,拍子位置,テキスト
0,5760,4.114285714285714,0:04:11,4.1.0,Cdim
1,6480,4.628571428571428,0:04:62,4.2.240,B
2,7440,5.314285714285714,0:05:31,4.4.240,Bbm
3,8400,6.0,0:06:00,5.2.240,Gbm/A
4,9600,6.857142857142858,0:06:85,6.1.0,Abm7
```
