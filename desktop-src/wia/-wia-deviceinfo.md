---
description: Das deviceInfo-Objekt ermöglicht den Zugriff auf die Eigenschaften eines Windows-Abbild Erfassungs Hardware Geräts (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Debug-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368758"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="42971-103">Debug-Objekt</span><span class="sxs-lookup"><span data-stu-id="42971-103">DeviceInfo object</span></span>

<span data-ttu-id="42971-104">Das **deviceInfo** -Objekt ermöglicht den Zugriff auf die Eigenschaften eines Windows-Abbild Erfassungs Hardware Geräts (WIA).</span><span class="sxs-lookup"><span data-stu-id="42971-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="42971-105">Außerdem bietet es mithilfe der [**Create**](-wia-iwiadeviceinfo-create.md) -Methode eine Möglichkeit für die Anwendung oder das Skript, eine Verbindung mit dem Gerät herzustellen und ein [**Element**](-wia-item.md) Objekt abzurufen, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="42971-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="42971-106">Verwenden Sie die [**Devices**](-wia-iwia-devices.md) -Methode, um eine Sammlung von **deviceInfo** -Objekten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42971-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="42971-107">Member</span><span class="sxs-lookup"><span data-stu-id="42971-107">Members</span></span>

<span data-ttu-id="42971-108">Das Objekt " **de viceinfo** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="42971-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="42971-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="42971-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="42971-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42971-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="42971-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="42971-111">Methods</span></span>

<span data-ttu-id="42971-112">Das **deviceInfo** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="42971-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="42971-113">Methode</span><span class="sxs-lookup"><span data-stu-id="42971-113">Method</span></span>                                                 | <span data-ttu-id="42971-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42971-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42971-115">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="42971-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="42971-116">Die [**Create**](-wia-iwiadeviceinfo-create.md) -Methode des **deviceInfo** -Objekts stellt eine Verbindung mit dem WIA-Gerät her, das durch das **deviceInfo** -Objekt angegeben wird, und gibt ein [**Element**](-wia-item.md) Objekt zurück, das das Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="42971-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="42971-117">**Getpropbyid**</span><span class="sxs-lookup"><span data-stu-id="42971-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="42971-118">Die [**getpropbyid**](-wia-iwiadeviceinfo-getpropbyid.md) -Methode des **deviceInfo** -Objekts verwendet die ID einer Geräte Eigenschaft, um ihren Wert zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="42971-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="42971-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="42971-119">Properties</span></span>

<span data-ttu-id="42971-120">Das Objekt " **de viceinfo** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="42971-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="42971-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="42971-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="42971-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="42971-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="42971-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42971-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="42971-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Name</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-126">Ruft die ID des WIA-Hardware Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="42971-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="42971-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Hersteller</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-129">Ruft den Namen des Herstellers dieses Hardware Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="42971-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="42971-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-132">Der Name des WIA-Hardware Geräts, wie er in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="42971-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="42971-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-134">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-135">Ruft den Port ab, mit dem das WIA-Hardware Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="42971-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="42971-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>type</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-137">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-138">Ruft den Typ des WIA-Hardware Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="42971-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="42971-139">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="42971-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="42971-140">Digitalcamera</span><span class="sxs-lookup"><span data-stu-id="42971-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="42971-141">Scanner</span><span class="sxs-lookup"><span data-stu-id="42971-141">Scanner</span></span></li>
<li><span data-ttu-id="42971-142">Streamingvideo</span><span class="sxs-lookup"><span data-stu-id="42971-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="42971-143">Standard</span><span class="sxs-lookup"><span data-stu-id="42971-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="42971-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>Uiclsid</strong></a></span><span class="sxs-lookup"><span data-stu-id="42971-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-145">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="42971-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="42971-146">Ruft die Klassen-ID der vom Hersteller bereitgestellten Benutzeroberfläche für dieses WIA-Hardware Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="42971-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="42971-147">Der Wert ist eine Zeichen folgen Darstellung einer GUID.</span><span class="sxs-lookup"><span data-stu-id="42971-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="42971-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42971-148">Requirements</span></span>



| <span data-ttu-id="42971-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42971-149">Requirement</span></span> | <span data-ttu-id="42971-150">Wert</span><span class="sxs-lookup"><span data-stu-id="42971-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42971-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42971-151">Minimum supported client</span></span><br/> | <span data-ttu-id="42971-152">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42971-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42971-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42971-153">Minimum supported server</span></span><br/> | <span data-ttu-id="42971-154">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42971-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="42971-155">DLL</span><span class="sxs-lookup"><span data-stu-id="42971-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42971-156"><dt>Wiascr.dll (Version 4,90 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="42971-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




