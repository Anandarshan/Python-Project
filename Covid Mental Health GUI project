import tkinter as tk
import tkinter.font as tkf
from PIL import ImageTk,Image
from win32com.client import Dispatch
import webbrowser
import docx
windows_speak=Dispatch('SAPI.Spvoice')
window=tk.Tk()
window.geometry('2000x1700')
e2=tk.Entry(window)
e2.place(x=580,y=450)
e1=tk.Entry(window)
e1.place(x=580,y=400)
f1=tkf.Font(family="Times New Roman",size=14)

label=tk.Label(text="Name:",bg="lightsteelblue1",fg="Black",font=f1,height="1",width="4")
def action():
    count=0
    string=e1.get();
    string2=e2.get();
    if((len(string)==0)and(len(string2)==0)):
        invalid=tk.Label(text="INVALID",bg="lightsteelblue1",fg="RED",font=f1,height="1",width="8")
        invalid.place(x=600,y=520)
    elif((int(string2)==0) or (int(string2)>123) or(string2.isalpha())):
         invalid=tk.Label(text="INVALID",bg="lightsteelblue1",fg="RED",font=f1,height="1",width="8")
         invalid.place(x=600,y=520)
    else:
        
        window.destroy()
        actualstring="Hello Welcome "+str(string)+", if you feel your mental health is suffering due to this pandemic, we're here to help."
        basic=tk.Tk()
        basic.geometry('2000x800')
        f2=tkf.Font(family="Times New Roman",size=16)
        labl1=tk.Label(basic,text="Check Your Symptoms : ",bg="lightsteelblue2",fg="Black",font=f1,height="1",width=20)
        labl2=tk.Label(basic,text="Motivational Videos : ",bg="lightsteelblue2",fg="Black",font=f1,height="1",width=20)
        labl3=tk.Label(basic,text="Contact psychiatrist : ",bg="lightsteelblue2",fg="Black",font=f1,height="1",width=20)
        labl4=tk.Label(basic,text="Help : ",bg="lightsteelblue2",fg="Black",font=f1,height="1",width=20)
        windows_speak.speak("Hello "+string+" select any one of these options")
        def check():
            windows_speak.speak("Check your symptoms")
            i=0
            j=0
            k=0
            z=0
            p=0
            new=tk.Tk()
            new.geometry('1100x700')
            newfont=tkf.Font(family="Phoreus Cherokee",size=22)
            newlabel=tk.Label(new,text="Please Answer The Following Questions: ",font=newfont,width=50,height=1)
            newlabel1=tk.Label(new,text="NOTE:-Once the question is answered click on done Button\n How often in the past one week have you felt/had",font=newfont,width=50,height=2)
            newlabel2=tk.Label(new,text="1. Sad or in a low mood?",font=18,width=50,height=1)
            def score():
                nonlocal j,p
                p+=1
                j=1
                nonlocal i
                i+=70
            def score2():
                nonlocal k,p
                p+=1
                k=1
                nonlocal i
                i+=30
            def score3():
                nonlocal z,p
                p+=1
                z=1
                nonlocal i
                i+=0
            
            bunew=tk.Button(new,text="Every day",command=score,bg="lightpink",fg="grey1",width=20)
            bunew2=tk.Button(new,text="Sometimes",command=score2,bg="lightpink",fg="grey1",width=20)
            bunew3=tk.Button(new,text="Never",command=score3,bg="lightpink",fg="grey1",width=20)
            def don():
                nonlocal j,k,z,p
                if(((j==0)and(k==0)and(z==0))and(p==0)):
                    over=tk.Label(new,text="Click on any one of these options",fg="Red",font=24,bg="White")
                    windows_speak.speak("Click on any one of these options")
                    over.place(x=100,y=400)
                    def again():
                        nonlocal z,j,k,i
                        if(j==1):
                            i-=70
                        elif(j==1):
                            i-=30
                        elif(z==1):
                            i-=0
                        z=0
                        j=0
                        k=0
                        over.destroy()
                        redo.destroy()
                        
                    redo=tk.Button(new,text="Redo",fg="white",bg="black",command=again)
                    redo.place(x=350,y=400)
                elif(((j==1)and(k==1)and(z==1)) or((j==1)and(k==1)) or (((j==1)and(z==1))) or(((k==1)and(z==1)))):
                    over=tk.Label(new,text="Click on any one of the options, not all",fg="Red",font=24,bg="White")
                    over.place(x=100,y=400)
                    windows_speak.speak("Click on any one of the options, not all")
                    def again():
                        nonlocal z,j,k,i
                        z=0
                        j=0
                        k=0
                        if(j==1):
                            i-=70
                        elif(j==1):
                            i-=30
                        elif(z==1):
                            i-=0
                        z=0
                        j=0
                        k=0
                        over.destroy()
                        redo.destroy()
                        
                    redo=tk.Button(new,text="Redo",fg="white",bg="black",command=again)
                    redo.place(x=390,y=400)
                elif((k==1)or(z==1)or(j==1)or(p==1)):
                    def question():
                        p=0
                        newlabel2.destroy();
                        another=tk.Label(new,text="2.Guilt-Ridden ?",font=18,width=50,height=1)
                        def don1():
                            nonlocal p,z,j,k
                            z,j,k=0,0,0
                            p=1
                            don()
                        def question1():
                            another.destroy()
                            nonlocal count
                            count+=1
                            if(count==1):
                                questionas=tk.Label(new,text="3. Suicidal or had thoughts of harming yourself?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==2):
                                questionas=tk.Label(new,text="4. Irritated or intolerant of others?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==3):
                                questionas=tk.Label(new,text="5. Difficulty in making decisions?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==4):
                                questionas=tk.Label(new,text="6. Difficulty in sleeping?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==5):
                                questionas=tk.Label(new,text="7. Unexplained headaches or pains?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==6):
                                questionas=tk.Label(new,text="8. Anxious or worried?",font=181,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==7):
                                questionas=tk.Label(new,text="9. Disinterested in doing certain tasks?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==8):
                                questionas=tk.Label(new,text="10. A lack of energy in your body?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==9):
                                questionas=tk.Label(new,text="11. Unable to interact with friends/family?",font=18,width=50,height=1)
                                questionas.place(x=100,y=200)
                            if(count==10):
                                nonlocal i
                                if(i==0):
                                    new.destroy()
                                    new2=tk.Tk()
                                    new2.geometry('1000x500')
                                    addon=tk.Label(new2,text="Congratulations! You're not showing any signs of depression. You seem to be completely fine!",width=100,height=1,font=newfont,fg="black",bg="lightpink")
                                    addon.place(x=40,y=100)
                                    new2.configure(bg="lightsteelblue1")
                                    windows_speak.speak("Congratulations! You seem to be perfectly fine")
                                elif(i>0 and i<=420):
                                    new.destroy()
                                    new2=tk.Tk()
                                    new2.geometry('1000x1000')
                                    addon=tk.Label(new2,text="It's advised to consult a psychiatrist or try some of these exercises at home",width=100,height=1,font=newfont,fg="black",bg="lightpink")
                                    windows_speak.speak("It's advised to consult a psychiatrist or try some of these exercises at home")
                                    addon.place(x=40,y=100)
                                    label1=tk.Label(new2,text="1.Practice yoga, do some physical exercises",fg="black",bg="peach puff",font=20)
                                    label2=tk.Label(new2,text="2.Meditate regularly",fg="black",bg="peach puff",font=20)
                                    label3=tk.Label(new2,text="3.Listen to energetic and upbeat songs",fg="black",bg="peach puff",font=20)
                                    label4=tk.Label(new2,text="4.Spend some time on your hobbies",fg="black",bg="peach puff",font=20)
                                    label5=tk.Label(new2,text="5.Video call your friends and loved ones to maintain a social connection",fg="black",bg="peach puff",font=20)
                                    label6=tk.Label(new2,text="6.Take breaks from social media",fg="black",bg="peach puff",font=20)
                                    label7=tk.Label(new2,text="7.Try taking up journal writing",fg="black",bg="peach puff",font=20)
                                    label8=tk.Label(new2,text="8.Do not neglect your diet. Maintain a nutritious and regular diet.",fg="black",bg="peach puff",font=20)
                                    label1.place(x=20,y=150)
                                    label2.place(x=20,y=180)
                                    label3.place(x=20,y=210)
                                    label4.place(x=20,y=240)
                                    label5.place(x=20,y=270)
                                    label6.place(x=20,y=300)
                                    label7.place(x=20,y=330)
                                    label8.place(x=20,y=360)
                                    def doc():
                                        document=docx.Document()
                                        document.add_paragraph('NATURAL REMEDIES\n\n1.Practice yoga, do some physical exercises\n2.Meditate regularly\n3.Listen to energetic and upbeat songs\n4.Spend some time on your hobbies\n5.Video call your friends and loved ones to maintain a social connection\n6.Watch motivational videos\n7.Take breaks from social media\n8.Try taking up journal writing\n9.Do not neglect your diet. Maintain a nutritious and regular diet.\n')
                                        document.save('natural_remedies.docx')
                                        windows_speak.speak("The file is saved in Desktop as natural remedies")
                                    button=tk.Button(new2,text="Save as Document",fg="white",bg="black",width=20,command=doc)
                                    button.place(x=250,y=500)
                                    new2.configure(bg="lightsteelblue1")
                                else:
                                    new.destroy()
                                    new2=tk.Tk()
                                    new2.geometry('1000x1000')
                                    addon=tk.Label(new2,text="You might be suffering emotionally, as well as physically.",width=100,height=1,font=newfont,fg="black",bg="lightpink")
                                    addon.place(x=40,y=100)
                                    label1=tk.Label(new2,text="Please consult a psychiatrist immediately!",fg="black",bg="peach puff",font=20)
                                    label2=tk.Label(new2,text="Hotline Number: 080-46110007",fg="black",bg="peach puff",font=20)
                                    label3=tk.Label(new2,text="OR",fg="black",bg="peach puff",font=20)
                                    windows_speak.speak("Please consult a psychiatrist immediately or use the hotline number provided.")
                                    label1.place(x=400,y=150)
                                    label3.place(x=500,y=200)
                                    label2.place(x=400,y=250)
                                    label4=tk.Label(new2,text="Related news articles",fg="black",bg="peach puff",font=20)
                                    def weba():
                                        webbrowser.open('https://www.news-medical.net/news/20200527/How-Indias-lockdown-has-affected-mental-health.aspx')
                                    button=tk.Button(new2,text="Click here",fg="white",bg="black",width=20,command=weba)
                                    label4.place(x=20,y=300)
                                    button.place(x=195,y=300)
                                    new2.configure(bg="lightsteelblue1")
                    
                                
                                    
                            
                            nextbut1=tk.Button(new,text="Next ->",fg="white",bg="black",command=question1)
                            nextbut1.place(x=600,y=500)
                        
                        
                        nextbut1=tk.Button(new,text="Next ->",fg="white",bg="black",command=question1)
                        done1=tk.Button(new,text="Done",bg="Black",fg="white",command=don1,width=20)
                        done1.place(x=150,y=250)
                        nextbut1.place(x=600,y=500)
                        another.place(x=100,y=200)
                    nextbut=tk.Button(new,text="Next ->",fg="white",bg="black",command=question)
                    nextbut.place(x=600,y=500)
                    
            done=tk.Button(new,text="Done",bg="Black",fg="white",command=don,width=20)
            done.place(x=150,y=250)
            bunew3.place(x=603,y=300)
            bunew2.place(x=600,y=250)
            bunew.place(x=600,y=200)
            newlabel2.place(x=100,y=200)
            newlabel.place(x=100,y=100)
            newlabel1.place(x=100,y=150)
            new.configure(bg="lightsteelblue1")
        
        def video():
            vid=tk.Tk()
            vid.geometry('300x300')
            newlabel=tk.Label(vid,text="Click On watch",fg="White",bg="black")
            label1=tk.Label(vid,text="Video 1: ",bg="lightsteelblue",fg="black")
            windows_speak.speak("watch any one of these videos")
            def play():
                webbrowser.open('https://youtu.be/Vw1_AEaoXtM')
            button1=tk.Button(vid,text="watch",bg="black",fg="white",command=play)
            label2=tk.Label(vid,text="Video 2: ",bg="lightsteelblue",fg="black")
            def play2():
                webbrowser.open('https://youtu.be/eAK14VoY7C0')
            button2=tk.Button(vid,text="watch",bg="black",fg="white",command=play2)
            label3=tk.Label(vid,text="Video 3: ",bg="lightsteelblue",fg="black")
            def play3():
                webbrowser.open('https://youtu.be/1I9ADpXbD6c')
            button3=tk.Button(vid,text="watch",bg="black",fg="white",command=play3)
            label4=tk.Label(vid,text="Video 4: ",bg="lightsteelblue",fg="black")
            def play4():
                webbrowser.open('https://youtu.be/W5tlGJwvmCQ')
            button4=tk.Button(vid,text="watch",bg="black",fg="white",command=play4)
            newlabel.place(x=100,y=0)
            label1.place(x=30,y=30)
            button1.place(x=100,y=30)
            label2.place(x=30,y=60)
            button2.place(x=100,y=60)
            label3.place(x=30,y=90)
            button3.place(x=100,y=90)
            label4.place(x=30,y=120)
            button4.place(x=100,y=120)
            vid.configure(bg="lightsteelblue1")
        def find():
            webbrowser.open('https://www.google.com/search?q=psychiatrist+near+me&rlz=1C1CHWL_enIN878IN878&oq=psychiatrist+near+me&aqs=chrome..69i57j0l7.6015j0j7&sourceid=chrome&ie=UTF-8')
            windows_speak.speak("Finding psychiatrists near you!")
        def hel():
            new=tk.Tk()
            new.geometry('1095x500')
            label=tk.Label(new,text="MindConnect was created as an effort to curb the number of suicides in the world, as well as to help anyone that is\ndealing with emotional or psychological stress during these tough times.\n\nUse the 'Check Your Symptoms' tab to assess your mental state. According to the severity of your symptoms, we shall\ndetermine what might be the best course of action that you can take to help elevate your mood. If you show mild symptoms\nrelated with depression, we shall direct you to a wide variety of motivational videos on YouTube, as well as provide you\nwith a list of various exercises that have been shown to reduce stress and increase happiness. But, if you show more\nsevere signs, then we will help you contact the nearest the psychiatrist available. Suicide hotline numbers relevant to\nyour location are also displayed for you to use.\n\nUse the 'Contact Psychiatrist' to immediately link you to the nearest available psychiatrist.\n\nAnd remember, we're all in this together, and we'll all make it out of this together. We believe in you!",width=100,font=18)
            label.place(x=100,y=100)
            new.configure(bg="lightsteelblue")
        form=tkf.Font(family="Times new Roman",size=28)    
        mindco=tk.Label(basic,text="MindConnect",fg="grey1",bg="white",width=20,font=form)    
        mindco.place(x=100,y=100)
        button2=tk.Button(basic,text="Check Here",fg="grey1",bg="old lace",command=check,width=30)
        button3=tk.Button(basic,text="Click here",fg="grey1",bg="old lace",command=video,width=30)
        button4=tk.Button(basic,text="Click here",fg="grey1",bg="old lace",command=find,width=30)
        button5=tk.Button(basic,text="Help!",fg="grey1",bg="old lace",width=30,command=hel)
        labl1.place(x=340,y=200) 
        button2.place(x=640,y=200)
        labl2.place(x=340,y=250)
        button3.place(x=640,y=250)
        labl3.place(x=340,y=300)
        button4.place(x=640,y=300)
        labl4.place(x=340,y=350)
        button5.place(x=640,y=350)
        lab=tk.Label(basic,text=actualstring,bg="white",fg="black",font=f2,height=1,width=90)
        basic.configure(bg="lightsteelblue2")
        lab.place(x=100,y=40)
    
    





button=tk.Button(text="Continue",fg="grey1",bg="old lace",command=action)
label1=tk.Label(text="Age :",bg="lightsteelblue1",fg="Black",font=f1,height="1",width="4")
label.place(x=529,y=395)
label1.place(x=529,y=445)
button.place(x=600,y=485)
window.configure(bg="lightsteelblue1")
windows_speak.speak("Welcome. Please enter your name and age")
window.mainloop()


