---
title: Authenticode-Signierung für Spieleentwickler
description: In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und die Authentifizierung in einen täglichen Buildprozess integrieren.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e41d9b0f1149394e1aa2634f5df2a428630bfc0e7bd006e86065567e28eb6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650430"
---
# <a name="authenticode-signing-for-game-developers"></a>Authenticode-Signierung für Spieleentwickler

Die Datenauthentifizierung wird für Spieleentwickler immer wichtiger. Windows Vista und Windows 7 verfügen über eine Reihe von Features, z. B. Jugendschutz, die erfordern, dass Spiele ordnungsgemäß signiert werden, um sicherzustellen, dass niemand die Daten manipuliert hat. Mit Microsoft Authenticode können Endbenutzer und das Betriebssystem überprüfen, ob Programmcode vom richtigen Besitzer stammt und nicht böswillig geändert oder versehentlich beschädigt wurde. In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und die Authentifizierung in einen täglichen Buildprozess integrieren.

-   [Hintergrund](#background)
-   [Erste Schritte](#getting-started)
-   [Verwenden einer vertrauenswürdigen Zertifizierungsstelle](#using-a-trusted-certificate-authority)
-   [Beispiel für die Verwendung eines Testzertifikats](#example-using-a-test-certificate)
-   [Integrieren von Codesignatur in das tägliche Buildsystem](#integrating-code-signing-into-the-daily-build-system)
-   [Widerruf](#revocation)
-   [Codesignierungstreiber](#code-signing-drivers)
-   [Zusammenfassung](#summary)
-   [Weitere Informationen](#more-information)

> [!Note]  
> Ab dem 1. Januar 2016 vertrauen Windows 7 und höher keinem SHA-1-Codesignaturzertifikat mehr mit einem Ablaufdatum vom 1. Januar 2016 oder höher. Weitere Informationen finden Sie [unter Windows Erzwingung von Authenticode-Codesignatur und Zeitstempeln.](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx)

 

## <a name="background"></a>Hintergrund

Digitale Zertifikate werden verwendet, um die Identität des Autors einzurichten. Digitale Zertifikate werden von einem vertrauenswürdigen Drittanbieter ausgestellt, der als Zertifizierungsstelle (Certificate Authority, CA) bezeichnet wird, z. B. VeriSign oder Thawte. Die Zertifizierungsstelle ist dafür verantwortlich, zu überprüfen, ob der Besitzer keine falsche Identifizierung anfordert. Nach dem Anwenden eines Zertifikats bei einer Zertifizierungsstelle können kommerzielle Entwickler in weniger als zwei Wochen eine Antwort auf ihre Anwendung erwarten.

Nachdem die Zertifizierungsstelle entschieden hat, dass Sie ihre Richtlinienkriterien erfüllen, generiert sie ein Codesignaturzertifikat, das X.509 entspricht, dem von der International Telecommunications Union erstellten Branchenstandardzertifikatformat mit Erweiterungen der Version 3. Dieses Zertifikat identifiziert Sie und enthält Ihren öffentlichen Schlüssel. Sie wird von der Zertifizierungsstelle zur Referenz gespeichert, und Sie erhalten eine elektronische Kopie. Gleichzeitig erstellen Sie auch einen privaten Schlüssel, den Sie schützen müssen und den Sie nicht für jemanden freigeben dürfen, auch nicht für die Zertifizierungsstelle.

Nachdem Sie über einen öffentlichen und einen privaten Schlüssel verfügen, können Sie mit der Verteilung signierter Software beginnen. Microsoft stellt Tools zur Verfügung, um dies im Windows SDK zu tun. Die Tools verwenden einen einseitigen Hash, erzeugen einen Digest fester Länge und generieren eine verschlüsselte Signatur mit einem privaten Schlüssel. Anschließend kombinieren sie diese verschlüsselte Signatur mit Ihrem Zertifikat und Ihren Anmeldeinformationen in einer Struktur, die als Signaturblock bezeichnet wird, und betten sie in das Dateiformat der ausführbaren Datei ein. Jede Art von ausführbarer Binärdatei kann signiert werden, einschließlich DLLs, ausführbaren Dateien und Cab-Dateien.

Die Signatur kann auf verschiedene Weise überprüft werden. Programme können die CertVerifyCertificateChainPolicy-Funktion aufrufen, und SignTool (signtool.exe) kann verwendet werden, um eine Signatur über die Eingabeaufforderung zu überprüfen. Windows Der Explorer verfügt auch über eine Registerkarte Digitale Signaturen in Dateieigenschaften, auf der jedes Zertifikat einer signierten Binärdatei angezeigt wird. (Die Registerkarte Digitale Signaturen wird nur unter Dateieigenschaften für signierte Dateien angezeigt.) Außerdem kann eine Anwendung mithilfe von [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy)selbst überprüft werden.

Authenticode-Signaturen sind nicht nur für die Datenauthentifizierung durch Endbenutzer nützlich, sondern auch für das Patchen von eingeschränkten Benutzerkonten und die Jugendschutzmaßnahmen in Windows Vista und Windows 7 erforderlich. Darüber hinaus kann es bei zukünftigen Technologien in Windows Betriebssystemen erforderlich sein, dass Code signiert wird. Daher wird dringend empfohlen, dass alle professionellen und professionellen Entwickler ein Codesignaturzertifikat von einer Zertifizierungsstelle erwerben. Weitere Informationen dazu finden Sie weiter unten in diesem Artikel unter [Verwenden einer vertrauenswürdigen Zertifizierungsstelle.](#using-a-trusted-certificate-authority)

Spielcode, Patcher und Installationsprogramme können die Authenticode-Signierung weiter nutzen, indem überprüft wird, ob Dateien im Code authentifiziert sind. Dies kann für Anti-Cheat und allgemeine Netzwerksicherheit verwendet werden. Beispielcode zum Überprüfen, ob eine Datei signiert ist finden Sie hier: [Beispiel C-Programm: Überprüfen der Signatur einer PE-Datei](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)und Beispielcode zum Überprüfen des Besitzes eines Signaturzertifikats für eine signierte Datei finden Sie hier: [Abrufen von Informationen aus signierten Authenticode-ausführbaren Dateien.](https://support.microsoft.com/kb/323809)

## <a name="getting-started"></a>Erste Schritte

Für den Einstieg stellt Microsoft Tools mit Visual Studio 2005 und Visual Studio 2008 sowie im [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)bereit, um den Codesignaturprozess auszuführen und zu überprüfen. Nach der Installation von Visual Studio oder des Windows SDK befinden sich die in diesem technischen Artikel beschriebenen Tools in einem Unterverzeichnis der Installation, das eine oder mehrere der folgenden Elemente enthalten kann:

-   %SystemDrive% \\ Programme \\ Microsoft Visual Studio 8 \\ SDK \\ v2.0 \\ Bin
-   %SystemDrive% \\ Programme \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ Bin
-   %SystemDrive% \\ Programme \\ Microsoft Visual Studio 9.0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   %SystemDrive% \\ Programme \\ Microsoft SDKs Windows \\ \\ v6.0A \\ bin\\

Die folgenden Tools sind am nützlichsten für das Signieren von Code:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Zertifikaterstellungstool (MakeCert.exe)
</dt> <dd>

Generiert ein X.509-Testzertifikat als CER-Datei, die Ihren öffentlichen Schlüssel und einen privaten Schlüssel enthält, als PVK-Datei. Dieses Zertifikat dient nur zu internen Testzwecken und kann nicht öffentlich verwendet werden.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Erstellt eine Datei mit persönlichen Informationen Exchange (PFX) aus einem Paar von CER- und PVK-Dateien. Die PFX-Datei enthält sowohl Ihren öffentlichen als auch den privaten Schlüssel.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Signiert die Datei mithilfe der PFX-Datei. SignTool unterstützt das Signieren von DLL-Dateien, ausführbaren Dateien, Windows Installer-Dateien (.msi) und .cab dateien.

</dd> </dl>

> [!Note]  
> Während Sie andere Dokumentationen lesen, finden Sie möglicherweise Verweise auf SignCode (SignCode.exe), aber dieses Tool ist veraltet und wird nicht mehr unterstützt. Verwenden Sie stattdessen SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Verwenden einer vertrauenswürdigen Zertifizierungsstelle

Um ein vertrauenswürdiges Zertifikat zu erhalten, müssen Sie eine Anwendung auf eine Zertifizierungsstelle (Ca) wie VeriSign oder Thawte anwenden. Microsoft empfiehlt keine Zertifizierungsstelle über eine andere. Wenn Sie jedoch in den Windows-Fehlerberichterstattung-Dienst (WER) integrieren möchten, sollten Sie veriSign verwenden, um das Zertifikat auszustellen, da für den Zugriff auf die WER-Datenbank ein WinQual-Konto erforderlich ist, das eine VeriSign-ID erfordert. Eine vollständige Liste der vertrauenswürdigen Zertifizierungsstellen von Drittanbietern finden Sie unter Mitglieder des [Microsoft-Stammzertifikatprogramms.](/previous-versions/ms995347(v=msdn.10)) Weitere Informationen zur Registrierung bei WER finden Sie unter[Einführung Windows-Fehlerberichterstattung](https://msdn.microsoft.com/)in [der ISV-Zone.](https://msdn.microsoft.com/)

Nachdem Sie Ihr Zertifikat von der Zertifizierungsstelle erhalten haben, können Sie Ihr Programm mit SignTool signieren und das Programm für die Öffentlichkeit freigeben. Sie müssen jedoch darauf achten, dass Sie Ihren privaten Schlüssel schützen, der in Ihren PFX- und PVK-Dateien enthalten ist. Achten Sie darauf, diese Dateien an einem sicheren Speicherort zu speichern.

## <a name="example-using-a-test-certificate"></a>Beispiel für die Verwendung eines Testzertifikats

Die folgenden Schritte veranschaulichen die Erstellung eines Codesignaturzertifikats zu Testzwecken, gefolgt von der Signierung eines Direct3D-Beispielprogramms (BasicHLSL.exe genannt) mit diesem Testzertifikat. Mit diesem Verfahren werden CER- und PVK-Dateien –Ihre öffentlichen bzw. privaten Schlüssel – erstellt, die nicht für die öffentliche Zertifizierung verwendet werden können.

In diesem Beispiel wird der Signatur auch ein Zeitstempel hinzugefügt. Ein Zeitstempel verhindert, dass die Signatur ungültig wird, wenn das Zertifikat abläuft. Code, der signiert ist, aber keinen Zeitstempel hat, wird nach Ablauf des Zertifikats nicht überprüft. Daher sollte der gesamte öffentlich freigegebene Code einen Zeitstempel aufweisen.

**So erstellen Sie ein Zertifikat und signieren ein Programm**

1.  Erstellen Sie mit dem Zertifikaterstellungstool (MakeCert.exe) ein Testzertifikat und einen privaten Schlüssel.

    Im folgenden Befehlszeilenbeispiel wird MyPrivateKey als Dateiname für die Datei mit dem privaten Schlüssel (PVK) angegeben, MyPublicKey als Dateiname für die Zertifikatdatei (CER) und MySoftwareCompany als Name des Zertifikats. Außerdem wird das Zertifikat selbstsigniert, sodass es nicht über eine nicht vertrauenswürdige Stammzertifizierungsstelle verfügt.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Erstellen Sie mithilfe von pvk2pfx.exe eine Datei mit persönlichen Informationen Exchange (PFX) aus Ihrer PVK- (PRIVATE KEY)-Datei und zertifikatsdatei (CER-Datei).

    Die PFX-Datei kombiniert Ihre öffentlichen und privaten Schlüssel in einer einzelnen Datei. Im folgenden Befehlszeilenbeispiel werden die PVK- und CER-Dateien aus dem vorherigen Schritt verwendet, um die PFX-Datei namens MyPFX mit dem Kennwort Für Ihr Kennwort zu \_ erstellen:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Signieren Sie Ihr Programm mitHilfe von SignTool mit Ihrer PFX-Datei (Personal Information Exchange).

    Sie können mehrere Optionen in der Befehlszeile angeben. Das folgende Befehlszeilenbeispiel verwendet die PFX-Datei aus dem vorherigen Schritt, gibt Ihr \_ Kennwort als Kennwort an, gibt BasicHLSL als zu signierte Datei an und ruft einen Zeitstempel von einem angegebenen Server ab:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > Die URL zum Zeitstempeldienst wird von der Zertifizierungsstelle bereitgestellt und ist für Tests optional. Es ist wichtig, dass die Produktionssignatur eine gültige Zeitstempelautorität enthält. Andernfalls kann die Signatur nicht überprüft werden, wenn das Zertifikat abläuft.

     

4.  Überprüfen Sie mit SignTool, ob das Programm signiert ist.

    Im folgenden Befehlszeilenbeispiel wird angegeben, dass SignTool versuchen soll, die Signatur auf BasicHLSL.exe zu überprüfen, indem alle verfügbaren Methoden verwendet werden, während eine ausführliche Ausgabe bereitgestellt wird:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    In diesem Beispiel sollte SignTool angeben, dass das Zertifikat angefügt ist, aber auch angeben, dass es nicht vertrauenswürdig ist, da es nicht von einer Zertifizierungsstelle ausgestellt wird.

5.  Vertrauen Sie dem Testzertifikat.

    Für Testzertifikate müssen Sie dem Zertifikat vertrauen. Dieser Schritt sollte für Zertifikate übersprungen werden, die von einer Zertifizierungsstelle bereitgestellt werden, da diese standardmäßig als vertrauenswürdig eingestuft werden.

    Führen Sie auf nur den Computern, auf denen Sie dem Testzertifikat vertrauen möchten, Folgendes aus:

    ```
    certmgr.msc
    ```

    

    Klicken Sie dann mit der rechten Maustaste auf Vertrauenswürdige Stammzertifizierungsstellen, und wählen Sie Alle Aufgaben \| importieren aus. Navigieren Sie dann zur PFX-Datei, die Sie erstellt haben, und führen Sie die Schritte des Assistenten aus, und platzieren Sie das Zertifikat im Vertrauenswürdige Stammzertifizierungsstellen.

    Nach Abschluss des Assistenten können Sie mit dem Testen des vertrauenswürdigen Zertifikats auf diesem Computer beginnen.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrieren von Codesignatur in das tägliche Buildsystem

Um die Codesignatur in ein Projekt zu integrieren, können Sie eine Batchdatei oder ein Skript erstellen, um die Befehlszeilentools auszuführen. Nachdem das Projekt erstellt wurde, führen Sie SignTool mit den richtigen Einstellungen aus (wie in Schritt 3 unseres Beispiels gezeigt).

Seien Sie beim Buildprozess besonders vorsichtig, um zu sichern, dass der Zugriff auf die PFX- und PVK-Dateien auf so wenige Computer und Benutzer wie möglich beschränkt ist. Als bewährte Methode sollten Entwickler Code nur mithilfe des Testzertifikats signieren, bis sie bereit für den Versand sind. Auch hier sollte der private Schlüssel (PVK) an einem sicheren Ort wie einem sicheren oder gesperrten Raum und idealerweise auf einem kryptografischen Gerät wie einer Smartcard aufbewahrt werden.

Eine weitere Schutzebene wird bereitgestellt, indem Microsoft Authenticode verwendet wird, um das Windows Installer-Paket selbst zu signieren. Dadurch wird das MSI-Paket vor Manipulationen und versehentlicher Beschädigung geschützt. Weitere Informationen zum Signieren von Paketen mit Authenticode finden Sie in der Dokumentation zu Ihrem MSI-Erstellungstool.

## <a name="revocation"></a>Widerruf

Falls die Sicherheit des privaten Schlüssels gefährdet ist oder ein sicherheitsbezogenes Ereignis ein Code-Signing Zertifikat ungültig macht, muss der Entwickler das Zertifikat widerrufen. Andernfalls würden die Integrität des Entwicklers und die Effektivität des Signierungscodes beeinträchtigt. Eine Zertifizierungsstelle kann auch eine Sperrung mit einer bestimmten Zeit ausstellen. Code, der mit einem Zeitstempel vor der Sperrzeit signiert ist, gilt weiterhin als gültig, aber Code mit einem nachfolgenden Zeitstempel ist ungültig. Die Zertifikatsperrung wirkt sich auf Code in anwendungen aus, die mit dem gesperrten Zertifikat signiert sind.

## <a name="code-signing-drivers"></a>Code-Signing-Treiber

Treiber können und sollten Authenticode-signiert sein. Kernelmodustreiber haben zusätzliche Anforderungen: 64-Bit-Editionen von Windows Vista und Windows 7 verhindern die Installation aller Treiber im nicht signierten Kernelmodus, und alle Versionen von Windows zeigen eine Warnungsaufforderung an, wenn ein Benutzer versucht, einen nicht signierten Treiber zu installieren. Darüber hinaus können Administratoren Gruppenrichtlinie festlegen, um zu verhindern, dass nicht signierte Treiber auf Microsoft Windows Server 2003, Windows XP Professional x64 Edition und 32-Bit-Editionen von Windows Vista und Windows 7 installiert werden.

Viele Treibertypen können mit einer vertrauenswürdigen Microsoft-Signatur signiert werden – im Rahmen des Windows Certification Program of [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) oder des [Unclassified Signature Program](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (ehemals Driver Reliability Signature), das es dem System ermöglicht, diesen Treibern vollständig zu vertrauen und sie auch ohne Administratoranmeldeinformationen zu installieren.

Treiber sollten mindestens authenticodesigniert sein, da Treiber, die nicht signiert oder selbstsigniert (d. h. mit einem Testzertifikat signiert) sind, nicht auf vielen Windows-basierten Plattformen installiert werden können. Weitere Informationen zu Signaturtreibern und Code sowie zu verwandten Features finden Sie unter [Driver Signing Requirements for Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) on Windows Hardware Developer [Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Zusammenfassung

Die Verwendung von Microsoft Authenticode ist ein einfacher Prozess. Nachdem Sie einen CER erhalten und einen privaten Schlüssel erstellt haben, ist es eine einfache Frage der Verwendung der von Microsoft bereitgestellten Tools. Anschließend können Sie wichtige Features in Windows Vista und Windows 7 aktivieren, z. B. die Jugendschutzmaßnahmen, und Kunden mitteilen, dass Ihr Produkt direkt vom richtigen Besitzer stammt.

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu Tools und Prozessen im Zusammenhang mit Signaturcode finden Sie unter den folgenden Links:

-   [Kryptografietools](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referenz zu Kryptografie-API-Tools](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Authenticode Overview and Turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Digitale Zertifikate](/windows/desktop/SecCrypto/digital-certificates)
-   [Bereitstellen von Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Vorgehensweise: Erstellen temporärer Zertifikate für die Verwendung während der Entwicklung](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
