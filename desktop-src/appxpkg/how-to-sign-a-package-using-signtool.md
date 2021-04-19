---
title: Signieren eines App-Pakets mithilfe von SignTool
description: Erfahren Sie, wie Sie mit SignTool Ihre Windows-App-Pakete signieren, damit Sie bereitgestellt werden können.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "106337687"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Signieren eines App-Pakets mithilfe von SignTool

> [!Note]  
> Informationen zum Signieren eines Windows-App-Pakets finden [Sie unter Signieren eines App-Pakets mit SignTool](/windows/msix/package/sign-app-package-using-signtool).

 

Erfahren Sie, wie Sie mit [**SignTool**](/windows-hardware/drivers/devtest/signtool) Ihre Windows-App-Pakete signieren, damit Sie bereitgestellt werden können. [**SignTool**](/windows-hardware/drivers/devtest/signtool) ist Teil des Windows Software Development Kit (SDK).

Alle Windows-App-Pakete müssen digital signiert werden, bevor Sie bereitgestellt werden können. Obwohl Microsoft Visual Studio 2012 und höher ein App-Paket während seiner Erstellung signieren können, sind Pakete, die Sie mit dem [App Packager-Tool (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) aus dem Windows SDK erstellen, nicht signiert.

> [!Note]  
> Sie können [**SignTool**](/windows-hardware/drivers/devtest/signtool) nur zum Signieren Ihrer Windows-App-Pakete unter Windows 8 und höher oder Windows Server 2012 und höher verwenden. Sie können **SignTool** nicht zum Signieren von App-Paketen auf Betriebssystemen unter Betriebssystemen wie Windows 7 oder Windows Server 2008 R2 verwenden.

 

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Tools zum Signieren von Dateien und Überprüfen von Signaturen](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Voraussetzungen

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), das Teil der Windows SDK
-   Ein gültiges Code Signaturzertifikat, z. b. eine PFX-Datei (Personal Information Exchange), die mit den [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) -und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Tools erstellt wurde.

    Informationen zum Erstellen eines gültigen Code Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).

