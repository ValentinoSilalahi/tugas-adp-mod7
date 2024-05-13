print ( " Nama : Valentino Silalahi " )
print ( " Nim  : 2310431015 " )
print ( " Program Konversi Suhu Cuy " )
print ( " ================================================== " )
print()

def k_sh(d_sh, s_sh):
     if  s_sh == 'C' and d_sh >= 0 and d_sh <= 100 :
          f = "{:.2f}".format((d_sh * 9/5) + 32)
          k = "{:.2f}".format(d_sh + 273.15)
          r = "{:.2f}".format(d_sh * 4/5)
          return f" || {'Fahrenheit':<15} || {f:<15} ||\n || {'Kelvin':<15} || {k:<15} ||\n || {'Reamur':<15} || {r:<15} || "
     elif  s_sh == 'F' and d_sh >= 32 and d_sh <= 212 :
          c = "{:.2f}".format((d_sh - 32) * 5/9)
          k = "{:.2f}".format(float(c) + 273.15)
          r = "{:.2f}".format((d_sh - 32) * 4/9)
          return f" || {'Celcius':<15} || {c:<15} ||\n || {'Kelvin':<15} || {k:<15} ||\n || {'Reamur':<15} || {r:<15} || "
     elif  s_sh == 'K' and d_sh >= 273.15 and d_sh <= 373.15 :
          c = "{:.2f}".format((d_sh - 273.15))
          f = "{:.2f}".format((float(c) * 9/5) +32)
          r = "{:.2f}".format(float(c) * 4/5)
          return f" || {'Celcius':<15} || {c:<15} ||\n || {'Fahrenheit':<15} || {f:<15} ||\n || {'Reamur':<15} || {r:<15} || "
     elif  s_sh == 'R' and d_sh >= 0 and d_sh <= 80 :
          c = "{:.2f}".format(d_sh * 5/4)
          f = "{:.2f}".format((float(c) * 9/5) + 32)
          k = "{:.2f}".format(float(c) + 273.15)
          return f" || {'Celcius':<15} || {c:<15} ||\n || {'Fahrenheit':<15} || {f:<15} ||\n || {'Kelvin':<15} || {k:<15} || "
     else :
          return " Suhu yang anda masukkan tidak valid "

def Pk_sh(d_sh, s_sh):
     
     Pk_sh1 = k_sh(d_sh, s_sh)
     print ( f" Suhu {d_sh} derajat {s_sh} dapat dikonversi menjadi : " )
     print ( " ======================================== " )
     print ( f" || {'Satuan Suhu':<15} || {'Derajat Suhu':<15} || " )
     print ( " ||-----------------||-----------------|| " )
     print ( Pk_sh1 )
     print ( " ======================================== " )

d_sh = float ( input ( " Masukkan derajat suhu : " ) )
s_sh = input ( " Masukkan satuan suhu  : " ).upper()
print()
Pk_sh(d_sh, s_sh)
print()
