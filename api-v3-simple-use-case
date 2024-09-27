import os
import json

from getpass import getpass

import urllib3
import requests
from requests.auth import HTTPBasicAuth


print("Let's build the API request, answer the folling prompted questions..")

print("Enter your console and user info")

CONSOLE_URL = os.environ.get("CONSOLE_URL")
if CONSOLE_URL is None:
CONSOLE_URL = input('Enter your console address (i.e.-https://example.rapid7.com:3780) :  ') # Example : https://example.rapid7.com:3780

 # Optionally use environment variables or CLI input.
CONSOLE_USER = os.environ.get("CONSOLE_USER")
if CONSOLE_USER is None:
    CONSOLE_USER = input('Enter your username:  ')
#
CONSOLE_PASS = os.environ.get("CONSOLE_PASS")
if CONSOLE_PASS is None:
    CONSOLE_PASS = getpass('Enter your password:  ')

print("This script is using the v3 API, using api/3")
print("Let's enter the API Endpoint..refer to this API v3 link to reference- https://help.rapid7.com/insightvm/en-us/api/index.html# ")

    API_ENDPOINT = os.environ.get("API ENDPOINT")
if API_ENDPOINT is None:
    API_ENDPOINT = input('Enter the API endpoint (i.e. Assets):  ')


base_url = f"{CONSOLE_URL}/api/3/{ENDPOINT}/"

print("You're using " base_url "as your base url")


print("Let's determine the request type...")
print("Below enter the request type, GET, PUT, POST, DELETE  ")

API_REQUEST_TYPE = os.environ.get("API REQUEST_TYPE")
if API_REQUEST_TYPE is None:
    API_REQUEST_TYPE = input('Enter the API request type:  ')



#
for request in request:
    url = base_url
    response = API_REQUEST_TYPE.(url,
    auth=HTTPBasicAuth(CONSOLE_USER, CONSOLE_PASS),
    verify=False,   # For consoles with self-signed SSL certificates.
                    # Set to True if your SSL Cert is signed by a valid CA.
                    # Causes an InsecureRequestWarning when set to False.
    timeout=REQUEST_TIMEOUT
    )

# Check the response status
    if response.status_code == 200:
        print(f"OK")
    if response.status_code == 401:
        print(f"Unauthorized")
    if response.status_code == 404:
        print(f"Not Found")
    if response.status_code == 500:
        print(f"Internal Server Error")
    if response.status_code == 503:
        print(f"Service Unavailable")
    else:
        print(f"Status code: {response.status_code}")
