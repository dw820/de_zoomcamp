FROM python:3.9.1

RUN apt-get install wget
RUN pip install pandas sqlalchemy psycopg2

WORKDIR /app
COPY ingest_data.py ingest_data.py

RUN URL="https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz"

ENTRYPOINT [ "python"]
CMD ["ingest_data.py","--user=root","--password=root","--host=localhost","--port=5432","--db=ny_taxi","--table_name=yellow_taxi_trips","--url='https://github.com/DataTalksClub/nyc-tlc-data/releases/download/yellow/yellow_tripdata_2021-01.csv.gz'"] 