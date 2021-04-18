---
description: Das safewia-Objekt ist ein &\# 0034; Safe for Scripting&\# 0034; der Einstiegspunkt für alle Funktionen zur WIA-Skripterstellung (Windows Image Acquisition).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Safewia-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345075"
---
# <a name="safewia-object"></a><span data-ttu-id="52f64-103">Safewia-Objekt</span><span class="sxs-lookup"><span data-stu-id="52f64-103">SafeWia object</span></span>

<span data-ttu-id="52f64-104">Das **safewia** -Objekt ist der Einstiegspunkt "sicher für Skripting" für alle Skriptfunktionen für die Windows-Abbild Erfassung (WIA).</span><span class="sxs-lookup"><span data-stu-id="52f64-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="52f64-105">Jede Anwendung, die das WIA-Skript Modell verwendet, muss ein **safewia** -oder [**WIA**](-wia-wia.md) -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="52f64-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="52f64-106">Verwenden Sie dieses Objekt zum Auflisten und Erstellen von Geräten sowie zum Empfangen von Benachrichtigungen über Hardware Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="52f64-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="52f64-107">Member</span><span class="sxs-lookup"><span data-stu-id="52f64-107">Members</span></span>

<span data-ttu-id="52f64-108">Das **safewia** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="52f64-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="52f64-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="52f64-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="52f64-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52f64-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="52f64-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="52f64-111">Methods</span></span>

<span data-ttu-id="52f64-112">Das **safewia** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="52f64-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="52f64-113">Methode</span><span class="sxs-lookup"><span data-stu-id="52f64-113">Method</span></span>                             | <span data-ttu-id="52f64-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52f64-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52f64-115">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="52f64-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="52f64-116">Die [**Create**](-wia-iwia-create.md) -Methode des [**WIA**](-wia-wia.md) -Objekts stellt eine Verbindung mit dem angegebenen WIA-Gerät her und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="52f64-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="52f64-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52f64-117">Properties</span></span>

<span data-ttu-id="52f64-118">Das **safewia** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="52f64-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="52f64-119">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="52f64-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="52f64-120">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="52f64-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="52f64-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52f64-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="52f64-122"><a href="-wia-iwia-devices.md"><strong>Geräte</strong></a></span><span class="sxs-lookup"><span data-stu-id="52f64-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="52f64-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="52f64-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="52f64-124">Sammlung von " <a href="-wia-deviceinfo.md"><strong>de viceinfo</strong></a> "-Objekten, die alle auf dem Computer installierten Geräte darstellen.</span><span class="sxs-lookup"><span data-stu-id="52f64-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="52f64-125">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="52f64-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="52f64-126">Diese Auflistung ist 0-basiert.</span><span class="sxs-lookup"><span data-stu-id="52f64-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="52f64-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52f64-127">Requirements</span></span>



| <span data-ttu-id="52f64-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52f64-128">Requirement</span></span> | <span data-ttu-id="52f64-129">Wert</span><span class="sxs-lookup"><span data-stu-id="52f64-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f64-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52f64-130">Minimum supported client</span></span><br/> | <span data-ttu-id="52f64-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52f64-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52f64-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52f64-132">Minimum supported server</span></span><br/> | <span data-ttu-id="52f64-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52f64-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="52f64-134">DLL</span><span class="sxs-lookup"><span data-stu-id="52f64-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52f64-135"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="52f64-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="52f64-136">IID</span><span class="sxs-lookup"><span data-stu-id="52f64-136">IID</span></span><br/>                      | <span data-ttu-id="52f64-137">CLSID \_ safewia</span><span class="sxs-lookup"><span data-stu-id="52f64-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="52f64-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52f64-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f64-139">**WIA**</span><span class="sxs-lookup"><span data-stu-id="52f64-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




