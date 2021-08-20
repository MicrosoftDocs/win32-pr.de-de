---
title: Benutzersicherheitsattribute
description: Zusätzlich zum Benennen von Eigenschaften für Benutzerobjekte, z. B. objectGUID, objectSid, cn, distinguishedName und so weiter, gibt es weitere Sicherheitseigenschaften, die für die Anmeldung, den Netzwerkzugriff und die Zugriffssteuerung verwendet werden.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Sicherheitsattribute, Verwenden von AD
- Benutzersicherheitsattribute AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfe23252002f2ffbbba3f8e8a8faf5a2d36ce348bdbd7503c0d99a816a81902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024888"
---
# <a name="user-security-attributes"></a>Benutzersicherheitsattribute

Zusätzlich zum Benennen von Eigenschaften für Benutzerobjekte, z. B. [**objectGUID,**](/windows/desktop/ADSchema/a-objectguid) [**objectSid,**](/windows/desktop/ADSchema/a-objectsid) [**cn,**](/windows/desktop/ADSchema/a-cn) [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)und so weiter, gibt es weitere Sicherheitseigenschaften, die für die Anmeldung, den Netzwerkzugriff und die Zugriffssteuerung verwendet werden. Diese Eigenschaften werden vom Windows 2000-Sicherheitssystem verwendet. Diese Eigenschaften können vom Snap-In Active Directory-Benutzer und -Computer angezeigt und verwaltet werden.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

Das [**accountExpires-Attribut**](/windows/desktop/ADSchema/a-accountexpires) gibt an, wann ein Konto abläuft. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von Intervallen von 100 Nanosekunden seit dem 1. Januar 1601 (UTC) darstellt. Der Wert **TIMEQ \_ FOREVER** (definiert in Lmaccess.h) gibt an, dass ein Konto nie abläuft.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

Das [**altSecurityIdentities-Attribut**](/windows/desktop/ADSchema/a-altsecurityidentities) ist ein mehrwertiges Attribut, das Zuordnungen für X.509-Zertifikate oder externe Kerberos-Benutzerkonten zu diesem Benutzer für die Authentifizierung enthält. Verschiedene Sicherheitspakete, einschließlich des Authentifizierungspakets für öffentliche Schlüssel und Kerberos, verwenden diese Daten, um Benutzer zu authentifizieren, wenn sie die alternative Form der Identifizierung wie Zertifikat, UNIX Kerberos-Ticket und so weiter präsentieren. Erstellen Sie Windows 2000-Token basierend auf dem entsprechenden Benutzerkonto, damit sie auf Systemressourcen zugreifen können.

Bei X.509-Zertifikaten sollten die Werte die Aussteller- und Betreffnamen in 509v3-Zertifikaten sein, die von einer externen öffentlichen Zertifizierungsstelle ausgestellt wurden und dem Benutzerkonto zugeordnet werden, das zum Suchen eines Kontos für die Authentifizierung verwendet wird. Das SSL-Paket (Schannel) verwendet die folgende Syntax: X509: <somecertinfotype> somecertinfo. Der folgende Wert gibt beispielsweise den Aussteller-DN " " mit dem \<I\> DN "C=US,O=InternetCA,CN=APublicCertificateAuthority" und dem Betreff DN " " mit dem \<S\> DN "C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith" an.


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Beachten Sie, dass \<S\> " oder " " " und " " " unterstützt \<I> \<S\> werden. Nur \<I\> "" wird nicht unterstützt. Anwendungen sollten die Werte in \<I\> "" oder "" nicht ändern, da \<S\> ein teilweiser DN-Abgleich nicht unterstützt wird.

Bei externen Kerberos-Konten sollten die Werte der Kerberos-Kontoname sein. Das Kerberos-Paket verwendet die folgende Syntax: "Kerberos:MITaccountname". Im Folgenden finden Sie beispielsweise den Wert für ein Konto Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Nicht repliziert. Das [**badPasswordTime-Attribut**](/windows/desktop/ADSchema/a-badpasswordtime) gibt an, zu welchem Zeitpunkt der Benutzer zuletzt versucht hat, sich mit einem falschen Kennwort beim Konto zu anmelden. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von Intervallen von 100 Nanosekunden seit dem 1. Januar 1601 (UTC) darstellt. Dieses Attribut wird separat auf jedem Domänencontroller in der Domäne verwaltet. Der Wert 0 bedeutet, dass der Zeitpunkt des letzten fehlerhaften Kennworts unbekannt ist. Um einen genauen Wert für den Zeitpunkt des letzten fehlerhaften Kennworts des Benutzers in der Domäne zu erhalten, muss jeder Domänencontroller in der Domäne abgefragt und der größte Wert verwendet werden.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Nicht repliziert. Das [**badPwdCount-Attribut**](/windows/desktop/ADSchema/a-badpwdcount) gibt an, wie oft der Benutzer versucht hat, sich mit einem falschen Kennwort beim Konto zu anmelden. Dieses Attribut wird separat auf jedem Domänencontroller in der Domäne verwaltet. Der Wert 0 gibt an, dass der Wert unbekannt ist. Um einen genauen Wert für die gesamten fehlerhaften Kennwortversuche des Benutzers in der Domäne zu erhalten, muss jeder Domänencontroller in der Domäne abgefragt werden, und die Summe der Werte sollte verwendet werden.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Codepage**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

