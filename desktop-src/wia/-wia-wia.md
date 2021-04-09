---
description: Das WIA-Objekt ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129380"
---
# <a name="wia-object"></a><span data-ttu-id="64635-103">WIA-Objekt</span><span class="sxs-lookup"><span data-stu-id="64635-103">Wia object</span></span>

<span data-ttu-id="64635-104">Das **WIA** -Objekt ist der Einstiegspunkt für alle WIA-Skriptfunktionen (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="64635-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="64635-105">Jede Anwendung, die das WIA-Skript Modell verwendet, muss ein [**safewia**](-wia-safewia.md) -oder **WIA** -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="64635-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="64635-106">Verwenden Sie dieses Objekt zum Auflisten und Erstellen von Geräten sowie zum Empfangen von Benachrichtigungen über Hardware Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="64635-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="64635-107">Dieses Objekt ist für die Skripterstellung nicht sicher.</span><span class="sxs-lookup"><span data-stu-id="64635-107">This object is not safe for scripting.</span></span> <span data-ttu-id="64635-108">Eine Version dieses Objekts, die für die Skripterstellung sicher ist, finden Sie unter [**safewia**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="64635-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="64635-109">Member</span><span class="sxs-lookup"><span data-stu-id="64635-109">Members</span></span>

<span data-ttu-id="64635-110">Das **WIA** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="64635-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="64635-111">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64635-111">Events</span></span>](#events)
-   [<span data-ttu-id="64635-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="64635-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="64635-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64635-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="64635-114">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="64635-114">Events</span></span>

<span data-ttu-id="64635-115">Das **WIA** -Objekt enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="64635-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="64635-116">Ereignis</span><span class="sxs-lookup"><span data-stu-id="64635-116">Event</span></span>                                                                 | <span data-ttu-id="64635-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64635-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="64635-118">**Onde viceconnected**</span><span class="sxs-lookup"><span data-stu-id="64635-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="64635-119">Das Ereignis tritt auf, wenn ein neues WIA-Hardware Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="64635-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="64635-120">**Ondevicegetrennte**</span><span class="sxs-lookup"><span data-stu-id="64635-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="64635-121">Das Ereignis tritt auf, wenn ein neues WIA-Hardware Gerät getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="64635-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="64635-122">**Ontransfercomplete**</span><span class="sxs-lookup"><span data-stu-id="64635-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="64635-123">Das Ereignis tritt auf, wenn eine Datenübertragung erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="64635-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="64635-124">Methoden</span><span class="sxs-lookup"><span data-stu-id="64635-124">Methods</span></span>

<span data-ttu-id="64635-125">Das **WIA** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="64635-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="64635-126">Methode</span><span class="sxs-lookup"><span data-stu-id="64635-126">Method</span></span>                             | <span data-ttu-id="64635-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64635-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64635-128">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="64635-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="64635-129">Die [**Create**](-wia-iwia-create.md) -Methode des **WIA** -Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="64635-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="64635-130">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="64635-130">Properties</span></span>

<span data-ttu-id="64635-131">Das **WIA** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="64635-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="64635-132">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="64635-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="64635-133">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="64635-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="64635-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64635-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="64635-135"><a href="-wia-iwia-devices.md"><strong>Geräte</strong></a></span><span class="sxs-lookup"><span data-stu-id="64635-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="64635-136">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="64635-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="64635-137">Sammlung von " <a href="-wia-deviceinfo.md"><strong>de viceinfo</strong></a> "-Objekten, die alle auf dem Computer installierten Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="64635-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="64635-138">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="64635-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="64635-139">Diese Auflistung ist 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="64635-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="64635-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64635-140">Requirements</span></span>



| <span data-ttu-id="64635-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64635-141">Requirement</span></span> | <span data-ttu-id="64635-142">Wert</span><span class="sxs-lookup"><span data-stu-id="64635-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64635-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64635-143">Minimum supported client</span></span><br/> | <span data-ttu-id="64635-144">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64635-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64635-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64635-145">Minimum supported server</span></span><br/> | <span data-ttu-id="64635-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64635-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="64635-147">DLL</span><span class="sxs-lookup"><span data-stu-id="64635-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64635-148"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="64635-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="64635-149">IID</span><span class="sxs-lookup"><span data-stu-id="64635-149">IID</span></span><br/>                      | <span data-ttu-id="64635-150">CLSID- \_ WIA</span><span class="sxs-lookup"><span data-stu-id="64635-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




