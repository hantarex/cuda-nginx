FROM cuda

RUN mkdir /www
ADD static /www/static

EXPOSE 1935
EXPOSE 8081

#ENTRYPOINT ["/opt/nginx/sbin/nginx"]

#FROM nvidia/cuda:9.1-devel-ubuntu16.04
#FROM nvidia/cuda:11.1.1-devel-ubuntu20.04
#FROM cuda



ENTRYPOINT ["tail", "-f", "/dev/null"]

#--enable-nonfree --enable-cuda-sdk --enable-libnpp --extra-cflags=-I/usr/local/cuda/include --extra-ldflags=-L/usr/local/cuda/lib64

#ffmpeg -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi -c:a copy -c:v h264 -b:v 5M 1.avi
#ffmpeg -vsync 0 -hwaccel cuda -c:v mpe1g4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi -c:a copy -c:v h264_nvenc -b:v 5M 1.avi

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuvid -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi -c:a copy -c:v h264_nvenc -b:v 5M 1.avi

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi \
# -vf "fps=1/15,thumbnail_cuda=3,scale_cuda=320:-1,hwdownload,format=nv12" -y -f image2 -update 1 thumb.jpg \
# -vf scale_cuda=1280:720 -c:a aac -c:v h264_nvenc -b:v 256k -b:a 32k -map 0 -f tee "[f=flv]1_1280.flv" \
# -vf scale_cuda=854:480 -c:a aac -c:v h264_nvenc -b:v 768k -b:a 96k -map 0 -f tee "[f=flv]1_854.flv" \
# -vf scale_cuda=426:240 -c:a aac -c:v h264_nvenc -b:v 1024k -b:a 128k -map 0 -f tee "[f=flv]1_426.flv"
#

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi \
# -vf "fps=1/15,thumbnail_cuda=3,scale_cuda=320:-1,hwdownload,format=nv12" -y -f image2 -update 1 thumb.jpg \
# -vf scale_cuda=1280:720 -c:a aac -c:v h264_nvenc -b:v 256k -b:a 32k -map 0 -f tee "[f=avi]1_1280.avi" \
# -vf scale_cuda=854:480 -c:a aac -c:v h264_nvenc -b:v 768k -b:a 96k -map 0 -f tee "[f=avi]1_854.avi" \
# -vf scale_cuda=426:240 -c:a aac -c:v h264_nvenc -b:v 1024k -b:a 128k -map 0 -f tee "[f=avi]1_426.avi"

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi \
# -vf "fps=1/15,thumbnail_cuda=3,scale_cuda=320:-1,hwdownload,format=nv12" -y -f image2 -update 1 thumb.jpg \
# -vf scale_cuda=1280:720 -c:a copy -c:v h264_nvenc -b:v 256k -map 0 -f tee "[f=avi]1_1280.avi" \
# -vf scale_cuda=854:480 -c:a copy -c:v h264_nvenc -b:v 768k -map 0 -f tee "[f=avi]1_854.avi" \
# -vf scale_cuda=426:240 -c:a copy -c:v h264_nvenc -b:v 1024k -map 0 -f tee "[f=avi]1_426.avi"

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v h264_cuvid -listen 1 -i rtmp://0.0.0.0:1935/live/123456 -max_muxing_queue_size 9999 \
# -vf scale_cuda=640:480 -c:a aac -r 30 -c:v h264_nvenc -b:v 3M -b:a 128k -map 0 -flags +global_header -g 2 -f tee "[f=flv]1_1280.flv"

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi \
# -filter_complex "split=2[v1][v2];[v1]scale_npp=854:480[mid];[v2]scale_npp=426:240[low]" \
# -c:v h264_nvenc -c:a copy -b:v 256k -flags +global_header -g 2 -map "[mid]" -map 0:a -f tee "[f=avi]a_mid.avi"
# -c:v h264_nvenc -c:a copy -b:v 256k -flags +global_header -g 2 -map "[low]" -map 0:a -f tee "[f=avi]a_low.avi"
#
#
#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v mpeg4_cuvid -i Avengers_Endgame_2019_HDRip___\[scarabey.org\].avi -vf "fps=1/15,thumbnail_cuda=3,scale_npp=320:-1,hwdownload,format=nv12" -y -f image2 -update 1 thumb.jpg

#ffmpeg -vsync 0 -hwaccel_output_format cuda -hwaccel cuda -c:v h264_cuvid -listen 1 -i rtmp://0.0.0.0/live/123456 -max_muxing_queue_size 9999 \
#                -vf "fps=1/15,thumbnail_cuda=2,scale_cuda=320:-1,hwdownload,format=nv12" -r 30 -y -f image2 -update 1 /application/data/thumbs/${name}/thumb.jpg \
#                -vf scale_cuda=1280:720 -c:a aac -c:v h264_nvenc -r 30 -b:v 1024k -b:a 128k -map 0 -flags +global_header -g 2 -f tee "[f=flv]${name}_hi.flv" \
#                -vf scale_cuda=854:480 -c:a aac -c:v h264_nvenc -r 30 -b:v 768k -b:a 96k -map 0 -flags +global_header -g 2 -f tee "[f=flv]${name}_mid.flv" \
#                -vf scale_cuda=426:240 -c:a aac -c:v h264_nvenc -r 30 -b:v 256k -b:a 32k -map 0 -flags +global_header -g 2 -f tee "[f=flv]${name}_low.flv"
