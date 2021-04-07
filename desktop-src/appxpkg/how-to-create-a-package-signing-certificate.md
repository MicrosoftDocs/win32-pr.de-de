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
# <a name="how-to-create-an-app-package-signing-certificate"></a><span data-ttu-id="6544e-103">How to create an app package signing certificate (So erstellen Sie ein App-Paketsignaturzertifikat)</span><span class="sxs-lookup"><span data-stu-id="6544e-103">How to create an app package signing certificate</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6544e-104">MakeCert.exe ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="6544e-104">MakeCert.exe is deprecated.</span></span> <span data-ttu-id="6544e-105">Aktuelle Anleitungen zum Erstellen eines Zertifikats finden Sie unter [Erstellen eines Zertifikats für die Paket Signierung](/windows/msix/package/create-certificate-package-signing).</span><span class="sxs-lookup"><span data-stu-id="6544e-105">For current guidance on creating a certificate, see [Create a certificate for package signing](/windows/msix/package/create-certificate-package-signing).</span></span>

 

<span data-ttu-id="6544e-106">Erfahren Sie, wie Sie mit [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) ein Test Code Signaturzertifikat erstellen, damit Sie Ihre Windows-App-Pakete signieren können.</span><span class="sxs-lookup"><span data-stu-id="6544e-106">Learn how to use [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your Windows app packages.</span></span>

<span data-ttu-id="6544e-107">Sie müssen ihre gepackten Windows-apps digital signieren, bevor Sie Sie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6544e-107">You must digitally sign your packaged Windows apps before you deploy them.</span></span> <span data-ttu-id="6544e-108">Wenn Sie nicht Microsoft Visual Studio 2012 verwenden, um Ihre APP-Pakete zu erstellen und zu signieren, müssen Sie Ihre eigenen Code Signatur Zertifikate erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="6544e-108">If you don't use Microsoft Visual Studio 2012 to create and sign your app packages, you need to create and manage your own code signing certificates.</span></span> <span data-ttu-id="6544e-109">Zertifikate können mithilfe von [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) aus dem Windows-Treiberkit (WDK) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6544e-109">You can create certificates by using [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) from the Windows Driver Kit (WDK).</span></span> <span data-ttu-id="6544e-110">Anschließend können Sie die Zertifikate zum Signieren der APP-Pakete verwenden, sodass Sie lokal zum Testen bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="6544e-110">Then you can use the certificates to sign the app packages, so they can be deployed locally for testing.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6544e-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="6544e-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6544e-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="6544e-112">Technologies</span></span>

-   <span data-ttu-id="6544e-113">[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6544e-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="6544e-114">[App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="6544e-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="6544e-115">Tools zum Signieren von Treibern</span><span class="sxs-lookup"><span data-stu-id="6544e-115">Tools for Signing Drivers</span></span>](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a><span data-ttu-id="6544e-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="6544e-116">Prerequisites</span></span>

-   <span data-ttu-id="6544e-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Tools aus dem WDK</span><span class="sxs-lookup"><span data-stu-id="6544e-117">[**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools from the WDK</span></span>

## <a name="instructions"></a><span data-ttu-id="6544e-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6544e-118">Instructions</span></span>

### <a name="step-1-determine-the-publisher-name-of-the-package"></a><span data-ttu-id="6544e-119">Schritt 1: Bestimmen des Herausgeber namens des Pakets</span><span class="sxs-lookup"><span data-stu-id="6544e-119">Step 1: Determine the publisher name of the package</span></span>

<span data-ttu-id="6544e-120">Damit das Signaturzertifikat, das Sie erstellen, für das App-Paket, das Sie signieren möchten, verwendbar ist, muss der Antragsteller Name des Signatur Zertifikats mit dem **Publisher** -Attribut des [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Elements im AppxManifest.xml für die betreffende App identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6544e-120">To make the signing certificate that you create usable with the app package that you want to sign, the subject name of the signing certificate must match the **Publisher** attribute of the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml for that app.</span></span> <span data-ttu-id="6544e-121">Nehmen Sie beispielsweise an, dass die AppxManifest.xml Folgendes enthält:</span><span class="sxs-lookup"><span data-stu-id="6544e-121">For example, suppose the AppxManifest.xml contains:</span></span>

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

<span data-ttu-id="6544e-122">Verwenden Sie für den *PublisherName* -Parameter, den Sie im nächsten Schritt mit dem Hilfsprogramm [**Makecert**](/windows-hardware/drivers/devtest/makecert) angeben, "CN = conjeso Software, O = conjeso Corporation, C = US".</span><span class="sxs-lookup"><span data-stu-id="6544e-122">For the *publisherName* parameter that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility in the next step, use "CN=Contoso Software, O=Contoso Corporation, C=US".</span></span>

> [!Note]  
> <span data-ttu-id="6544e-123">Diese Parameter Zeichenfolge wird in Anführungszeichen angegeben und ist sowohl groß-als auch Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6544e-123">This parameter string is specified in quotes and is both case and whitespace sensitive.</span></span>

 

<span data-ttu-id="6544e-124">Die Attribut Zeichenfolge für den **Verleger** , die für das [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Element in der AppxManifest.xml definiert ist, muss mit der Zeichenfolge identisch sein, die Sie mit dem [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n-Parameter für den Zertifikat Antragsteller Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="6544e-124">The **Publisher** attribute string that is defined for the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the AppxManifest.xml must be identical to the string that you specify with the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n parameter for the certificate subject name.</span></span> <span data-ttu-id="6544e-125">Kopieren Sie die Zeichenfolge, und fügen Sie Sie ein.</span><span class="sxs-lookup"><span data-stu-id="6544e-125">Copy and paste the string where possible.</span></span>

### <a name="step-2-create-a-private-key-using-makecertexe"></a><span data-ttu-id="6544e-126">Schritt 2: Erstellen eines privaten Schlüssels mit MakeCert.exe</span><span class="sxs-lookup"><span data-stu-id="6544e-126">Step 2: Create a private key using MakeCert.exe</span></span>

<span data-ttu-id="6544e-127">Verwenden Sie das Hilfsprogramm [**Makecert**](/windows-hardware/drivers/devtest/makecert) , um ein selbst signiertes Test Zertifikat und einen privaten Schlüssel zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="6544e-127">Use the [**MakeCert**](/windows-hardware/drivers/devtest/makecert) utility to create a self-signed test certificate and private key:</span></span>

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

<span data-ttu-id="6544e-128">Mit diesem Befehl werden Sie aufgefordert, ein Kennwort für die PVK-Datei anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6544e-128">This command prompts you to provide a password for the .pvk file.</span></span> <span data-ttu-id="6544e-129">Es wird empfohlen, dass Sie ein sicheres [Kennwort](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) auswählen und den privaten Schlüssel an einem sicheren Ort aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="6544e-129">We recommend that you choose a [strong password](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) and keep your private key in a secure location.</span></span>

<span data-ttu-id="6544e-130">Aus folgenden Gründen wird empfohlen, die vorgeschlagenen Parameter aus dem vorangehenden Beispiel zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="6544e-130">We recommend that you use the suggested parameters in the preceding example for these reasons:</span></span>

<dl> <dt>

<span data-ttu-id="6544e-131"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="6544e-131"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="6544e-132">Erstellt ein selbst signiertes Stamm Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="6544e-132">Creates a self-signed root certificate.</span></span> <span data-ttu-id="6544e-133">Dies vereinfacht die Verwaltung Ihres Test Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="6544e-133">This simplifies management for your test certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6544e-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span><span class="sxs-lookup"><span data-stu-id="6544e-134"><span id="_h_0"></span><span id="_H_0"></span>**/h 0**</span></span>
</dt> <dd>

<span data-ttu-id="6544e-135">Markiert die grundlegende Einschränkung für das Zertifikat als Endentität.</span><span class="sxs-lookup"><span data-stu-id="6544e-135">Marks the basic constraint for the certificate as an end-entity.</span></span> <span data-ttu-id="6544e-136">Dadurch wird verhindert, dass das Zertifikat als Zertifizierungsstelle (Certification Authority, ca) verwendet wird, die andere Zertifikate ausstellen kann.</span><span class="sxs-lookup"><span data-stu-id="6544e-136">This prevents the certificate from being used as a Certification Authority (CA) that can issue other certificates.</span></span>

</dd> <dt>

<span data-ttu-id="6544e-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span><span class="sxs-lookup"><span data-stu-id="6544e-137"><span id="_eku"></span><span id="_EKU"></span>**/eku**</span></span>
</dt> <dd>

<span data-ttu-id="6544e-138">Legt die EKU-Werte (Enhanced Key Usage) für das Zertifikat fest.</span><span class="sxs-lookup"><span data-stu-id="6544e-138">Sets the Enhanced Key Usage (EKU) values for the certificate.</span></span>

> [!Note]  
> <span data-ttu-id="6544e-139">Platzieren Sie keinen Leerraum zwischen den beiden durch Trennzeichen getrennten Werten.</span><span class="sxs-lookup"><span data-stu-id="6544e-139">Don't put a space between the two comma-delimited values.</span></span>

 

-   <span data-ttu-id="6544e-140">1.3.6.1.5.5.7.3.3 gibt an, dass das Zertifikat zum Signieren von Code gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6544e-140">1.3.6.1.5.5.7.3.3 indicates that the certificate is valid for code signing.</span></span> <span data-ttu-id="6544e-141">Geben Sie diesen Wert immer an, um die beabsichtigte Verwendung des Zertifikats einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="6544e-141">Always specify this value to limit the intended use for the certificate.</span></span>
-   <span data-ttu-id="6544e-142">1.3.6.1.4.1.311.10.3.13 gibt an, dass das Zertifikat die Lebensdauer Signierung respektiert.</span><span class="sxs-lookup"><span data-stu-id="6544e-142">1.3.6.1.4.1.311.10.3.13 indicates that the certificate respects lifetime signing.</span></span> <span data-ttu-id="6544e-143">Wenn eine Signatur mit einem Zeitstempel versehen ist, bleibt die Signatur in der Regel gültig, auch wenn das Zertifikat zum Zeitpunkt des Zeitstempels gültig war.</span><span class="sxs-lookup"><span data-stu-id="6544e-143">Typically, if a signature is time stamped, as long as the certificate was valid at the point when it was time stamped, the signature remains valid even if the certificate expires.</span></span> <span data-ttu-id="6544e-144">Diese EKU erzwingt, dass die Signatur abläuft, unabhängig davon, ob die Signatur Zeitstempel ist.</span><span class="sxs-lookup"><span data-stu-id="6544e-144">This EKU forces the signature to expire regardless of whether the signature is time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="6544e-145"><span id="_e"></span><span id="_E"></span>**/e**</span><span class="sxs-lookup"><span data-stu-id="6544e-145"><span id="_e"></span><span id="_E"></span>**/e**</span></span>
</dt> <dd>

<span data-ttu-id="6544e-146">Legt das Ablaufdatum des Zertifikats fest.</span><span class="sxs-lookup"><span data-stu-id="6544e-146">Sets the expiration date of the certificate.</span></span> <span data-ttu-id="6544e-147">Geben Sie einen Wert für den *ExpirationDate* -Parameter im Format mm/dd/yyyy an.</span><span class="sxs-lookup"><span data-stu-id="6544e-147">Provide a value for the *expirationDate* parameter in the mm/dd/yyyy format.</span></span> <span data-ttu-id="6544e-148">Es wird empfohlen, dass Sie ein Ablaufdatum nur so lange auswählen, wie es für Ihre Testzwecke erforderlich ist (in der Regel weniger als ein Jahr).</span><span class="sxs-lookup"><span data-stu-id="6544e-148">We recommend that you choose an expiration date only as long as necessary for your testing purposes, typically less than a year.</span></span> <span data-ttu-id="6544e-149">Dieses Ablaufdatum in Verbindung mit der Lebensdauer Signatur-EKU kann helfen, das Fenster einzuschränken, in dem das Zertifikat kompromittiert und missbraucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="6544e-149">This expiration date in conjunction with the lifetime signing EKU can help to limit the window in which the certificate can be compromised and misused.</span></span>

</dd> </dl>

<span data-ttu-id="6544e-150">Weitere Informationen zu anderen Optionen finden Sie unter [**Makecert**](/windows-hardware/drivers/devtest/makecert).</span><span class="sxs-lookup"><span data-stu-id="6544e-150">For more info about other options, see [**MakeCert**](/windows-hardware/drivers/devtest/makecert).</span></span>

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a><span data-ttu-id="6544e-151">Schritt 3: Erstellen einer PFX-Datei (Personal Information Exchange) mithilfe Pvk2Pfx.exe</span><span class="sxs-lookup"><span data-stu-id="6544e-151">Step 3: Create a Personal Information Exchange (.pfx) file using Pvk2Pfx.exe</span></span>

<span data-ttu-id="6544e-152">Verwenden Sie das Hilfsprogramm [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) , um die PVK-und CER-Dateien, die [**Makecert**](/windows-hardware/drivers/devtest/makecert) erstellt hat, in eine PFX-Datei zu konvertieren, die Sie mit [SignTool](/windows/desktop/SecCrypto/signtool) zum Signieren eines App-Pakets verwenden können:</span><span class="sxs-lookup"><span data-stu-id="6544e-152">Use the [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) utility to convert the .pvk and .cer files that [**MakeCert**](/windows-hardware/drivers/devtest/makecert) created to a .pfx file that you can use with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package:</span></span>

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

<span data-ttu-id="6544e-153">Die Dateien *myKey. pvk* und *myKey. CER* sind dieselben Dateien, die [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="6544e-153">The *MyKey.pvk* and *MyKey.cer* files are the same files that [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) created in the previous step.</span></span> <span data-ttu-id="6544e-154">Wenn Sie den optionalen/po-Parameter verwenden, können Sie ein anderes Kennwort für die resultierende PFX-Dateien angeben. Andernfalls hat die PFX-Datei das gleiche Kennwort wie *myKey. pvk*.</span><span class="sxs-lookup"><span data-stu-id="6544e-154">By using the optional /po parameter, you can specify a different password for the resulting .pfx; otherwise, the .pfx has the same password as *MyKey.pvk*.</span></span>

<span data-ttu-id="6544e-155">Weitere Informationen zu anderen Optionen finden Sie unter [**Pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span><span class="sxs-lookup"><span data-stu-id="6544e-155">For more info about other options, see [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).</span></span>

## <a name="remarks"></a><span data-ttu-id="6544e-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6544e-156">Remarks</span></span>

<span data-ttu-id="6544e-157">Nachdem Sie die PFX-Datei erstellt haben, können Sie die Datei mit [SignTool](/windows/desktop/SecCrypto/signtool) verwenden, um ein App-Paket zu signieren.</span><span class="sxs-lookup"><span data-stu-id="6544e-157">After you create the .pfx file, you can use the file with [SignTool](/windows/desktop/SecCrypto/signtool) to sign an app package.</span></span> <span data-ttu-id="6544e-158">Weitere Informationen finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="6544e-158">For more info, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="6544e-159">Das Zertifikat wird jedoch immer noch vom lokalen Computer für die Bereitstellung von App-Paketen als vertrauenswürdig eingestuft, bis Sie es im Speicher für vertrauenswürdige Zertifikate auf dem lokalen Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="6544e-159">But the certificate is still not trusted by the local computer for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="6544e-160">Sie können [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10))verwenden, die in Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="6544e-160">You can use [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), which comes with Windows.</span></span>

<span data-ttu-id="6544e-161">**So installieren Sie Zertifikate mit WindowsCertutil.exe**</span><span class="sxs-lookup"><span data-stu-id="6544e-161">**To install certificates with WindowsCertutil.exe**</span></span>

1.  <span data-ttu-id="6544e-162">Führen Sie **Cmd.exe** als Administrator aus.</span><span class="sxs-lookup"><span data-stu-id="6544e-162">Run **Cmd.exe** as administrator.</span></span>
2.  <span data-ttu-id="6544e-163">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="6544e-163">Run this command:</span></span>

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

<span data-ttu-id="6544e-164">Es wird empfohlen, die Zertifikate zu entfernen, wenn Sie nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6544e-164">We recommend that you remove the certificates if they are no longer in use.</span></span> <span data-ttu-id="6544e-165">Führen Sie an derselben Administrator Eingabeaufforderung den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="6544e-165">From the same administrator command prompt, run this command:</span></span>

``` syntax
Certutil -delStore TrustedPeople certID
```

<span data-ttu-id="6544e-166">Die **CertID** ist die Seriennummer des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="6544e-166">The **certID** is the serial number of the certificate.</span></span> <span data-ttu-id="6544e-167">Führen Sie diesen Befehl aus, um die Seriennummer des Zertifikats zu bestimmen:</span><span class="sxs-lookup"><span data-stu-id="6544e-167">Run this command to determine the certificate serial number:</span></span>

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a><span data-ttu-id="6544e-168">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="6544e-168">Security Considerations</span></span>

<span data-ttu-id="6544e-169">Wenn Sie einem Zertifikat [Speicher des lokalen](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)Computers ein Zertifikat hinzufügen, haben Sie Auswirkungen auf die Zertifikats Vertrauensstellung aller Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="6544e-169">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="6544e-170">Es wird empfohlen, dass Sie alle Code Signatur Zertifikate installieren, die Sie zum Testen von App-Paketen im Zertifikat Speicher für vertrauenswürdige Personen benötigen.</span><span class="sxs-lookup"><span data-stu-id="6544e-170">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store.</span></span> <span data-ttu-id="6544e-171">Entfernen Sie diese Zertifikate unverzüglich, wenn Sie nicht mehr benötigt werden, um zu verhindern, dass Sie zur Gefährdung der System Vertrauensstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6544e-171">Promptly remove those certificates when they are no longer necessary, to prevent them from being used to compromise system trust.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6544e-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6544e-172">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6544e-173">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="6544e-173">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="6544e-174">App-Paket erstellen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="6544e-174">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="6544e-175">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="6544e-175">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="6544e-176">[Bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6544e-176">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6544e-177">Signieren eines App-Pakets mit SignTool</span><span class="sxs-lookup"><span data-stu-id="6544e-177">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

<span data-ttu-id="6544e-178">[Signieren eines App-Pakets](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="6544e-178">[Signing an app package](/previous-versions/br230260(v=vs.110))</span></span>
</dt> </dl>

 

 