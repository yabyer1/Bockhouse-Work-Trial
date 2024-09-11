Blockhouse web dev coding test:

Instructions: 

To run backend -> Navigate to the backends folder from next-js-dashboard and run these commands: 
 python manage.py migrate
python manage.py runserver

To run frontend ->
Navigate to the proj folder and run
 npm run build
 npm run dev

Libraries: 
 Axios, recharts, react-financial-data.


Thought process:
1. set up backend first with Django, and used rest framework and charts. Constructed mock data within views.py, and urls.py contains API calls to request said data
2. Set frontend up to immediately display chart data. Used recharts for all charts except candlestick, and used react-financial-data for the candlestick chart. 
3. All the rechart charts follow a similar pattern: First fetch data from backend via axios, data is received as an array of both labels and data, so we need to transform once again, mapping the label and data at an index. We then call a function to set the data on a chart. Then use the respective chart containers to display the chart. For candlestick data, we take the data and then we need to label high open low and close in order to label the main points of interest given to us, and use the points to render the graph.