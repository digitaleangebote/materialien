---
title: email einrichten in emailclients
author: chantal
date: 2023-05-24
category: Jekyll
layout: post
---
# warum mehrere emailadressen und -postfächer?

wir alle "tanzen" im internet sozusagen „auf mehreren hochzeiten“. wir sind "beruflich" und "privat" unterwegs. und genau dieser aspekt ist der grund dafür, auf mehrere emailadressen zu setzen: die unterschiedlichen arten der nutzung

um zum beispiel mit der geschäftlichen emailadresse von zu viel spamnachrichten verschont zu bleiben, sollten wir diese nur für berufliche zwecke nutzen. eine weitere emailadressee eignet sich nur für den bereich shopping. und eine dritte kann beispielsweise dazu verwendet werden, sich in sozialen netzwerken anzumelden usw. usf.

# emailverkehr

elektronische post wird über mailserver transportiert und in postfächer gespeichert.  
wir können mithilfe von clients darauf zugreifen

# der zugriff auf die postfächer

der zugriff auf die postfächer erfolgt entweder über eine mehr oder weniger nette weboberfläche im browser oder über einen beliebigen emailclient.  
letztgenannte sprechen mit den postfächern über die etablierten standardverfahren  
IMAP, POP3 und SMTP  
den link zu der weboberfläche erfahren wir bei unserem emailanbieter  

# es gibt 2 arten von emailpostfächern
diese clients greifen auf protokolle zurück, um die emails anzuzeigen  
je nach verwendetem protokoll ist die vorgehensweise eine andere  
das netzwerkprotokoll IMAP öffnet die nachrichten direkt auf dem server,
das übertragungsprotokoll POP3 lädt die nachrichten erst herunter und öffnet sie dann lokal

# der zugriff auf emailpostfächer
IMAP
das Internet Message Access Protocol – kurz IMAP – ist ein textbasiertes netzwerkprotokoll, das den zugriff auf emails ermöglicht, die sich auf einem mailserver befinden.  
wenn wir unser konto mit IMAP einrichten (eingerichtet haben), stellt der emailclient bei jedem login eine verbindung zum server her, die während der gesamten sitzung bestehen bleibt.
wir können in dieser zeit auf einzelne ordner und emails zugreifen, deren inhalte auf anfrage angezeigt werden. dabei bleiben alle nachrichten und angelegten ordnerstrukturen auf dem server gespeichert, bis sie gelöscht werden.  
dadurch können wir von überall aus und mit mehreren clients auf den mailserver zugreifen und finden immer den gleichen, aktuellen datenbestand vor  

die verbindung zwischen server und IMAP-client wird über TCP/IP auf Port 143 (bei gesicherter verbindung Port 993) hergestellt 

POP3
das Post Office Protocol (POP3) ermöglicht das abrufen von emails mithilfe eines clients.  
zu diesem zweck stellt der client eine verbindung zu einem posteingangsserver her, auf dem die notwendige POP3-Server-Software installiert sein muss   
die dort liegenden emails werden heruntergeladen und auf dem rechner des clients gespeichert   anschließend werden die elektronischen nachrichten vom mailserver gelöscht und die verbindung getrennt   
den inhalt der emails können wir dann lokal öffnen und bearbeiten, ohne dass client und server verbunden sind  
je nach größe der mailinhalte bzw. -anhänge variiert die dauer des abholungsprozesses  
jede nachricht kann nur von einem POP3-Client heruntergeladen werden
beim verbindungsprozess zum mailserver über TCP/IP greifen POP3-Clients auf Port 110 zurück   
ist die verbindung verschlüsselt, wird Port 995 genutzt 

## der unterschied zwischen imap und pop3

ein vergleich der beiden protokolle zeigt, dass es einige elementare unterschiede zwischen IMAP und POP3 gibt: 

während clients mit IMAP eine dauerhafte verbindung zum mailserver herstellen, besteht die verbindung von POP3-client und POP3-server nur, während die nachrichten abgerufen werden   
eng damit verbunden ist auch der unterschiedliche umgang mit abgerufenen emails 
mit POP3 heruntergeladene mails werden im anschluss vom mailserver gelöscht   
beim netzwerkprotokoll IMAP, bleiben sämtliche nachrichten solange auf dem server, bis sie manuell gelöscht werden   
das ist auch der grund, warum bei der verwendung von IMAP mehrere clients zur selben zeit zugriff auf den gleichen datenbestand haben können 

mit POP3 ist der zugriff auf einen einzelnen client beschränkt, da immer alle erhaltenen mails auf den lokalen rechner heruntergeladen werden

# mails mit smartphone und/oder tablet
da wir unsere mails mit smartphone und/oder tablet bzw. mit mehreren clients abrufen wollen, ist IMAP sicher die bessere wahl. insbesondere, wenn wir unterwegs nur auf die mobile datenverbindung zurückgreifen können, ist es von vorteil, dass IMAP nur die gewünschten mails abruft – so können wir nachrichten mit großen inhalten stattdessen zu hause am rechner öffnen. da keine lokale version der mails heruntergeladen wird, benötigen wir jedoch in jedem fall eine bestehende internetverbindung. über die funktion des emailabrufs hinaus ist es mit dem netzwerkprotokoll IMAP auch möglich, ordnerstrukturen anzulegen und zu verwalten, den bearbeitungsstatus der mails zu kennzeichnen und versendete nachrichten zu archivieren. durch diese zusätzlichen funktionen und die tatsache, dass die emails bis zur löschung auf dem server gespeichert sind, führt IMAP zu einer deutlich stärkeren auslastung des mailservers als POP3  


# das SMTP protokoll
smtp ist das simple mail transfer protocol also das mailsendeprotokoll

# welche daten gehören zu einem emailpostfach?

die einrichtungsdaten für emailclients sind immer folgende:
- die emailadresse an sich
- der benutzername
- das passwort
- der eingangsserver - imap und sein port
- der ausgangsserver - smtp und sein port
- die verschlüsselung - ssl oder tls

um also, die uni emailadresse auf deinen geräten einzurichten, musst du dir erst einmal diese daten zusammensuchen  
da alle emailpostfachkunden von allen ihren emailanbietern diese daten brauchen, werden diese eigentlich prominent angezeigt  
leider hat sich die uni aber dazu entschieden microsoft exchange zwischenzuschalten ;-((  

## die persönlichen daten    
die emailadresse, die die uni für uns angelegt hat, finden wir in prisma  
den benutzernamen auch  
das passwort haben wir selbst verändert und kennen es selbstverständlich auswendig ;-))  

## die allgemeinen daten (ohne microsoft)

der (eingangsserver) imapserver heißt imap.uni-bielefeld.de , sein port ist der 993 und seine verschlüsselung ist der sicherheitstyp ssl/tsl

der (ausgangsserver) smtpserver heißt smtp.uni-bielefeld.de , sein port ist der 587 und seine verschlüsselung ist ssl/tsl

bleibt die frage, wo du diese daten jetzt eingeben musst

# emailclients

## macosx
der mailclient auf dem mac heißt mail

## windows

für windows gibt es unterschiedliche mailclients
- outlook ist ein client, der aber auch eine menge anderer daten verwaltet
- thunderbird
- mail?

## linux

der mailclient thunderbird ist wahrscheinlich der bekannteste

## ios

der mailclient auf den ios geräten heißt mail

## android

bluemail scheint neu und sehr gut zu sein
k-9 mail ist schon älter





