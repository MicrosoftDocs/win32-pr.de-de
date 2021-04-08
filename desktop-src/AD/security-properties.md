---
title: Benutzersicherheitsattribute
description: Zusätzlich zu den Benennungs Eigenschaften für Benutzer Objekte (z. b. "objectGUID", "objectSID", "CN", "Unterscheid Name" usw.) gibt es weitere Sicherheitseigenschaften, die für die Anmeldung, den Netzwerk Zugriff und die Zugriffs Steuerung verwendet werden.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Sicherheits Attribute mit AD
- Benutzer Sicherheits Attribute ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "103949196"
---
# <a name="user-security-attributes"></a>Benutzersicherheitsattribute

Zusätzlich zu den Benennungs Eigenschaften für Benutzer Objekte (z. b. " [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)", " [**objectSID**](/windows/desktop/ADSchema/a-objectsid)", " [**CN**](/windows/desktop/ADSchema/a-cn)", " [**Unterscheid Name**](/windows/desktop/ADSchema/a-distinguishedname)" usw.) gibt es weitere Sicherheitseigenschaften, die für die Anmeldung, den Netzwerk Zugriff und die Zugriffs Steuerung verwendet werden. Diese Eigenschaften werden vom Sicherheitssystem von Windows 2000 verwendet. Diese Eigenschaften können über das Active Directory Benutzer-und Computer-Snap-in angezeigt und verwaltet werden.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

Das [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires) -Attribut gibt an, wann ein Konto abläuft. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Ein Wert von **timeq \_ Forever** (definiert in "lmaccess. h") gibt an, dass ein Konto nie abläuft.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altsecurityidentitäten**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

Das Attribut " [**altsecurityidentities**](/windows/desktop/ADSchema/a-altsecurityidentities) " ist ein mehr wertiges Attribut, das Zuordnungen für X. 509-Zertifikate oder externe Kerberos-Benutzerkonten für diesen Benutzer zum Zweck der Authentifizierung enthält. Verschiedene Sicherheitspakete, einschließlich des Public Key-Authentifizierungs Pakets und der Kerberos-Authentifizierung, verwenden diese Daten zum Authentifizieren von Benutzern, wenn Sie die Alternative identifikationsform (z. b. Zertifikat, UNIX-Kerberos-Ticket usw.) darstellen. Erstellen Sie ein Windows 2000-Token basierend auf dem entsprechenden Benutzerkonto, damit Sie auf Systemressourcen zugreifen können.

Bei X. 509-Zertifikaten sollten die Werte der Aussteller-und Antragsteller Namen in 509v3-Zertifikaten sein, die von einer externen öffentlichen Zertifizierungsstelle ausgestellt wurden und die dem Benutzerkonto zugeordnet sind, das für die Suche nach einem Konto für die Authentifizierung verwendet wird. Das SSL-Paket (SChannel) verwendet die folgende Syntax: X509: <somecertinfotype> somecertinfo. Der folgende Wert gibt beispielsweise den Aussteller-DN "" \<I\> mit dem DN "c = US, O = internetca, CN = apubliccertificateauthority" und "Subject DN" \<S\> mit dem DN "c = US, o = fabrikam, OU = Sales, CN = Jeff Smith" an.


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Beachten Sie, dass " \<S\> " oder " \<I> " und "" \<S\> unterstützt werden. Die Verwendung von " \<I\> " wird nicht unterstützt. Anwendungen sollten die Werte in " \<I\> " oder "" nicht ändern, \<S\> da die partielle DN-Übereinstimmung nicht unterstützt wird.

