=========
Get Woeid
=========

This function gives us woeid of given city from metaweather api



.. code-block:: python

   def get_woeid(city_name):
       
      r = requests.get('https://www.metaweather.com/api/location/search/?query='+ str(city_name))
      woeid = r.json()[0]['woeid']
      return(get_weather_stats(woeid))



















