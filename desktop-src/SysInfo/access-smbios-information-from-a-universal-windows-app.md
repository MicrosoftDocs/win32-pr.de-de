---
description: Zugreifen auf BIOS-Informationen (SMBIOS) der Systemverwaltung über eine universelle Windows App.
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Zugreifen auf SMBIOS-Informationen über eine universelle Windows-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936d30a653059b3573e962b2e52770aa2bd000180ee0612c1855de3d6a1a9778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764954"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Zugreifen auf SMBIOS-Informationen über eine universelle Windows-App

> [HINWEIS] Einige Informationen beziehen sich auf vorab veröffentlichte Produkte, die möglicherweise erheblich geändert werden, bevor es im Handel veröffentlicht wird. Microsoft übernimmt bezüglich der hier bereitgestellten Informationen keine Gewährleistungen, weder ausdrücklich noch konkludent.

Zugreifen auf BIOS-Informationen (SMBIOS) der Systemverwaltung über eine universelle Windows App.

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Zugreifen auf SMBIOS-Informationen über eine Universelle Windows Plattform-App

Ab Windows 10 Version 1803 können universelle Windows-Apps [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) und [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) verwenden, um auf SMBIOS-Informationen zuzugreifen, indem sie die eingeschränkte **smbios-Funktion** im App-Manifest deklarieren.

> [!IMPORTANT]
> Nur der Zugriff auf UN-SMBIOS-Firmwaretabellen (RSMB) wird von einer Universal Windows-App unterstützt. **ACCESS \_ DENIED** wird zurückgegeben, wenn Sie versuchen, von einer Universellen Windows-App auf andere Firmwaretabellentypen zu zugreifen.

 

Um die **eingeschränkte Smbios-Funktion** im App-Manifest zu deklarieren, fügen Sie den **rescap-Namespace** und die **smbios-Funktion** wie folgt hinzu:

``` syntax
<Package
  ...
  xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
  IgnorableNamespaces="uap mp rescap">  
  ...
  <Capabilities>
    <rescap:Capability Name="smbios"/>
  </Capabilities>
</Package>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Spezielle und eingeschränkte Funktionen](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[Zugreifen auf UEFI-Firmwarevariablen über eine universelle Windows-App](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
