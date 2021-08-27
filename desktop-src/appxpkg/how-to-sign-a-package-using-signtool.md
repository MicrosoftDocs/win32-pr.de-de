---
title: Signieren eines App-Pakets mithilfe von SignTool
description: Erfahren Sie, wie Sie SignTool verwenden, um Ihre Windows-App-Pakete zu signieren, damit sie bereitgestellt werden können.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4e4c0941cbcced30053b8fd31e44100adc9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474886"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Signieren eines App-Pakets mithilfe von SignTool

> [!Note]  
> Informationen zum Signieren eines Windows App-Pakets finden Sie unter [Signieren eines App-Pakets mit SignTool.](/windows/msix/package/sign-app-package-using-signtool)

 

Erfahren Sie, wie Sie [**SignTool**](/windows-hardware/drivers/devtest/signtool) verwenden, um Ihre Windows-App-Pakete zu signieren, damit sie bereitgestellt werden können. [**SignTool**](/windows-hardware/drivers/devtest/signtool) ist Teil des Windows Software Development Kit (SDK).

Alle Windows-App-Pakete müssen digital signiert werden, bevor sie bereitgestellt werden können. Während Microsoft Visual Studio 2012 und höher ein App-Paket während der Erstellung signieren können, werden Pakete, die Sie mithilfe des [Tools app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) aus dem Windows SDK erstellen, nicht signiert.

> [!Note]  
> Sie können [**SignTool**](/windows-hardware/drivers/devtest/signtool) nur verwenden, um Ihre Windows-App-Pakete auf Windows 8 und höher oder Windows Server 2012 und höher zu signieren. Sie können **SignTool** nicht zum Signieren von App-Paketen auf downleveln Betriebssystemen wie Windows 7 oder Windows Server 2008 R2 verwenden.

 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [App-Pakete und Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Tools zum Signieren von Dateien und Überprüfen von Signaturen](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Voraussetzungen

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), das Teil des Windows SDK ist
-   Ein gültiges Codesignaturzertifikat, z. B. eine PFX-Datei (Personal Information Exchange), die mit den [**toolsMakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) erstellt wurde

    Informationen zum Erstellen eines gültigen Codesignaturzertifikats finden Sie unter [Erstellen eines App-Paketsignaturzertifikats.](how-to-create-a-package-signing-certificate.md)

-   Eine gepackte Windows-App, z.B. eine APPX-Datei, die mit dem [Tool app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) erstellt wurde.

**Weitere Überlegungen**

Das Zertifikat, das Sie zum Signieren des App-Pakets verwenden, muss die folgenden Kriterien erfüllen:

-   Der Antragstellername des Zertifikats muss mit dem **Publisher** Attribut übereinstimmen, das im [**Identity-Element**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) der AppxManifest.xml-Datei enthalten ist, die im Paket gespeichert ist. Der Herausgebername ist Teil der Identität einer gepackten Windows-App, sodass Sie den Antragstellernamen des Zertifikats mit dem Herausgebernamen der App abgleichen müssen. Dadurch kann die Identität signierter Pakete anhand der digitalen Signatur überprüft werden. Informationen zu Signaturfehlern, die beim Signieren eines App-Pakets mit [**SignTool**](/windows-hardware/drivers/devtest/signtool)auftreten können, finden Sie im Abschnitt Hinweise unter [Erstellen eines App-Paketsignaturzertifikats.](how-to-create-a-package-signing-certificate.md)
-   Das Zertifikat muss für die Codesignatur gültig sein. Dies bedeutet, dass beide Elemente zutreffen müssen:

    -   Das Feld Erweiterte Schlüsselverwendung (Extended Key Usage, EKU) des Zertifikats muss entweder nicht bestimmt sein oder den EKU-Wert für codesignieren (1.3.6.1.5.5.7.3.3) enthalten.
    -   Das Feld Schlüsselverwendung (Key Usage, KU) des Zertifikats muss entweder nicht fest sein oder das Nutzungsbit für die digitale Signatur (0x80) enthalten.

-   Das Zertifikat enthält einen privaten Schlüssel.
-   Das Zertifikat ist gültig. Sie ist aktiv, ist nicht abgelaufen und wurde nicht widerrufen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Schritt 1: Bestimmen des zu verwendende Hashalgorithmus

