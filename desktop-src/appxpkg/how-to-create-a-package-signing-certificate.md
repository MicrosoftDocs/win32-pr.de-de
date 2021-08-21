---
title: How to create an app package signing certificate (So erstellen Sie ein App-Paketsignaturzertifikat)
description: Erfahren Sie, wie Sie MakeCert.exe und Pvk2Pfx.exe verwenden, um ein Testcodesignaturzertifikat zu erstellen, damit Sie Ihre Windows signieren können.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc495c27e63dc4ee3a42db1b2763f4f59f7647a3a98d20193d8049dcfad965c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049068"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>How to create an app package signing certificate (So erstellen Sie ein App-Paketsignaturzertifikat)

> [!IMPORTANT]
> MakeCert.exe ist veraltet. Aktuelle Anleitungen zum Erstellen eines Zertifikats finden Sie unter [Erstellen eines Zertifikats für die Paketsignatur.](/windows/msix/package/create-certificate-package-signing)

 

Erfahren Sie, [**wie**](/windows-hardware/drivers/devtest/makecert)MakeCert.exe [**und**](/windows-hardware/drivers/devtest/pvk2pfx)Pvk2Pfx.exeverwenden, um ein Testcodesignaturzertifikat zu erstellen, damit Sie Ihre Windows signieren können.

