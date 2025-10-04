# 👻 I-Module Yokuphepha kwa-Ghost
**Ithuluzi Lokuqinisa Ukuphepha kwa-Windows ne-Azure Elisuselwe ku-PowerShell**

> **Ukuqinisa ukuphepha okusebenzayo kumaphuzu okuphela kwa-Windows nemvelo ye-Azure.** I-Ghost inikeza imisebenzi yokuqinisa esuselwe ku-PowerShell engasiza ekwehliseni ama-vector okuhlasela avamile ngokuvala amasevisi namaphrothokholi angadingeki.

## ⚠️ Izitatimende Zokuziphephisa Ezibalulekile

**UKUHLOLWA KUYADINGEKA**: Hlola i-Ghost njalo kuqala kwezindawo ezingeyona ezokhiqizo. Ukuvala amasevisi kungathinta imisebenzi yebhizinisi esemthethweni.

**AWUKHO UMQINISEKO**: Nakuba i-Ghost igxile kuma-vector okuhlasela avamile, awukho ubuchwepheshe bokuphepha obungavimbela konke ukuhlaselwa. Lokhu kuyingxenye ye-strategy yokuphepha ehlanganisiwe.

**UMTHELELA WOKUSEBENZA**: Eminye imisebenzi ingathinta ukusebenza kwesistimu. Buyekeza ngokucophelela ukusetha okukodwa ngaphambi kokuhambisa.

**UKUHLOLWA KWENGOTI**: Kwezindawo ezokhiqizo, bonisana nezingoti zokuphepha ukuze uqinisekise ukuthi ukusetha kuvumelana nezidingo zenhlangano yakho.

## 📊 Indawo Yokuphepha

Ukulimala kwe-Ransomware kufinyelele **ku-$57 billion ngo-2025**, ucwaningo lubonisa ukuthi ukuhlaselwa okuningi okuphumelelayo kusebenzisa amasevisi ama-Windows asisisekelo nokumiswa okungalungile. Ama-vector okuhlasela avamile afaka:

- **90% yezigameko ze-ransomware** zibandakanya ukusetshenziswa kwe-RDP
- **Ubuthakathaka be-SMBv1** okwavumela ukuhlaselwa okufana ne-WannaCry ne-NotPetya
- **Ama-macro amadokhumenti** asaqhubeka njengendlela eyinhloko yokuthunyelwa kwe-malware
- **Ukuhlaselwa okususelwe ku-USB** kuqhubeka nokugxila emanetwekini aphakathi komoya
- **Ukusetshenziswa kabi kwe-PowerShell** kwenyuke kakhulu eminyakeni yamuva

## 🛡️ Imisebenzi Yokuphepha ka-Ghost

I-Ghost inikeza **16 imisebenzi yokuqinisa kwa-Windows** kanye **nokuhlanganiswa kokuphepha kwe-Azure**:

### Ukuqinisa Iphuzu Lokuphela kwa-Windows

| Umsebenzi | Inhloso | Ukucabangela |
|----------|---------|----------------|
| `Set-RDP` | Iphethe ukufinyelela kwe-Remote Desktop | Kungathinta ukulawula okukude |
| `Set-SMBv1` | Ilawula iphrothokholi yakudala ye-SMB | Iyadingeka kumasistemu amadala kakhulu |
| `Set-AutoRun` | Ilawula i-AutoPlay/AutoRun | Kungathinta ukulula komsebenzisi |
| `Set-USBStorage` | Ikhawulela amadivayisi okugcina i-USB | Kungathinta ukusebenzisa i-USB okusemthethweni |
| `Set-Macros` | Ilawula ukwenziwa kwama-macro e-Office | Kungathinta amadokhumenti avumela ama-macro |
| `Set-PSRemoting` | Iphethe i-PowerShell remoting | Kungathinta ukulawula okukude |
| `Set-WinRM` | Ilawula i-Windows Remote Management | Kungathinta ukulawula okukude |
| `Set-LLMNR` | Iphethe iphrothokholi yokuxazulula amagama | Ngokuvamile kuphephile ukuyivala |
| `Set-NetBIOS` | Ilawula i-NetBIOS phezu kwe-TCP/IP | Kungathinta izinhlelo zokusebenza zakudala |
| `Set-AdminShares` | Iphethe ukwabelana kokulawula | Kungathinta ukufinyelela kwefayela okukude |
| `Set-Telemetry` | Ilawula ukuqoqwa kwedatha | Kungathinta amakhono okuxilonga |
| `Set-GuestAccount` | Iphethe i-akhawunti yesivakashi | Ngokuvamile kuphephile ukuyivala |
| `Set-ICMP` | Ilawula izimpendulo ze-ping | Kungathinta ukuxilonga kwenethiwekhi |
| `Set-RemoteAssistance` | Iphethe usizo olukude | Kungathinta ukusebenza kwe-helpdesk |
| `Set-NetworkDiscovery` | Ilawula ukuthola kwenethiwekhi | Kungathinta ukuphequlula kwenethiwekhi |
| `Set-Firewall` | Iphethe i-Windows Firewall | Kubalulekile ekuphepheni kwenethiwekhi |