Wenn Sie das App-Paket signieren, müssen Sie den gleichen Hashalgorithmus verwenden, den Sie beim Erstellen des App-Pakets verwendet haben. Wenn Sie die Standardeinstellungen zum Erstellen des App-Pakets verwendet haben, wird der Hashalgorithmus SHA256 verwendet.

Wenn Sie den App Packager mit einem bestimmten Hashalgorithmus zum Erstellen des App-Pakets verwendet haben, verwenden Sie den gleichen Algorithmus, um das Paket zu signieren. Um den Hashalgorithmus zu bestimmen, der zum Signieren eines Pakets verwendet werden soll, können Sie den Paketinhalt extrahieren und die AppxBlockMap.xml Datei untersuchen. Das **HashMethod-Attribut** des [**BlockMap-Elements**](/uwp/schemas/blockmapschema/element-blockmap) gibt den Hashalgorithmus an, der beim Erstellen des App-Pakets verwendet wurde. Beispiel:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

Das vorangehende [**BlockMap-Element**](/uwp/schemas/blockmapschema/element-blockmap) gibt an, dass der SHA256-Algorithmus verwendet wurde. In dieser Tabelle ist die Zuordnung der derzeit verfügbaren Algorithmen aufgeführt:

| **HashMethod-Wert**                            | zu verwendende *hashAlgorithm* |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (.appx-Standard) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Schritt 2: Ausführen von SignTool.exe zum Signieren des Pakets

**So signieren Sie das Paket mit einem Signaturzertifikat aus einer PFX-Datei**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) verwendet den Parameter /fd *hashAlgorithm* standardmäßig auf SHA1, wenn er nicht angegeben ist, und SHA1 ist für das Signieren von App-Paketen nicht gültig. Daher müssen Sie diesen Parameter angeben, wenn Sie ein App-Paket signieren. Um ein App-Paket zu signieren, das mit dem STANDARDMÄßIGEN SHA256-Hash erstellt wurde, geben Sie den Parameter /fd *hashAlgorithm* als SHA256 an:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Sie können den */p-Kennwortparameter* weglassen, wenn Sie eine PFX-Datei verwenden, die nicht kennwortgeschützt ist. Sie können auch andere Zertifikatauswahloptionen verwenden, die von [**SignTool**](/windows-hardware/drivers/devtest/signtool) unterstützt werden, um App-Pakete zu signieren. Weitere Informationen zu diesen Optionen finden Sie unter [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> Sie können den [](/windows-hardware/drivers/devtest/signtool) SignTool-Zeitstempelvorgang nicht für ein signiertes App-Paket verwenden. der Vorgang wird nicht unterstützt.

 

Wenn Sie das App-Paket mit einem Zeitstempel versehen möchten, müssen Sie es während des Signierens durchführen. Beispiel:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Machen Sie den Parameter /tr *timestampServerUrl* gleich der URL für einen RFC 3161-Zeitstempelserver.

## <a name="remarks"></a>Hinweise

In diesem Abschnitt wird die Problembehandlung bei Signaturfehlern für App-Pakete erläutert.

### <a name="troubleshooting-app-package-signing-errors"></a>Behandeln von Fehlern beim Signieren von App-Paketen

Zusätzlich zu den Signaturfehlern, die [**SignTool**](/windows-hardware/drivers/devtest/signtool) zurückgeben kann, kann **SignTool** auch Fehler zurückgeben, die spezifisch für das Signieren von App-Paketen sind. Diese Fehler werden in der Regel als interne Fehler angezeigt:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Wenn der Fehlercode mit 0x8008 beginnt, z. B. 0x80080206 APPX \_ E \_ CORRUPT \_ CONTENT), deutet dies darauf hin, dass das signierte Paket ungültig ist. In diesem Fall müssen Sie das Paket neu erstellen, bevor Sie das Paket signieren können. Die vollständige Liste der 0x8008 \* Fehler finden Sie unter [**COM-Fehlercodes (Sicherheit und Setup).**](/windows/desktop/com/com-error-codes-4)

In der Regel ist der Fehler 0x8007000b (ERROR \_ BAD \_ FORMAT). In diesem Fall finden Sie spezifischere Fehlerinformationen im Ereignisprotokoll:

