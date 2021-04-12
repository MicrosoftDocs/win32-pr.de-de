---
title: Geräteparameter
description: Geräteparameter
ms.assetid: d8774c85-b5c0-4d9e-8a8e-d60ffdf59549
keywords:
- Windows Media Device Manager, Geräteparameter
- Device Manager, Geräteparameter
- Programmier Handbuch, Geräteparameter
- Dienstanbieter, Geräteparameter
- Erstellen von Dienstanbietern, Geräteparametern
- Geräteparameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3ad1a1bfc6a24736fdad8385e6cc03e0b20be2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309768"
---
# <a name="device-parameters"></a><span data-ttu-id="682f9-109">Geräteparameter</span><span class="sxs-lookup"><span data-stu-id="682f9-109">Device Parameters</span></span>

<span data-ttu-id="682f9-110">Windows Media Device Manager verwendet Geräteparameter, um das Verhalten eines Geräts zu steuern.</span><span class="sxs-lookup"><span data-stu-id="682f9-110">Windows Media Device Manager uses device parameters to control the behavior of a device.</span></span> <span data-ttu-id="682f9-111">Diese Parameter werden der Registrierung entsprechend der Angabe in der Installationsdatei des Geräts (INF-Datei) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="682f9-111">These parameters are added to the registry as specified in the device's installation file (INF file).</span></span> <span data-ttu-id="682f9-112">In der folgenden Tabelle sind die Geräteparameter aufgeführt, die von Windows Media Device Manager werden.</span><span class="sxs-lookup"><span data-stu-id="682f9-112">The following table lists the device parameters that Windows Media Device Manager queries.</span></span>



