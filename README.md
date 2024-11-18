# MiAI_FaceRecog_3
Nhận diện khuôn mặt khá chuẩn xác bằng MTCNN và Facenet!
Chạy trên Tensorflow 2.x

Article link: http://miai.vn/2019/09/11/face-recog-2-0-nhan-dien-khuon-mat-trong-video-bang-mtcnn-va-facenet/

* Cài đặt requirements: 
pip install -r requirements.txt

* Cắt khuôn mặt để dùng train: 
python src/align_dataset_mtcnn.py  Dataset/FaceData/raw Dataset/FaceData/processed --image_size 160 --margin 32  --random_order --gpu_memory_fraction 0.25

* Train nhận diện: 
python src/classifier.py TRAIN Dataset/FaceData/processed Models/20180402-114759.pb Models/facemodel.pkl --batch_size 1000

* Chạy nhận diện từ camera: 
python src/face_rec_cam.py 