### Ukuphepha Kwefu Ye-Azure

| Umsebenzi | Inhloso | Izidingo |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Ivula ukuphepha kwezisekelo kwe-Azure AD | Izimvume ze-Microsoft Graph |
| `Set-AzureConditionalAccess` | Ilungisa amasu okufinyelela | Ukulayisensa kwe-Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Ihlola ama-akhawunti anemvume ekhethekile | Izimvume ze-Global Admin |

### Izinketho Zokuhambisa Kwamabhizinisi

| Indlela | Icala Lokusetshenziswa | Izidingo |
|--------|----------|--------------|
| **Ukwenziwa Okuqondile** | Ukuhlola, izindawo ezincane | Amalungelo omlawuli wendawo |
| **Group Policy** | Izindawo zesizinda | Umlawuli wesizinda, ukulawula i-GP |
| **Microsoft Intune** | Amadivayisi alawulwa yifu | Ukulayisensa kwe-Intune, Graph API |

## 🚀 Ukuqala Ngokushesha

### Ukuhlola Ukuphepha
```powershell
# Layisha i-module ka-Ghost
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')

# Hlola isimo sokuphepha samanje
Get-Ghost
```

### Ukuqinisa Okuyisisekelo (Hlola Kuqala)
```powershell
# Ukuqinisa okubalulekile - hlola endaweni yelabhorethri kuqala
Set-Ghost -SMBv1 -AutoRun -Macros

# Buyekeza izinguquko
Get-Ghost
```

