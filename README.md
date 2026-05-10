## a. How much data your publisher program will send to the message broker in one run?
Dalam satu kali run, publisher program akan mengirim 5 data/message ke message broker. Setiap message berisi data UserCreatedEventMessage dengan user_id dan user_name yg berbeda, yaitu dari 1 sampai 5.

## b. The url of: `amqp://guest:guest@localhost:5672` is the same as in the subscriber program, what does it mean?
URL itu adalah connection string utk menghubungkan program ke RabbitMQ.

Artinya:
- amqp = protokol komunikasi message queue
- guest yg pertama = username
- guest yg kedua = password
- localhost = server RabbitMQ dijalankan di komputer lokal
- 5672 = port default utk koneksi AMQP

Jadi, publisher dan subscriber memakai URL yg sama karena keduanya terhubung ke RabbitMQ yg sama utk saling kirim dan terima message.