# Chromescraper

This project is intended to be used with headless chrome on an AWS ec-2 instance.

## Configure AWS ec-2 to run Headless Chrome

https://devopsqa.wordpress.com/2018/03/08/install-google-chrome-and-chromedriver-in-amazon-linux-machine/

```
wget https://chromedriver.storage.googleapis.com/2.37/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
sudo mv chromedriver /usr/bin/chromedriver

curl https://intoli.com/install-google-chrome.sh | bash
mv /usr/bin/google-chrome-stable /usr/bin/google-chrome

sudo yum -y erase google-chrome
sudo yum update google-chrome-stable
```

## Usage

### Locally

TODO - Won't really work unless you have headless chrome configured locally.

```
git clone https://github.com/geocolumbus/chromescraper.git
cd chromescraper
mvn clean package
java -jar target/chromescraper-1.0-SNAPSHOT.jar
```

### On ec-2

Copy ```target/chromescraper-1.0-SNAPSHOT.jar``` up to the configured ec-2 instance and run it there.

## References

* https://ksah.in/introduction-to-chrome-headless/
