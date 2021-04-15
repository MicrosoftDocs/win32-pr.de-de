---
description: Zugreifen auf Systemverwaltungs-BIOS-Informationen (SMBIOS) aus einer universellen Windows-App
ms.assetid: 4D185319-C093-4B1B-A182-E845E72FEA5D
title: Zugreifen auf SMBIOS-Informationen aus einer universellen Windows-App
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76791622ad4bcba15ddd889f36a6f0feeb5e3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529318"
---
# <a name="access-smbios-information-from-a-universal-windows-app"></a>Zugreifen auf SMBIOS-Informationen aus einer universellen Windows-App

> Nebenbei Einige Informationen beziehen sich auf ein vorab veröffentlichtes Produkt, das möglicherweise erheblich geändert wird, bevor es kommerziell veröffentlicht wird. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.

Zugreifen auf Systemverwaltungs-BIOS-Informationen (SMBIOS) aus einer universellen Windows-App

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a>Zugreifen auf SMBIOS-Informationen aus einer universelle Windows-Plattform-App

Ab Windows 10, Version 1803, können universelle Windows-apps [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) und [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) verwenden, um auf SMBIOS-Informationen zuzugreifen, indem Sie die eingeschränkte **SMBIOS** -Funktion im App-Manifest deklarieren.

> [!IMPORTANT]
> Nur der Zugriff auf unformatierte SMBIOS-firmwaretabellen (RSMB) wird von einer universellen Windows-App unterstützt. **Zugriff \_ DENIED** wird zurückgegeben, wenn Sie versuchen, von einer universellen Windows-App aus auf andere firmwaretypen zuzugreifen.

 

Um die eingeschränkte **SMBIOS** -Funktion im App-Manifest zu deklarieren, fügen Sie den c# **-Namespace** und die **SMBIOS** -Funktion wie folgt hinzu:

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

[Zugreifen auf UEFI-Firmware-Variablen über eine universelle Windows-App](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