Sie müssen Ihre gepackten Apps Windows signieren, bevor Sie sie bereitstellen. Wenn Sie nicht Microsoft Visual Studio 2012 verwenden, um Ihre App-Pakete zu erstellen und zu signieren, müssen Sie Ihre eigenen Codesignaturzertifikate erstellen und verwalten. Sie können Zertifikate mithilfe von [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) [**und**](/windows-hardware/drivers/devtest/pvk2pfx)Pvk2Pfx.exeaus dem Windows Driver Kit (WDK) erstellen. Anschließend können Sie die Zertifikate verwenden, um die App-Pakete zu signieren, damit sie lokal zum Testen bereitgestellt werden können.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [App-Pakete und Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Tools zum Signieren von Treibern](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Voraussetzungen

-   [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Tools aus dem WDK

## <a name="instructions"></a>Anweisungen

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Schritt 1: Bestimmen des Herausgebernamens des Pakets

Damit das Signaturzertifikat, das Sie erstellen, mit dem App-Paket verwendet werden kann, das Sie signieren möchten, muss der Betreffname des Signaturzertifikats mit dem **Publisher-Attribut** des [**Identity-Elements**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) in der AppxManifest.xml für diese App übereinstimmen. Angenommen, die AppxManifest.xml enthält Folgendes:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Verwenden Sie für den *parameter publisherName,* den Sie im nächsten Schritt mit dem [**MakeCert-Hilfsprogramm**](/windows-hardware/drivers/devtest/makecert) angeben, "CN=Contoso Software, O=Contoso Corporation, C=US".

> [!Note]  
> Diese Parameterzeichenfolge wird in Anführungszeichen angegeben und berücksichtigt sowohl Die Kleinschreibung als auch Leerzeichen.

 

Die **Publisher** Attributzeichenfolge, die für das [**Identity-Element**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) in der AppxManifest.xml definiert ist, muss mit der Zeichenfolge identisch sein, die Sie mit dem [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n-Parameter für den Zertifikatsubjektnamen angeben. Kopieren Sie die Zeichenfolge, und fügen Sie sie nach Möglichkeit ein.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Schritt 2: Erstellen eines privaten Schlüssels mit MakeCert.exe

Verwenden Sie [**das Hilfsprogramm MakeCert,**](/windows-hardware/drivers/devtest/makecert) um ein selbstsigniertes Testzertifikat und einen privaten Schlüssel zu erstellen:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Mit diesem Befehl werden Sie aufgefordert, ein Kennwort für die PVK-Datei einzugeben. Es wird empfohlen, ein sicheres [Kennwort zu wählen](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) und Ihren privaten Schlüssel an einem sicheren Ort zu speichern.

Es wird empfohlen, die vorgeschlagenen Parameter im vorherigen Beispiel aus den folgenden Gründen zu verwenden:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Erstellt ein selbstsigniertes Stammzertifikat. Dies vereinfacht die Verwaltung ihres Testzertifikats.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Markiert die grundlegende Einschränkung für das Zertifikat als Endentität. Dadurch wird verhindert, dass das Zertifikat als Zertifizierungsstelle verwendet wird, die andere Zertifikate aushing.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Legt die Werte der erweiterten Schlüsselverwendung (Enhanced Key Usage, EKU) für das Zertifikat fest.

> [!Note]  
> Legen Sie kein Leerzeichen zwischen den beiden durch Trennzeichen getrennten Werten ab.

 

-   1.3.6.1.5.5.7.3.3 gibt an, dass das Zertifikat für die Codesignatur gültig ist. Geben Sie diesen Wert immer an, um die beabsichtigte Verwendung für das Zertifikat zu beschränken.
-   1.3.6.1.4.1.311.10.3.13 gibt an, dass das Zertifikat die Lebensdauersignatur beachtet. Wenn eine Signatur mit einem Zeitstempel versehen ist, bleibt die Signatur in der Regel gültig, solange das Zertifikat zum Zeitpunkt der Zeitstempelung gültig war. Dies gilt auch, wenn das Zertifikat abläuft. Diese EKU erzwingt, dass die Signatur abläuft, unabhängig davon, ob die Signatur mit einem Zeitstempel versehen ist.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Legt das Ablaufdatum des Zertifikats fest. Geben Sie einen Wert für *den expirationDate-Parameter* im Format mm/tt/yyyy an. Es wird empfohlen, ein Ablaufdatum nur so lange zu wählen, wie es für Ihre Testzwecke erforderlich ist, in der Regel weniger als ein Jahr. Dieses Ablaufdatum in Verbindung mit der Lebensdauersignatur-EKU kann dabei helfen, das Fenster zu begrenzen, in dem das Zertifikat kompromittiert und missbraucht werden kann.

</dd> </dl>

Weitere Informationen zu anderen Optionen finden Sie unter [**MakeCert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Schritt 3: Erstellen einer PFX-Datei (Personal Information Exchange) mit Pvk2Pfx.exe

Verwenden Sie [**das Hilfsprogramm Pvk2Pfx,**](/windows-hardware/drivers/devtest/pvk2pfx) um die PVK- und CER-Dateien, die [**von MakeCert**](/windows-hardware/drivers/devtest/makecert) erstellt wurden, in eine PFX-Datei zu konvertieren, die Sie mit [SignTool](/windows/desktop/SecCrypto/signtool) zum Signieren eines App-Pakets verwenden können:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Die *Dateien MyKey.pvk* und *MyKey.cer* sind dieselben Dateien, [**dieMakeCert.exe**](/windows-hardware/drivers/devtest/makecert) vorherigen Schritt erstellt wurden. Mithilfe des optionalen /po-Parameters können Sie ein anderes Kennwort für die resultierende PFX-Datei angeben. Andernfalls hat die PFX-Datei das gleiche Kennwort wie *MyKey.pvk.*

Weitere Informationen zu anderen Optionen finden Sie unter [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Hinweise

Nachdem Sie die PFX-Datei erstellt haben, können Sie die Datei mit [SignTool verwenden,](/windows/desktop/SecCrypto/signtool) um ein App-Paket zu signieren. Weitere Informationen finden Sie unter [SignTool zum Signieren eines App-Pakets.](how-to-sign-a-package-using-signtool.md) Das Zertifikat wird jedoch vom lokalen Computer für die Bereitstellung von App-Paketen immer noch nicht als vertrauenswürdig eingestuft, bis Sie es im Speicher für vertrauenswürdige Zertifikate des lokalen Computers installieren. Sie können [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))verwenden, das im Windows.

**So installieren Sie Zertifikate mit WindowsCertutil.exe**

1.  Führen **Cmd.exe** als Administrator aus.
2.  Führen Sie den folgenden Befehl aus:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Es wird empfohlen, die Zertifikate zu entfernen, wenn sie nicht mehr verwendet werden. Führen Sie an derselben Administratorbefehlsaufforderung den folgenden Befehl aus:

``` syntax
Certutil -delStore TrustedPeople certID
```

Die **certID** ist die Seriennummer des Zertifikats. Führen Sie den folgenden Befehl aus, um die Seriennummer des Zertifikats zu ermitteln:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Durch das Hinzufügen eines Zertifikats [zu zertifikatspeichern](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)auf dem lokalen Computer wirken Sie sich auf die Zertifikatvertrauensstellung aller Benutzer auf dem Computer aus. Es wird empfohlen, alle Codesignaturzertifikate, die Sie zum Testen von App-Paketen wünschen, im Zertifikatspeicher für vertrauenswürdige Personen zu installieren. Entfernen Sie diese Zertifikate umgehend, wenn sie nicht mehr benötigt werden, um zu verhindern, dass sie verwendet werden, um die Systemvertrauensstellung zu gefährden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[Beispiel zum Erstellen eines App-Pakets](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Konzepte**
</dt> <dt>

[Bewährte Methoden für die Codesignatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Signieren eines App-Pakets](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 