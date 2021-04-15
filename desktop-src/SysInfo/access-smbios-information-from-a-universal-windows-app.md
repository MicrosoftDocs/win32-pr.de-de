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
# <a name="access-smbios-information-from-a-universal-windows-app"></a><span data-ttu-id="ee79d-103">Zugreifen auf SMBIOS-Informationen aus einer universellen Windows-App</span><span class="sxs-lookup"><span data-stu-id="ee79d-103">Access SMBIOS information from a Universal Windows App</span></span>

> <span data-ttu-id="ee79d-104">Nebenbei Einige Informationen beziehen sich auf ein vorab veröffentlichtes Produkt, das möglicherweise erheblich geändert wird, bevor es kommerziell veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="ee79d-104">[NOTE] Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ee79d-105">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.</span><span class="sxs-lookup"><span data-stu-id="ee79d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="ee79d-106">Zugreifen auf Systemverwaltungs-BIOS-Informationen (SMBIOS) aus einer universellen Windows-App</span><span class="sxs-lookup"><span data-stu-id="ee79d-106">How to access System Management BIOS (SMBIOS) information from a Universal Windows app.</span></span>

## <a name="access-smbios-information-from-a-universal-windows-platform-app"></a><span data-ttu-id="ee79d-107">Zugreifen auf SMBIOS-Informationen aus einer universelle Windows-Plattform-App</span><span class="sxs-lookup"><span data-stu-id="ee79d-107">Access SMBIOS information from a Universal Windows Platform App</span></span>

<span data-ttu-id="ee79d-108">Ab Windows 10, Version 1803, können universelle Windows-apps [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) und [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) verwenden, um auf SMBIOS-Informationen zuzugreifen, indem Sie die eingeschränkte **SMBIOS** -Funktion im App-Manifest deklarieren.</span><span class="sxs-lookup"><span data-stu-id="ee79d-108">Starting with Windows 10, version 1803, Universal Windows apps can use [GetSystemFirmwareTable](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable) and [EnumSystemFirmwareTables](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables) to access SMBIOS information by declaring the **smbios** restricted capability in the app manifest.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee79d-109">Nur der Zugriff auf unformatierte SMBIOS-firmwaretabellen (RSMB) wird von einer universellen Windows-App unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ee79d-109">Only access to raw SMBIOS (RSMB) firmware tables is supported from a Universal Windows app.</span></span> <span data-ttu-id="ee79d-110">**Zugriff \_ DENIED** wird zurückgegeben, wenn Sie versuchen, von einer universellen Windows-App aus auf andere firmwaretypen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee79d-110">**ACCESS\_DENIED** will be returned if you try to access other firmware table types from a Universal Windows app.</span></span>

 

<span data-ttu-id="ee79d-111">Um die eingeschränkte **SMBIOS** -Funktion im App-Manifest zu deklarieren, fügen Sie den c# **-Namespace** und die **SMBIOS** -Funktion wie folgt hinzu:</span><span class="sxs-lookup"><span data-stu-id="ee79d-111">To declare the **smbios** restricted capability in the app manifest, add the **rescap** namespace and **smbios** capability as follows:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ee79d-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee79d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee79d-113">Spezielle und eingeschränkte Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee79d-113">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="ee79d-114">GetSystemFirmwareTable</span><span class="sxs-lookup"><span data-stu-id="ee79d-114">GetSystemFirmwareTable</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemfirmwaretable)
</dt> <dt>

[<span data-ttu-id="ee79d-115">EnumSystemFirmwareTables</span><span class="sxs-lookup"><span data-stu-id="ee79d-115">EnumSystemFirmwareTables</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-enumsystemfirmwaretables)
</dt> <dt>

[<span data-ttu-id="ee79d-116">Zugreifen auf UEFI-Firmware-Variablen über eine universelle Windows-App</span><span class="sxs-lookup"><span data-stu-id="ee79d-116">Access UEFI firmware variables from a Universal Windows App</span></span>](access-uefi-firmware-variables-from-a-universal-windows-app.md)
</dt> </dl>

 

 
