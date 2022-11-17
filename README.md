# Registratsiyaf
l = {}
def register():
    
    
        foydalanuvchi = input("Ismizni kiriting: ").capitalize()
        familiya = input("Familiyanguzni kiriting: ").capitalize()
        parol = input("Parol: ")
        if f'{foydalanuvchi}|{familiya}' in list(l.keys()):
            print('Siz allaqachon ro`yxatdan o`tgansiz, iltimos boshqa foydalanuvchi ismini kirting')
            print(l)
        else:
            l[f'{foydalanuvchi}|{familiya}'] = parol
            print("Ro`yxatdan muvaffaqiyatli o`tdingiz")

def view():
    print("Parolni unutdingizmi? Unda")
    foydalanuvchi = input("Ismizni kiriting: ").capitalize()
    familiya = input("Familiyanguzni kiriting: ").capitalize()
    if f'{foydalanuvchi}|{familiya}' in list(l.keys()):
        print(l[f'{foydalanuvchi}|{familiya}'])
    else:
        print("Siz ro`yxatdan o`tmagansiz")

def signin():
    ism = input("Ismni kiriting: ").capitalize()
    familiya = input("Familiyani kiriting: ").capitalize()
    parol = input("Parolni kiriting: ")
    if f'{ism}|{familiya}' in list(l.keys()):
        if parol == l[f'{ism}|{familiya}']:
            print("Ishchi oynaga xush kelibsiz")
        else:
            view()


register()

signin()l = {}
