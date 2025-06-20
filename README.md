# GeolocationTracker
import requests

def get_location():
    try:
        response = requests.get("https://ipinfo.io")
        data = response.json()
        print(f"IP: {data.get('ip')}")
        print(f"City: {data.get('city')}")
        print(f"Region: {data.get('region')}")
        print(f"Country: {data.get('country')}")
        print(f"Location (lat,long): {data.get('loc')}")
    except Exception as e:
        print("Error fetching location:", e)

get_location()
