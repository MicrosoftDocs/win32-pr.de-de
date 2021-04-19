---
title: Authenticode-Signierung für Spieleentwickler
description: In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und wie Sie die Authentifizierung in einen täglichen Buildprozess integrieren.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f304e6cc8e185264699709987f62dfdca17bf8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341948"
---
# <a name="authenticode-signing-for-game-developers"></a>Authenticode-Signierung für Spieleentwickler

Die Daten Authentifizierung ist für Spieleentwickler zunehmend wichtig. Windows Vista und Windows 7 verfügen über eine Reihe von Features, wie z. b. Steuerelemente, bei denen Spiele ordnungsgemäß signiert werden müssen, um sicherzustellen, dass die Daten nicht manipuliert wurden. Microsoft Authenticode ermöglicht es Endbenutzern und dem Betriebssystem, zu überprüfen, ob der Programmcode vom rechtmäßigen Besitzer stammt und nicht böswillig geändert oder versehentlich beschädigt wurde. In diesem Artikel wird erläutert, wie Sie mit der Authentifizierung Ihres Spiels beginnen und wie Sie die Authentifizierung in einen täglichen Buildprozess integrieren.

-   [Hintergrund](#background)
-   [Erste Schritte](#getting-started)
-   [Verwenden einer vertrauenswürdigen Zertifizierungsstelle](#using-a-trusted-certificate-authority)
-   [Beispiel für die Verwendung eines Test Zertifikats](#example-using-a-test-certificate)
-   [Integrieren der Code Signierung in das tägliche Buildsystem](#integrating-code-signing-into-the-daily-build-system)
-   [Widerruf](#revocation)
-   [Code Signatur Treiber](#code-signing-drivers)
-   [Zusammenfassung](#summary)
-   [Weitere Informationen](#more-information)

> [!Note]  
> Ab dem 1. Januar 2016 Vertrauen Windows 7 und höher nicht mehr auf SHA-1-Code Signatur Zertifikate mit einem Ablaufdatum von 1. Januar 2016 oder höher. Weitere Informationen finden Sie unter Windows-Erzwingung [von Authenticode-Code Signierung und-Zeitstempel](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) .

 

## <a name="background"></a>Hintergrund

Digitale Zertifikate werden verwendet, um die Identität des Autors festzulegen. Digitale Zertifikate werden von einem vertrauenswürdigen Drittanbieter ausgestellt, der als Zertifizierungsstelle (ca) bezeichnet wird, z. b. VeriSign oder Thawte. Die Zertifizierungsstelle ist dafür verantwortlich, zu überprüfen, ob der Besitzer keinen falschen Identifizierungswert beansprucht. Nach der Anwendung auf eine Zertifizierungsstelle für ein Zertifikat können kommerzielle Entwickler in weniger als zwei Wochen eine Antwort auf Ihre Anwendung erwarten.

Nachdem die Zertifizierungsstelle beschlossen hat, dass Sie Ihre Richtlinien Kriterien erfüllen, generiert Sie ein Code Signaturzertifikat, das X. 509 entspricht, dem Branchenstandard-Zertifikat Format, das von der internationalen Telekommunikations Union mit Version 3-Erweiterungen erstellt wurde. Dieses Zertifikat identifiziert Sie und enthält Ihren öffentlichen Schlüssel. Sie wird von der Zertifizierungsstelle zur Referenz gespeichert, und Sie erhalten eine Kopie elektronisch. Gleichzeitig erstellen Sie auch einen privaten Schlüssel, den Sie sicher aufbewahren müssen, und den Sie nicht für andere Benutzer freigeben dürfen, auch für die Zertifizierungsstelle.

Nachdem Sie über einen öffentlichen und einen privaten Schlüssel verfügen, können Sie mit der Verteilung signierter Software beginnen. Microsoft stellt Tools bereit, um dies im Windows SDK zu tun. Die Tools verwenden einen unidirektionalen Hash, erzeugen einen Digest mit fester Länge und generieren eine verschlüsselte Signatur mit einem privaten Schlüssel. Anschließend kombinieren Sie diese verschlüsselte Signatur mit Ihrem Zertifikat und den Anmelde Informationen in einer Struktur, die als Signatur Block bezeichnet wird, und Betten Sie in das Dateiformat der ausführbaren Datei ein. Jeder Typ von ausführbarer Binärdatei kann signiert werden, einschließlich DLLs, ausführbaren Dateien und CAB-Dateien.

Die Signatur kann auf verschiedene Weise überprüft werden. Programme können die CertVerifyCertificateChainPolicy-Funktion und SignTool (signtool.exe) zum Überprüfen einer Signatur von der Befehlszeilen Aufforderung aus verwenden. Windows-Explorer verfügt auch über eine Registerkarte Digitale Signaturen in den Dateieigenschaften, die jedes Zertifikat einer signierten Binärdatei anzeigt. (Die Registerkarte Digitale Signaturen wird nur in den Dateieigenschaften für signierte Dateien angezeigt.) Außerdem kann eine Anwendung über die Verwendung von [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy)selbst überprüft werden.

Die Authenticode-Signierung ist nicht nur für die Daten Authentifizierung durch Endbenutzer nützlich, sondern auch für das Patchen von eingeschränkten Benutzerkonten und durch die Jugendschutz Maßnahmen in Windows Vista und Windows 7. Darüber hinaus kann es bei zukünftigen Technologien in Windows-Betriebssystemen erforderlich sein, dass Code signiert ist, daher wird dringend empfohlen, dass alle professionellen und Amateur Entwickler ein Code Signaturzertifikat von einer Zertifizierungsstelle erhalten. Weitere Informationen hierzu finden Sie weiter unten in diesem Artikel unter [Verwenden einer vertrauenswürdigen Zertifizierungs](#using-a-trusted-certificate-authority)Stelle.

Spielcode, Patcher und Installationsprogramme können die autorifizierung von authenicode weiter nutzen, indem Sie überprüfen, ob die Dateien im Code authentisch sind. Dies kann für Anticheat-und allgemeine Netzwerksicherheit verwendet werden. Beispielcode für die Überprüfung, ob eine Datei signiert ist, finden Sie hier: [Beispiel C-Programm: Überprüfen der Signatur einer PE-Datei](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)und Beispielcode für die Überprüfung des Besitzes eines Signatur Zertifikats für eine signierte Datei finden Sie hier: [Informationen zum erhalten von Informationen aus authentifizierten ausführbaren Dateien mit Authenticode](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Erste Schritte

Für den Einstieg bietet Microsoft Tools mit Visual Studio 2005 und Visual Studio 2008 und in der [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx), um den Code Signatur Prozess zu unterstützen und zu überprüfen. Nach der Installation von Visual Studio oder der Windows SDK befinden sich die in diesem technischen Artikel beschriebenen Tools in einem Unterverzeichnis der-Installation, das möglicherweise eine oder mehrere der folgenden Komponenten enthält:

-   % System Drive% \\ Program Files \\ Microsoft Visual Studio 8 \\ SDK \\ v 2.0 \\ bin
-   % System Drive% \\ Program Files \\ Microsoft Visual Studio 8 \\ VC \\ platformsdk \\ bin
-   % System Drive% \\ Programme \\ Microsoft Visual Studio 9,0 \\ smartdevices \\ SDK \\ sdktools\\
-   % System Drive% \\ Program Files \\ Microsoft sdert \\ Windows \\ v 6.0 a \\ bin\\

Die folgenden Tools sind die nützlichsten für das Signieren von Code:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Zertifikaterstellungs-Tool (MakeCert.exe)
</dt> <dd>

Generiert ein X. 509-Test Zertifikat als CER-Datei, das Ihren öffentlichen Schlüssel und einen privaten Schlüssel als PVK-Datei enthält. Dieses Zertifikat dient nur zu internen Testzwecken und kann nicht öffentlich verwendet werden.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Erstellt eine PFX-Datei (Personal Information Exchange) aus einem Paar von CER-und PVK-Dateien. Die PFX-Datei enthält sowohl den öffentlichen als auch den privaten Schlüssel.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Signiert die Datei mithilfe der PFX-Datei. SignTool unterstützt das Signieren von DLL-Dateien, ausführbaren Dateien, Windows Installer Dateien (MSI-Dateien) und CAB-Dateien (CAB-Dateien).

</dd> </dl>

> [!Note]  
> Beim Lesen anderer Dokumentationen finden Sie möglicherweise Verweise auf Signcode (SignCode.exe). dieses Tool ist jedoch veraltet und wird nicht mehr unterstützt – verwenden Sie stattdessen SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Verwenden einer vertrauenswürdigen Zertifizierungsstelle

Zum Abrufen eines vertrauenswürdigen Zertifikats müssen Sie eine Zertifizierungsstelle (ca), z. b. VeriSign oder Thawte, anwenden. Microsoft empfiehlt keine Zertifizierungsstelle, aber wenn Sie in den Windows-Fehlerberichterstattung (wer)-Dienst integrieren möchten, sollten Sie die Verwendung von VeriSign zum Ausstellen des Zertifikats in Erwägung ziehen, da der Zugriff auf die wer-Datenbank ein Winqual-Konto erfordert, das eine VeriSign-ID erfordert. Eine umfassende Liste der vertrauenswürdigen Drittanbieter-Zertifizierungsstellen finden Sie unter [Mitglieder des Microsoft Root Certificate Program](/previous-versions/ms995347(v=msdn.10)). Weitere Informationen zum Registrieren bei wer finden Sie unter "[Introducing Windows-Fehlerberichterstattung](https://msdn.microsoft.com/)" in der [ISV-Zone](https://msdn.microsoft.com/).

Nachdem Sie Ihr Zertifikat von der Zertifizierungsstelle erhalten haben, können Sie das Programm mithilfe von SignTool Signieren und das Programm öffentlich veröffentlichen. Allerdings müssen Sie darauf achten, den privaten Schlüssel zu schützen, der in ihren PFX-und PVK-Dateien enthalten ist. Stellen Sie sicher, dass Sie diese Dateien an einem sicheren Ort aufbewahren.

## <a name="example-using-a-test-certificate"></a>Beispiel für die Verwendung eines Test Zertifikats

In den folgenden Schritten wird veranschaulicht, wie Sie ein Code Signaturzertifikat zu Testzwecken erstellen, gefolgt vom Signieren eines Direct3D-Beispiel Programms (mit dem Namen "BasicHLSL.exe") mit diesem Test Zertifikat. Diese Prozedur erstellt CER-und PVK-Dateien – ihre öffentlichen und privaten Schlüssel –, die nicht für die öffentliche Zertifizierung verwendet werden können.

In diesem Beispiel wird der Signatur auch ein Zeitstempel hinzugefügt. Ein Zeitstempel verhindert, dass die Signatur ungültig wird, wenn das Zertifikat abläuft. Code, der signiert ist, aber keinen Zeitstempel hat, wird nicht überprüft, nachdem das Zertifikat abläuft. Daher sollte der gesamte öffentlich freigegebene Code über einen Zeitstempel verfügen.

**So erstellen Sie ein Zertifikat und Signieren ein Programm**

1.  Erstellen Sie mit dem Tool zum Erstellen von Zertifikaten (MakeCert.exe) ein Test Zertifikat und einen privaten Schlüssel.

    Im folgenden Befehlszeilen Beispiel wird myprivatekey als Dateiname für die Datei mit dem privaten Schlüssel (PVK-Datei), mypublickey als Dateiname für die Zertifikatsdatei (. cer) und MySoftwareCompany als Name des Zertifikats angegeben. Außerdem wird das Zertifikat selbst signiert, sodass es nicht über eine nicht vertrauenswürdige Stamm Zertifizierungsstelle verfügt.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Erstellen Sie mithilfe pvk2pfx.exe eine PFX-Datei (Personal Information Exchange) aus Ihrer Datei mit dem privaten Schlüssel (PVK-Datei) und der Zertifikatsdatei (CER-Datei).

    Die PFX-Datei kombiniert ihre öffentlichen und privaten Schlüssel in einer einzelnen Datei. Im folgenden Befehlszeilen Beispiel werden die PVK-und CER-Dateien aus dem vorherigen Schritt verwendet, um die PFX-Datei mit dem Kennwort für Ihr \_ Kennwort zu erstellen:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Signieren Sie Ihr Programm mit der PFX-Datei (Personal Information Exchange) mithilfe von SignTool.

    Sie können mehrere Optionen in der Befehlszeile angeben. Im folgenden Befehlszeilen Beispiel wird die PFX-Datei aus dem vorherigen Schritt verwendet, Ihr \_ Kennwort als Kennwort angegeben, basichlsl als zu Signier Ende Datei angegeben und ein Zeitstempel von einem angegebenen Server abgerufen:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > Die URL zum Zeitstempeldienst wird von der Zertifizierungsstelle bereitgestellt und ist für Tests optional. Es ist wichtig, dass die Produktions Signatur eine gültige Zeitstempel Zertifizierungsstelle enthält, oder die Signatur kann nicht überprüft werden, wenn das Zertifikat abläuft.

     

4.  Überprüfen Sie, ob das Programm mit SignTool signiert ist.

    Im folgenden Befehlszeilen Beispiel wird angegeben, dass SignTool versuchen soll, die Signatur auf BasicHLSL.exe zu überprüfen, indem Sie alle verfügbaren Methoden verwenden, während Sie eine ausführliche Ausgabe bereitstellen:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    In diesem Beispiel sollte SignTool angeben, dass das Zertifikat angefügt ist, und auch angeben, dass es nicht vertrauenswürdig ist, da es nicht von einer Zertifizierungsstelle ausgestellt wird.

5.  Vertrauen Sie dem Test Zertifikat.

    Für Test Zertifikate müssen Sie das Zertifikat als vertrauenswürdig einstufen. Dieser Schritt sollte für Zertifikate übersprungen werden, die von einer Zertifizierungsstelle bereitgestellt werden, da diese standardmäßig vertrauenswürdig sind.

    Führen Sie auf den Computern, auf denen Sie das Test Zertifikat als vertrauenswürdig einstufen möchten, Folgendes aus:

    ```
    certmgr.msc
    ```

    

    Klicken Sie dann mit der rechten Maustaste auf vertrauenswürdige Stamm Zertifizierungsstellen, und wählen Sie alle Aufgaben \| importieren Navigieren Sie dann zu der von Ihnen erstellten PFX-Datei, und befolgen Sie die Schritte des Assistenten, indem Sie das Zertifikat in den vertrauenswürdigen Stamm Zertifizierungsstellen platzieren.

    Wenn der Assistent abgeschlossen ist, können Sie mit dem vertrauenswürdigen Zertifikat auf diesem Computer beginnen.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrieren der Code Signierung in das tägliche Buildsystem

Um die Code Signierung in ein Projekt zu integrieren, können Sie eine Batchdatei oder ein Skript erstellen, um die Befehlszeilen Tools auszuführen. Nachdem das Projekt erstellt wurde, führen Sie signtool mit den richtigen Einstellungen aus (wie in Schritt 3 dieses Beispiels gezeigt).

Seien Sie im Buildprozess besonders vorsichtig, um sicherzustellen, dass der Zugriff auf die PFX-und PVK-Dateien auf so wenige Computer und Benutzer wie möglich beschränkt ist. Als bewährte Vorgehensweise sollten Entwickler nur dann Code mithilfe des Test Zertifikats signieren, wenn Sie bereit sind, ausgeliefert zu werden. Auch hier sollte der private Schlüssel (PVK) an einem sicheren Ort aufbewahrt werden, wie z. b. einem sicheren oder gesperrten Raum, und idealerweise auf einem kryptografiegerät, wie z. b. eine Smartcard.

Eine weitere Schutz Ebene wird durch die Verwendung von Microsoft Authenticode zum Signieren des Windows Installer (MSI)-Pakets bereitgestellt. Dies trägt zum Schutz des MSI-Pakets vor Manipulationen und versehentlicher Beschädigung bei. Weitere Informationen zum Signieren von Paketen mit Authenticode finden Sie in der Dokumentation zu Ihrem MSI-Erstellungs Tool.

## <a name="revocation"></a>Widerruf

Wenn die Sicherheit des privaten Schlüssels gefährdet ist oder ein Sicherheits bezogenes Ereignis ein ungültiges Code-Signing Zertifikat rendert, muss der Entwickler das Zertifikat widerrufen. Wenn Sie dies nicht tun, würde dies die Integrität des Entwicklers und die Effektivität des Signatur Codes Schwächen. Eine Zertifizierungsstelle kann auch eine Sperrung mit einer bestimmten Zeit ausstellen. Code, der vor der Sperr Zeit mit einem Zeitstempel signiert wurde, wird weiterhin als gültig angesehen, aber der Code mit einem nachfolgenden Zeitstempel ist ungültig. Die Zertifikat Sperrung wirkt sich auf den Code in allen Anwendungen aus, die mit dem gesperrten Zertifikat signiert sind.

## <a name="code-signing-drivers"></a>Code-Signing Treiber

Treiber können und mit Authenticode signiert werden. Kernelmodustreiber haben zusätzliche Anforderungen: 64-Bit-Editionen von Windows Vista und Windows 7 verhindern die Installation aller nicht signierten Kernelmodustreiber, und alle Versionen von Windows zeigen eine Warnmeldung an, wenn ein Benutzer versucht, einen nicht signierten Treiber zu installieren. Außerdem können Administratoren Gruppenrichtlinie festlegen, um zu verhindern, dass nicht signierte Treiber auf Microsoft Windows Server 2003, Windows XP Professional x64 Edition und 32-Bit-Editionen von Windows Vista und Windows 7 installiert werden.

Viele Treiber Typen können mit einer von Microsoft vertrauenswürdigen Signatur signiert werden – als Teil des Windows-Zertifizierungsprogramms von [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) oder des [nicht klassifizierten Signatur Programms](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (früher als "Treiber Zuverlässigkeits Signatur" bezeichnet) – mit dem das System diese Treiber vollständig als vertrauenswürdig einstufen und auch ohne administrative Anmelde Informationen installieren kann.

Treiber müssen mindestens mit Authenticode signiert werden, da nicht signierte oder selbst signierte Treiber (d. h. mit einem Test Zertifikat signiert) auf vielen Windows-basierten Plattformen nicht installiert werden können. Weitere Informationen zu Signatur Treibern und Code und zugehöriger Funktion finden Sie unter [Treiber Signierungs Anforderungen für Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) auf [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Zusammenfassung

Die Verwendung von Microsoft Authenticode ist ein einfacher Prozess. Nachdem Sie einen CER abgerufen und einen privaten Schlüssel erstellt haben, ist es einfach, die von Microsoft bereitgestellten Tools zu verwenden. Sie können dann wichtige Features in Windows Vista und Windows 7 aktivieren, wie z. b. Jugend schutzkontrollen, und den Kunden mitteilen, dass Ihr Produkt direkt von seinem rechtmäßigen Besitzer stammt.

## <a name="more-information"></a>Weitere Informationen

Weitere Informationen zu Tools und Prozessen im Zusammenhang mit dem Signieren von Code finden Sie unter den folgenden Links:

-   [Kryptografietools](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referenz zur Crypto-API-Tools](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Übersicht über Authenticode und turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Digitale Zertifikate](/windows/desktop/SecCrypto/digital-certificates)
-   [Bereitstellen von Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Vorgehensweise: Erstellen von temporären Zertifikaten für die Verwendung während der Entwicklung](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 