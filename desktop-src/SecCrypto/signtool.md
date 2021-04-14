---
title: SignTool
description: SignTool ist ein Befehlszeilen Tool, das Dateien digital signiert, Signaturen in Dateien und Zeitstempel-Dateien überprüft.
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: 884d4c132a2877a51cef7610dd32e8ef6b9c4bc3
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "104391178"
---
# <a name="signtool"></a>SignTool

SignTool ist ein Befehlszeilen Tool, das Dateien digital signiert, Signaturen in Dateien und Zeitstempel-Dateien überprüft. Informationen dazu, warum das Signieren von Dateien wichtig ist, finden [Sie unter Einführung in die Code Signatur](cryptography-tools.md). Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.

SignTool ist als Teil des Windows SDK verfügbar, das Sie von herunterladen können <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> .

> [!Note]  
> Das Windows 10 SDK, Windows 10 HLK, Windows 10 WDK und Windows 10 ADK **Build 20236 und höher** erfordern nun die Angabe des Digest-Algorithmus. Der SignTool Sign-Befehl erfordert `file digest algorithm` , dass die/FD-Option und die/TD- `timestamp digest algorithm` Option beim Signieren bzw. Zeitstempel angegeben werden. Eine Warnung (anfänglich Fehlercode 0) wird ausgelöst, wenn/FD nicht während der Signierung angegeben wird und/TD nicht während des Zeitstempels angegeben wird. In späteren Versionen von SignTool wird aus dieser Warnung ein Fehler. SHA256 wird empfohlen und gilt in der Branche als sicherer als SHA1.  


## <a name="syntax"></a>Syntax  
  
```console  
signtool [command] [options] [file_name | ...]  
```  

## <a name="parameters"></a>Parameter  
  
|Argument|BESCHREIBUNG|  
|----|----|  
|`command`|Einer von vier Befehlen (`catdb`, `sign`, `Timestamp` oder `Verify`), der einen für eine Datei auszuführenden Vorgang angibt. In der folgenden Tabelle finden Sie eine Beschreibung der einzelnen Befehle.|  
|`options`|Eine Option, die einen Befehl ändert. Neben der globalen `/q`-Option und `/v`-Option wird von jedem Befehl ein eindeutiger Satz von Optionen unterstützt.|  
|`file_name`|Der Pfad zu einer zu signierenden Datei.| 


Die folgenden Befehle werden von SignTool unterstützt.

