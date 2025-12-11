<div align="center">

# 📦 AWS-Lambda-psycopg2
psycopg2_python3.12.zip, psycopg2_python3.13.zip
<br>
This is a ZIP file for creating a psycopg2 Lambda layer for AWS Lambda Python.
<br>
It takes the official AWS Lambda ("OS":"Amazon Linux 2023") Python image ("public.ecr.aws/lambda/python:3.xx") and compresses the libraries with psycopg2("ver":"2.9.11") installed. x86_64.

<br>

![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)

<br>

</div>

---

## 🚀 Example of the procedure for creating a ZIP file
echo 'psycopg2-binary' > requirements.txt
<br>
docker run --rm --entrypoint "" -v "$PWD":/var/task "public.ecr.aws/lambda/python:3.13" /bin/sh -c "pip install -r requirements.txt -t python/lib/python3.13/site-packages/; exit"
<br>
sudo chmod -R 755 python
<br>
zip -r psycopg2_python3.13.zip python
<br>
