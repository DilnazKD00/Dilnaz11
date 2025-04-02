pip install pymysql google-cloud-sql
import pymysql

# Cloud SQL параметрлері
host = 'my-cloud-sql-region.mysql.database.gcp.com'  # Өз серверіңізді жазыңыз
database = 'my_database'  # Дерекқордың аты
user = 'root'  # Логин
password = 'MySecurePassword'  # Құпиясөз

try:
    conn = pymysql.connect(host=host, user=user, password=password, database=database)
    cursor = conn.cursor()
    print("Cloud SQL-ге сәтті қосылдық!")

    # Дерекқордан мәлімет оқу
    cursor.execute("SHOW DATABASES")
    rows = cursor.fetchall()

    print("Дерекқор тізімі:")
    for row in rows:
        print(row[0])

    # Байланысты жабу
    conn.close()
except Exception as e:
    print("Қате пайда болды:", e)
    pip install google-cloud-storage
    from google.cloud import storage

# Cloud Storage параметрлері
bucket_name = "my-gcp-storage"
blob_name = "example.png"
file_path = "example.png"

# Клиент жасау
storage_client = storage.Client()
bucket = storage_client.bucket(bucket_name)
blob = bucket.blob(blob_name)

# Файлды жүктеу
blob.upload_from_filename(file_path)
print(f"Файл {blob_name} сәтті жүктелді! URL: {blob.public_url}")
def hello_gcp(request):
    return "Hello, GCP!"
    gcloud functions deploy hello_gcp --runtime python39 --trigger-http --allow-unauthenticated
    git init
git remote add origin https://github.com/your_username/gcp-cloud-project.git
git add .
git commit -m "GCP жобасы үшін дайын кодтар"
git push origin main
