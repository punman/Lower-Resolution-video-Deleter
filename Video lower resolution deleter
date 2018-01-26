import os
import re

path='path specify by user'
files=os.listdir(path)
toDel=[]
reso = ['1080p','720p','480p','360p','240p']


for i in files:
    if re.findall('1080p',i):
        patt=i.split('1080p')[0]
        for j in files:
            if re.findall(patt,j):
                if not re.findall('1080p',j):
                    toDel.append(j)
                    
for i in files:
    if re.findall('720p',i):
        patt=i.split('720p')[0]
        for j in files:
            if re.findall(patt,j):
                if not (re.findall('720p',j) or re.findall('1080p',j) ):
                    toDel.append(j)
                    
for i in files:
    if re.findall('480p',i):
        patt=i.split('480p')[0]
        for j in files:
            if re.findall(patt,j):
                if not (re.findall('480p',j) or re.findall('720p',j)or re.findall('1080p',j) ):
                    toDel.append(j)

setdel=set(toDel)

l2=[] 
for item in files:
    for res in list(reversed(reso)):
        if re.findall(res,item):
            l2.append(item)
  
setdel=set(toDel)
for i in setdel:
    os.remove(os.path.join(path,i))