### Ukuhambisa Kwamabhizinisi
```powershell
# Ukuhambisa kwe-Group Policy (izindawo zesizinda)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Ukuhambisa kwe-Intune (amadivayisi alawulwa yifu)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Izindlela Zokufaka

### Ukukhetha 1: Ukulanda Okuqondile (Ukuhlola)
```powershell
IEX(Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1')
```

### Ukukhetha 2: Ukufaka I-Module
```powershell
# Faka kusuka ku-PowerShell Gallery (uma kutholakala)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Ukukhetha 3: Ukuhambisa Kwamabhizinisi
```powershell
# Kopisha endaweni yenethiwekhi ukuhambisa kwe-Group Policy
# Lungiselela ama-script e-Intune PowerShell ukuhambisa kwefu
```

## 💼 Izibonelo Zamacala Okusetshenziswa

### Ibhizinisi Elincane
```powershell
# Ukuvikela okuyisisekelo ngomthelela omncane
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Indawo Yokunakekelwa Kwempilo
```powershell
# Ukuqinisa okugxile ku-HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Amasevisi Ezezimali
```powershell
# Ukumisa ukuphepha okuphezulu
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Inhlangano Yefu-Kuqala
```powershell
# Ukuhambisa okulawulwa yi-Intune
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Imininingwane Yemisebenzi

### Imisebenzi Yokuqinisa Eyinhloko

#### Amasevisi Enethiwekhi
- **RDP**: Ivimbela ukufinyelela kwe-desktop okukude noma ihlanganise isango
- **SMBv1**: Ivala iphrothokholi yakudala yokwabelana ngefayela
- **ICMP**: Ivimbela izimpendulo ze-ping zokuhlola
- **LLMNR/NetBIOS**: Ivimbela amaphrothokholi akudala okuxazulula amagama

#### Ukuphepha Kohlelo Lokusebenza
- **Ama-macro**: Ivala ukwenziwa kwama-macro ezinhlelweni zokusebenza ze-Office
- **AutoRun**: Ivimbela ukwenziwa okuzenzakalelayo kusuka kumedia esusekayo

#### Ukulawula Okukude
- **PSRemoting**: Ivala izihlangano ze-PowerShell ezikude
- **WinRM**: Imisa i-Windows Remote Management
- **Remote Assistance**: Ivimbela ukuxhumana nosizo olukude

#### Ukulawula Ukufinyelela
- **Admin Shares**: Ivala ukwabelana kwe-C$, ADMIN$
- **Guest Account**: Ivala ukufinyelela kwe-akhawunti yesivakashi
- **USB Storage**: Ikhawulela ukusetshenziswa kwedivayisi ye-USB

### Ukuhlanganiswa kwe-Azure
```powershell
# Xhuma ku-tenant ye-Azure
Connect-AzureGhost -Interactive

# Vula ukumisa okuvamile kokuphepha
Set-AzureSecurityDefaults -Enable

# Lungiselela ukufinyelela okubandakanyayo
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Hlola abasebenzisi abanemvume ekhethekile
Set-AzurePrivilegedUsers -AuditOnly
```

### Ukuhlanganiswa kwe-Intune (Okusha ku-v2)
```powershell
# Xhuma ku-Intune
Connect-IntuneGhost -Interactive

# Hambisa ngamasu e-Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Ukucabangela Okubalulekile

### Izidingo Zokuhlola
- **Indawo Yelabhorethri**: Hlola wonke amasetha endaweni ehlukaniselwe kuqala
- **Ukuhambisa Ngezigaba**: Nweba kancane kancane ukuthola izinkinga
- **Uhlelo Lokubuyela Emuva**: Qinisekisa ukuthi ungakwazi ukuguqula izinguquko uma kudingeka
- **Ukubhalwa**: Qopha ukuthi yiziphi izilungiselelo ezisebenza endaweni yakho

### Umthelela Ongaba Khona
- **Ukukhiqiza Komsebenzisi**: Ezinye izilungiselelo zingathinta ukuhamba komsebenzi wansuku zonke
- **Izinhlelo Zokusebenza Zakudala**: Amasistimu amadala angadinga amaphrothokholi athile
- **Ukufinyelela Okukude**: Cabangela umthelela kukulawula okukude okusemthethweni
- **Izinqubo Zebhizinisi**: Qinisekisa ukuthi izilungiselelo aziphuli imisebenzi ebalulekile

### Imikhawulo Yokuphepha
- **Ukuzivikela Okujulile**: I-Ghost iyisendlalelo esisodwa sokuphepha, hhayi isisombululo esigcwele
- **Ukulawula Okuqhubekayo**: Ukuphepha kudinga ukuqapha nokuguqula okuqhubekayo
- **Ukuqeqeshwa Komsebenzisi**: Ukulawula kwezobuchwepheshe kumele kuhlanganiswe nokuqaphela ukuphepha
- **Ukuguquka Kwezinsongo**: Izindlela zokuhlasela ezintsha zingadlula ukuvikela kwamanje

## 🎯 Izibonelo Zezimo Zokuhlasela

Nakuba i-Ghost igxile kuma-vector okuhlasela avamile, ukuvimba okukhethekile kuncike ekusetshenzisweni okufanele nokuhloleni:

### Ukuhlaselwa Kwehlobo le-WannaCry
- **Ukunciphisa**: `Set-Ghost -SMBv1` kuvala iphrothokholi ebuthakathaka
- **Ukucabangela**: Qinisekisa ukuthi awukho uhlelo lwakudala oludinga i-SMBv1

### I-Ransomware Esuselwe ku-RDP
- **Ukunciphisa**: `Set-Ghost -RDP` kuvimbela ukufinyelela kwe-desktop okukude
- **Ukucabangela**: Kungadingeka izindlela zokufinyelela okukude ezinye

### I-Malware Esuselwe Emadokhumenti
- **Ukunciphisa**: `Set-Ghost -Macros` kuvala ukwenziwa kwama-macro
- **Ukucabangela**: Kungathinta amadokhumenti asemthethweni anamakro

### Izinsongo Ezilethwa yi-USB
- **Ukunciphisa**: `Set-Ghost -USBStorage -AutoRun` kukhawulela ukusebenza kwe-USB
- **Ukucabangela**: Kungathinta ukusetshenziswa kwedivayisi ye-USB okusemthethweni

## 🏢 Izici Zamabhizinisi

### Ukusekela i-Group Policy
```powershell
# Sebenzisa izilungiselelo ngereijisethi ye-Group Policy
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Izilungiselelo zisebenza kuso sonke isizinda ngemuva kokuvuselela i-GP
gpupdate /force
```

### Ukuhlanganiswa kwe-Microsoft Intune
```powershell
# Dala amasu e-Intune azilungiselelo zika-Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Amasu ahambisa ngokuzenzakalela kumadivayisi alawulwayo
```

### Ukubika Ukuvumelana
```powershell
# Khiqiza umbiko wokuhlola ukuphepha
Get-Ghost | Export-Csv -Path "Ukuhlola-Ukuphepha-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Umbiko wesimo sokuphepha se-Azure
Get-AzureGhost | Out-File "Umbiko-Ukuphepha-Azure.txt"
```

## 📚 Izinqubo Ezinhle Kakhulu

### Ngaphambi Kokuhambisa
1. **Bhala Isimo Samanje**: Qalisa `Get-Ghost` ngaphambi kwezinguquko
2. **Hlola Ngokuphelele**: Qinisekisa endaweni engeyona eyokhiqizo
3. **Hlela Ukubuyela Emuva**: Azi ukuthi ungaguqula kanjani ukusetha okukodwa
4. **Ukubuyekezwa Kwababambe Iqhaza**: Qinisekisa ukuthi izingxenye zebhizinisi ziyavuma izinguquko

### Ngesikhathi Sokuhambisa
1. **Indlela Yezigaba**: Hambisa emaqenjini apayona kuqala
2. **Qapha Umthelela**: Bhekela izikhalo zabasebenzisi noma izinkinga zesistimu
3. **Bhala Izinkinga**: Qopha noma yiziphi izinkinga zesikhathi esizayo
4. **Xhumana Ngezinguquko**: Tshela abasebenzisi ngokuthuthukiswa kokuphepha

### Ngemuva Kokuhambisa
1. **Ukuhlola Njalonjalo**: Qalisa `Get-Ghost` ngezikhathi ezithile ukuqinisekisa izilungiselelo
2. **Buyekeza Ukubhalwa**: Gcina ukumiswa kokuphepha kwakamuva
3. **Buyekeza Ukusebenza**: Qapha izigameko zokuphepha
4. **Ukuthuthukiswa Okuqhubekayo**: Lungisa izilungiselelo ngokuya ngendawo yezinsongo

## 🔧 Ukuxazulula Izinkinga

### Izinkinga Ezivamile
- **Amaphutha Emvume**: Qinisekisa isihlangano se-PowerShell esiphakanyisiwe
- **Ukuncika Kwesevisi**: Amanye amasevisi angaba nokuncika
- **Ukuvumelana Kohlelo Lokusebenza**: Hlola ngezinhlelo zokusebenza zebhizinisi
- **Ukuxhumana Kwenethiwekhi**: Qinisekisa ukuthi ukufinyelela okukude kusasebenza

### Izinketho Zokubuyisela
```powershell
# Vula kabusha amasevisi athile uma kudingeka
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Mayelana Nombhali

**Jim Tyler** - Microsoft MVP we-PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ abayifaka egazini)
- **Iphepha Lezindaba**: [PowerShell.News](https://powershell.news) - Ulwazi lweviki ngalunye lwokuphepha
- **Umbhali**: "PowerShell for Systems Engineers"
- **Isipiliyoni**: Amashumi eminyaka we-PowerShell automation nokuphepha kwa-Windows

## 📄 Ilayisense Nokuziphephisa

### Ilayisense ye-MIT
I-Ghost inikezwa ngaphansi kwelayisense ye-MIT yokusetshenziswa kwalapha, ukuguqula nokusabalalisa.

### Ukuziphephisa Kokuphepha
- **Awukho Umqiniseko**: I-Ghost inikezwa "njengoba injalo" ngaphandle kwamaqiniseko anoma yiluphi uhlobo
- **Ukuhlola Kuyadingeka**: Hlola njalo kuqala ezindaweni ezingeyona ezokhiqizo
- **Ukuhola Kwengoti**: Bonisana nezingoti zokuphepha zokuhambisa okukhiqizayo
- **Umthelela Wokusebenza**: Ababhali abaziphenduleli noma yikuphi ukuphazamiseka kokusebenza
- **Ukuphepha Okugcwele**: I-Ghost iyingxenye ye-strategy yokuphepha egcwele

### Ukusekela
- **GitHub Issues**: [Bika amaphutha noma ucele izici](https://github.com/jimrtyler/Ghost/issues)
- **Ukubhalwa**: Sebenzisa `Get-Help <function> -Full` usizo oluningi
- **Umphakathi**: Amafomo omphakathi we-PowerShell nokuphepha

---

**🔒 Qinisa isimo sakho sokuphepha nge-Ghost - kodwa njalo hlola kuqala.**

```powershell
# Qala ngokuhlola, hhayi ngokucabanga
Get-Ghost
```

**⭐ Nika le repository inkanyezi uma i-Ghost isiza ukuthuthukisa isimo sakho sokuphepha!**