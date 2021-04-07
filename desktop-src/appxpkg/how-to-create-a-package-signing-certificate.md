---
title: How to create an app package signing certificate (So erstellen Sie ein App-Paketsignaturzertifikat)
description: Erfahren Sie, wie Sie mit MakeCert.exe und Pvk2Pfx.exe ein Test Code Signaturzertifikat erstellen, damit Sie Ihre Windows-App-Pakete signieren können.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038814"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>How to create an app package signing certificate (So erstellen Sie ein App-Paketsignaturzertifikat)

> [!IMPORTANT]
> MakeCert.exe ist veraltet. Aktuelle Anleitungen zum Erstellen eines Zertifikats finden Sie unter [Erstellen eines Zertifikats für die Paket Signierung](/windows/msix/package/create-certificate-package-signing).

 

Erfahren Sie, wie Sie mit [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) ein Test Code Signaturzertifikat erstellen, damit Sie Ihre Windows-App-Pakete signieren können.

Sie müssen ihre gepackten Windows-apps digital signieren, bevor Sie Sie bereitstellen. Wenn Sie nicht Microsoft Visual Studio 2012 verwenden, um Ihre APP-Pakete zu erstellen und zu signieren, müssen Sie Ihre eigenen Code Signatur Zertifikate erstellen und verwalten. Zertifikate können mithilfe von [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) aus dem Windows-Treiberkit (WDK) erstellt werden. Anschließend können Sie die Zertifikate zum Signieren der APP-Pakete verwenden, sodass Sie lokal zum Testen bereitgestellt werden können.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Tools zum Signieren von Treibern](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Voraussetzungen

-   [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Tools aus dem WDK

## <a name="instructions"></a>Anweisungen

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Schritt 1: Bestimmen des Herausgeber namens des Pakets

Damit das Signaturzertifikat, das Sie erstellen, für das App-Paket, das Sie signieren möchten, verwendbar ist, muss der Antragsteller Name des Signatur Zertifikats mit dem **Publisher** -Attribut des [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Elements im AppxManifest.xml für die betreffende App identisch sein. Nehmen Sie beispielsweise an, dass die AppxManifest.xml Folgendes enthält:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Verwenden Sie für den *PublisherName* -Parameter, den Sie im nächsten Schritt mit dem Hilfsprogramm [**Makecert**](/windows-hardware/drivers/devtest/makecert) angeben, "CN = conjeso Software, O = conjeso Corporation, C = US".

> [!Note]  
> Diese Parameter Zeichenfolge wird in Anführungszeichen angegeben und ist sowohl groß-als auch Leerzeichen.

 

Die Attribut Zeichenfolge für den **Verleger** , die für das [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Element in der AppxManifest.xml definiert ist, muss mit der Zeichenfolge identisch sein, die Sie mit dem [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n-Parameter für den Zertifikat Antragsteller Namen angeben. Kopieren Sie die Zeichenfolge, und fügen Sie Sie ein.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Schritt 2: Erstellen eines privaten Schlüssels mit MakeCert.exe

Verwenden Sie das Hilfsprogramm [**Makecert**](/windows-hardware/drivers/devtest/makecert) , um ein selbst signiertes Test Zertifikat und einen privaten Schlüssel zu erstellen:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Mit diesem Befehl werden Sie aufgefordert, ein Kennwort für die PVK-Datei anzugeben. Es wird empfohlen, dass Sie ein sicheres [Kennwort](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) auswählen und den privaten Schlüssel an einem sicheren Ort aufbewahren.

Aus folgenden Gründen wird empfohlen, die vorgeschlagenen Parameter aus dem vorangehenden Beispiel zu verwenden:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Erstellt ein selbst signiertes Stamm Zertifikat. Dies vereinfacht die Verwaltung Ihres Test Zertifikats.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Markiert die grundlegende Einschränkung für das Zertifikat als Endentität. Dadurch wird verhindert, dass das Zertifikat als Zertifizierungsstelle (Certification Authority, ca) verwendet wird, die andere Zertifikate ausstellen kann.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Legt die EKU-Werte (Enhanced Key Usage) für das Zertifikat fest.

> [!Note]  
> Platzieren Sie keinen Leerraum zwischen den beiden durch Trennzeichen getrennten Werten.

 

-   1.3.6.1.5.5.7.3.3 gibt an, dass das Zertifikat zum Signieren von Code gültig ist. Geben Sie diesen Wert immer an, um die beabsichtigte Verwendung des Zertifikats einzuschränken.
-   1.3.6.1.4.1.311.10.3.13 gibt an, dass das Zertifikat die Lebensdauer Signierung respektiert. Wenn eine Signatur mit einem Zeitstempel versehen ist, bleibt die Signatur in der Regel gültig, auch wenn das Zertifikat zum Zeitpunkt des Zeitstempels gültig war. Diese EKU erzwingt, dass die Signatur abläuft, unabhängig davon, ob die Signatur Zeitstempel ist.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Legt das Ablaufdatum des Zertifikats fest. Geben Sie einen Wert für den *ExpirationDate* -Parameter im Format mm/dd/yyyy an. Es wird empfohlen, dass Sie ein Ablaufdatum nur so lange auswählen, wie es für Ihre Testzwecke erforderlich ist (in der Regel weniger als ein Jahr). Dieses Ablaufdatum in Verbindung mit der Lebensdauer Signatur-EKU kann helfen, das Fenster einzuschränken, in dem das Zertifikat kompromittiert und missbraucht werden kann.

</dd> </dl>

Weitere Informationen zu anderen Optionen finden Sie unter [**Makecert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Schritt 3: Erstellen einer PFX-Datei (Personal Information Exchange) mithilfe Pvk2Pfx.exe

Verwenden Sie das Hilfsprogramm [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) , um die PVK-und CER-Dateien, die [**Makecert**](/windows-hardware/drivers/devtest/makecert) erstellt hat, in eine PFX-Datei zu konvertieren, die Sie mit [SignTool](/windows/desktop/SecCrypto/signtool) zum Signieren eines App-Pakets verwenden können:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Die Dateien *myKey. pvk* und *myKey. CER* sind dieselben Dateien, die [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) im vorherigen Schritt erstellt haben. Wenn Sie den optionalen/po-Parameter verwenden, können Sie ein anderes Kennwort für die resultierende PFX-Dateien angeben. Andernfalls hat die PFX-Datei das gleiche Kennwort wie *myKey. pvk*.

Weitere Informationen zu anderen Optionen finden Sie unter [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Bemerkungen

Nachdem Sie die PFX-Datei erstellt haben, können Sie die Datei mit [SignTool](/windows/desktop/SecCrypto/signtool) verwenden, um ein App-Paket zu signieren. Weitere Informationen finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md). Das Zertifikat wird jedoch immer noch vom lokalen Computer für die Bereitstellung von App-Paketen als vertrauenswürdig eingestuft, bis Sie es im Speicher für vertrauenswürdige Zertifikate auf dem lokalen Computer installieren. Sie können [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))verwenden, die in Windows verfügbar ist.

**So installieren Sie Zertifikate mit WindowsCertutil.exe**

1.  Führen Sie **Cmd.exe** als Administrator aus.
2.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Es wird empfohlen, die Zertifikate zu entfernen, wenn Sie nicht mehr verwendet werden. Führen Sie an derselben Administrator Eingabeaufforderung den folgenden Befehl aus:

``` syntax
Certutil -delStore TrustedPeople certID
```

Die **CertID** ist die Seriennummer des Zertifikats. Führen Sie diesen Befehl aus, um die Seriennummer des Zertifikats zu bestimmen:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Wenn Sie einem Zertifikat [Speicher des lokalen](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)Computers ein Zertifikat hinzufügen, haben Sie Auswirkungen auf die Zertifikats Vertrauensstellung aller Benutzer auf dem Computer. Es wird empfohlen, dass Sie alle Code Signatur Zertifikate installieren, die Sie zum Testen von App-Paketen im Zertifikat Speicher für vertrauenswürdige Personen benötigen. Entfernen Sie diese Zertifikate unverzüglich, wenn Sie nicht mehr benötigt werden, um zu verhindern, dass Sie zur Gefährdung der System Vertrauensstellung verwendet werden.

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

[Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Signieren eines App-Pakets](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 