---
description: Die folgenden Konstanten bilden den Satz gültiger Hardware Geräte Befehle zur Windows-Abbild Beschaffung (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: WIA-Geräte Befehle (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862667"
---
# <a name="wia-device-commands"></a><span data-ttu-id="a167f-103">WIA-Geräte Befehle</span><span class="sxs-lookup"><span data-stu-id="a167f-103">WIA Device Commands</span></span>

<span data-ttu-id="a167f-104">Die folgenden Konstanten bilden den Satz gültiger Hardware Geräte Befehle zur Windows-Abbild Beschaffung (WIA).</span><span class="sxs-lookup"><span data-stu-id="a167f-104">The following constants form the set of valid Windows Image Acquisition (WIA) hardware device commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="a167f-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="a167f-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="a167f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a167f-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <span data-ttu-id="a167f-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-107"><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-108">Bewirkt, dass der Mini Treiber des Geräts zwischengespeicherte Elemente mit dem Hardware Gerät synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="a167f-108">Causes the device's minidriver to synchronize cached items with the hardware device.</span></span> <span data-ttu-id="a167f-109">Wenn das Gerät die <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>iwiaitem:: analyzeitem</strong></a> -Methode unterstützt, bewirkt die Ausgabe dieses Befehls, dass der Mini Treiber die Analyseergebnisse verworfen und das Element in seinen ursprünglichen Zustand zurücksetzt.</span><span class="sxs-lookup"><span data-stu-id="a167f-109">If the device supports the <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem</strong></a> method, issuing this command causes the minidriver to discard the analysis results and reset the item to its initial state.</span></span> <span data-ttu-id="a167f-110">Alle Treiber müssen diesen Befehl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a167f-110">All drivers must support this command.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <span data-ttu-id="a167f-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-111"><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-112">Bewirkt, dass ein WIA-Gerät ein Image aberhält.</span><span class="sxs-lookup"><span data-stu-id="a167f-112">Causes a WIA device to acquire an image.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <span data-ttu-id="a167f-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-113"><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-114">Weist das Gerät an, alle Elemente zu löschen, die aus der Struktur von <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Objekten, die das Gerät darstellen, gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="a167f-114">Tells the device to delete all items that can be deleted from the tree of <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> objects that represent the device.</span></span> <span data-ttu-id="a167f-115">Das Löschen von Elementen wird verhindert, indem die Eigenschaften des Elements festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a167f-115">Item deletion is prevented by setting the item's properties.</span></span> <span data-ttu-id="a167f-116">Weitere Informationen finden Sie unter <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>iwiapropertystorage:: setpropertystream</strong></a> und <a href="-wia-property-attributes.md">Property-Attribute</a>.</span><span class="sxs-lookup"><span data-stu-id="a167f-116">For details, see <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage::SetPropertyStream</strong></a> and <a href="-wia-property-attributes.md">Property Attributes</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <span data-ttu-id="a167f-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-117"><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-118">Wird für Dokument Scanner verwendet.</span><span class="sxs-lookup"><span data-stu-id="a167f-118">Used for document scanners.</span></span> <span data-ttu-id="a167f-119">Bewirkt, dass der Scanner die nächste Seite in seinem Dokument Handler lädt.</span><span class="sxs-lookup"><span data-stu-id="a167f-119">Causes the scanner to load the next page in its document handler.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <span data-ttu-id="a167f-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-120"><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-121">Wird für Dokument Scanner verwendet.</span><span class="sxs-lookup"><span data-stu-id="a167f-121">Used for document scanners.</span></span> <span data-ttu-id="a167f-122">Weist das Gerät an, alle verbleibenden Seiten im Dokument Handler zu entladen.</span><span class="sxs-lookup"><span data-stu-id="a167f-122">Tells the device to unload all remaining pages in its document handler.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <span data-ttu-id="a167f-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-123"><dt><strong>WIA_CMD_START_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-124">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen.</span><span class="sxs-lookup"><span data-stu-id="a167f-124">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="a167f-125">Weist das Gerät an, den feedermotor zu starten.</span><span class="sxs-lookup"><span data-stu-id="a167f-125">Tells the device to start the feeder motor.</span></span> <span data-ttu-id="a167f-126">Diese Funktion ist ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a167f-126">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a167f-127">Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a167f-127">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <span data-ttu-id="a167f-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-128"><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-129">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen.</span><span class="sxs-lookup"><span data-stu-id="a167f-129">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="a167f-130">Weist das Gerät an, den feedermotor anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a167f-130">Tells the device to stop the feeder motor.</span></span> <span data-ttu-id="a167f-131">Diese Funktion ist ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a167f-131">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a167f-132">Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL</strong> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a167f-132">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <span data-ttu-id="a167f-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="a167f-133"><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="a167f-134">Wird für Dokument Scanner verwendet, die über einen Seiten feedertyp verfügen.</span><span class="sxs-lookup"><span data-stu-id="a167f-134">Used for document scanners that have a page feeder.</span></span> <span data-ttu-id="a167f-135">Weist das Gerät an, den feedermotor anzuhalten.</span><span class="sxs-lookup"><span data-stu-id="a167f-135">Tells the device to pause the feeder motor.</span></span> <span data-ttu-id="a167f-136">Diese Funktion ist ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a167f-136">This feature is available starting with Windows 8.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a167f-137">Der WIA-Mini Treiber muss diesen Befehl ablehnen und <strong>WIA_ERROR_INVALID_COMMAND</strong> zurückgeben, wenn die <strong>WIA_IPS_FEEDER_CONTROL</strong> -Eigenschaft nicht unterstützt wird oder auf WIA_FEEDER_CONTROL_AUTO festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a167f-137">The WIA minidriver must reject this command and return <strong>WIA_ERROR_INVALID_COMMAND</strong> when the <strong>WIA_IPS_FEEDER_CONTROL</strong> property is not supported, or is set to WIA_FEEDER_CONTROL_AUTO.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="a167f-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a167f-138">Requirements</span></span>



| <span data-ttu-id="a167f-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a167f-139">Requirement</span></span> | <span data-ttu-id="a167f-140">Wert</span><span class="sxs-lookup"><span data-stu-id="a167f-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a167f-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a167f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a167f-142">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a167f-142">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a167f-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a167f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a167f-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a167f-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a167f-145">Header</span><span class="sxs-lookup"><span data-stu-id="a167f-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a167f-146"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="a167f-146"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
