import requests, json
from tkinter import *


exp = ""
def inp(name) :
    try :
        
        url = "https://weatherapi-com.p.rapidapi.com/forecast.json"
        querystring = {"q": name ,"days":"3"}

        headers = {
            'x-rapidapi-key': "5a036438c7mshdf715452ee24a05p18fc6cjsn348beccd8b41",
            'x-rapidapi-host': "weatherapi-com.p.rapidapi.com"
            }

        response = requests.request("GET", url, headers=headers, params=querystring)

        r = response
        s = r.json()
        rf.insert(10,s['location']['region'] )
        cof.insert(10,s['location']['country'])
        cutf.insert(10,s['current']['temp_c'])
        matf.insert(10,s['forecast']['forecastday'][0]['day']['maxtemp_c'])
        mitf.insert(10,s['forecast']['forecastday'][0]['day']['mintemp_c'])
        cf.insert(10,s['current']['condition']['text'])
        wsf.insert(10,s['current']['wind_kph'])
        wdf.insert(10,s['current']['wind_dir'])
        hf.insert(10,s['current']['humidity'])
        pf.insert(10,s['current']['precip_mm'])
        clf.insert(10,s['current']['cloud'])
        flf.insert(10,s['current']['feelslike_c'])
        name = ""
    
    except :
        rf.insert(10,"Unknown Location")
        name = ""
        
def find():
    name = nf.get()
    inp(name)
        
def clear():
    nf.delete(0,END)
    rf.delete(0,END)
    cof.delete(0,END)
    cutf.delete(0,END)
    matf.delete(0,END)
    mitf.delete(0,END)
    cf.delete(0,END)
    wsf.delete(0,END)
    wdf.delete(0,END)
    hf.delete(0,END)
    pf.delete(0,END)
    clf.delete(0,END)
    flf.delete(0,END)

if __name__ == '__main__':
    w = Tk()
    w.title("Weather Report")
    w.configure(background = 'light green')
    w.geometry("600x500")
    hlabel = Label(w, text = "Welcome to my Weather App", fg = "red")
    label1 = Label(w, text = "City :", fg = 'blue' )
    l2 = Label(w, text = 'Region :', fg = 'black')
    l3 = Label(w, text = 'Country :', fg = 'black')
    l4 = Label(w, text = 'Current Temperature :(C)', fg = 'black')
    l5 = Label(w, text = 'Maximum Temperature :(C)', fg = 'black')
    l6 = Label(w, text = 'Minimum Temperature :(C)', fg = 'black')
    l7 = Label(w, text = 'Condition :', fg = 'black')
    l8 = Label(w, text = 'Humidity :(%)', fg = 'black')
    l9 = Label(w, text = 'Wind Speed :(KPH)', fg = 'black')
    l10 = Label(w, text = 'Wind Direction :', fg = 'black')
    l11 = Label(w, text = 'Precipitation :(mm)', fg = 'black')
    l12 = Label(w, text = 'Cloud :(%)', fg = 'black')
    l13 = Label(w, text = 'Feels Like :(C)', fg = 'black')
    
    
    hlabel.grid(row = 0, column = 1)
    label1.grid(row = 2, column = 0, sticky = 'E')
    l2.grid(row = 4, column = 0, sticky = 'E')
    l3.grid(row = 5, column = 0, sticky = 'E')
    l4.grid(row = 6, column = 0, sticky = 'E')
    l5.grid(row = 7, column = 0, sticky = 'E')
    l6.grid(row = 8, column = 0, sticky = 'E')
    l7.grid(row = 9, column = 0, sticky = 'E')
    l8.grid(row = 10, column = 0, sticky = 'E')
    l9.grid(row = 11, column = 0, sticky = 'E')
    l10.grid(row = 12, column = 0, sticky = 'E')
    l11.grid(row = 13, column = 0, sticky = 'E')
    l12.grid(row = 14, column = 0, sticky = 'E')
    l13.grid(row = 15, column = 0, sticky = 'E')
    
     
    nf = Entry(w)
    rf = Entry(w)
    cof = Entry(w)
    cutf = Entry(w)
    matf = Entry(w)
    mitf = Entry(w)
    cf = Entry(w)
    hf = Entry(w)
    wsf = Entry(w)
    wdf = Entry(w)
    pf = Entry(w)
    clf = Entry(w)
    flf = Entry(w)
    
    nf.grid(row = 2, column = 1, ipadx = '100')
    rf.grid(row = 4, column = 1, ipadx = '100')
    cof.grid(row = 5, column = 1, ipadx = '100')
    cutf.grid(row = 6, column = 1, ipadx = '100')
    matf.grid(row = 7, column = 1, ipadx = '100')
    mitf.grid(row = 8, column = 1, ipadx = '100')
    cf.grid(row = 9, column = 1, ipadx = '100')
    hf.grid(row = 10, column = 1, ipadx = '100')
    wsf.grid(row = 11, column = 1, ipadx = '100')
    wdf.grid(row = 12, column = 1, ipadx = '100')
    pf.grid(row = 13, column = 1, ipadx = '100')
    clf.grid(row = 14, column = 1, ipadx = '100')
    flf.grid(row = 15, column = 1, ipadx = '100')
    
    bt1 = Button(w, text = "Result", bg = 'red' , fg = 'white',command = find)
    bt1.grid(row = 2, column = 2)
    
    bt2 = Button(w, text = 'Clear all', bg = 'red', fg ='white', command = clear )
    bt2.grid(row = 17, column = 1)
    
    bt3 = Button(w, text = "Exit", bg = "red", fg = 'white', command = w.destroy)
    bt3.grid(row = 18 , column = 1)
    
    
    w.mainloop()
