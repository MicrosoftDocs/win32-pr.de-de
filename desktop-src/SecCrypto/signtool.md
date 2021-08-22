---
title: SignTool
description: SignTool ist ein Befehlszeilentool, das Dateien digital signiert, die Signaturen in Dateien und Zeitstempeldateien überprüft.
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: f7105e81b958e463612a5065003ed04c24b913f87f52d8d72bb7a708917ebbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897955"
---
# <a name="signtool"></a>SignTool

SignTool ist ein Befehlszeilentool, das Dateien digital signiert, die Signaturen in Dateien und Zeitstempeldateien überprüft. Informationen dazu, warum das Signieren von Dateien wichtig ist, finden Sie unter [Einführung in die Codesignatur.](cryptography-tools.md) Das Tool wird im Ordner Bin des Installationspfads des \\ Microsoft Windows Software Development Kit (SDK) installiert (Beispiel: C:\Programme (x86)\Windows Kits\10\bin\10.0.19041.0\x64\signtool.exe).

SignTool ist als Teil des Windows SDK verfügbar, das Sie unter herunterladen <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> können.

> [!Note]  
> Für Windows 10 SDK, Windows 10 HLK, Windows 10 WDK und Windows 10 ADK-Builds **ab 20236** muss nun der Digestalgorithmus angegeben werden. Für den SignTool-Befehl sign müssen die Option /fd bzw. /td während der Signierung bzw. des `file digest algorithm` `timestamp digest algorithm` Zeitstempels angegeben werden. Eine Warnung (Fehlercode 0, anfänglich) wird ausgelöst, wenn /fd während der Signierung nicht angegeben wird und /td während der Zeitstempelung nicht angegeben wird. In späteren Versionen von SignTool wird aus dieser Warnung ein Fehler. SHA256 wird empfohlen und gilt in der Branche als sicherer als SHA1.  


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

|Befehl|Beschreibung|  
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

 
## <a name="catdb-command-options"></a>Catdb-Befehlsoptionen  

 In der folgenden Tabelle werden die Optionen aufgeführt, die mit dem `Catdb`-Befehl verwendet werden können.

| Catdb-Option | Beschreibung |
|----|----| 
| **/d** | Gibt an, dass die Standardkatalogdatenbank aktualisiert werden soll. Wenn weder **die Option /d** noch **/g** verwendet wird, aktualisiert SignTool die Systemkomponente und die Treiberdatenbank. |
| **/g** *GUID* | Gibt an, dass die durch die GUID identifizierte Katalogdatenbank aktualisiert werden soll.|
| **/r** | Entfernt den angegebenen Katalog aus der Katalogdatenbank. Wenn diese Option nicht angegeben ist, fügt SignTool der Katalogdatenbank den angegebenen Katalog hinzu.|
| **/u** | Gibt an, dass für die hinzugefügten Katalogdateien automatisch ein eindeutiger Name generiert wird. Ggf. werden die Katalogdateien umbenannt, um Namenskonflikte mit vorhandenen Katalogdateien zu verhindern. Wenn diese Option nicht angegeben ist, überschreibt SignTool alle vorhandenen Kataloge, die denselben Namen wie der hinzugefügte Katalog haben.|