Das [**codePage-Attribut**](/windows/desktop/ADSchema/a-codepage) gibt die Codepage für die vom Benutzer ausgewählte Sprache an. Dieser Wert wird nicht von Windows 2000 verwendet.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**Countrycode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

Das [**countryCode-Attribut**](/windows/desktop/ADSchema/a-countrycode) gibt den Länder-/Regioncode für die Sprache des Benutzers an. Dieser Wert wird nicht von Windows 2000 verwendet.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

Das [**homeDirectory-Attribut**](/windows/desktop/ADSchema/a-homedirectory) gibt den Pfad des Startverzeichnisses für den Benutzer an. Die Zeichenfolge kann NULL sein.

Wenn [**homeDrive festgelegt**](/windows/desktop/ADSchema/a-homedrive) ist und einen Laufwerkbuchstaben angibt, [**sollte homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) ein UNC-Pfad sein. Der Pfad muss ein UNC-Netzwerkpfad des \\ \\ Formularserverfreigabeverzeichnisses \\ \\ sein. Dieser Wert kann eine NULL-Zeichenfolge sein.

Wenn [**homeDrive nicht**](/windows/desktop/ADSchema/a-homedrive) festgelegt ist, [**sollte homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) ein lokaler Pfad sein, z. B. C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

Das [**homeDrive-Attribut**](/windows/desktop/ADSchema/a-homedrive) gibt den Laufwerkbuchstaben an, dem der durch **homeDirectory** angegebene UNC-Pfad zuordnen soll. Der Laufwerkbuchstaben muss in der folgenden Form angegeben werden:


```C++
<drive letter>:
```



Wobei " \<drive letter\> " der Buchstabe des zu zuordnenden Laufwerks ist. Beispiel:


```C++
Z:
```



Wenn dieses Attribut nicht festgelegt ist, sollte [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) ein lokaler Pfad sein, z. B. C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Nicht repliziert. Das [**lastLogoff-Attribut**](/windows/desktop/ADSchema/a-lastlogoff) gibt an, wann die letzte Abmelde erfolgt ist. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von Intervallen von 100 Nanosekunden seit dem 1. Januar 1601 (UTC) darstellt. Der hohe Teil dieser großen ganzen Zahl entspricht dem **dwHighDateTime-Member** der [**FILETIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) und der untere Teil entspricht dem **dwLowDateTime-Member** der **FILETIME-Struktur.** Dieses Attribut wird separat auf jedem Domänencontroller in der Domäne verwaltet. Der Wert 0 bedeutet, dass der Zeitpunkt der letzten Abmeldezeit unbekannt ist. Um einen genauen Wert für die letzte Abmeldeung des Benutzers in der Domäne zu erhalten, muss jeder Domänencontroller in der Domäne abgefragt und der größte Wert verwendet werden.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Nicht repliziert. Das [**lastLogon-Attribut**](/windows/desktop/ADSchema/a-lastlogon) gibt an, wann die letzte Anmeldung erfolgt ist. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von Intervallen von 100 Nanosekunden seit dem 1. Januar 1601 (UTC) darstellt. Der hohe Teil dieser großen ganzen Zahl entspricht dem **dwHighDateTime-Member** der [**FILETIME-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) und der untere Teil entspricht dem **dwLowDateTime-Member** der **FILETIME-Struktur.** Dieses Attribut wird separat auf jedem Domänencontroller in der Domäne verwaltet. Der Wert 0 bedeutet, dass der Zeitpunkt der letzten Anmeldung unbekannt ist. Um einen genauen Wert für die letzte Anmeldung des Benutzers in der Domäne zu erhalten, muss jeder Domänencontroller in der Domäne abgefragt und der größte Wert verwendet werden.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

