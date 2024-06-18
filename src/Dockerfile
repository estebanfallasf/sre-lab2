FROM alpine
EXPOSE 5000
WORKDIR /app
RUN apk update && apk add python3 py3-pip
RUN pip install flask --break-system-packages
COPY . .
CMD ["flask", "run", "--host", "0.0.0.0"]