-   Eine gepackte Windows-APP, z. b. eine AppX-Datei, die mit dem [App Packager-Tool (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) erstellt wurde

**Weitere Überlegungen**

Das Zertifikat, das Sie zum Signieren des App-Pakets verwenden, muss folgende Kriterien erfüllen:

-   Der Antragsteller Name des Zertifikats muss dem **Verleger** Attribut entsprechen, das im [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Element der AppxManifest.xml Datei enthalten ist, die im Paket gespeichert ist. Der Herausgeber Name ist Teil der Identität einer gepackten Windows-app. Daher müssen Sie den Antragsteller Namen des Zertifikats mit dem Namen des Herausgebers der APP vergleichen. Dadurch kann die Identität von signierten Paketen anhand der digitalen Signatur überprüft werden. Informationen zu Signatur Fehlern, die beim Signieren eines App-Pakets mithilfe von [**SignTool**](/windows-hardware/drivers/devtest/signtool)auftreten können, finden Sie im Abschnitt "Hinweise" unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).
-   Das Zertifikat muss für die Code Signatur gültig sein. Dies bedeutet, dass beide Elemente zutreffen müssen:

    -   Das EKU-Feld (Extended Key Usage) des Zertifikats muss entweder nicht festgelegt sein oder den EKU-Wert für die Code Signatur (1.3.6.1.5.5.7.3.3) enthalten.
    -   Das Feld "Schlüssel Verwendung" des Zertifikats muss entweder nicht festgelegt sein oder das Verwendungs Bit für die digitale Signatur (0x80) enthalten.

-   Das Zertifikat enthält einen privaten Schlüssel.
-   Das Zertifikat ist gültig. Es ist aktiv, nicht abgelaufen und wurde nicht widerrufen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Schritt 1: Bestimmen des zu verwendenden Hash Algorithmus

Wenn Sie das App-Paket signieren, müssen Sie denselben Hash Algorithmus verwenden, den Sie beim Erstellen des App-Pakets verwendet haben. Wenn Sie die Standardeinstellungen zum Erstellen des App-Pakets verwendet haben, lautet der verwendete Hash Algorithmus SHA256.

Wenn Sie den App-Packager mit einem bestimmten Hash Algorithmus verwendet haben, um das App-Paket zu erstellen, verwenden Sie den gleichen Algorithmus, um das Paket zu signieren. Um den Hash Algorithmus zu ermitteln, der zum Signieren eines Pakets verwendet werden soll, können Sie den Paket Inhalt extrahieren und die AppxBlockMap.xml Datei überprüfen. Das **hashmethod** -Attribut des [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) -Elements gibt den Hash Algorithmus an, der beim Erstellen des App-Pakets verwendet wurde. Beispiel:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

Das vorangehende [**Block Map**](/uwp/schemas/blockmapschema/element-blockmap) -Element gibt an, dass der SHA256-Algorithmus verwendet wurde. In dieser Tabelle ist die Zuordnung der derzeit verfügbaren Algorithmen aufgeführt:

| **Hashmethod** -Wert                            | zu verwendende *HashAlgorithm* |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (. AppX-Standard) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Schritt 2: Ausführen SignTool.exe zum Signieren des Pakets

**So signieren Sie das Paket mit einem Signaturzertifikat aus einer PFX-Datei**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) verwendet standardmäßig den Parameter/FD *HashAlgorithm* auf SHA1, wenn er nicht angegeben ist und SHA1 nicht für das Signieren von App-Paketen gültig ist. Daher müssen Sie diesen Parameter angeben, wenn Sie ein App-Paket signieren. Zum Signieren eines App-Pakets, das mit dem standardmäßigen SHA256-Hash erstellt wurde, geben Sie den/FD *HashAlgorithm* -Parameter als SHA256 an:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Sie können den Parameter "/p *Password* " weglassen, wenn Sie eine PFX-Datei verwenden, die nicht mit einem Kennwort geschützt ist. Sie können auch andere Optionen für die Zertifikat Auswahl verwenden, die von [**SignTool**](/windows-hardware/drivers/devtest/signtool) zum Signieren von App-Paketen unterstützt werden. Weitere Informationen zu diesen Optionen finden Sie unter [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> Der [**SignTool**](/windows-hardware/drivers/devtest/signtool) -Zeitstempel Vorgang kann nicht für ein signiertes App-Paket verwendet werden. der Vorgang wird nicht unterstützt.

 

Wenn Sie einen Zeitstempel für das App-Paket verwenden möchten, müssen Sie es während des Signierungs Vorgangs ausführen. Beispiel:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Legen Sie den/TR *timestampServerUrl* -Parameter der URL für einen RFC 3161-Zeitstempel Server entsprechend fest.

## <a name="remarks"></a>Bemerkungen

In diesem Abschnitt wird die Behandlung von Signatur Fehlern für App-Pakete erläutert.

### <a name="troubleshooting-app-package-signing-errors"></a>Problembehandlung bei App-Paket Signatur Fehlern

Zusätzlich zu den Signatur Fehlern, die [**SignTool**](/windows-hardware/drivers/devtest/signtool) zurückgeben kann, kann **SignTool** auch Fehler zurückgeben, die für das Signieren von App-Paketen spezifisch sind. Diese Fehler werden normalerweise als interne Fehler angezeigt:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Wenn der Fehlercode mit 0x8008 beginnt, z. b. 0x80080206 AppX \_ E beschädigte \_ \_ Inhalte), weist dies darauf hin, dass das signierte Paket ungültig ist. In diesem Fall müssen Sie das Paket neu erstellen, bevor Sie es signieren können. Die vollständige Liste der 0x8008- \* Fehler finden Sie unter [**com-Fehler Codes (Sicherheit und Setup)**](/windows/desktop/com/com-error-codes-4).

Im Allgemeinen ist der Fehler 0x8007000B (fehlerhaftes \_ \_ Format). In diesem Fall können Sie spezifischere Fehlerinformationen im Ereignisprotokoll finden:

**So durchsuchen Sie das Ereignisprotokoll**