Das [**lmPwdHistory-Attribut**](/windows/desktop/ADSchema/a-lmpwdhistory) ist der Kennwortverlauf des Benutzers im OWF-Format (One-Way Format) von LAN Manager (LM). Die LM-OWF wird für die Kompatibilität mit LAN Manager 2.x-Clients, Windows 95 und Windows 98 verwendet. Dieses Attribut wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das Klartextkennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Nicht repliziert. Das [**LogonCount-Attribut**](/windows/desktop/ADSchema/a-logoncount) zählt die Anzahl der erfolgreichen Anmeldezeiten des Benutzers bei diesem Konto. Dieses Attribut wird auf jedem Domänencontroller in der Domäne beibehalten. Der Wert 0 gibt an, dass der Wert unbekannt ist. Um einen genauen Wert für die Gesamtzahl der erfolgreichen Anmeldeversuche des Benutzers in der Domäne zu erhalten, muss jeder Domänencontroller in der Domäne abgefragt werden, und die Summe der Werte sollte verwendet werden.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**Mail**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

Das [**mail-Attribut**](/windows/desktop/ADSchema/a-mail) ist ein einwertiges Attribut, das die SMTP-Adresse für den Benutzer enthält, z. B. " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

Das [**maxStorage-Attribut**](/windows/desktop/ADSchema/a-maxstorage) gibt die maximale Menge an Festplattenlaufwerkspeicher an, die der Benutzer verwenden kann. Verwenden Sie **den Wert USER \_ MAXSTORAGE \_ UNLIMITED** (definiert in Lmaccess.h), um den verfügbaren Speicherplatz zu nutzen.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**Memberof**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

Das [**memberOf-Attribut**](/windows/desktop/ADSchema/a-memberof) ist ein mehrwertiges Attribut, das Gruppen enthält, deren direktes Mitglied der Benutzer ist, mit Ausnahme der primären Gruppe, die durch [**primaryGroupId dargestellt wird.**](/windows/desktop/ADSchema/a-primarygroupid) Die Gruppenmitgliedschaft hängt vom Domänencontroller (DC) ab, von dem dieses Attribut abgerufen wird:

-   Auf einem Domänencontroller für die Domäne, die den Benutzer enthält, ist [**memberOf**](/windows/desktop/ADSchema/a-memberof) für den Benutzer in Bezug auf die Mitgliedschaft für Gruppen in dieser Domäne vollständig. memberOf **enthält** jedoch nicht die Mitgliedschaft des Benutzers in lokalen und globalen Domänengruppen in anderen Domänen.
-   Auf einem GC-Server [**ist memberOf**](/windows/desktop/ADSchema/a-memberof) für den Benutzer in Bezug auf alle universellen Gruppenmitgliedschaften vollständig.

Wenn beide Bedingungen für den DC erfüllt sind, sind beide Sätze von Daten in [**memberOf enthalten.**](/windows/desktop/ADSchema/a-memberof)

Beachten Sie, dass dieses Attribut die Gruppen auflistet, die den Benutzer in seinem Memberattribut enthalten– es enthält nicht die rekursive Liste der geschachtelten Vorgänger. Wenn benutzer O beispielsweise Mitglied von Gruppe C ist und Gruppe B und Gruppe B in Gruppe A geschachtelt sind, würde das [**memberOf-Attribut**](/windows/desktop/ADSchema/a-memberof) von Benutzer O Gruppe C und Gruppe B auflisten, aber nicht Gruppe A.

Dieses Attribut wird nicht gespeichert– es ist ein berechnetes Backlinkattribut.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

Das [**ntPwdHistory-Attribut**](/windows/desktop/ADSchema/a-ntpwdhistory) ist der Kennwortverlauf des Benutzers im Windows NT-OWF (One-Way Format). Windows 2000 verwendet die Windows NT OWF. Dieses Attribut wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das Klartextkennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

Das [**otherMailbox-Attribut**](/windows/desktop/ADSchema/a-othermailbox) ist ein mehrwertiges Attribut, das andere zusätzliche E-Mail-Adressen in einem Formular enthält, z. B. "CCMAIL: JeffGefäss".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