> [!Note]  
> Katalogdatenbanken werden für die automatische Suche nach Katalogdateien verwendet.


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
|`/dg`  *Pfad*|Generiert den zu signierten Digest und die nicht signierten PKCS7-Dateien. Die Ausgabeh digest- und PKCS7-Dateien sind: *Path\FileName.dig* und *Path\FileName.p7u*. Informationen zur Ausgabe einer zusätzlichen XML-Datei finden Sie unter <strong>/dxml</strong>.|  
|`/di`  *Pfad*|Erstellt die Signatur durch Erfassung des signierten Digests in der nicht signierten PKCS7-Datei. Der eingegebene signierte Digest und die nicht signierten PKCS7-Dateien sollten: *Path\FileName.dig.signed* und *Path\FileName.p7u sein.*|  
|`/dlib`  *Dll*|Gibt die DLL an, die die <code>AuthenticodeDigestSign</code> Funktion implementiert, mit der der Digest signiert werden soll. Diese Option entspricht der getrennten Verwendung von <strong>SignTool</strong> mit den Schaltern <strong>/dg,</strong> <strong>/ds</strong>und <strong>/di,</strong> außer dass diese Option alle drei als einen atomaren Vorgang aufruft.|  
|`/dmdf`  *Dateiname*|Bei Verwendung mit der <strong>Option /dg</strong> übergibt den Inhalt der Datei ohne <code>AuthenticodeDigestSign</code> Änderung an die Funktion.|  
|`/ds`  |Signiert nur den Digest. Die Eingabedatei sollte der Digest sein, der von der <strong>Option /dg generiert</strong> wird. Die Ausgabedatei ist: *File.signed*.|  
|`/du`  *URL*|Gibt eine URL (Uniform Resource Locator) für die erweiterte Beschreibung des signierten Inhalts an.|  
|`/dxml`  |Bei Verwendung mit der <strong>Option /dg</strong> erzeugt eine XML-Datei. Die Ausgabedatei ist: *Path\FileName.dig.xml*.|  
|`/f`  *SignCertFile*|Gibt das Signaturzertifikat in einer Datei an. Wenn die Datei im PFX-Format (Personal Information Exchange) vorliegt und mit einem Kennwort gesichert ist, verwenden Sie zur Angabe des Kennworts die `/p`-Option. Wenn die Datei keine privaten Schlüssel aufweist, verwenden Sie die `/csp`-Option und `/kc`-Option, um den CSP-Namen und den Namen des privaten Schlüsselcontainers anzugeben.|  
|`/fd`*alg*|Gibt den Dateihashwertalgorithmus zum Erstellen von Dateisignaturen an. </br> **Hinweis:** Es wird eine Warnung generiert, wenn der Schalter <strong>/fd</strong> beim Signieren nicht bereitgestellt wird. Die Standardeinstellung ist SHA1, sha256 wird jedoch empfohlen.|
|`/fd` *certHash*|Durch Angabe der Zeichenfolge certHash wird standardmäßig der auf dem Signaturzertifikat verwendete Algorithmus verwendet. </br> **Hinweis:** Nur in Windows 10 Kit-Builds 20236 und höher verfügbar.|  
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
|`/td`  *alg*|Wird mit der `/tr`-Option zum Anfordern eines vom RFC 3161-Zeitstempelserver verwendeten Digestalgorithmus genutzt. </br> **Hinweis:** Es wird eine Warnung generiert, wenn der Schalter <strong>/td</strong> während des Zeitstempels nicht bereitgestellt wird. Die Standardeinstellung ist SHA1, sha256 wird jedoch empfohlen. <br/> Der <strong>Schalter /td</strong> muss nach dem Schalter <strong>/tr</strong> deklariert werden, nicht zuvor. Wenn der <strong>Schalter /td</strong> vor dem Schalter <strong>/tr</strong> deklariert wird, stammt der zurückgegebene Zeitstempel von einem SHA1-Algorithmus anstelle des beabsichtigten SHA256-Algorithmus. |
|`/tr`  *URL*|Gibt die URL des RFC 3161-Zeitstempelservers an. Wenn diese Option (oder `/t`) nicht vorhanden ist, wird der signierten Datei kein Zeitstempel hinzugefügt. Im Fall eines Fehlers beim Hinzufügen des Zeitstempels wird eine Warnung generiert. Diese Option kann nicht mit der `/t`-Option verwendet werden.|  
|`/u`  *Usage*|Gibt die verbesserte Schlüsselverwendung (EKU) an, die im Signaturzertifikat vorhanden sein muss. Der Verwendungswert kann durch einen OID oder eine Zeichenfolge angegeben werden. Die Standardverwendung lautet "Codesignatur" (1.3.6.1.5.5.7.3.3).|  
|`/uw`|Gibt die Verwendung von "Verifizierung von Windows-Systemkomponenten" (1.3.6.1.4.1.311.10.3.6) an.|  
  
 Verwendungsbeispiele finden Sie unter [Using SignTool to Sign a File (Signieren einer Datei mit SignTool)](using-signtool-to-sign-a-file.md).  
  

## <a name="timestamp-command-options"></a>TimeStamp-Befehlsoptionen  

 In der folgenden Tabelle werden die Optionen aufgeführt, die mit dem `TimeStamp`-Befehl verwendet werden können.  
  
|TimeStamp-Option|Beschreibung|  
|----|----|  
|`/p7`|Fügt PKCS #7-Dateien Zeitstempel hinzu.|  
|`/t`  *URL*|Gibt die URL des Zeitstempelservers an. Vor dem Hinzufügen eines Zeitstempels muss die jeweilige Datei signiert werden. Entweder die `/t`-Option oder die `/tr`-Option ist erforderlich.|  
|`/td`  *alg*|Wird mit der `/tr`-Option zum Anfordern eines vom RFC 3161-Zeitstempelserver verwendeten Digestalgorithmus genutzt. </br> **Hinweis:** Es wird eine Warnung generiert, wenn der Schalter <strong>/td</strong> während des Zeitstempels nicht bereitgestellt wird. Die Standardeinstellung ist SHA1, sha256 wird jedoch empfohlen. <br/> Der <strong>Schalter /td</strong> muss nach dem Schalter <strong>/tr</strong> deklariert werden, nicht zuvor. Wenn der <strong>Schalter /td</strong> vor dem Schalter <strong>/tr</strong> deklariert wird, stammt der zurückgegebene Zeitstempel von einem SHA1-Algorithmus anstelle des beabsichtigten SHA256-Algorithmus. |
|`/tp` *index*|Fügt der Signatur bei *Index* einen Zeitstempel hinzu|  
|`/tr`  *URL*|Gibt die URL des RFC 3161-Zeitstempelservers an. Vor dem Hinzufügen eines Zeitstempels muss die jeweilige Datei signiert werden. Entweder die `/tr`-Option oder die `/t`-Option ist erforderlich.|  


