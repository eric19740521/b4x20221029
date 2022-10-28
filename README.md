# b4x20221029
B4X實驗:  架設HLS Video Server/StreamServer.網路影音服務器(B4J)
B4X實驗:  架設HLS Video Server/StreamServer.網路影音服務器(B4J)
Insider Tips:Because of the ability, there is no English document. But you can use google translate
參考資料:
前端如何播放m3u8格式的影片
https://www.gushiciku.cn/pl/pXXF/zh-tw 
ffmpeg-ffmpeg简单使用
https://blog.csdn.net/lch_cui/article/details/79688653
Web 前端如何播放 HLS(.m3u8) 视频
https://gist.github.com/ufologist/1ec2b820738a95b25cf7d805ed615949

1.下載點
https://www.gyan.dev/ffmpeg/builds/#release-builds
ffmpeg-5.1.2-full_build.7z

2.
将mp4格式的视频转换成m3u8格式
e:\ffmpeg\bin\ffmpeg -y -i test.mp4 -vcodec copy -acodec copy -vbsf h264_mp4toannexb test.ts

再将test.ts文件切片并生成test.m3u8，5s切一个片，生成的文件名为test001.ts，test002.ts，test003.ts，……
e:\ffmpeg\bin\ffmpeg -i test.ts -c copy -map 0 -f segment -segment_list test.m3u8 -segment_time 5 test%03d.ts


4.服務器架設
https://youtu.be/TMrzQdk3n3c
https://youtu.be/RpGafdvAOMA

5.
VPS頻寬	
1 TB

6.程式碼說明

9.未來!!結合手機 現場錄製...直播

HLS/RTMP/RTSP  Streaming  ...vlc Play




 