Bei externen Kerberos-Konten muss es sich bei den Werten um den Kerberos-Kontonamen handeln. Das Kerberos-Paket verwendet die folgende Syntax: "Kerberos: mitaccountname". Beispielsweise ist Folgendes der Wert für ein Konto unter fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Nicht repliziert. Das [**badpasswordtime**](/windows/desktop/ADSchema/a-badpasswordtime) -Attribut gibt den Zeitpunkt an, zu dem der Benutzer das letzte Mal versucht hat, sich mit einem falschen Kennwort beim Konto anzumelden. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Dieses Attribut wird auf jedem Domänen Controller in der Domäne separat verwaltet. Der Wert 0 (null) bedeutet, dass die letzte ungültige Kenn Wort Zeit unbekannt ist. Um einen exakten Wert für das letzte ungültige Kennwort des Benutzers in der Domäne zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und der größte Wert sollte verwendet werden.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Nicht repliziert. Das [**BadPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) -Attribut gibt an, wie oft der Benutzer versucht hat, sich mit einem falschen Kennwort beim Konto anzumelden. Dieses Attribut wird auf jedem Domänen Controller in der Domäne separat verwaltet. Der Wert 0 gibt an, dass der Wert unbekannt ist. Um einen exakten Wert für die Gesamtanzahl fehlerhafter Kenn Wörter des Benutzers in der Domäne zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und die Summe der Werte sollte verwendet werden.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Codepage**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

Das [**Codepage**](/windows/desktop/ADSchema/a-codepage) -Attribut gibt die Codepage für die gewählte Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**CountryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

Das [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) -Attribut gibt den Länder-/Regionscode für die Sprache des Benutzers an. Dieser Wert wird von Windows 2000 nicht verwendet.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homedirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

Das [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) -Attribut gibt den Pfad des Basisverzeichnisses für den Benutzer an. Die Zeichenfolge kann NULL sein.

Wenn [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) festgelegt ist und einen Laufwerk Buchstaben angibt, muss das [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) ein UNC-Pfad sein. Der Pfad muss ein Netzwerk-UNC-Pfad des Formular \\ \\ Server \\ Freigabe- \\ Verzeichnisses sein. Dieser Wert kann eine NULL-Zeichenfolge sein.

Wenn [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) nicht festgelegt ist, muss das [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) ein lokaler Pfad sein, z. b \\ . C: mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

Das [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) -Attribut gibt den Laufwerk Buchstaben an, dem der von **Homedirectory** angegebene UNC-Pfad zugeordnet werden soll. Der Laufwerk Buchstabe muss in der folgenden Form angegeben werden:


```C++
<drive letter>:
```



dabei \<drive letter\> ist "" der Buchstabe des zuzuordnenden Laufwerks. Beispiel:


```C++
Z:
```



