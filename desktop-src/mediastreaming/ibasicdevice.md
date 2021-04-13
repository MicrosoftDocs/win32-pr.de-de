---
title: Ibasicdevice-Schnittstelle
description: Kapselt die Methoden und Ereignisse, die erforderlich sind, um ein DLNA-Gerät zu modellieren.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- Ibasicdevice-Schnittstelle Medien Streaming-API
- Ibasicdevice-Schnittstelle Medien Streaming-API, beschrieben
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/21/2020
ms.locfileid: "104391207"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="38568-105">Ibasicdevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="38568-105">IBasicDevice interface</span></span>

<span data-ttu-id="38568-106">Kapselt die Methoden und Ereignisse, die erforderlich sind, um ein DLNA-Gerät zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="38568-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="38568-107">Member</span><span class="sxs-lookup"><span data-stu-id="38568-107">Members</span></span>

<span data-ttu-id="38568-108">Die **ibasicdevice** -Schnittstelle erbt von [**iinspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="38568-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="38568-109">**Ibasicdevice** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="38568-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="38568-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="38568-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="38568-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="38568-111">Methods</span></span>

<span data-ttu-id="38568-112">Die **ibasicdevice** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="38568-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="38568-113">Methode</span><span class="sxs-lookup"><span data-stu-id="38568-113">Method</span></span>                                                                                 | <span data-ttu-id="38568-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38568-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38568-115">**\_connectionstatuschge hinzufügen**</span><span class="sxs-lookup"><span data-stu-id="38568-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="38568-116">Registriert einen Ereignishandler für das [**connectionstatuschangi-Ereignis**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="38568-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="38568-117">**Canwake-Geräte**</span><span class="sxs-lookup"><span data-stu-id="38568-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="38568-118">Ruft einen Wert ab, der angibt, ob das Gerät aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="38568-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="38568-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38568-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="38568-120">Gibt einen-Enumerationswert zurück, der angibt, ob das Gerät derzeit online, offline oder im Ruhezustand ist, aber wach stellbar ist.</span><span class="sxs-lookup"><span data-stu-id="38568-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="38568-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38568-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="38568-122">Ruft eine Beschreibung des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="38568-123">**Discoveredoncurrentnetwork**</span><span class="sxs-lookup"><span data-stu-id="38568-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="38568-124">Ruft einen Wert ab, der angibt, ob sich das Gerät im aktuellen Netzwerk befindet.</span><span class="sxs-lookup"><span data-stu-id="38568-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="38568-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="38568-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="38568-126">Ruft den anzeigen amen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="38568-127">**Icons**</span><span class="sxs-lookup"><span data-stu-id="38568-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="38568-128">Gibt einen Vektor von [**ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) -Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="38568-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="38568-129">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="38568-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="38568-130">Gibt einen Vektor von IP-Adressen zurück.</span><span class="sxs-lookup"><span data-stu-id="38568-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="38568-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="38568-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="38568-132">Ruft den Herstellernamen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="38568-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="38568-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="38568-134">Ruft die Hersteller-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="38568-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="38568-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="38568-136">Ruft den Modellnamen des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="38568-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="38568-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="38568-138">Ruft die Modellnummer des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="38568-139">**Modelurl**</span><span class="sxs-lookup"><span data-stu-id="38568-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="38568-140">Ruft die Modell-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="38568-141">**Physicaladressen**</span><span class="sxs-lookup"><span data-stu-id="38568-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="38568-142">Gibt einen Vektor physischer Adressen zurück.</span><span class="sxs-lookup"><span data-stu-id="38568-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="38568-143">**Presentationurl**</span><span class="sxs-lookup"><span data-stu-id="38568-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="38568-144">Ruft die Präsentations-URL des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="38568-145">**Remotestreamingurls**</span><span class="sxs-lookup"><span data-stu-id="38568-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="38568-146">Gibt einen Vektor von Remotestreaming-URLs zurück.</span><span class="sxs-lookup"><span data-stu-id="38568-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="38568-147">**\_connectionstatuschge entfernen**</span><span class="sxs-lookup"><span data-stu-id="38568-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="38568-148">Hebt die Registrierung eines Ereignis Handlers für das [**connectionstatuschge**](connectionstatuschanged.md) -Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="38568-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="38568-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="38568-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="38568-150">Ruft die Seriennummer des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="38568-151">**type**</span><span class="sxs-lookup"><span data-stu-id="38568-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="38568-152">Ruft einen Enumerationswert ab, der den Gerätetyp des DLNA-Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="38568-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="38568-153">**Uniquedevicename**</span><span class="sxs-lookup"><span data-stu-id="38568-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="38568-154">Ruft den eindeutigen Gerätenamen (User Name, udn) des Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="38568-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="38568-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38568-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38568-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="38568-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