| <span data-ttu-id="682f9-113">Geräteparameter Name</span><span class="sxs-lookup"><span data-stu-id="682f9-113">Device parameter name</span></span> | <span data-ttu-id="682f9-114">Registrierungs Datentyp</span><span class="sxs-lookup"><span data-stu-id="682f9-114">Registry data type</span></span> | <span data-ttu-id="682f9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="682f9-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="682f9-116">*Wmdmspclsid*</span><span class="sxs-lookup"><span data-stu-id="682f9-116">*WMDMSPCLSID*</span></span>         | <span data-ttu-id="682f9-117">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="682f9-117">**REG\_SZ**</span></span>        | <span data-ttu-id="682f9-118">-Wert, der die CLSID des Dienstanbieters angibt, der dieses Gerät steuert.</span><span class="sxs-lookup"><span data-stu-id="682f9-118">Value that specifies the CLSID of the service provider controlling this device.</span></span> <span data-ttu-id="682f9-119">Dieser Parameter ist für die PNP-Unterstützung obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="682f9-119">This parameter is mandatory for PnP support.</span></span><br/> <span data-ttu-id="682f9-120">Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein.</span><span class="sxs-lookup"><span data-stu-id="682f9-120">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span> <span data-ttu-id="682f9-121">Dieser Parameter ist für die Unterstützung von Plug & Play (PNP) unter Windows Media Device Manager obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="682f9-121">This parameter is mandatory to support Plug and Play (PnP) under Windows Media Device Manager.</span></span> <span data-ttu-id="682f9-122">Weitere Informationen finden Sie unter [Aktivieren von PNP für Geräte](enabling-pnp-for-devices.md).</span><span class="sxs-lookup"><span data-stu-id="682f9-122">For more information, see [Enabling PnP for Devices](enabling-pnp-for-devices.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="682f9-123">*Optimaltransfersize*</span><span class="sxs-lookup"><span data-stu-id="682f9-123">*OptimalTransferSize*</span></span> | <span data-ttu-id="682f9-124">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="682f9-124">**REG\_DWORD**</span></span>     | <span data-ttu-id="682f9-125">Optionaler Wert, der die bevorzugte Übertragungs Größe angibt, die von Windows Media Device Manager bei Lese-und Schreibvorgängen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="682f9-125">Optional value that specifies the preferred transfer size that Windows Media Device Manager uses during read and write operations.</span></span> <span data-ttu-id="682f9-126">Wenn Sie nicht angegeben wird, wird eine Standard Übertragungs Größe verwendet.</span><span class="sxs-lookup"><span data-stu-id="682f9-126">If it is not supplied, a default transfer size is used.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="682f9-127">*UseMetadataViews*</span><span class="sxs-lookup"><span data-stu-id="682f9-127">*UseMetadataViews*</span></span>    | <span data-ttu-id="682f9-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="682f9-128">**REG\_DWORD**</span></span>     | <span data-ttu-id="682f9-129">Ein optionaler Parameter, der angibt, ob der Inhalt von Windows Media Device Manager bei der Darstellung von Geräte Inhalten an Anwendungen nach Metadaten organisiert wird.</span><span class="sxs-lookup"><span data-stu-id="682f9-129">Optional parameter that specifies whether Windows Media Device Manager organizes the content by metadata while presenting device content to applications.</span></span> <span data-ttu-id="682f9-130">Wenn dieser Wert fehlt, wird der Standardwert 0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="682f9-130">If not specified, the default value is 0.</span></span><br/> <span data-ttu-id="682f9-131">Wenn Anwendungen den Inhalt der Speicher eines portablen Audioplayers aufzählen, können Windows Media-Device Manager den Inhalt nach Metadaten organisiert darstellen.</span><span class="sxs-lookup"><span data-stu-id="682f9-131">When applications enumerate the content on the storages of a portable audio player, Windows Media Device Manager can present the content organized by metadata.</span></span> <span data-ttu-id="682f9-132">Dies ist besonders bei Geräten mit umfangreicher Speicherkapazität nützlich.</span><span class="sxs-lookup"><span data-stu-id="682f9-132">This is especially useful for devices with large storage capacity.</span></span><br/> <span data-ttu-id="682f9-133">Anwendungen und Geräte können dieses Verhalten steuern.</span><span class="sxs-lookup"><span data-stu-id="682f9-133">Applications and devices have the ability to control this behavior.</span></span> <span data-ttu-id="682f9-134">Geräte geben Ihre bevorzugte Einstellung durch den Geräteparameter *UseMetadataViews* an.</span><span class="sxs-lookup"><span data-stu-id="682f9-134">Devices indicate their preference through the device parameter *UseMetadataViews*.</span></span><br/> <span data-ttu-id="682f9-135">Die folgenden beiden ganzzahligen Werte werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="682f9-135">The following two integer values are supported:</span></span><br/> <span data-ttu-id="682f9-136">Fordert an, dass Inhalt den Anwendungen genau so angezeigt wird, wie er im Dateisystem des Geräts angeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="682f9-136">Requests that content be presented to the applications exactly as organized on the file system of the device.</span></span><br/> <span data-ttu-id="682f9-137">Fordert an, dass der Inhalt den von den Metadaten organisierten Anwendungen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="682f9-137">Requests that the content be presented to the applications organized by metadata.</span></span><br/> |
| <span data-ttu-id="682f9-138">*Showinshell*</span><span class="sxs-lookup"><span data-stu-id="682f9-138">*ShowInShell*</span></span>         | <span data-ttu-id="682f9-139">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="682f9-139">**REG\_DWORD**</span></span>     | <span data-ttu-id="682f9-140">Optionaler Parameter, der angibt, ob das Gerät in Windows-Explorer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="682f9-140">Optional parameter that specifies whether the device should appear in Windows Explorer.</span></span> <span data-ttu-id="682f9-141">Der Wert 1 gibt an, dass das Gerät in Windows-Explorer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="682f9-141">The value 1 indicates that the device should appear in Windows Explorer.</span></span> <span data-ttu-id="682f9-142">Weitere Informationen finden Sie unter [Anforderungen für tragbare Audioplayer werden im Windows-Explorer angezeigt](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span><span class="sxs-lookup"><span data-stu-id="682f9-142">For more information, see [Requirements for Portable Audio Players to Appear in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="682f9-143">*Useextendedwmdm*</span><span class="sxs-lookup"><span data-stu-id="682f9-143">*UseExtendedWmdm*</span></span>     | <span data-ttu-id="682f9-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="682f9-144">**REG\_DWORD**</span></span>     | <span data-ttu-id="682f9-145">Ein optionaler Parameter, der Windows Media-Device Manager benachrichtigt, dass der Dienstanbieter **IMDSPDevice3**, **IMDSPObject2** und **IMDSPStorage4** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="682f9-145">Optional parameter that alerts Windows Media Device Manager that the service provider supports **IMDSPDevice3**, **IMDSPObject2**, and **IMDSPStorage4**.</span></span> <span data-ttu-id="682f9-146">Ohne dieses Flag werden diese Schnittstellen von Windows Media Device Manager nie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="682f9-146">Without this flag, Windows Media Device Manager will never call these interfaces.</span></span> <span data-ttu-id="682f9-147">Der Wert 1 gibt an, dass diese Schnittstellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="682f9-147">The value 1 indicates that these interfaces are supported.</span></span><br/> <span data-ttu-id="682f9-148">Dieses Flag ist für Dienstanbieter erforderlich, die mit Windows Media Player synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="682f9-148">This flag is required for service providers that synchronize with Windows Media Player.</span></span> <span data-ttu-id="682f9-149">(Siehe [Aktivieren der Synchronisierung mit Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span><span class="sxs-lookup"><span data-stu-id="682f9-149">(See [Enabling Synchronization with Windows Media Player](enabling-synchronization-with-windows-media-player.md)).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="682f9-150">**Codieren der INF-Datei**</span><span class="sxs-lookup"><span data-stu-id="682f9-150">**Coding the INF file**</span></span>

<span data-ttu-id="682f9-151">Der folgende Beispielcode aus der INF-Datei eines Geräts veranschaulicht das Festlegen einiger Geräteparameter während der Geräteinstallation.</span><span class="sxs-lookup"><span data-stu-id="682f9-151">The following example code from a device's INF file demonstrates setting some device parameters during device installation.</span></span>


```C++
; Set parameters on Windows 95 and Windows 98 operating systems.
[DriverInstall.hw]
AddReg=DriverHwPropReg

; Set parameters on Windows NT-based operating systems.
[DriverInstall.NT.hw]
AddReg=DriverHwPropReg

; Related section that specifies the device parameters.
[DriverHwPropReg]
; Add your own CLSID here.
HKR,,WMDMSPCLSID,,"{00000000-0000-0000-0000-000000000000}"
HKR,,OptimalTransferSize,0x10001,0x10000
HKR,,UseMetadataViews,0x10001,0x1
```



## <a name="related-topics"></a><span data-ttu-id="682f9-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="682f9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="682f9-153">**Erstellen eines Dienstanbieters**</span><span class="sxs-lookup"><span data-stu-id="682f9-153">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="682f9-154">**IMDServiceProvider2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="682f9-154">**IMDServiceProvider2 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2)
</dt> <dt>

[<span data-ttu-id="682f9-155">**IMDServiceProvider2:: kreatedevice**</span><span class="sxs-lookup"><span data-stu-id="682f9-155">**IMDServiceProvider2::CreateDevice**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice)
</dt> <dt>

[<span data-ttu-id="682f9-156">**Iwmdmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="682f9-156">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> </dl>

 

 