Das Kennwortablaufdatum ist kein Attribut für das Benutzerobjekt. Es handelt sich um einen berechneten Wert, der auf der Summe [**von pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) für den Benutzer und [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) der Domäne des Benutzers basiert. Um das Ablaufdatum des Kennworts zu erhalten, erhalten Sie die [**IADsUser.PasswordExpirationDate-Eigenschaft.**](/windows/desktop/ADSI/iadsuser-property-methods) Sie können dieses Attribut für einen Benutzer nicht ändern. Legen Sie stattdessen die [**IADsDomain.MaxPasswordAge-Eigenschaft**](/windows/desktop/ADSI/iadsdomain-property-methods) fest, um die Einstellung für die Domäne zu ändern.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

Das [**primaryGroupId-Attribut**](/windows/desktop/ADSchema/a-primarygroupid) ist ein einwertiges Attribut, das [**das primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) der Gruppe enthält, die die primäre Gruppe des Objekts ist. Die primäre Gruppe des -Objekts ist nicht im [**memberOf-Attribut**](/windows/desktop/ADSchema/a-memberof) enthalten. Beispielsweise ist die primäre Gruppe eines Benutzerobjekts standardmäßig **das primaryGroupToken** der Gruppe Domänenbenutzer, aber die Gruppe Domänenbenutzer ist nicht Teil des **memberOf-Attributs** des Benutzerobjekts.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

Das [**profilePath-Attribut**](/windows/desktop/ADSchema/a-profilepath) gibt einen Pfad zum Profil des Benutzers an. Dieser Wert kann eine NULL-Zeichenfolge, ein lokaler absoluter Pfad oder ein UNC-Pfad sein.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

Das [**pwdLastSet-Attribut**](/windows/desktop/ADSchema/a-pwdlastset) gibt an, wann das Kennwort zuletzt geändert wurde. Dieser Wert wird als große ganze Zahl gespeichert, die die Anzahl von Intervallen von 100 Nanosekunden seit dem 1. Januar 1601 (UTC) darstellt.

Das System verwendet den Wert dieses Attributs und das [**maxPwdAge-Attribut**](/windows/desktop/ADSchema/a-maxpwdage) der Domäne, die das Benutzerobjekt enthält, um das Ablaufdatum des Kennworts zu berechnen. Das heißt, die Summe von [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) für den Benutzer und **maxPwdAge** der Domäne des Benutzers.

Dieses Attribut steuert, ob der Benutzer das Kennwort ändern muss, wenn sich der Benutzer als Nächstes anmeldet. Wenn [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) 0 (null) ist, muss der Benutzer das Kennwort bei der nächsten Anmeldung ändern. Der Wert -1 gibt an, dass der Benutzer das Kennwort bei der nächsten Anmeldung nicht ändern muss. Das System legt diesen Wert auf -1 fest, nachdem der Benutzer das Kennwort festgelegt hat.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

Das [**sAMAccountType-Attribut**](/windows/desktop/ADSchema/a-samaccounttype) gibt eine ganze Zahl an, die den Kontotyp darstellt. Dies wird vom Betriebssystem festgelegt, wenn das -Objekt erstellt wird.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

Das [**scriptPath-Attribut**](/windows/desktop/ADSchema/a-scriptpath) gibt den Pfad des Anmeldeskripts, der CMD-, .exe- oder .bat an. Die Zeichenfolge kann NULL sein.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

Das [**unicodePwd-Attribut**](/windows/desktop/ADSchema/a-unicodepwd) ist das Benutzerkennwort.

Verwenden Sie zum Festlegen des Benutzerkennworts die [**IADsUser.ChangePassword-Methode,**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) wenn ihr Skript oder Ihre Anwendung es dem Benutzer ermöglicht, sein eigenes Kennwort oder die [**IADsUser.SetPassword-Methode**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) zu ändern, wenn Ihr Skript oder Ihre Anwendung einem Administrator das Zurücksetzen eines Kennworts erlaubt.

Das Kennwort des Benutzers im Windows NT-OWF (One-Way Format). Windows 2000 verwendet die Windows NT OWF. Dieses Attribut wird nur vom Betriebssystem verwendet. Beachten Sie, dass Sie das Klartextkennwort nicht aus der OWF-Form des Kennworts ableiten können.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

Das [**userAccountControl-Attribut**](/windows/desktop/ADSchema/a-useraccountcontrol) gibt Flags an, die das Verhalten von Kennwörtern, Sperren, Deaktivieren/Aktivieren, Skripts und des Startverzeichnisses für den Benutzer steuern. Dieses Attribut enthält auch ein Flag, das den Kontotyp des Objekts angibt. Für das Benutzerobjekt ist normalerweise UF \_ NORMAL \_ ACCOUNT festgelegt.