|Get-Help|Beschreibung|  
|----|----|  
|`Catdb`|Fügt einer Katalogdatenbank eine Katalogdatei hinzu oder entfernt sie daraus. Katalogdatenbanken werden für die automatische Suche von Katalogdateien verwendet und mit einer GUID gekennzeichnet. Eine Liste der vom `catdb`-Befehl unterstützten Optionen finden Sie unter [catdb-Befehlsoptionen](/dotnet/framework/tools/signtool-exe#catdb-command-options).|  
|`Sign`|Signiert Dateien digital. Digitale Signaturen schützen Dateien vor Manipulationen und ermöglichen es Benutzern, den Signaturgeber anhand eines Signaturzertifikats zu überprüfen. Eine Liste der vom `sign`-Befehl unterstützten Optionen finden Sie unter [sign-Befehlsoptionen](/dotnet/framework/tools/signtool-exe#sign-command-options).|  
|`Timestamp`|Fügt Dateien Timestamps hinzu. Eine Liste der vom `TimeStamp`-Befehl unterstützten Optionen finden Sie unter [TimeStamp-Befehlsoptionen](/dotnet/framework/tools/signtool-exe#timestamp-command-options).|  
|`Verify`|Überprüft die digitale Signatur von Dateien, indem ermittelt wird, ob das Signaturzertifikat von einer vertrauenswürdigen Zertifizierungsstelle ausgestellt wurde, ob das Signaturzertifikat widerrufen wurde, und (optional) ob das Signaturzertifikat für eine bestimmte Richtlinie gültig ist. Eine Liste der vom `Verify`-Befehl unterstützten Optionen finden Sie unter [Verify-Befehlsoptionen](/dotnet/framework/tools/signtool-exe#verify-command-options).|

 Die folgenden Optionen gelten für alle Signierungstoolbefehle.  
  
|Globale Option|Beschreibung|  
|----|----|  
|**/q**|Bei erfolgreicher Ausführung des Befehls erfolgt keine Ausgabe, bei einen Fehler werden minimale Daten ausgegeben|  
|**/v**|Zeigt unabhängig von der erfolgreichen Ausführung des Befehls eine ausführliche Ausgabe und Warnmeldungen an.|  
|**/debug**|Zeigt Debuginformationen an.|  

 
## <a name="catdb-command-options"></a>Optionen für den Befehl "Befehl"  

 In der folgenden Tabelle werden die Optionen aufgeführt, die mit dem `Catdb`-Befehl verwendet werden können.

| Catdb-Option | Beschreibung |
|----|----| 
| **/d** | Gibt an, dass die Standardkatalog Datenbank aktualisiert werden soll. Wenn weder die Option **/d** noch **/g** verwendet wird, aktualisiert SignTool die Systemkomponente und die Treiberdatenbank. |
| **/g** - *GUID* | Gibt an, dass die durch die GUID identifizierte Katalog Datenbank aktualisiert werden soll.|
| **/r** | Entfernt den angegebenen Katalog aus der Katalog Datenbank. Wenn diese Option nicht angegeben ist, wird der angegebene Katalog von SignTool der Katalog Datenbank hinzugefügt.|
| **/u** | Gibt an, dass automatisch ein eindeutiger Name für die hinzugefügten Katalogdateien generiert wird. Ggf. werden die Katalogdateien umbenannt, um Namenskonflikte mit vorhandenen Katalogdateien zu verhindern. Wenn diese Option nicht angegeben wird, überschreibt SignTool alle vorhandenen Kataloge, die denselben Namen wie der hinzugefügte Katalog haben.|

> [!Note]  
> Katalog Datenbanken werden für die automatische Suche von Katalogdateien verwendet.


## <a name="sign-command-options"></a>Sign-Befehlsoptionen  

 In der folgenden Tabelle werden die Optionen aufgeführt, die mit dem `sign`-Befehl verwendet werden können.  
  
|Sign-Befehlsoption|Beschreibung|  
|----|----| 
|`/a`|Wählt automatisch das beste Signaturzertifikat aus. Das Signierungstool findet alle gültigen Zertifikate, die sämtliche angegebenen Bedingungen erfüllen, und wählt das Zertifikat mit der längsten Gültigkeitsdauer aus. Wenn diese Option nicht vorhanden ist, wird vom Signierungstool nur ein bestehendes gültiges Signaturzertifikat erwartet.|  
|`/ac`  *file*|Fügt dem Signaturblock ein zusätzliches Zertifikat aus *file* hinzu.|  
|`/as`|Fügt diese Signatur an. Wenn keine Primärsignatur vorhanden ist, wird diese Signatur stattdessen zur Primärsignatur.|  
|`/c`  *CertTemplateName*|Gibt den Zertifikatsvorlagennamen (eine Microsoft-Erweiterung) für das Signaturzertifikat an.|  
|`/csp`  *CSPName*|Gibt den Kryptografiedienstanbieter (CSP) an, der den privaten Schlüsselcontainer enthält.|  
|`/d`  *Desc*|Gibt eine Beschreibung des signierten Inhalts an.|  
|`/dg`  *ADS*|Generiert den zu Signier enden Digest und die unsignierten PKCS7-Dateien. Der Ausgabe Digest und die PKCS7-Dateien lauten: *path\dateiname.Dig* und *path\dateiname.p7u*. Informationen zum Ausgeben einer zusätzlichen XML-Datei finden Sie unter <strong>/DXML</strong>.|  
|`/di`  *ADS*|Erstellt die Signatur, indem der signierte Digest in die nicht signierte PKCS7-Datei erfasst wird. Die Eingabe signierte Digest-und Ganzzahl ohne Vorzeichen PKCS7-Dateien sollten lauten: *Path\FileName.Dig.Signed* und *path\dateiname.p7u*.|  
|`/dlib`  *DLL*|Gibt die DLL <code>AuthenticodeDigestSign</code> an, die die Funktion zum Signieren des Digest implementiert. Diese Option entspricht der automatischen Verwendung von <strong>SignTool</strong> mit den Switches <strong>/DG</strong>, <strong>/DS</strong>und <strong>/di</strong> , mit dem Unterschied, dass diese Option Alle drei als einen atomaren Vorgang aufruft.|  
|`/dmdf`  *Einfügen*|Wenn Sie mit der <strong>/DG</strong> -Option verwendet wird, übergibt den Inhalt der Datei <code>AuthenticodeDigestSign</code> ohne Änderung an die Funktion.|  
|`/ds`  |Signiert nur den Digest. Die Eingabedatei sollte der Digest sein, der von der <strong>/DG</strong> -Option generiert wird. Die Ausgabedatei lautet: *file. Signed*.|  
|`/du`  *URL*|Gibt eine URL (Uniform Resource Locator) für die erweiterte Beschreibung des signierten Inhalts an.|  
|`/dxml`  |Bei Verwendung mit der <strong>/DG</strong> -Option wird eine XML-Datei erstellt. Die Ausgabedatei lautet: *Path\FileName.dig.xml*.|  
|`/f`  *SignCertFile*|Gibt das Signaturzertifikat in einer Datei an. Wenn die Datei im PFX-Format (Personal Information Exchange) vorliegt und mit einem Kennwort gesichert ist, verwenden Sie zur Angabe des Kennworts die `/p`-Option. Wenn die Datei keine privaten Schlüssel aufweist, verwenden Sie die `/csp`-Option und `/kc`-Option, um den CSP-Namen und den Namen des privaten Schlüsselcontainers anzugeben.|  
|`/fd`*ALG*|Gibt den Dateihashwertalgorithmus zum Erstellen von Dateisignaturen an. </br> **Hinweis:** Eine Warnung wird generiert, wenn der <strong>/FD</strong> -Schalter beim Signieren nicht angegeben wird. Der Standardwert für ALG ist SHA1, aber SHA256 wird empfohlen.|
|`/fd` *certHash*|Durch Angabe der Zeichenfolge certHash wird standardmäßig der auf dem Signaturzertifikat verwendete Algorithmus verwendet. </br> **Hinweis:** Nur verfügbar in Windows 10 Kit-Builds 20236 und höher.|  
|`/i`  *IssuerName*|Gibt den Namen des Ausstellers des Signaturzertifikats an. Dieser Wert kann eine Teilzeichenfolge des gesamten Ausstellernamens sein.|  
|`/kc`  *PrivKeyContainerName*|Gibt den Namen des privaten Schlüsselcontainers an.|  
|`/n`  *SubjectName*|Gibt den Namen des Antragstellers des Signaturzertifikats an. Dieser Wert kann eine Teilzeichenfolge des gesamten Antragstellernamens sein.|  
|`/nph`|Wenn unterstützt, werden Seitenhashes für ausführbare Dateien unterdrückt. Die Standardeinstellung wird von der SIGNTOOL_PAGE_HASHES-Umgebungsvariablen und der wintrust.dll-Version bestimmt. Für nicht portable ausführbare Dateien wird diese Option ignoriert.|  
|`/p`  *Password*|Gibt das Kennwort zum Öffnen einer PFX-Datei an. (Verwenden Sie die `/f`-Option, um eine PFX-Datei anzugeben.)|  
|`/p7` *Pfad*|Gibt an, dass für jede ausgewählte Inhaltsdatei eine PKCS #7-Datei (Public Key Cryptography Standards) erstellt wird. PKCS #7-Dateien erhalten die Bezeichnung „*Pfad*\\*Dateiname*.p7“.|  
|`/p7ce` *Value*|Gibt Optionen für den signierten PKCS #7-Inhalt an. Legen Sie *Wert* auf „Embedded“ fest, um den signierten Inhalt in die PKCS #7-Datei einzubetten, oder auf „DetachedSignedData“, um den signierten Datenabschnitt einer getrennten PKCS #7-Datei zu erstellen. Ohne Verwendung der `/p7ce`-Option wird der signierte Inhalt standardmäßig eingebettet.|  
|`/p7co` *\<OID>*|Gibt den Objektbezeichner (OID) zur Identifizierung des signierten PKCS #7-Inhalts an.|  
|`/ph`|Wenn unterstützt, werden Seitenhashes für ausführbare Dateien generiert.|  
|`/r`  *RootSubjectName*|Gibt den Antragstellernamen des Stammzertifikats an, mit dem das Signaturzertifikat verkettet werden muss. Dieser Wert kann eine Teilzeichenfolge des gesamten Antragstellernamens des Stammzertifikats sein.|  
|`/s`  *StoreName*|Gibt den beim Suchen des Zertifikats zu öffnenden Speicher an. Ohne Angabe dieser Option wird der `My`-Speicher geöffnet.|  
|`/sha1`  *Hash*|Gibt den SHA1-Hash des Signaturzertifikats an. In der Regel wird der SHA1-Hash angegeben, wenn die von den verbleibenden Schaltern festgelegten Kriterien von mehreren Zertifikaten erfüllt werden.|  
|`/sm`|Gibt an, dass anstatt eines Benutzerspeichers ein Computerspeicher verwendet wird.|  
|`/t`  *URL*|Gibt die URL des Zeitstempelservers an. Wenn diese Option (oder `/tr`) nicht vorhanden ist, wird der signierten Datei kein Zeitstempel hinzugefügt. Im Fall eines Fehlers beim Hinzufügen des Zeitstempels wird eine Warnung generiert. Diese Option kann nicht mit der `/tr`-Option verwendet werden.|  
|`/td`  *alg*|Wird mit der `/tr`-Option zum Anfordern eines vom RFC 3161-Zeitstempelserver verwendeten Digestalgorithmus genutzt. </br> **Hinweis:** Eine Warnung wird generiert, wenn der <strong>/TD</strong> -Schalter beim Timestampwert nicht angegeben wird. Der Standardwert für ALG ist SHA1, aber SHA256 wird empfohlen. <br/> Der Schalter <strong>/TD</strong> muss nach dem <strong>/TR</strong> -Switch und nicht vor vor deklariert werden. Wenn der <strong>/TD</strong> -Schalter vor dem <strong>/TR</strong> -Schalter deklariert wird, wird der Zeitstempel, der zurückgegeben wird, von einem SHA1-Algorithmus anstelle des vorgesehenen SHA256-Algorithmus. |
|`/tr`  *URL*|Gibt die URL des RFC 3161-Zeitstempelservers an. Wenn diese Option (oder `/t`) nicht vorhanden ist, wird der signierten Datei kein Zeitstempel hinzugefügt. Im Fall eines Fehlers beim Hinzufügen des Zeitstempels wird eine Warnung generiert. Diese Option kann nicht mit der `/t`-Option verwendet werden.|  
|`/u`  *Usage*|Gibt die verbesserte Schlüsselverwendung (EKU) an, die im Signaturzertifikat vorhanden sein muss. Der Verwendungswert kann durch einen OID oder eine Zeichenfolge angegeben werden. Die Standardverwendung lautet "Codesignatur" (1.3.6.1.5.5.7.3.3).|  
|`/uw`|Gibt die Verwendung von "Verifizierung von Windows-Systemkomponenten" (1.3.6.1.4.1.311.10.3.6) an.|  
  
 Verwendungsbeispiele finden Sie unter [Using SignTool to Sign a File (Signieren einer Datei mit SignTool)](using-signtool-to-sign-a-file.md).  
  

## <a name="timestamp-command-options"></a>Timestamp-Befehlsoptionen  

 In der folgenden Tabelle werden die Optionen aufgeführt, die mit dem `TimeStamp`-Befehl verwendet werden können.  
  
|TimeStamp-Option|Beschreibung|  
|----|----|  
|`/p7`|Fügt PKCS #7-Dateien Zeitstempel hinzu.|  
|`/t`  *URL*|Gibt die URL des Zeitstempelservers an. Vor dem Hinzufügen eines Zeitstempels muss die jeweilige Datei signiert werden. Entweder die `/t`-Option oder die `/tr`-Option ist erforderlich.|  
|`/td`  *alg*|Wird mit der `/tr`-Option zum Anfordern eines vom RFC 3161-Zeitstempelserver verwendeten Digestalgorithmus genutzt. </br> **Hinweis:** Eine Warnung wird generiert, wenn der <strong>/TD</strong> -Schalter beim Timestampwert nicht angegeben wird. Der Standardwert für ALG ist SHA1, aber SHA256 wird empfohlen. <br/> Der Schalter <strong>/TD</strong> muss nach dem <strong>/TR</strong> -Switch und nicht vor vor deklariert werden. Wenn der <strong>/TD</strong> -Schalter vor dem <strong>/TR</strong> -Schalter deklariert wird, wird der Zeitstempel, der zurückgegeben wird, von einem SHA1-Algorithmus anstelle des vorgesehenen SHA256-Algorithmus. |
|`/tp` *index*|Fügt der Signatur bei *Index* einen Zeitstempel hinzu|  
|`/tr`  *URL*|Gibt die URL des RFC 3161-Zeitstempelservers an. Vor dem Hinzufügen eines Zeitstempels muss die jeweilige Datei signiert werden. Entweder die `/tr`-Option oder die `/t`-Option ist erforderlich.|  


## <a name="verify-command-options"></a>Überprüfen der Befehlsoptionen  

|"Verify"-Option|Beschreibung|
|----|----|
| **/a** | Gibt an, dass alle Methoden zum Überprüfen der Datei verwendet werden können. Zuerst werden die Katalogdatenbanken durchsucht, um zu ermitteln, ob die Datei in einem Katalog signiert ist. Wenn die Datei nicht in einem Katalog signiert ist, versucht SignTool, die eingebettete Signatur der Datei zu überprüfen. Diese Option wird zum Überprüfen von Dateien empfohlen, die möglicherweise, jedoch nicht unbedingt in einem Katalog signiert sind. Beispiele für Dateien, die signiert oder nicht signiert werden können, sind Windows-Dateien oder Treiber. |
| **/ad** | Sucht den Katalog in der Standardkatalogdatenbank. |
| **/all** | Überprüft alle Signaturen in einer Datei mit mehreren Signaturen. |
| **/as** | Sucht den Katalog in der Katalogdatenbank der Systemkomponenten (Treiber). |
| **/AG** - *ID-GUID* | Sucht den Katalog in der Katalog Datenbank, der durch die **GUID** identifiziert wird. |
| **/c** - *Datei* | Gibt die Katalogdatei anhand des Namens an. |
| **/d** | Druckt die Beschreibung und Beschreibungs-URL.<br/> **Windows Vista und früher:** Dieses Flag wird nicht unterstützt.<br/> |
| **/DS** - *Index* | Überprüft die Signatur an einer bestimmten Position. |
| **/Hash**{**SHA1** \| **SHA256**} | Gibt einen optionalen Hashalgorithmus zum Suchen einer Datei in einem Katalog an. |
| **/kp** | Führt die Überprüfung mithilfe der x64-Kernel Modus-Treiber Signatur Richtlinie durch. |
| **/MS** | Verwendet mehrere Überprüfungssemantiken. Dies ist das Standardverhalten eines [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) -Aufrufes. |
| **/o** - *Version* | Überprüft die Datei anhand der Betriebssystemversion. Der Versions Parameter hat folgendes Format:<br/> *PlatformID ***:*** VerMajor ***.*** VerMinor ***.*** BuildNumber*<br/> Die Verwendung des */o* -Schalters wird empfohlen. Wenn */o* nicht angegeben ist, gibt SignTool möglicherweise unerwartete Ergebnisse zurück. Wenn Sie z. b. den */o* -Schalter nicht einschließen, werden System Kataloge, die auf einem älteren Betriebssystem ordnungsgemäß überprüft werden, unter einem neueren Betriebssystem möglicherweise nicht ordnungsgemäß überprüft. |
| **/p7** | Überprüfen Sie die PKCS \# 7-Dateien. Für die PKCS 7-Überprüfung werden keine vorhandenen Richtlinien verwendet \# . Die Signatur wird überprüft, und für das Signaturzertifikat wird eine Kette erstellt. |
| **/pa** | Gibt an, dass die Standard Richtlinie für die Authentifizierungs Überprüfung verwendet wird. Wenn die **/PA** -Option nicht angegeben ist, verwendet SignTool die Richtlinie für die Windows-Treiber Überprüfung. Diese Option kann nicht **mit den Optionen** von "-Optionen" verwendet werden. |
| **/PG** *policyguid* | Gibt eine Überprüfungs Richtlinie nach **GUID** an. Die **GUID** entspricht der Aktions-ID der Überprüfungs Richtlinie. Diese Option kann nicht **mit den Optionen** von "-Optionen" verwendet werden. |
| **/pH** | Seiten Hash Werte drucken und überprüfen.<br/> **Windows Vista und früher:** Dieses Flag wird nicht unterstützt.<br/>  |
| **/r** *rootsubjetname* | Gibt den Antragstellernamen des Stammzertifikats an, mit dem das Signaturzertifikat verkettet werden muss. Dieser Wert kann eine Teilzeichenfolge des gesamten Antragstellernamens des Stammzertifikats sein. |
| **/tw** | Gibt an, dass eine Warnung generiert wird, wenn die Signatur nicht mit einem Zeitstempel versehen ist.|


Der SignTool **Verify** -Befehl bestimmt, ob das Signaturzertifikat von einer vertrauenswürdigen Zertifizierungsstelle ausgestellt wurde, ob das Signaturzertifikat widerrufen wurde, und optional, ob das Signaturzertifikat für eine bestimmte Richtlinie gültig ist.  

Der Befehl SignTool **Verify** gibt den **eingebetteten** Signatur Status aus, es sei denn, für die Suche eines Katalogs wird eine Option angegeben (/a,/AD,/as,/AG,/c).


## <a name="return-value"></a>Rückgabewert  

 Beim Beenden wird vom Signierungstool einer der folgenden Exitcodes zurückgegeben.  
  
|Exitcode|BESCHREIBUNG|  
|----|----| 
|0|Ausführung war erfolgreich.|  
|1|Ausführung ist fehlgeschlagen.|  
|2|Ausführung wurde mit Warnungen abgeschlossen.|


## <a name="examples"></a>Beispiele  

 Durch den folgenden Befehl wird der Systemkomponenten- und Treiberdatenbank die Katalogdatei "MyCatalogFileName.cat" hinzugefügt. Mit der `/u`-Option wird ggf. ein eindeutiger Name generiert, um das Ersetzen einer möglicherweise vorhandenen Katalogdatei mit dem Namen `MyCatalogFileName.cat` zu verhindern.  
  
```console  
signtool catdb /v /u MyCatalogFileName.cat  
```  
  
 Durch den folgenden Befehl wird eine Datei automatisch mit dem besten Zertifikat signiert.  
  
```console  
signtool sign /a /fd SHA256 MyFile.exe 
```  
  
 Durch den folgenden Befehl wird eine Datei mit einem in einer kennwortgeschützten PFX-Datei gespeicherten Zertifikat digital signiert.  
  
```console  
signtool sign /f MyCert.pfx /p MyPassword /fd SHA256 MyFile.exe 
```  
  
 Durch den folgenden Befehl wird eine Datei digital signiert und mit einem Zeitstempel versehen. Das zum Signieren der Datei verwendete Zertifikat ist in einer PFX-Datei gespeichert.  
  
```console  
signtool sign /f MyCert.pfx /t http://timestamp.digicert.com /fd SHA256 MyFile.exe 
```  
  
 Durch den folgenden Befehl wird eine Datei mit einem Zertifikat aus dem `My`-Speicher signiert, das den Antragstellernamen `My Company Certificate` aufweist.  
  
```console  
signtool sign /n "My Company Certificate" /fd SHA256 MyFile.exe 
```  
  
 Der folgende Befehl signiert ein ActiveX-Steuerelement und stellt Informationen bereit, die dem Benutzer in Internet Explorer bei der Aufforderung zum Installieren des Steuerelements angezeigt werden.  
  
```console  
Signtool sign /f MyCert.pfx /d: "MyControl" /du http://www.example.com/MyControl/info.html /fd SHA256 MyControl.exe 
```  
  
 Durch den folgenden Befehl wird einer bereits digital signierten Datei ein Zeitstempel hinzugefügt.  
  
```console  
signtool timestamp /t http://timestamp.digicert.com MyFile.exe
```  

Der folgende Befehl versieht eine Datei unter Verwendung eines RFC 3161-Zeitstempelservers mit einem Zeitstempel.  
  
```console  
signtool timestamp /tr http://timestamp.digicert.com /td SHA256 MyFile.exe
```  
  
 Durch den folgenden Befehl wird überprüft, ob eine Datei signiert wurde.  
  
```console  
signtool verify MyFile.exe  
```  
  
 Durch den folgenden Befehl wird eine möglicherweise in einem Katalog signierte Systemdatei überprüft.  
  
```console  
signtool verify /a SystemFile.dll  
```  
  
 Durch den folgenden Befehl wird eine Systemdatei überprüft, die in einem Katalog mit dem Namen `MyCatalog.cat` signiert ist.  
  
```console  
signtool verify /c MyCatalog.cat SystemFile.dll  
```  
