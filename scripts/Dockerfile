# docker config for a stand-alone inference script instance

FROM clearlinux/python:3.9
WORKDIR /app
COPY ["inference.py", "requirements.txt", "./"]
COPY ["model/model.bin", "model/"]
RUN pip install -r requirements.txt
EXPOSE 9696
ENTRYPOINT ["python", "inference.py"]