## <a name="verify-command-options"></a>Überprüfen der Befehlsoptionen  

|"Verify"-Option|Beschreibung|
|----|----|
| **/a** | Gibt an, dass alle Methoden zum Überprüfen der Datei verwendet werden können. Zuerst werden die Katalogdatenbanken durchsucht, um zu ermitteln, ob die Datei in einem Katalog signiert ist. Wenn die Datei in keinem Katalog signiert ist, versucht SignTool, die eingebettete Signatur der Datei zu überprüfen. Diese Option wird zum Überprüfen von Dateien empfohlen, die möglicherweise, jedoch nicht unbedingt in einem Katalog signiert sind. Beispiele für Dateien, die signiert werden können oder nicht, sind Windows Dateien oder Treiber. |
| **/ad** | Sucht den Katalog in der Standardkatalogdatenbank. |
| **/all** | Überprüft alle Signaturen in einer Datei mit mehreren Signaturen. |
| **/as** | Sucht den Katalog in der Katalogdatenbank der Systemkomponenten (Treiber). |
| **/ag** *CatDBGUID* | Sucht den Katalog in der Katalogdatenbank, die durch die **GUID** identifiziert wird. |
| **/c** *CatFile* | Gibt die Katalogdatei anhand des Namens an. |
| **/d** | Drucken Sie die Beschreibung und die Beschreibungs-URL.<br/> **Windows Vista und früher:** Dieses Flag wird nicht unterstützt.<br/> |
| **/ds** *Index* | Überprüft die Signatur an einer bestimmten Position. |
| **/hash**{**SHA1** \| **SHA256**} | Gibt einen optionalen Hashalgorithmus zum Suchen einer Datei in einem Katalog an. |
| **/kp** | Führt die Überprüfung mithilfe der x64-Kernelmodus-Treibersignaturrichtlinie aus. |
| **/ms** | Verwendet mehrere Überprüfungssemantiken. Dies ist das Standardverhalten eines [**WinVerifyTrust-Aufrufs.**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) |
| **/o** *Version* | Überprüft die Datei anhand der Betriebssystemversion. Der Versionsparameter hat folgendes Format:<br/> *PlatformID***:**_VerMajor_*_._ *_VerMinor_*_._ * _BuildNumber_<br/> Die Verwendung des Schalters */o* wird empfohlen. Wenn */o* nicht angegeben ist, gibt SignTool möglicherweise unerwartete Ergebnisse zurück. Wenn Sie z. B. den Schalter */o* nicht einschließen, werden Systemkataloge, die auf einem älteren Betriebssystem ordnungsgemäß überprüft werden, unter einem neueren Betriebssystem möglicherweise nicht ordnungsgemäß überprüft. |
| **/p7** | Überprüfen Sie PKCS \# 7-Dateien. Für die PKCS 7-Überprüfung werden keine vorhandenen Richtlinien \# verwendet. Die Signatur wird überprüft, und für das Signaturzertifikat wird eine Kette erstellt. |
| **/pa** | Gibt an, dass die Standardauthentifizierungsüberprüfungsrichtlinie verwendet wird. Wenn die Option **/pa** nicht angegeben ist, verwendet SignTool die Windows Treiberüberprüfungsrichtlinie. Diese Option kann nicht mit den **catdb-Optionen** verwendet werden. |
| **/pg** *PolicyGUID* | Gibt eine Überprüfungsrichtlinie nach **GUID** an. Die **GUID** entspricht der ActionID der Überprüfungsrichtlinie. Diese Option kann nicht mit den **catdb-Optionen** verwendet werden. |
| **/ph** | Seitenhashwerte drucken und überprüfen.<br/> **Windows Vista und früher:** Dieses Flag wird nicht unterstützt.<br/>  |
| **/r** *RootSubjectName* | Gibt den Antragstellernamen des Stammzertifikats an, mit dem das Signaturzertifikat verkettet werden muss. Dieser Wert kann eine Teilzeichenfolge des gesamten Antragstellernamens des Stammzertifikats sein. |
| **/tw** | Gibt an, dass eine Warnung generiert wird, wenn die Signatur nicht mit einem Zeitstempel versehen ist.|


Der Befehl SignTool **verify** bestimmt, ob das Signaturzertifikat von einer vertrauenswürdigen Autorität ausgestellt wurde, ob das Signaturzertifikat widerrufen wurde und optional, ob das Signaturzertifikat für eine bestimmte Richtlinie gültig ist.  

Der Befehl SignTool **verify** gibt den Status der **eingebetteten** Signatur aus, es sei denn, eine Option zum Durchsuchen eines Katalogs (/a, /ad, /as, /ag, /c) ist angegeben.


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