Wenn dieses Attribut nicht festgelegt ist, sollte das [**Homedirectory**](/windows/desktop/ADSchema/a-homedirectory) ein lokaler Pfad sein, z. b. C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastlogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Nicht repliziert. Das [**lastlogoff**](/windows/desktop/ADSchema/a-lastlogoff) -Attribut gibt an, wann die letzte Abmeldung aufgetreten ist. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur. Dieses Attribut wird auf jedem Domänen Controller in der Domäne separat verwaltet. Der Wert 0 (null) bedeutet, dass die letzte Abmelde Zeit unbekannt ist. Um einen exakten Wert für die letzte Abmeldung des Benutzers in der Domäne zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und der größte Wert sollte verwendet werden.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Nicht repliziert. Das [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon) -Attribut gibt an, wann die letzte Anmeldung aufgetreten ist. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt. Der hohe Teil dieser großen Ganzzahl entspricht dem **dwHighDateTime** -Member der [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, und der niedrige Teil entspricht dem **dwLowDateTime** -Member der **FILETIME** -Struktur. Dieses Attribut wird auf jedem Domänen Controller in der Domäne separat verwaltet. Der Wert 0 (null) bedeutet, dass die Uhrzeit der letzten Anmeldung unbekannt ist. Um einen exakten Wert für die letzte Anmeldung des Benutzers in der Domäne zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und der größte Wert sollte verwendet werden.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmpwdhistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

Das [**lmpwdhistory**](/windows/desktop/ADSchema/a-lmpwdhistory) -Attribut ist der Kenn Wort Verlauf des Benutzers im LAN-Manager (LM) (unidirektionales Format). Der LM-owf wird für die Kompatibilität mit LAN-Manager 2. x-Clients, Windows 95 und Windows 98 verwendet. Dieses Attribut wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das Klartext-Kennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**LogonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Nicht repliziert. Das [**LogonCount**](/windows/desktop/ADSchema/a-logoncount) -Attribut zählt, wie oft der Benutzer versucht hat, sich bei diesem Konto anzumelden. Dieses Attribut wird auf jedem Domänen Controller in der Domäne verwaltet. Der Wert 0 gibt an, dass der Wert unbekannt ist. Um einen exakten Wert für die Gesamtzahl erfolgreicher Anmeldeversuche in der Domäne des Benutzers zu erhalten, muss jeder Domänen Controller in der Domäne abgefragt werden, und die Summe der Werte sollte verwendet werden.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**Mail@@**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

Das [**Mail**](/windows/desktop/ADSchema/a-mail) -Attribut ist ein einwertiges Attribut, das die SMTP-Adresse für den Benutzer enthält, z jeff@Fabrikam.com . b. "".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxstorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

Das [**maxstorage**](/windows/desktop/ADSchema/a-maxstorage) -Attribut gibt die maximale Menge an Festplattenspeicher an, die vom Benutzer verwendet werden kann. Verwenden Sie den Wert **Benutzer \_ maxstorage \_ Unlimited** (in lmaccess. h definiert), um den gesamten verfügbaren Speicherplatz zu verwenden.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

Das Attribut Attribut ist ein mehr [**wertiges Attribut,**](/windows/desktop/ADSchema/a-memberof) das Gruppen enthält, in denen der Benutzer ein direkter Member ist, mit Ausnahme der primären Gruppe, die durch die [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)repräsentiert wird. Die Gruppenmitgliedschaft ist abhängig vom Domänen Controller (DC), von dem das Attribut abgerufen wird:

-   Auf einem Domänen Controller für die Domäne, in der der Benutzer enthalten [**ist, ist**](/windows/desktop/ADSchema/a-memberof) die Mitgliedschaft für den Benutzer in Bezug auf die Mitgliedschaft in Gruppen in dieser Domäne vollständig. die Mitgliedschaft der Benutzer in lokalen und globalen Domänen Gruppen in anderen Domänen ist jedoch nicht in der **Mitgliedschaften** enthalten.
-   Auf einem GC-Server ist die [**Mitgliedschaft**](/windows/desktop/ADSchema/a-memberof) für den Benutzer in Bezug auf alle universellen Gruppenmitgliedschaften vollständig.

Wenn beide Bedingungen für den DC zutreffen, sind beide Datensätze in der [**Mitgliedschaft**](/windows/desktop/ADSchema/a-memberof)enthalten.

Beachten Sie, dass dieses Attribut die Gruppen auflistet, die den Benutzer in Ihrem Member-Attribut enthalten – es enthält nicht die rekursive Liste der in der Tabelle enthaltenen Vorgänger. Wenn Benutzer o z. b. ein Mitglied der Gruppe c ist und Gruppe b und Gruppe b in Gruppe a eingefügt wurden, listet [**das Attribut Attribut von User**](/windows/desktop/ADSchema/a-memberof) o die Gruppe c und Gruppe b, jedoch nicht Gruppe a auf.

Dieses Attribut ist nicht gespeichert – es handelt sich um ein berechnetes Backlinkattribut.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntpwdhistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

Das [**ntpwdhistory**](/windows/desktop/ADSchema/a-ntpwdhistory) -Attribut ist der Kenn Wort Verlauf des Benutzers im unidirektionalen Windows NT-Format (owf). Windows 2000 verwendet Windows NT owf. Dieses Attribut wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das Klartext-Kennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**othermailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

Das [**othermailbox**](/windows/desktop/ADSchema/a-othermailbox) -Attribut ist ein mehr wertiges Attribut, das andere zusätzliche e-Mail-Adressen in einem Formular enthält, z. b. "CCMAIL: JeffSmith".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**Passwordexpirationdate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

Das Ablaufdatum für das Kennwort ist kein Attribut für das User-Objekt. Es ist ein berechneter Wert, der auf der Summe von [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) für den Benutzer und [**maxpwdage**](/windows/desktop/ADSchema/a-maxpwdage) der Domäne des Benutzers basiert. Um das Ablaufdatum für das Kennwort zu erhalten, holen Sie sich die [**IADsUser. passwordexpirationdate**](/windows/desktop/ADSI/iadsuser-property-methods) -Eigenschaft. Dieses Attribut kann für einen Benutzer nicht geändert werden. Legen Sie stattdessen die [**iadsdomain. maxpasswordage**](/windows/desktop/ADSI/iadsdomain-property-methods) -Eigenschaft fest, um die Einstellung für die Domäne zu ändern.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

Das [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) -Attribut ist ein einwertiges Attribut, das das [**primarygrouptoken**](/windows/desktop/ADSchema/a-primarygrouptoken) der Gruppe enthält, die die primäre Gruppe des Objekts ist. Die primäre Gruppe des-Objekts ist nicht im Attribut [**für die Mitgliedschaft**](/windows/desktop/ADSchema/a-memberof) enthalten. Beispielsweise ist die primäre Gruppe eines Benutzer Objekts standardmäßig das **primarygrouptoken** der Domänen Benutzergruppe, die Domänen Benutzergruppe ist jedoch nicht Teil des Attributs **für** das Benutzerobjekt.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**Profilpfad**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

Das Attribut " [**ProfilePath**](/windows/desktop/ADSchema/a-profilepath) " gibt einen Pfad zum Profil des Benutzers an. Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

Das [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) -Attribut gibt an, wann das Kennwort zuletzt geändert wurde. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von 100-Nanosekunden-Intervallen seit dem 1. Januar 1601 (UTC) darstellt.

Das System verwendet den Wert dieses Attributs und das Attribut [**maxpwdage**](/windows/desktop/ADSchema/a-maxpwdage) der Domäne, die das Benutzerobjekt enthält, um das Ablaufdatum des Kennworts zu berechnen. Das heißt, die Summe von " [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) " für "User" und " **maxpwdage** " der Domäne des Benutzers.

Dieses Attribut steuert, ob der Benutzer das Kennwort ändern muss, wenn sich der Benutzer beim nächsten anmeldet. Wenn [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) gleich 0 (null) ist, muss der Benutzer das Kennwort bei der nächsten Anmeldung ändern. Der Wert-1 gibt an, dass der Benutzer das Kennwort bei der nächsten Anmeldung nicht ändern muss. Das System legt diesen Wert auf-1 fest, nachdem der Benutzer das Kennwort festgelegt hat.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**samAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

Das [**samAccountType**](/windows/desktop/ADSchema/a-samaccounttype) -Attribut gibt eine ganze Zahl an, die den Kontotyp darstellt. Dies wird vom Betriebssystem festgelegt, wenn das Objekt erstellt wird.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

Das [**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath) -Attribut gibt den Pfad des Anmelde Skripts des Benutzers, der cmd-, exe-oder bat-Datei an. Die Zeichenfolge kann NULL sein.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

Das [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) -Attribut ist das Benutzer Kennwort.

Um das Benutzer Kennwort festzulegen, verwenden Sie die [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) -Methode, wenn das Skript oder die Anwendung es dem Benutzer ermöglicht, sein eigenes Kennwort zu ändern, oder die [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) -Methode, wenn Ihr Skript oder Ihre Anwendung einem Administrator das Zurücksetzen eines Kennworts gestattet.

Das Kennwort des Benutzers im unidirektionalen Windows NT-Format (owf). Windows 2000 verwendet Windows NT owf. Dieses Attribut wird nur von einem Betriebssystem verwendet. Beachten Sie, dass Sie das Klartext-Kennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

Das [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Attribut gibt Flags an, die das Verhalten von Kennwort, Sperre, deaktivieren/aktivieren, Skript und Basisverzeichnis des Benutzers steuern. Dieses Attribut enthält auch ein Flag, das den Kontotyp des Objekts angibt. Das Benutzerobjekt verfügt in der Regel über das Standardkonto "UF" \_ \_ .

Die folgenden Flags sind in "lmaccess. h" definiert.



| Flag                     | Beschreibung                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UF- \_ Skript               | Das ausgeführte Anmelde Skript. Dieser Wert muss für den LAN-Manager 2,0 oder Windows NT festgelegt werden.                                                                             |
| UF \_ accountdeaktiviert       | Das Benutzerkonto ist deaktiviert.                                                                                                                                    |
| "UF \_ homedir" \_ erforderlich    | Das Basisverzeichnis ist erforderlich. Dieser Wert wird in Windows NT und Windows 2000 ignoriert.                                                                            |
| UF \_ passwd \_ notreqd      | Es ist kein Kennwort erforderlich.                                                                                                                                         |
| "UF \_ passwd cant"- \_ \_ Änderung | Der Benutzer kann das Kennwort nicht ändern.                                                                                                                             |
| UF- \_ Sperre              | Das Konto ist zurzeit gesperrt. Dieser Wert kann gelöscht werden, um ein zuvor gesperrtes Konto zu entsperren. Dieser Wert kann nicht zum Sperren eines zuvor gesperrten Kontos verwendet werden. |
| "UF \_ 't \_ expire \_ passwd" | Stellt das Kennwort dar, das nie für das Konto ablaufen soll.                                                                                               |



 

Die folgenden Flags beschreiben den Kontotyp. Es kann nur ein Wert festgelegt werden. Der Kontotyp kann nicht geändert werden.



| Flag                            | Beschreibung                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_normales \_ Konto             | Dies ist ein Standard Kontotyp, der einen typischen Benutzer darstellt.                                                                                                                                                                                  |
| \_Konto für Temp Temp- \_ Duplizierung \_    | Dies ist ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet. Dieses Konto ermöglicht dem Benutzer den Zugriff auf diese Domäne, jedoch nicht auf eine Domäne, die dieser Domäne vertraut. Der Benutzer-Manager verweist auf diesen Kontotyp als lokales Benutzerkonto. |
| Konto der Vertrauensstellung der \_ \_ Vertrauensstellung \_ | Hierbei handelt es sich um ein Computer Konto für einen Windows NT-Arbeitsstations-/Windows 2000 Professional-oder Windows NT Server/Windows 2000-Server, der Mitglied dieser Domäne ist.                                                                                     |
| \_ \_ \_ Konto Vertrauens Konto für den Server      | Hierbei handelt es sich um ein Computer Konto für einen Windows NT-Sicherungs Domänen Controller, der Mitglied dieser Domäne ist.                                                                                                                                           |
| Konto für die Vertrauensstellung der \_ Verbindungs Domäne \_ \_ | Dies ist ein vertrauenswürdiges Konto für eine Windows NT-Domäne, die anderen Domänen vertraut.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

Das [**userCertificate**](/windows/desktop/ADSchema/a-usercertificate) -Attribut ist ein mehr wertiges Attribut, das die für den Benutzer ausgestellten X509v3-Zertifikate enthält. Beachten Sie, dass dieses Attribut die Zertifikate des öffentlichen Schlüssels enthält, die für diesen Benutzer vom Microsoft-Zertifikat Dienst ausgestellt wurden.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**usersharedfolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

Das [**usersharedfolder**](/windows/desktop/ADSchema/a-usersharedfolder) -Attribut gibt einen UNC-Pfad zum freigegebenen Dokument Ordner des Benutzers an. Der Pfad muss ein Netzwerk-UNC-Pfad des Formular \\ \\ Server \\ Freigabe- \\ Verzeichnisses sein. Dieser Wert kann eine NULL-Zeichenfolge sein.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**Benutzer Arbeitsstationen**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

Das [**userworkstations**](/windows/desktop/ADSchema/a-userworkstations) -Attribut ist ein einwertiges Attribut, das die NetBIOS-Namen der Arbeitsstationen enthält, an denen sich der Benutzer anmelden kann. Jeder NetBIOS-Name wird durch ein Komma getrennt.

Wenn keine Werte festgelegt sind, ist dies ein Hinweis darauf, dass keine Einschränkung vorhanden ist. Um Anmeldungen von allen Arbeitsstationen für dieses Konto zu deaktivieren, legen Sie den Wert für den Wert "UF \_ accountdeaktivieren" (definiert in "lmaccess. h") im [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) -Attribut fest.

</dd> </dl>

 

 
