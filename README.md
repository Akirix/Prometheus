yum install git -y

useradd -m prometheus

cd /home/prometheus

su - prometheus -c "git clone https://github.com/Akirix/Prometheus.git"

cp Prometheus/systemd/* /etc/systemd/system/

systemctl daemon-reload

systemctl enable node_exporter.service

systemctl start node_exporter