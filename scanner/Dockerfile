FROM alpine


RUN apk update
RUN apk add python py-pip gcc python-dev musl-dev libffi-dev openssl-dev

RUN pip install impacket

COPY *.py /scanner/

RUN chmod +x /scanner/wannacry_tlscan.py

ENTRYPOINT ["/scanner/wannacry_tlscan.py"]
