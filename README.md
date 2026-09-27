Multi-Agent Trading Dashboard
News + Price + Sentiment एजेंट्स का मिला-जुला विश्लेषण
{% for s in symbols %}
{{ s }}
{% endfor %}
🔄 Refresh Data
Final Recommendation
{{ data.decision.recommendation }}
{{ data.decision.explanation }}

Price Agent — {{ data.symbol }}
Current Price
{{ data.price.price }}
SMA (9)
{{ data.price.sma_fast }}
SMA (21)
{{ data.price.sma_slow }}
RSI (14)
{{ data.price.rsi }}
{{ data.price.signal }}
{{ data.price.reason }}

Sentiment Agent
{{ data.sentiment.label }}
Score: {{ data.sentiment.score }} (headlines के keywords पर आधारित)

News Agent — Latest Headlines
{% for item in data.news %}
{{ item.title }}
{{ item.source }}
{% else %}
फिलहाल कोई न्यूज़ लोड नहीं हो पाई।

{% endfor %}
यह सिस्टम सिर्फ जानकारी और सुझाव के लिए है, यह financial advice नहीं है।
कोई भी असली ट्रेड लेने से पहले अपनी समझ और जोखिम क्षमता का ध्यान 
