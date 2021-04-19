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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Zugreifen auf UEFI-Firmware-Variablen über eine universelle Windows-App

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Zugreifen auf Unified Extensible Firmware Interface (UEFI)-firmwarevariablen aus einer universellen Windows-app.

Ab Windows 10, Version 1803, können universelle Windows-apps [**getfirmwareumgebungsvariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) und [**setfirmwareumgebungsvariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (und ihre "ex"-Varianten) verwenden, um auf UEFI-firmwarevariablen zuzugreifen. gehen Sie hierzu wie folgt vor:

-   Deklarieren Sie die Funktion " **Microsoft. firmwareread \_ cw5n1h2txyewy** Custom" im Manifest, um eine firmwarevariable zu lesen, und/oder die **Microsoft. firmwarewrite \_ cw5n1h2txyewy** -Funktion, um eine firmwarevariable zu schreiben.
-   Deklarieren Sie außerdem die eingeschränkte **protectedapp** -Funktion im App-Manifest.
-   Beispielsweise ermöglichen die folgenden App-Manifest-Ergänzungen der universellen Windows-APP das Lesen von Firmware-Variablen:

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

-   Legen Sie die Linkeroption **/INTEGRITYCHECK** für alle Projekt Konfigurationen fest, bevor Sie die APP an den Microsoft Store senden. Dadurch wird sichergestellt, dass die APP als geschützte App gestartet wird. Weitere Informationen finden [Sie unter/INTEGRITYCHECK (Signatur Prüfung erforderlich)](/cpp/build/reference/integritycheck-require-signature-check) .
-   Abrufen einer signierten sccd-Datei ( [Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) ) von Microsoft. Unter [Erstellen einer benutzerdefinierten Funktion zum Koppeln eines Treibers mit einer Hardware Support-app (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) und [Verwenden einer benutzerdefinierten Funktion zum Koppeln einer Hardware Support-app (HSA) mit einem Treiber](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) finden Sie Informationen dazu, wie Sie signierte sccd-Dateien von Microsoft abrufen, wie Sie diese mit Ihrer APP Verpacken und wie Sie den Entwicklermodus aktivieren. Im folgenden finden Sie ein Beispiel für eine SSCD-Datei aus dem [customcapability](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability)-Beispiel:
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

    

-   Senden Sie die APP an die Microsoft Store, um Sie zu signieren. Zu Entwicklungszwecken können Sie das Signieren überspringen, indem Sie die Test Signierung in der Start Konfigurations Datenbank (Boot Configuration Database, BCD) aktivieren. Weitere Informationen finden Sie in [der Start Konfigurations Option TESTSIGNING](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezielle und eingeschränkte Funktionen](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**Getfirmwareumgebungs-Variable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**Getfirmwareumgebungs variableex**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**Setfirmwareumgebungs-Variable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**Setfirmwareumgebungs variableex**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Zugreifen auf SMBIOS-Informationen aus einer universellen Windows-App](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
