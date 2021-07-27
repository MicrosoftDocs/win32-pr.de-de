---
title: Authenticode Signing for Game Developers
description: In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und die Authentifizierung in einen täglichen Buildprozess integrieren.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256b1cec0693787e76cfa479940524fca28d508e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436455"
---
# <a name="authenticode-signing-for-game-developers"></a>Authenticode Signing for Game Developers

Die Datenauthentifizierung wird für Spieleentwickler immer wichtiger. Windows Vista und Windows 7 verfügen über eine Reihe von Features, z. B. Jugendschutz, die erfordern, dass Spiele ordnungsgemäß signiert werden, um sicherzustellen, dass niemand die Daten manipuliert hat. Mit Microsoft Authenticode können Endbenutzer und das Betriebssystem überprüfen, ob Programmcode vom richtigen Besitzer stammt und nicht böswillig geändert oder versehentlich beschädigt wurde. In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und die Authentifizierung in einen täglichen Buildprozess integrieren.

-   [Hintergrund](#background)
-   [Erste Schritte](#getting-started)
-   [Verwenden einer vertrauenswürdigen Zertifizierungsstelle](#using-a-trusted-certificate-authority)
-   [Beispiel für die Verwendung eines Testzertifikats](#example-using-a-test-certificate)
-   [Integrieren der Codesignatur in das tägliche Buildsystem](#integrating-code-signing-into-the-daily-build-system)
-   [Widerruf](#revocation)
-   [Treiber für die Codesignatur](#code-signing-drivers)
-   [Zusammenfassung](#summary)
-   [Weitere Informationen](#more-information)

> [!Note]  
> Ab dem 1. Januar 2016 vertrauen Windows 7 und höher keinem SHA-1-Codesignaturzertifikat mehr mit einem Ablaufdatum vom 1. Januar 2016 oder höher. Weitere Windows finden Sie unter Erzwingung von [Authenticode-Codesignatur](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) und Zeitstempel.

 

## <a name="background"></a>Hintergrund

Digitale Zertifikate werden verwendet, um die Identität des Autors zu erstellen. Digitale Zertifikate werden von einem vertrauenswürdigen Drittanbieter ausgestellt, der als Zertifizierungsstelle (Certificate Authority, CA) bezeichnet wird, z. B. VeriSign oder Thawte. Die Zertifizierungsstelle ist dafür verantwortlich, zu überprüfen, ob der Besitzer keine falsche Identifizierung vorliegt. Nach dem Anwenden auf eine Zertifizierungsstelle für ein Zertifikat können kommerzielle Entwickler in weniger als zwei Wochen eine Antwort auf ihre Anwendung erwarten.

Nachdem die Zertifizierungsstelle entschieden hat, dass sie ihre Richtlinienkriterien erfüllt, generiert sie ein Signaturzertifikat, das X.509 entspricht, dem von der International Telecommunications Union erstellten Branchenstandardzertifikatformat mit Erweiterungen der Version 3. Dieses Zertifikat identifiziert Sie und enthält Ihren öffentlichen Schlüssel. Sie wird von der Zertifizierungsstelle als Referenz gespeichert, und Ihnen wird eine Kopie übermittelt. Gleichzeitig erstellen Sie auch einen privaten Schlüssel, den Sie schützen müssen und den Sie nicht für andere Personen freigeben dürfen, auch nicht für die Zertifizierungsstelle.

Nachdem Sie über einen öffentlichen und privaten Schlüssel verfügen, können Sie mit der Verteilung signierter Software beginnen. Microsoft stellt tools zur Verfügung, um dies im Windows SDK zu tun. Die Tools verwenden einen one-way-Hash, erzeugen einen Digest mit fester Länge und generieren eine verschlüsselte Signatur mit einem privaten Schlüssel. Anschließend kombinieren sie diese verschlüsselte Signatur mit Ihrem Zertifikat und Ihren Anmeldeinformationen in einer Struktur, die als Signaturblock bezeichnet wird, und betten sie in das Dateiformat der ausführbaren Datei ein. Jeder Typ von ausführbarer Binärdatei kann signiert werden, einschließlich DLLs, ausführbaren Dateien und Cabinet-Dateien.

Die Signatur kann auf verschiedene Weise überprüft werden. Programme können die Funktion CertVerifyCertificateChainPolicy aufrufen, und SignTool (signtool.exe) kann verwendet werden, um eine Signatur über die Eingabeaufforderung zu überprüfen. Windows Explorer verfügt auch über die Registerkarte Digitale Signaturen in Dateieigenschaften, auf der jedes Zertifikat einer signierten Binärdatei angezeigt wird. (Die Registerkarte Digitale Signaturen wird nur in den Dateieigenschaften für signierte Dateien angezeigt.) Außerdem kann eine Anwendung mithilfe von [**CertVerifyCertificateChainPolicy selbstverifiziert werden.**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy)

Authenticode-Signierung ist nicht nur für die Datenauthentifizierung durch Endbenutzer nützlich, sondern auch für das Patchen von eingeschränkten Benutzerkonten und von Jugendkontrollen in Windows Vista und Windows 7. Darüber hinaus erfordern zukünftige Technologien in Windows-Betriebssystemen möglicherweise auch, dass Code signiert ist. Daher wird dringend empfohlen, dass alle professionellen und großen Entwickler ein Signaturzertifikat von einer Zertifizierungsstelle erwerben. Weitere Informationen dazu finden Sie weiter in diesem Artikel unter Verwenden einer [vertrauenswürdigen Zertifizierungsstelle.](#using-a-trusted-certificate-authority)

Spielcode, Patcher und Installationsprogramme können die Authenticode-Signierung weiter nutzen, indem sie überprüfen, ob Dateien im Code authentifiziert sind. Dies kann für Anti-Cheat und allgemeine Netzwerksicherheit verwendet werden. Beispielcode zum Überprüfen, ob eine Datei signiert ist, finden Sie hier: Beispiel [C-Programm:](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)Überprüfen der Signatur einer PE-Datei, und Beispielcode zum Überprüfen des Besitzes eines Signaturzertifikats für eine signierte Datei finden Sie hier: [How To Get Information from Authenticode Signed Executables](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Erste Schritte

Für den Einstieg stellt Microsoft Tools mit Visual Studio 2005 und Visual Studio 2008 sowie im [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)bereit, um das Ausführen und Überprüfen des Codesignaturprozesses zu unterstützen. Nach der Installation Visual Studio oder des Windows SDK befinden sich die in diesem technischen Artikel beschriebenen Tools in einem Unterverzeichnis der Installation, das eines oder mehrere der folgenden Punkte enthalten kann:

-   %SystemDrive% \\ Programme Microsoft Visual Studio \\ 8 \\ SDK \\ v2.0 \\ Bin
-   %SystemDrive% \\ Programme Microsoft Visual Studio \\ 8 \\ VC \\ PlatformSDK \\ Bin
-   %SystemDrive% \\ Programme Microsoft Visual Studio \\ 9.0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   %SystemDrive% \\ Programme \\ Microsoft SDKs Windows \\ \\ v6.0A \\ bin\\

Die folgenden Tools sind für das Signieren von Code am nützlichsten:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Zertifikaterstellungstool (MakeCert.exe)
</dt> <dd>

Generiert ein X.509-Testzertifikat als CER-Datei, das Ihren öffentlichen Schlüssel und einen privaten Schlüssel als PVK-Datei enthält. Dieses Zertifikat dient nur internen Testzwecken und kann nicht öffentlich verwendet werden.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Erstellt eine DATEI Exchange (PFX) aus einem Paar aus CER- und PVK-Dateien. Die PFX-Datei enthält ihren öffentlichen und privaten Schlüssel.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Signiert die Datei mithilfe der PFX-Datei. SignTool unterstützt das Signieren von DLL-Dateien, ausführbaren Dateien, Windows Installer-Dateien (.msi) und cabinet-Dateien (.cab).

</dd> </dl>

> [!Note]  
> Beim Lesen anderer Dokumentationen finden Sie möglicherweise Verweise auf SignCode (SignCode.exe), aber dieses Tool ist veraltet und wird nicht mehr unterstützt. Verwenden Sie stattdessen SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Verwenden einer vertrauenswürdigen Zertifizierungsstelle

Um ein vertrauenswürdiges Zertifikat zu erhalten, müssen Sie eine Zertifizierungsstelle (Certificate Authority, CA) wie VeriSign oder Thawte beantragen. Microsoft empfiehlt keine Zertifizierungsstelle über eine andere, aber wenn Sie in den Windows-Fehlerberichterstattung-Dienst (WER) integrieren möchten, sollten Sie erwägen, VeriSign zum Aushingen des Zertifikats zu verwenden, da für den Zugriff auf die WER-Datenbank ein WinQual-Konto erforderlich ist, für das eine VeriSign-ID erforderlich ist. Eine vollständige Liste der vertrauenswürdigen Zertifizierungsstellen von Drittanbietern finden Sie unter [Mitglieder des Microsoft-Stammzertifikatprogramms.](/previous-versions/ms995347(v=msdn.10)) Weitere Informationen zum Registrieren bei WER finden Sie unter "[Introducing Windows-Fehlerberichterstattung](https://msdn.microsoft.com/)" in [ISV Zone](https://msdn.microsoft.com/).

Nachdem Sie Ihr Zertifikat von der Zertifizierungsstelle erhalten haben, können Sie Ihr Programm mit SignTool signieren und Ihr Programm für die Öffentlichkeit veröffentlichen. Sie müssen jedoch darauf achten, ihren privaten Schlüssel zu schützen, der in Ihren PFX- und PVK-Dateien enthalten ist. Stellen Sie sicher, dass diese Dateien an einem sicheren Speicherort gespeichert werden.

## <a name="example-using-a-test-certificate"></a>Beispiel für die Verwendung eines Testzertifikats

Die folgenden Schritte veranschaulichen die Erstellung eines Codesignaturzertifikats zu Testzwecken, gefolgt von der Signierung eines Direct3D-Beispielprogramms (BasicHLSL.exe) mit diesem Testzertifikat. Mit diesem Verfahren werden CER- und PVK-Dateien – Ihre öffentlichen bzw. privaten Schlüssel – erstellt, die nicht für die öffentliche Zertifizierung verwendet werden können.

In diesem Beispiel wird der Signatur auch ein Zeitstempel hinzugefügt. Ein Zeitstempel verhindert, dass die Signatur ungültig wird, wenn das Zertifikat abläuft. Code, der signiert ist, aber keinen Zeitstempel hat, wird nach Ablauf des Zertifikats nicht überprüft. Daher sollte jeder öffentlich freigegebene Code über einen Zeitstempel verfügen.

**So erstellen Sie ein Zertifikat und signieren ein Programm**

1.  Erstellen Sie ein Testzertifikat und einen privaten Schlüssel mithilfe des Zertifikaterstellungstools (Certificate Creation Tool, MakeCert.exe).

    Im folgenden Befehlszeilenbeispiel wird MyPrivateKey als Dateiname für die Datei mit dem privaten Schlüssel (PVK), MyPublicKey als Dateiname für die Zertifikatdatei (CER) und MySoftwareCompany als Name des Zertifikats angegeben. Außerdem wird das Zertifikat selbstsigniert, sodass es nicht über eine nicht vertrauenswürdige Stammzertifizierungsstelle verfügt.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Erstellen Sie mit Exchange eine PFX-Datei (Personal Information Exchange) aus Ihrer Datei mit dem privaten Schlüssel (PVK) und der Zertifikatdatei (CERpvk2pfx.exe.

    Die PFX-Datei kombiniert Ihre öffentlichen und privaten Schlüssel in einer einzelnen Datei. Im folgenden Befehlszeilenbeispiel werden die PVK- und CER-Dateien aus dem vorherigen Schritt verwendet, um die PFX-Datei namens MyPFX mit dem Kennwort Ihres Kennworts zu \_ erstellen:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Signieren Sie Ihr Programm mithilfe von SignTool Exchange (PFX)-Datei mit Ihren persönlichen Informationen.

    Sie können mehrere Optionen in der Befehlszeile angeben. Das folgende Befehlszeilenbeispiel verwendet die PFX-Datei aus dem vorherigen Schritt, gibt Ihr Kennwort als Kennwort an, gibt BasicHLSL als zu signierte Datei an und ruft einen Zeitstempel von einem angegebenen Server \_ ab:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > Die URL zum Zeitstempeldienst wird von der Zertifizierungsstelle bereitgestellt und ist für Tests optional. Es ist wichtig, dass die Produktionssignatur eine gültige Zeitstempelstelle enthält, da die Signatur nicht überprüft werden kann, wenn das Zertifikat abläuft.

     

4.  Überprüfen Sie mit SignTool, ob das Programm signiert ist.

    Im folgenden Befehlszeilenbeispiel wird angegeben, dass SignTool versuchen soll, die Signatur auf BasicHLSL.exe mithilfe aller verfügbaren Methoden zu überprüfen und gleichzeitig eine ausführliche Ausgabe zu erhalten:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    In diesem Beispiel sollte SignTool angeben, dass das Zertifikat angefügt ist, und gleichzeitig angeben, dass es nicht vertrauenswürdig ist, da es nicht von einer Zertifizierungsstelle ausgestellt wird.

5.  Vertrauen Sie dem Testzertifikat.

    Für Testzertifikate müssen Sie dem Zertifikat vertrauen. Dieser Schritt sollte für Zertifikate übersprungen werden, die von einer Zertifizierungsstelle bereitgestellt werden, da diese standardmäßig als vertrauenswürdig eingestuft werden.

    Führen Sie auf nur den Computern, auf denen Sie dem Testzertifikat vertrauen möchten, Folgendes aus:

    ```
    certmgr.msc
    ```

    

    Klicken Sie dann mit der rechten Maustaste auf Vertrauenswürdige Stammzertifizierungsstellen, und wählen Sie Alle Tasks \| importieren aus. Navigieren Sie dann zur erstellten PFX-Datei, und führen Sie die Schritte des Assistenten aus, und platzieren Sie das Zertifikat im Vertrauenswürdige Stammzertifizierungsstellen.

    Nach Abschluss des Assistenten können Sie mit dem Testen des vertrauenswürdigen Zertifikats auf diesem Computer beginnen.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrieren der Codesignatur in das tägliche Buildsystem

Um die Codesignierung in ein Projekt zu integrieren, können Sie eine Batchdatei oder ein Skript erstellen, um die Befehlszeilentools auszuführen. Nachdem das Projekt erstellt wurde, führen Sie SignTool mit den richtigen Einstellungen aus (wie in Schritt 3 unseres Beispiels gezeigt).

Seien Sie besonders vorsichtig bei Ihrem Buildprozess, um sich zu schützen, dass der Zugriff auf die PFX- und PVK-Dateien auf so wenige Computer und Benutzer wie möglich beschränkt ist. Als bewährte Methode sollten Entwickler code nur mithilfe des Testzertifikats signieren, bis sie bereit für den Versand sind. Auch hier sollte der private Schlüssel (PVK) an einem geschützten Ort wie einem sicheren oder gesperrten Raum und idealerweise auf einem kryptografischen Gerät wie einer Smartcard aufbewahrt werden.

Eine weitere Schutzebene wird durch die Verwendung von Microsoft Authenticode bereitgestellt, um das paket Windows Installer (MSI) selbst zu signieren. Dadurch wird das MSI-Paket vor Manipulationen und versehentlichen Beschädigungen geschützt. Weitere Informationen zum Signieren von Paketen mit Authenticode finden Sie in der Dokumentation zu Ihrem MSI-Erstellungstool.

## <a name="revocation"></a>Widerruf

Wenn die Sicherheit des privaten Schlüssels kompromittiert wird oder ein sicherheitsbezogenes Ereignis ein Code-Signing ungültig macht, muss der Entwickler das Zertifikat widerrufen. Anderndes würde die Integrität des Entwicklers und die Effektivität des Signierens von Code gefährden. Eine Zertifizierungsstelle kann auch eine Sperrung mit einer bestimmten Zeit aus. Code, der vor der Sperrzeit mit einem Zeitstempel signiert wurde, gilt weiterhin als gültig, code mit einem nachfolgenden Zeitstempel ist jedoch ungültig. Die Zertifikatsperrung wirkt sich auf Code in allen Anwendungen aus, die mit dem widerrufenen Zertifikat signiert sind.

## <a name="code-signing-drivers"></a>Code-Signing Treiber

Treiber können und sollten authenticodesigniert sein. Für Kernelmodustreiber gelten zusätzliche Anforderungen: 64-Bit-Editionen von Windows Vista und Windows 7 verhindern die Installation aller nicht signierten Kernelmodustreiber, und alle Versionen von Windows geben eine Warnungsaufforderung aus, wenn ein Benutzer versucht, einen nicht signierten Treiber zu installieren. Darüber hinaus können Administratoren Gruppenrichtlinie festlegen, um zu verhindern, dass nicht signierte Treiber unter Microsoft Windows Server 2003, Windows XP Professional x64 Edition und 32-Bit-Editionen von Windows Vista und Windows 7 installiert werden.

Viele Typen von Treibern können mit einer von Microsoft vertrauenswürdigen Signatur signiert werden – als Teil des Windows Certification Program von [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) oder des [Unclassified Signature Program](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (ehemals Driver Reliability Signature) – wodurch das System diesen Treibern vollständig vertrauen und sie auch ohne Administratoranmeldeinformationen installieren kann.

Treiber sollten mindestens authenticodesigniert sein, da Treiber, die nicht signiert oder selbstsigniert (d. h. mit einem Testzertifikat signiert) sind, auf vielen Windows-basierten Plattformen nicht installiert werden können. Weitere Informationen zum Signieren von Treibern und Code sowie zum zugehörigen Feature finden Sie unter [Driver Signing Requirements for Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) on Windows Hardware Developer [Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Zusammenfassung

Die Verwendung von Microsoft Authenticode ist ein einfacher Prozess. Nachdem Sie einen CER erhalten und einen privaten Schlüssel erstellt haben, ist es einfach, die von Microsoft bereitgestellten Tools zu verwenden. Anschließend können Sie wichtige Features in Windows Vista und Windows 7 aktivieren, z. B. Jugendschutz, und Kunden darüber informieren, dass Ihr Produkt direkt von seinem richtigen Besitzer stammt.

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu Tools und Prozessen im Zusammenhang mit dem Signieren von Code finden Sie unter den folgenden Links:

-   [Kryptografietools](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referenz zu Krypto-API-Tools](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Übersicht über Authenticode undTorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Digitale Zertifikate](/windows/desktop/SecCrypto/digital-certificates)
-   [Bereitstellen von Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [How To: Erstellen temporärer Zertifikate für die Verwendung während der Entwicklung](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