Die folgenden Flags sind in Lmaccess.h definiert.



| Flag                     | Beschreibung                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_UF-SKRIPT               | Das ausgeführte Anmeldeskript. Dieser Wert muss für LAN Manager 2.0 oder Windows NT festgelegt werden.                                                                             |
| UF \_ ACCOUNTDISABLE       | Das Benutzerkonto ist deaktiviert.                                                                                                                                    |
| UF \_ HOMEDIR \_ ERFORDERLICH    | Das Startverzeichnis ist erforderlich. Dieser Wert wird in den Windows NT und Windows 2000 ignoriert.                                                                            |
| UF \_ PASSWD \_ NOTREQD      | Es ist kein Kennwort erforderlich.                                                                                                                                         |
| UF \_ PASSWD \_ CANT \_ CHANGE | Der Benutzer kann das Kennwort nicht ändern.                                                                                                                             |
| UF \_ LOCKOUT              | Das Konto ist derzeit gesperrt. Dieser Wert kann zum Entsperren eines zuvor gesperrten Kontos aufgehoben werden. Dieser Wert kann nicht verwendet werden, um ein zuvor gesperrtes Konto zu sperren. |
| UF \_ DONT \_ EXPIRE \_ PASSWD | Stellt das Kennwort dar, das für das Konto nie ablaufen sollte.                                                                                               |



 

Die folgenden Flags beschreiben den Kontotyp. Es kann nur ein Wert festgelegt werden. Sie können den Kontotyp nicht ändern.



| Flag                            | Beschreibung                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NORMALES \_ \_ UF-KONTO             | Dies ist ein Standardkontotyp, der einen typischen Benutzer darstellt.                                                                                                                                                                                  |
| TEMPORÄRES \_ DOPPELTES \_ UF-KONTO \_    | Dies ist ein Konto für Benutzer, deren primäres Konto sich in einer anderen Domäne befindet. Dieses Konto bietet Benutzerzugriff auf diese Domäne, aber nicht auf eine Domäne, die dieser Domäne vertraut. Der Benutzer-Manager bezieht sich auf diesen Kontotyp als lokales Benutzerkonto. |
| UF \_ WORKSTATION \_ TRUST \_ ACCOUNT | Dies ist ein Computerkonto für eine Windows NT-Arbeitsstation/Windows 2000 Professional oder einen Windows NT Server/Windows 2000-Server, der Mitglied dieser Domäne ist.                                                                                     |
| UF \_ SERVER \_ TRUST \_ ACCOUNT      | Dies ist ein Computerkonto für einen Windows NT Backup-Domänencontroller, der Mitglied dieser Domäne ist.                                                                                                                                           |
| UF \_ INTERDOMAIN \_ TRUST \_ ACCOUNT | Dies ist eine Genehmigung zum Vertrauenswürdigkeitskonto für eine Windows NT-Domäne, die anderen Domänen vertraut.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

Das [**userCertificate-Attribut**](/windows/desktop/ADSchema/a-usercertificate) ist ein mehrwertiges Attribut, das die DER-codierten X509v3-Zertifikate enthält, die für den Benutzer ausgestellt wurden. Beachten Sie, dass dieses Attribut die Öffentlichen Schlüsselzertifikate enthält, die diesem Benutzer vom Microsoft-Zertifikatdienst ausgestellt wurden.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

Das [**userSharedFolder-Attribut**](/windows/desktop/ADSchema/a-usersharedfolder) gibt einen UNC-Pfad zum Ordner für freigegebene Dokumente des Benutzers an. Der Pfad muss ein UNC-Netzwerkpfad des \\ \\ Formularserverfreigabeverzeichnisses \\ \\ sein. Dieser Wert kann eine NULL-Zeichenfolge sein.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

Das [**userWorkstations-Attribut**](/windows/desktop/ADSchema/a-userworkstations) ist ein einwertiges Attribut, das die NetBIOS-Namen der Arbeitsstationen enthält, bei denen sich der Benutzer anmelden kann. Jeder NetBIOS-Name wird durch ein Komma getrennt.

Wenn keine Werte festgelegt sind, bedeutet dies, dass keine Einschränkung besteht. Um Anmeldungen von allen Arbeitsstationen für dieses Konto zu deaktivieren, legen Sie den UF \_ ACCOUNTDISABLE-Wert (definiert in Lmaccess.h) im [**userAccountControl-Attribut**](/windows/desktop/ADSchema/a-useraccountcontrol) fest.

</dd> </dl>

 

 