1.  Führen Sie eventvwr. msc aus.
2.  Öffnen Sie das Ereignisprotokoll: Ereignisanzeige (local) > Anwendungs-und Dienst Protokolle > Microsoft > Windows > appxpackagingom > Microsoft-Windows-appxpackaging/Operational
3.  Suchen Sie nach dem letzten Fehler Ereignis.

Der interne Fehler entspricht in der Regel einer der folgenden:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Ereignis-ID</th>
<th>Beispiel Ereignis Zeichenfolge</th>
<th>Vorschlag</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>150</td>
<td>Fehler 0x8007000B: der Herausgeber Name des App-Manifests (CN = ca) muss mit dem Antragsteller Namen des Signatur Zertifikats (CN = C = US) identisch sein.</td>
<td>Der Herausgeber Name des App-Manifests muss exakt mit dem Antragsteller Namen der Signatur übereinstimmen.
<blockquote>
[!Note]<br />
Diese Namen werden in Anführungszeichen angegeben und sind sowohl Groß-/Kleinschreibung als auch Leerraum sensibel.
</blockquote>
<br/> Sie können die Attribut Zeichenfolge für den <strong>Verleger</strong> , die für das <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> -Element in der AppxManifest.xml-Datei definiert ist, so aktualisieren, dass Sie mit dem Antragsteller Namen des vorgesehenen Signatur Zertifikats Oder wählen Sie ein anderes Signaturzertifikat mit einem Antragsteller Namen aus, der dem Herausgeber Namen des App-Manifests entspricht. Der Name des Manifest-Verlegers und der Zertifikat Antragsteller Name werden in der Ereignismeldung aufgeführt.</td>
</tr>
<tr class="even">
<td>151</td>
<td>Fehler 0x8007000B: die angegebene Signatur Hash Methode (SHA512) muss mit der in der APP-Paket Block Zuordnung (SHA256) verwendeten Hash Methode identisch sein.</td>
<td>Der im/FD-Parameter angegebene HashAlgorithm ist falsch (siehe Schritt 1: Bestimmen des zu verwendenden Hash Algorithmus). Führen Sie <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> erneut mit dem HashAlgorithm aus, der mit der APP-Paket Block Zuordnung übereinstimmt.</td>
</tr>
<tr class="odd">
<td>152</td>
<td>Fehler 0x8007000B: der Inhalt des App-Pakets muss anhand seiner Block Zuordnung überprüft werden.</td>
<td>Das App-Paket ist beschädigt und muss neu erstellt werden, um eine neue Block Zuordnung zu generieren. Weitere Informationen zum Erstellen eines App-Pakets finden Sie unter Erstellen eines App-Pakets mit <a href="make-appx-package--makeappx-exe-.md">App Packager</a> oder <a href="/previous-versions/hh975357(v=vs.110)">Erstellen eines App-Pakets mit Visual Studio 2012</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Nachdem das Paket signiert wurde, muss das Zertifikat, das Sie zum Signieren des Pakets verwendet haben, weiterhin von dem Computer als vertrauenswürdig eingestuft werden, auf dem das Paket bereitgestellt werden soll. Wenn Sie einem Zertifikat [Speicher des lokalen](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)Computers ein Zertifikat hinzufügen, haben Sie Auswirkungen auf die Zertifikats Vertrauensstellung aller Benutzer auf dem Computer. Es wird empfohlen, dass Sie alle Code Signatur Zertifikate installieren, die Sie zum Testen von App-Paketen im Zertifikat Speicher für vertrauenswürdige Personen benötigen, und diese Zertifikate unverzüglich entfernen, wenn Sie nicht mehr benötigt werden. Wenn Sie eigene Test Zertifikate zum Signieren von App-Paketen erstellen, empfiehlt es sich auch, die dem Test Zertifikat zugeordneten Berechtigungen einzuschränken. Weitere Informationen zum Erstellen von Test Zertifikaten zum Signieren von App-Paketen finden [Sie unter Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[App-Paket erstellen (Beispiel)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Konzepte**
</dt> <dt>

[Bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Signieren eines Pakets in Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[App-Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[So erstellst du ein App-Paketsignaturzertifikat](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

