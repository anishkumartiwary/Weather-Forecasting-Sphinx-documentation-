=============
Audio To Text
=============

This function will convert audio to text  



.. code-block:: python

   def Audio_to_text(audio):
       '''
       Parmaaudio = take audio clip as input
       return = city name after converting and spiliting the senstences
       '''
	try:
	    print("You said " + r.recognize_google(audio))
	except sr.UnknownValueError:
	    print("Could not understand audio")
	except sr.RequestError as e:
	    print("Could not request results; {0}".format(e))
        city_name = str(r.recognize_google(audio).split(' ')[-1])
        
        return city_name

















