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
# <a name="how-to-sign-an-app-package-using-signtool"></a><span data-ttu-id="d7864-103">Signieren eines App-Pakets mithilfe von SignTool</span><span class="sxs-lookup"><span data-stu-id="d7864-103">How to sign an app package using SignTool</span></span>

> [!Note]  
> <span data-ttu-id="d7864-104">Informationen zum Signieren eines Windows-App-Pakets finden [Sie unter Signieren eines App-Pakets mit SignTool](/windows/msix/package/sign-app-package-using-signtool).</span><span class="sxs-lookup"><span data-stu-id="d7864-104">For signing a Windows app package, see [Sign an app package using SignTool](/windows/msix/package/sign-app-package-using-signtool).</span></span>

 

<span data-ttu-id="d7864-105">Erfahren Sie, wie Sie mit [**SignTool**](/windows-hardware/drivers/devtest/signtool) Ihre Windows-App-Pakete signieren, damit Sie bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="d7864-105">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages so they can be deployed.</span></span> <span data-ttu-id="d7864-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) ist Teil des Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d7864-106">[**SignTool**](/windows-hardware/drivers/devtest/signtool) is part of the Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="d7864-107">Alle Windows-App-Pakete müssen digital signiert werden, bevor Sie bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="d7864-107">All Windows app packages must be digitally signed before they can be deployed.</span></span> <span data-ttu-id="d7864-108">Obwohl Microsoft Visual Studio 2012 und höher ein App-Paket während seiner Erstellung signieren können, sind Pakete, die Sie mit dem [App Packager-Tool (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) aus dem Windows SDK erstellen, nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="d7864-108">While Microsoft Visual Studio 2012 and later can sign an app package during its creation, packages that you create by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool from the Windows SDK aren't signed.</span></span>

> [!Note]  
> <span data-ttu-id="d7864-109">Sie können [**SignTool**](/windows-hardware/drivers/devtest/signtool) nur zum Signieren Ihrer Windows-App-Pakete unter Windows 8 und höher oder Windows Server 2012 und höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7864-109">You can only use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your Windows app packages on Windows 8 and later or Windows Server 2012 and later.</span></span> <span data-ttu-id="d7864-110">Sie können **SignTool** nicht zum Signieren von App-Paketen auf Betriebssystemen unter Betriebssystemen wie Windows 7 oder Windows Server 2008 R2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7864-110">You can't use **SignTool** to sign app packages on down-level operating systems such as Windows 7 or Windows Server 2008 R2.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="d7864-111">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d7864-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="d7864-112">Technologien</span><span class="sxs-lookup"><span data-stu-id="d7864-112">Technologies</span></span>

-   <span data-ttu-id="d7864-113">[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7864-113">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   <span data-ttu-id="d7864-114">[App-Pakete und-Bereitstellung](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="d7864-114">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
-   [<span data-ttu-id="d7864-115">Tools zum Signieren von Dateien und Überprüfen von Signaturen</span><span class="sxs-lookup"><span data-stu-id="d7864-115">Tools to Sign Files and Check Signatures</span></span>](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a><span data-ttu-id="d7864-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d7864-116">Prerequisites</span></span>

-   <span data-ttu-id="d7864-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), das Teil der Windows SDK</span><span class="sxs-lookup"><span data-stu-id="d7864-117">[**SignTool**](/windows-hardware/drivers/devtest/signtool), which is part of the Windows SDK</span></span>
-   <span data-ttu-id="d7864-118">Ein gültiges Code Signaturzertifikat, z. b. eine PFX-Datei (Personal Information Exchange), die mit den [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) -und [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) Tools erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d7864-118">A valid code signing certificate, for example, a Personal Information Exchange (.pfx) file created with the [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) tools</span></span>

    <span data-ttu-id="d7864-119">Informationen zum Erstellen eines gültigen Code Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="d7864-119">For info about creating a valid code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

-   <span data-ttu-id="d7864-120">Eine gepackte Windows-APP, z. b. eine AppX-Datei, die mit dem [App Packager-Tool (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="d7864-120">A packaged Windows app, for example, an .appx file created by using the [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) tool</span></span>

<span data-ttu-id="d7864-121">**Weitere Überlegungen**</span><span class="sxs-lookup"><span data-stu-id="d7864-121">**Additional considerations**</span></span>

<span data-ttu-id="d7864-122">Das Zertifikat, das Sie zum Signieren des App-Pakets verwenden, muss folgende Kriterien erfüllen:</span><span class="sxs-lookup"><span data-stu-id="d7864-122">The certificate that you use to sign the app package must meet these criteria:</span></span>

-   <span data-ttu-id="d7864-123">Der Antragsteller Name des Zertifikats muss dem **Verleger** Attribut entsprechen, das im [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Element der AppxManifest.xml Datei enthalten ist, die im Paket gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d7864-123">The subject name of the certificate must match the **Publisher** attribute that is contained in the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element of the AppxManifest.xml file that is stored within the package.</span></span> <span data-ttu-id="d7864-124">Der Herausgeber Name ist Teil der Identität einer gepackten Windows-app. Daher müssen Sie den Antragsteller Namen des Zertifikats mit dem Namen des Herausgebers der APP vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d7864-124">The publisher name is part of the identity of a packaged Windows app, so you have to make the subject name of the certificate match the publisher name of the app.</span></span> <span data-ttu-id="d7864-125">Dadurch kann die Identität von signierten Paketen anhand der digitalen Signatur überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="d7864-125">This allows the identity of signed packages to be checked against the digital signature.</span></span> <span data-ttu-id="d7864-126">Informationen zu Signatur Fehlern, die beim Signieren eines App-Pakets mithilfe von [**SignTool**](/windows-hardware/drivers/devtest/signtool)auftreten können, finden Sie im Abschnitt "Hinweise" unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="d7864-126">For info about signing errors that can arise from signing an app package using [**SignTool**](/windows-hardware/drivers/devtest/signtool), see the Remarks section of [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>
-   <span data-ttu-id="d7864-127">Das Zertifikat muss für die Code Signatur gültig sein.</span><span class="sxs-lookup"><span data-stu-id="d7864-127">The certificate must be valid for code signing.</span></span> <span data-ttu-id="d7864-128">Dies bedeutet, dass beide Elemente zutreffen müssen:</span><span class="sxs-lookup"><span data-stu-id="d7864-128">This means that both of these items must be true:</span></span>

    -   <span data-ttu-id="d7864-129">Das EKU-Feld (Extended Key Usage) des Zertifikats muss entweder nicht festgelegt sein oder den EKU-Wert für die Code Signatur (1.3.6.1.5.5.7.3.3) enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7864-129">The Extended Key Usage (EKU) field of the certificate must either be unset or contain the EKU value for code signing (1.3.6.1.5.5.7.3.3).</span></span>
    -   <span data-ttu-id="d7864-130">Das Feld "Schlüssel Verwendung" des Zertifikats muss entweder nicht festgelegt sein oder das Verwendungs Bit für die digitale Signatur (0x80) enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7864-130">The Key Usage (KU) field of the certificate must either be unset or contain the usage bit for digital signature (0x80).</span></span>

-   <span data-ttu-id="d7864-131">Das Zertifikat enthält einen privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d7864-131">The certificate contains a private key.</span></span>
-   <span data-ttu-id="d7864-132">Das Zertifikat ist gültig.</span><span class="sxs-lookup"><span data-stu-id="d7864-132">The certificate is valid.</span></span> <span data-ttu-id="d7864-133">Es ist aktiv, nicht abgelaufen und wurde nicht widerrufen.</span><span class="sxs-lookup"><span data-stu-id="d7864-133">It is active, hasn't expired, and hasn't been revoked.</span></span>

## <a name="instructions"></a><span data-ttu-id="d7864-134">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="d7864-134">Instructions</span></span>

### <a name="step-1-determine-the-hash-algorithm-to-use"></a><span data-ttu-id="d7864-135">Schritt 1: Bestimmen des zu verwendenden Hash Algorithmus</span><span class="sxs-lookup"><span data-stu-id="d7864-135">Step 1: Determine the hash algorithm to use</span></span>

<span data-ttu-id="d7864-136">Wenn Sie das App-Paket signieren, müssen Sie denselben Hash Algorithmus verwenden, den Sie beim Erstellen des App-Pakets verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="d7864-136">When you sign the app package, you must use the same hash algorithm that you used when you created the app package.</span></span> <span data-ttu-id="d7864-137">Wenn Sie die Standardeinstellungen zum Erstellen des App-Pakets verwendet haben, lautet der verwendete Hash Algorithmus SHA256.</span><span class="sxs-lookup"><span data-stu-id="d7864-137">If you used default settings to create the app package, the hash algorithm used is SHA256.</span></span>

<span data-ttu-id="d7864-138">Wenn Sie den App-Packager mit einem bestimmten Hash Algorithmus verwendet haben, um das App-Paket zu erstellen, verwenden Sie den gleichen Algorithmus, um das Paket zu signieren.</span><span class="sxs-lookup"><span data-stu-id="d7864-138">If you used the app packager with a specific hash algorithm to create the app package, use the same algorithm to sign the package.</span></span> <span data-ttu-id="d7864-139">Um den Hash Algorithmus zu ermitteln, der zum Signieren eines Pakets verwendet werden soll, können Sie den Paket Inhalt extrahieren und die AppxBlockMap.xml Datei überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d7864-139">To determine the hash algorithm to use for signing a package, you can extract the package contents and inspect the AppxBlockMap.xml file.</span></span> <span data-ttu-id="d7864-140">Das **hashmethod** -Attribut des [**blockmap**](/uwp/schemas/blockmapschema/element-blockmap) -Elements gibt den Hash Algorithmus an, der beim Erstellen des App-Pakets verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d7864-140">The **HashMethod** attribute of the [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates the hash algorithm that was used when creating the app package.</span></span> <span data-ttu-id="d7864-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7864-141">For example:</span></span>

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

<span data-ttu-id="d7864-142">Das vorangehende [**Block Map**](/uwp/schemas/blockmapschema/element-blockmap) -Element gibt an, dass der SHA256-Algorithmus verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d7864-142">The preceding [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) element indicates that the SHA256 algorithm was used.</span></span> <span data-ttu-id="d7864-143">In dieser Tabelle ist die Zuordnung der derzeit verfügbaren Algorithmen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="d7864-143">This table lists the mapping of the currently available algorithms:</span></span>

| <span data-ttu-id="d7864-144">**Hashmethod** -Wert</span><span class="sxs-lookup"><span data-stu-id="d7864-144">**HashMethod** value</span></span>                            | <span data-ttu-id="d7864-145">zu verwendende *HashAlgorithm*</span><span class="sxs-lookup"><span data-stu-id="d7864-145">*hashAlgorithm* to use</span></span> |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | <span data-ttu-id="d7864-146">SHA256 (. AppX-Standard)</span><span class="sxs-lookup"><span data-stu-id="d7864-146">SHA256 (.appx default)</span></span> |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | <span data-ttu-id="d7864-147">SHA384</span><span class="sxs-lookup"><span data-stu-id="d7864-147">SHA384</span></span>                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | <span data-ttu-id="d7864-148">SHA512</span><span class="sxs-lookup"><span data-stu-id="d7864-148">SHA512</span></span>                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a><span data-ttu-id="d7864-149">Schritt 2: Ausführen SignTool.exe zum Signieren des Pakets</span><span class="sxs-lookup"><span data-stu-id="d7864-149">Step 2: Run SignTool.exe to sign the package</span></span>

<span data-ttu-id="d7864-150">**So signieren Sie das Paket mit einem Signaturzertifikat aus einer PFX-Datei**</span><span class="sxs-lookup"><span data-stu-id="d7864-150">**To sign the package with a signing certificate from a .pfx file**</span></span>

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

<span data-ttu-id="d7864-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) verwendet standardmäßig den Parameter/FD *HashAlgorithm* auf SHA1, wenn er nicht angegeben ist und SHA1 nicht für das Signieren von App-Paketen gültig ist.</span><span class="sxs-lookup"><span data-stu-id="d7864-151">[**SignTool**](/windows-hardware/drivers/devtest/signtool) defaults the /fd *hashAlgorithm* parameter to SHA1 if it's not specified, and SHA1 isn't valid for signing app packages.</span></span> <span data-ttu-id="d7864-152">Daher müssen Sie diesen Parameter angeben, wenn Sie ein App-Paket signieren.</span><span class="sxs-lookup"><span data-stu-id="d7864-152">So, you must specify this parameter when you sign an app package.</span></span> <span data-ttu-id="d7864-153">Zum Signieren eines App-Pakets, das mit dem standardmäßigen SHA256-Hash erstellt wurde, geben Sie den/FD *HashAlgorithm* -Parameter als SHA256 an:</span><span class="sxs-lookup"><span data-stu-id="d7864-153">To sign an app package that was created with the default SHA256 hash, you specify the /fd *hashAlgorithm* parameter as SHA256:</span></span>

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

<span data-ttu-id="d7864-154">Sie können den Parameter "/p *Password* " weglassen, wenn Sie eine PFX-Datei verwenden, die nicht mit einem Kennwort geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="d7864-154">You can omit the /p *password* parameter if you use a .pfx file that isn't password protected.</span></span> <span data-ttu-id="d7864-155">Sie können auch andere Optionen für die Zertifikat Auswahl verwenden, die von [**SignTool**](/windows-hardware/drivers/devtest/signtool) zum Signieren von App-Paketen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d7864-155">You can also use other certificate selection options that are supported by [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign app packages.</span></span> <span data-ttu-id="d7864-156">Weitere Informationen zu diesen Optionen finden Sie unter [SignTool](/windows/desktop/SecCrypto/signtool).</span><span class="sxs-lookup"><span data-stu-id="d7864-156">For more info about these options, see [SignTool](/windows/desktop/SecCrypto/signtool).</span></span>

> [!Note]  
> <span data-ttu-id="d7864-157">Der [**SignTool**](/windows-hardware/drivers/devtest/signtool) -Zeitstempel Vorgang kann nicht für ein signiertes App-Paket verwendet werden. der Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d7864-157">You can't use the [**SignTool**](/windows-hardware/drivers/devtest/signtool) time stamp operation on a signed app package; the operation isn't supported.</span></span>

 

<span data-ttu-id="d7864-158">Wenn Sie einen Zeitstempel für das App-Paket verwenden möchten, müssen Sie es während des Signierungs Vorgangs ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7864-158">If you want to time stamp the app package, you must do it during the sign operation.</span></span> <span data-ttu-id="d7864-159">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d7864-159">For example:</span></span>

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

<span data-ttu-id="d7864-160">Legen Sie den/TR *timestampServerUrl* -Parameter der URL für einen RFC 3161-Zeitstempel Server entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="d7864-160">Make the /tr *timestampServerUrl* parameter equal to the URL for an RFC 3161 time stamp server.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7864-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7864-161">Remarks</span></span>

<span data-ttu-id="d7864-162">In diesem Abschnitt wird die Behandlung von Signatur Fehlern für App-Pakete erläutert.</span><span class="sxs-lookup"><span data-stu-id="d7864-162">This section discusses troubleshooting signing errors for app packages.</span></span>

### <a name="troubleshooting-app-package-signing-errors"></a><span data-ttu-id="d7864-163">Problembehandlung bei App-Paket Signatur Fehlern</span><span class="sxs-lookup"><span data-stu-id="d7864-163">Troubleshooting app package signing errors</span></span>

<span data-ttu-id="d7864-164">Zusätzlich zu den Signatur Fehlern, die [**SignTool**](/windows-hardware/drivers/devtest/signtool) zurückgeben kann, kann **SignTool** auch Fehler zurückgeben, die für das Signieren von App-Paketen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="d7864-164">In addition to the signing errors that [**SignTool**](/windows-hardware/drivers/devtest/signtool) can return, **SignTool** can also return errors that are specific to the signing of app packages.</span></span> <span data-ttu-id="d7864-165">Diese Fehler werden normalerweise als interne Fehler angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7864-165">These errors usually appear as internal errors:</span></span>

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

<span data-ttu-id="d7864-166">Wenn der Fehlercode mit 0x8008 beginnt, z. b. 0x80080206 AppX \_ E beschädigte \_ \_ Inhalte), weist dies darauf hin, dass das signierte Paket ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="d7864-166">If the error code starts with 0x8008, such as 0x80080206 APPX\_E\_CORRUPT\_CONTENT), it indicates that the package being signed is invalid.</span></span> <span data-ttu-id="d7864-167">In diesem Fall müssen Sie das Paket neu erstellen, bevor Sie es signieren können.</span><span class="sxs-lookup"><span data-stu-id="d7864-167">In this case, before you can sign the package, you must rebuild the package.</span></span> <span data-ttu-id="d7864-168">Die vollständige Liste der 0x8008- \* Fehler finden Sie unter [**com-Fehler Codes (Sicherheit und Setup)**](/windows/desktop/com/com-error-codes-4).</span><span class="sxs-lookup"><span data-stu-id="d7864-168">For the full list of 0x8008\* errors, see [**COM Error Codes (Security and Setup)**](/windows/desktop/com/com-error-codes-4).</span></span>

<span data-ttu-id="d7864-169">Im Allgemeinen ist der Fehler 0x8007000B (fehlerhaftes \_ \_ Format).</span><span class="sxs-lookup"><span data-stu-id="d7864-169">More commonly, the error is 0x8007000b (ERROR\_BAD\_FORMAT).</span></span> <span data-ttu-id="d7864-170">In diesem Fall können Sie spezifischere Fehlerinformationen im Ereignisprotokoll finden:</span><span class="sxs-lookup"><span data-stu-id="d7864-170">In this case, you can find more specific error information in the event log:</span></span>

<span data-ttu-id="d7864-171">**So durchsuchen Sie das Ereignisprotokoll**</span><span class="sxs-lookup"><span data-stu-id="d7864-171">**To search the event log**</span></span>

1.  <span data-ttu-id="d7864-172">Führen Sie eventvwr. msc aus.</span><span class="sxs-lookup"><span data-stu-id="d7864-172">Run Eventvwr.msc.</span></span>
2.  <span data-ttu-id="d7864-173">Öffnen Sie das Ereignisprotokoll: Ereignisanzeige (local) > Anwendungs-und Dienst Protokolle > Microsoft > Windows > appxpackagingom > Microsoft-Windows-appxpackaging/Operational</span><span class="sxs-lookup"><span data-stu-id="d7864-173">Open the event log: Event Viewer (Local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational</span></span>
3.  <span data-ttu-id="d7864-174">Suchen Sie nach dem letzten Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="d7864-174">Look for the most recent error event.</span></span>

<span data-ttu-id="d7864-175">Der interne Fehler entspricht in der Regel einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="d7864-175">The internal error usually corresponds to one of these:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7864-176">Ereignis-ID</span><span class="sxs-lookup"><span data-stu-id="d7864-176">Event ID</span></span></th>
<th><span data-ttu-id="d7864-177">Beispiel Ereignis Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d7864-177">Example event string</span></span></th>
<th><span data-ttu-id="d7864-178">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="d7864-178">Suggestion</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7864-179">150</span><span class="sxs-lookup"><span data-stu-id="d7864-179">150</span></span></td>
<td><span data-ttu-id="d7864-180">Fehler 0x8007000B: der Herausgeber Name des App-Manifests (CN = ca) muss mit dem Antragsteller Namen des Signatur Zertifikats (CN = C = US) identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d7864-180">error 0x8007000B: The app manifest publisher name (CN=Contoso) must match the subject name of the signing certificate (CN=Contoso, C=US).</span></span></td>
<td><span data-ttu-id="d7864-181">Der Herausgeber Name des App-Manifests muss exakt mit dem Antragsteller Namen der Signatur übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="d7864-181">The app manifest publisher name must exactly match the subject name of the signing.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d7864-182">Diese Namen werden in Anführungszeichen angegeben und sind sowohl Groß-/Kleinschreibung als auch Leerraum sensibel.</span><span class="sxs-lookup"><span data-stu-id="d7864-182">These names are specified in quotes and are both case and whitespace sensitive.</span></span>
</blockquote>
<br/> <span data-ttu-id="d7864-183">Sie können die Attribut Zeichenfolge für den <strong>Verleger</strong> , die für das <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> -Element in der AppxManifest.xml-Datei definiert ist, so aktualisieren, dass Sie mit dem Antragsteller Namen des vorgesehenen Signatur Zertifikats</span><span class="sxs-lookup"><span data-stu-id="d7864-183">You can update the <strong>Publisher</strong> attribute string that is defined for the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> element in the AppxManifest.xml file to match the subject name of the intended signing certificate.</span></span> <span data-ttu-id="d7864-184">Oder wählen Sie ein anderes Signaturzertifikat mit einem Antragsteller Namen aus, der dem Herausgeber Namen des App-Manifests entspricht.</span><span class="sxs-lookup"><span data-stu-id="d7864-184">Or, select a different signing certificate with a subject name that matches the app manifest publisher name.</span></span> <span data-ttu-id="d7864-185">Der Name des Manifest-Verlegers und der Zertifikat Antragsteller Name werden in der Ereignismeldung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7864-185">The manifest publisher name and the certificate subject name are both listed in the event message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7864-186">151</span><span class="sxs-lookup"><span data-stu-id="d7864-186">151</span></span></td>
<td><span data-ttu-id="d7864-187">Fehler 0x8007000B: die angegebene Signatur Hash Methode (SHA512) muss mit der in der APP-Paket Block Zuordnung (SHA256) verwendeten Hash Methode identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d7864-187">error 0x8007000B: The signature hash method specified (SHA512) must match the hash method used in the app package block map (SHA256).</span></span></td>
<td><span data-ttu-id="d7864-188">Der im/FD-Parameter angegebene HashAlgorithm ist falsch (siehe Schritt 1: Bestimmen des zu verwendenden Hash Algorithmus).</span><span class="sxs-lookup"><span data-stu-id="d7864-188">The hashAlgorithm specified in the /fd parameter is incorrect (see Step 1: Determine the hash algorithm to use).</span></span> <span data-ttu-id="d7864-189">Führen Sie <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> erneut mit dem HashAlgorithm aus, der mit der APP-Paket Block Zuordnung übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="d7864-189">Rerun <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> with the hashAlgorithm that matches the app package block map.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7864-190">152</span><span class="sxs-lookup"><span data-stu-id="d7864-190">152</span></span></td>
<td><span data-ttu-id="d7864-191">Fehler 0x8007000B: der Inhalt des App-Pakets muss anhand seiner Block Zuordnung überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="d7864-191">error 0x8007000B: The app package contents must validate against its block map.</span></span></td>
<td><span data-ttu-id="d7864-192">Das App-Paket ist beschädigt und muss neu erstellt werden, um eine neue Block Zuordnung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d7864-192">The app package is corrupt and needs to be rebuilt to generate a new block map.</span></span> <span data-ttu-id="d7864-193">Weitere Informationen zum Erstellen eines App-Pakets finden Sie unter Erstellen eines App-Pakets mit <a href="make-appx-package--makeappx-exe-.md">App Packager</a> oder <a href="/previous-versions/hh975357(v=vs.110)">Erstellen eines App-Pakets mit Visual Studio 2012</a>.</span><span class="sxs-lookup"><span data-stu-id="d7864-193">For more info about creating an app package, see creating an app package with <a href="make-appx-package--makeappx-exe-.md">app packager</a> or <a href="/previous-versions/hh975357(v=vs.110)">Creating an app package with Visual Studio 2012</a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a><span data-ttu-id="d7864-194">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d7864-194">Security Considerations</span></span>

<span data-ttu-id="d7864-195">Nachdem das Paket signiert wurde, muss das Zertifikat, das Sie zum Signieren des Pakets verwendet haben, weiterhin von dem Computer als vertrauenswürdig eingestuft werden, auf dem das Paket bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7864-195">After the package is signed, the certificate that you used to sign the package must still be trusted by the computer on which the package is to be deployed.</span></span> <span data-ttu-id="d7864-196">Wenn Sie einem Zertifikat [Speicher des lokalen](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)Computers ein Zertifikat hinzufügen, haben Sie Auswirkungen auf die Zertifikats Vertrauensstellung aller Benutzer auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="d7864-196">By adding a certificate to [local machine certificate stores](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), you affect the certificate trust of all users on the computer.</span></span> <span data-ttu-id="d7864-197">Es wird empfohlen, dass Sie alle Code Signatur Zertifikate installieren, die Sie zum Testen von App-Paketen im Zertifikat Speicher für vertrauenswürdige Personen benötigen, und diese Zertifikate unverzüglich entfernen, wenn Sie nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7864-197">We recommend that you install any code signing certificates that you want for testing app packages to the Trusted People certificate store, and promptly remove those certificates when no longer necessary.</span></span> <span data-ttu-id="d7864-198">Wenn Sie eigene Test Zertifikate zum Signieren von App-Paketen erstellen, empfiehlt es sich auch, die dem Test Zertifikat zugeordneten Berechtigungen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="d7864-198">If you create your own test certificates for signing app packages, we also recommend that you restrict the privileges associated with the test certificate.</span></span> <span data-ttu-id="d7864-199">Weitere Informationen zum Erstellen von Test Zertifikaten zum Signieren von App-Paketen finden [Sie unter Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="d7864-199">For more info about creating test certificates for signing app packages, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7864-200">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7864-200">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d7864-201">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="d7864-201">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="d7864-202">App-Paket erstellen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="d7864-202">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="d7864-203">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="d7864-203">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="d7864-204">[Bewährte Methoden für die Code Signatur](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7864-204">[Code-Signing Best Practices](/previous-versions/windows/hardware/design/dn653556(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d7864-205">[Signieren eines Pakets in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span><span class="sxs-lookup"><span data-stu-id="d7864-205">[Signing a package in Visual Studio 2012](/previous-versions/br230260(v=vs.110))</span></span>
</dt> <dt>

[<span data-ttu-id="d7864-206">SignTool</span><span class="sxs-lookup"><span data-stu-id="d7864-206">SignTool</span></span>](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[<span data-ttu-id="d7864-207">App-Packager (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="d7864-207">App packager (MakeAppx.exe)</span></span>](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[<span data-ttu-id="d7864-208">So erstellst du ein App-Paketsignaturzertifikat</span><span class="sxs-lookup"><span data-stu-id="d7864-208">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

