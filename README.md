Cài đặt môi trường
Miniconda
https://docs.anaconda.com/free/miniconda/index.html

Khởi tạo môi trường
conda create --name myenv python=3.9

conda activate myenv
Cài đặt các gói liên quan
pip install rasa
Tạo project Rasa
Tạo thư mục chứa project
mkdir ChatRasa

cd ChatRasa
Khởi tạo project
rasa init
Chuẩn bị dữ liệu
nlu.yml

rules.yml

stories.yml

Train chatbot
Sau khi hoàn thành chuẩn bị data

rasa train
Serving Model
Cho model thực hiện trả lời các câu hỏi từ người dùng, để làm được điều này cần chạy model trên một server

Cài đặt ngrok
https://ngrok.com/docs

Kết nối với một Channel Connector (Telegram)
https://rasa.com/docs/rasa/connectors/telegram

Chạy server với model Rasa
rasa run

ngrok http 5005 
Note: Cần thay đường dẫn ngrok cung cấp để bot telegram gửi được request đến server