**So durchsuchen Sie das Ereignisprotokoll**

1.  Führen Sie Eventvwr.msc aus.
2.  Öffnen Sie das Ereignisprotokoll: Ereignisanzeige (lokal) > Anwendungs- und Dienstprotokolle > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Suchen Sie nach dem letzten Fehlerereignis.

Der interne Fehler entspricht in der Regel einer der folgenden:


| Ereignis-ID | Beispielereigniszeichenfolge | Vorschlag | 
|----------|----------------------|------------|
| 150 | Fehler 0x8007000B: Der Herausgebername des App-Manifests (CN=Contoso) muss mit dem Antragstellernamen des Signaturzertifikats (CN=Contoso, C=US) übereinstimmen. | Der Herausgebername des App-Manifests muss genau mit dem Antragstellernamen der Signierung übereinstimmen.<blockquote>[!Note]<br />Diese Namen werden in Anführungszeichen angegeben und achten sowohl auf Groß-/Kleinschreibung als auch auf Leerzeichen.</blockquote><br /> Sie können die <strong>Publisher</strong> Attributzeichenfolge, die für das <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity-Element</strong></a> in der AppxManifest.xml-Datei definiert ist, so aktualisieren, dass sie dem Antragstellernamen des beabsichtigten Signaturzertifikats entspricht. Alternativ können Sie ein anderes Signaturzertifikat mit einem Antragstellernamen auswählen, der dem Herausgebernamen des App-Manifests entspricht. Der Name des Manifestherausgebers und der Name des Zertifikatsubjekts werden beide in der Ereignismeldung aufgeführt. | 
| 151 | Fehler 0x8007000B: Die angegebene Signaturhashmethode (SHA512) muss mit der Hashmethode übereinstimmen, die in der App-Paketblockzuordnung (SHA256) verwendet wird. | Der im /fd-Parameter angegebene hashAlgorithm ist falsch (siehe Schritt 1: Bestimmen des zu verwendende Hashalgorithmus). Erneutes Ausführen <a href="/windows-hardware/drivers/devtest/signtool"><strong>von SignTool</strong></a> mit hashAlgorithm, das der Blockzuordnung des App-Pakets entspricht. | 
| 152 | Error 0x8007000B: Der Inhalt des App-Pakets muss anhand seiner Blockzuordnung überprüft werden. | Das App-Paket ist beschädigt und muss neu erstellt werden, um eine neue Blockzuordnung zu generieren. Weitere Informationen zum Erstellen eines App-Pakets finden Sie unter Erstellen eines App-Pakets mit <a href="make-appx-package--makeappx-exe-.md">app packager</a> oder <a href="/previous-versions/hh975357(v=vs.110)">Erstellen eines App-Pakets mit Visual Studio 2012</a>. | 




 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Nachdem das Paket signiert wurde, muss das Zertifikat, das Sie zum Signieren des Pakets verwendet haben, weiterhin vom Computer, auf dem das Paket bereitgestellt werden soll, als vertrauenswürdig eingestuft werden. Durch Hinzufügen eines Zertifikats zum [Zertifikatspeicher des lokalen Computers](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)wirken Sie sich auf die Zertifikatvertrauensstellung aller Benutzer auf dem Computer aus. Es wird empfohlen, alle Codesignaturzertifikate, die Sie zum Testen von App-Paketen benötigen, im Zertifikatspeicher für vertrauenswürdige Personen zu installieren und diese Zertifikate sofort zu entfernen, wenn sie nicht mehr benötigt werden. Wenn Sie eigene Testzertifikate zum Signieren von App-Paketen erstellen, sollten Sie auch die Berechtigungen einschränken, die dem Testzertifikat zugeordnet sind. Weitere Informationen zum Erstellen von Testzertifikaten zum Signieren von App-Paketen finden Sie unter [Erstellen eines App-Paketsignaturzertifikats.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[Beispiel zum Erstellen eines App-Pakets](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Konzepte**
</dt> <dt>

[Bewährte Methoden für codesignieren](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Signieren eines Pakets in Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[App Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[So erstellst du ein App-Paketsignaturzertifikat](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

