---
description: Zugreifen auf Unified Extensible Firmware Interface (UEFI)-firmwarevariablen aus einer universellen Windows-app.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Zugreifen auf UEFI-Firmware-Variablen über eine universelle Windows-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353522"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="395c1-103">Zugreifen auf UEFI-Firmware-Variablen über eine universelle Windows-App</span><span class="sxs-lookup"><span data-stu-id="395c1-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="395c1-104">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="395c1-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="395c1-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="395c1-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="395c1-106">Zugreifen auf Unified Extensible Firmware Interface (UEFI)-firmwarevariablen aus einer universellen Windows-app.</span><span class="sxs-lookup"><span data-stu-id="395c1-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="395c1-107">Ab Windows 10, Version 1803, können universelle Windows-apps [**getfirmwareumgebungsvariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) und [**setfirmwareumgebungsvariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (und ihre "ex"-Varianten) verwenden, um auf UEFI-firmwarevariablen zuzugreifen. gehen Sie hierzu wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="395c1-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="395c1-108">Deklarieren Sie die Funktion " **Microsoft. firmwareread \_ cw5n1h2txyewy** Custom" im Manifest, um eine firmwarevariable zu lesen, und/oder die **Microsoft. firmwarewrite \_ cw5n1h2txyewy** -Funktion, um eine firmwarevariable zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="395c1-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="395c1-109">Deklarieren Sie außerdem die eingeschränkte **protectedapp** -Funktion im App-Manifest.</span><span class="sxs-lookup"><span data-stu-id="395c1-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="395c1-110">Beispielsweise ermöglichen die folgenden App-Manifest-Ergänzungen der universellen Windows-APP das Lesen von Firmware-Variablen:</span><span class="sxs-lookup"><span data-stu-id="395c1-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="395c1-111">Legen Sie die Linkeroption **/INTEGRITYCHECK** für alle Projekt Konfigurationen fest, bevor Sie die APP an den Microsoft Store senden.</span><span class="sxs-lookup"><span data-stu-id="395c1-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="395c1-112">Dadurch wird sichergestellt, dass die APP als geschützte App gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="395c1-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="395c1-113">Weitere Informationen finden [Sie unter/INTEGRITYCHECK (Signatur Prüfung erforderlich)](/cpp/build/reference/integritycheck-require-signature-check) .</span><span class="sxs-lookup"><span data-stu-id="395c1-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="395c1-114">Abrufen einer signierten sccd-Datei ( [Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) ) von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="395c1-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="395c1-115">Unter [Erstellen einer benutzerdefinierten Funktion zum Koppeln eines Treibers mit einer Hardware Support-app (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) und [Verwenden einer benutzerdefinierten Funktion zum Koppeln einer Hardware Support-app (HSA) mit einem Treiber](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) finden Sie Informationen dazu, wie Sie signierte sccd-Dateien von Microsoft abrufen, wie Sie diese mit Ihrer APP Verpacken und wie Sie den Entwicklermodus aktivieren.</span><span class="sxs-lookup"><span data-stu-id="395c1-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="395c1-116">Im folgenden finden Sie ein Beispiel für eine SSCD-Datei aus dem [customcapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability)-Beispiel:</span><span class="sxs-lookup"><span data-stu-id="395c1-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="395c1-117">Senden Sie die APP an die Microsoft Store, um Sie zu signieren.</span><span class="sxs-lookup"><span data-stu-id="395c1-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="395c1-118">Zu Entwicklungszwecken können Sie das Signieren überspringen, indem Sie die Test Signierung in der Start Konfigurations Datenbank (Boot Configuration Database, BCD) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="395c1-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="395c1-119">Weitere Informationen finden Sie in [der Start Konfigurations Option TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .</span><span class="sxs-lookup"><span data-stu-id="395c1-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="395c1-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="395c1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="395c1-121">Spezielle und eingeschränkte Funktionen</span><span class="sxs-lookup"><span data-stu-id="395c1-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="395c1-122">**Getfirmwareumgebungs-Variable**</span><span class="sxs-lookup"><span data-stu-id="395c1-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="395c1-123">**Getfirmwareumgebungs variableex**</span><span class="sxs-lookup"><span data-stu-id="395c1-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="395c1-124">**Setfirmwareumgebungs-Variable**</span><span class="sxs-lookup"><span data-stu-id="395c1-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="395c1-125">**Setfirmwareumgebungs variableex**</span><span class="sxs-lookup"><span data-stu-id="395c1-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="395c1-126">Zugreifen auf SMBIOS-Informationen aus einer universellen Windows-App</span><span class="sxs-lookup"><span data-stu-id="395c1-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
