blacklistedWords = ['membunuh', 'anjing', 'penjara', 'laporin', 'hukuman', 'mati']
kalimat = input('Masukkan kalimat: ')

for word in blacklistedWords:
    if word in kalimat:
        if len(word) > 3:
            kalimat = kalimat.replace(word, word[:-3] + '***')
        else:
            kalimat = kalimat.replace(word, '*' * len(word))

print(kalimat)
