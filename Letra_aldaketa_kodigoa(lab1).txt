testua = input("Sartu testua: ")

hizkiak = [*testua]

balioak = ["e","a","o","l","s","n","d","r","u","i","t","c"
          ,"p","m","y","q","b","h","g","f","v","j","ñ","z","x","k","w"]

alfabetoa = ["A","B","C","D","E","F","G","H","I","J"
             ,"K","L","M","N","Ñ","O","P","Q","R","S","T"
             ,"U","V","W","X","Y","Z"]

kopurua = [0] * len(balioak)

for i in range(len(hizkiak)):
    for j in range(len(alfabetoa)):
        if (hizkiak[i] == alfabetoa[j]):
            kopurua[j] = kopurua[j] + 1

for i in range(len(alfabetoa)):
    print(alfabetoa[i] + ":", str(kopurua[i]) + ", ", end="")
print()
print("Hizki ohikoenak ordenean:")
print(balioak)
    
while(True):

    hizkiKendu = input("Sartu aldatu nahi duzun hizkia edo -1 ateratzeko:")     
    
    if (hizkiKendu == "-1" ):
        break
       
    hizkiJarri = input("Sartu aldatu nahi duzun hizkia: ")
    
    testua = testua.replace(hizkiKendu, hizkiJarri)

    print(testua)
    
print(testua)