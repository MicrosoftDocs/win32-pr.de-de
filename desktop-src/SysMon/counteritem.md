---
title: Zählelement-Objekt (isysmon. h)
description: Verwenden Sie diese Klasse, um den Pfad und den Wert eines Zählers abzurufen und die Farbe anzugeben, die zum Diagramm des Zählers verwendet wird. Um dieses Objekt abzurufen, rufen Sie Counters. Item auf.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Initialisiererobjekt-sysmon
- Objekt-sysmon, beschrieben
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741913"
---
# <a name="counteritem-object"></a><span data-ttu-id="909c1-106">"Count"-Objekt</span><span class="sxs-lookup"><span data-stu-id="909c1-106">CounterItem object</span></span>

<span data-ttu-id="909c1-107">Verwenden Sie diese Klasse, um den Pfad und den Wert eines Zählers abzurufen und die Farbe anzugeben, die zum Diagramm des Zählers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="909c1-107">Use this class to retrieve the path and value of a counter and to specify the color used to graph the counter.</span></span>

<span data-ttu-id="909c1-108">Um dieses Objekt abzurufen, rufen Sie [**Counters. Item**](counters-item.md)auf.</span><span class="sxs-lookup"><span data-stu-id="909c1-108">To retrieve this object, call [**Counters.Item**](counters-item.md).</span></span>

## <a name="members"></a><span data-ttu-id="909c1-109">Member</span><span class="sxs-lookup"><span data-stu-id="909c1-109">Members</span></span>

<span data-ttu-id="909c1-110">Das **ratteritem** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="909c1-110">The **CounterItem** object has these types of members:</span></span>

-   [<span data-ttu-id="909c1-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="909c1-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="909c1-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="909c1-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="909c1-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="909c1-113">Methods</span></span>

<span data-ttu-id="909c1-114">Das **ratteritem** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="909c1-114">The **CounterItem** object has these methods.</span></span>



| <span data-ttu-id="909c1-115">Methode</span><span class="sxs-lookup"><span data-stu-id="909c1-115">Method</span></span>                                             | <span data-ttu-id="909c1-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="909c1-116">Description</span></span>                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="909c1-117">**Getdataat**</span><span class="sxs-lookup"><span data-stu-id="909c1-117">**GetDataAt**</span></span>](counteritem-getdataat.md)         | <span data-ttu-id="909c1-118">Ruft die Daten des Zählers von einem bestimmten Punkt im Liniendiagramm ab.</span><span class="sxs-lookup"><span data-stu-id="909c1-118">Retrieves the counter data from a specific point in the line graph.</span></span><br/> |
| [<span data-ttu-id="909c1-119">**Getstatistics**</span><span class="sxs-lookup"><span data-stu-id="909c1-119">**GetStatistics**</span></span>](counteritem-getstatistics.md) | <span data-ttu-id="909c1-120">Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="909c1-120">Retrieves the average, maximum, and minimum values for the counter.</span></span><br/> |
| [<span data-ttu-id="909c1-121">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="909c1-121">**GetValue**</span></span>](counteritem-getvalue.md)           | <span data-ttu-id="909c1-122">Ruft den letzten Wert des Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="909c1-122">Retrieves the last value of the counter.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="909c1-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="909c1-123">Properties</span></span>

<span data-ttu-id="909c1-124">Das **ratteritem** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="909c1-124">The **CounterItem** object has these properties.</span></span>



| <span data-ttu-id="909c1-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="909c1-125">Property</span></span>                                                  | <span data-ttu-id="909c1-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="909c1-126">Description</span></span>                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="909c1-127">**Farbe**</span><span class="sxs-lookup"><span data-stu-id="909c1-127">**Color**</span></span>](counteritem-color.md)<br/>             | <span data-ttu-id="909c1-128">Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="909c1-128">Retrieves or sets the color used to graph the counter value.</span></span><br/>         |
| [<span data-ttu-id="909c1-129">**LineStyle**</span><span class="sxs-lookup"><span data-stu-id="909c1-129">**LineStyle**</span></span>](counteritem-linestyle.md)<br/>     | <span data-ttu-id="909c1-130">Ruft den Linienstil zum Diagramm des Leistungsindikators ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="909c1-130">Retrieves or sets the line style used to graph the counter value.</span></span><br/>    |
| [<span data-ttu-id="909c1-131">**ADS**</span><span class="sxs-lookup"><span data-stu-id="909c1-131">**Path**</span></span>](counteritem-path.md)<br/>               | <span data-ttu-id="909c1-132">Ruft den Pfad des Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="909c1-132">Retrieves the path of the counter.</span></span><br/>                                   |
| [<span data-ttu-id="909c1-133">**ScaleFactor**</span><span class="sxs-lookup"><span data-stu-id="909c1-133">**ScaleFactor**</span></span>](counteritem-scalefactor.md)<br/> | <span data-ttu-id="909c1-134">Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="909c1-134">Retrieves or sets the scale factor used to graph the counter value.</span></span><br/>  |
| [<span data-ttu-id="909c1-135">**Ausgewählt**</span><span class="sxs-lookup"><span data-stu-id="909c1-135">**Selected**</span></span>](counteritem-selected.md)<br/>       | <span data-ttu-id="909c1-136">Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="909c1-136">Retrieves or sets a value that indicates if the counter is selected.</span></span><br/> |
| [<span data-ttu-id="909c1-137">**Wert**</span><span class="sxs-lookup"><span data-stu-id="909c1-137">**Value**</span></span>](counteritem-value.md)<br/>             | <span data-ttu-id="909c1-138">Ruft den aktuellen Wert des Zählers ab.</span><span class="sxs-lookup"><span data-stu-id="909c1-138">Retrieves the current value of the counter.</span></span><br/>                          |
| [<span data-ttu-id="909c1-139">**Sichtbar**</span><span class="sxs-lookup"><span data-stu-id="909c1-139">**Visible**</span></span>](counteritem-visible.md)<br/>         | <span data-ttu-id="909c1-140">Ruft einen Wert ab, der angibt, ob der Leistungsindikators grafisch dargestellt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="909c1-140">Retrieves or sets a value that indicates if the counter is graphed.</span></span><br/>  |
| [<span data-ttu-id="909c1-141">**Breite**</span><span class="sxs-lookup"><span data-stu-id="909c1-141">**Width**</span></span>](counteritem-width.md)<br/>             | <span data-ttu-id="909c1-142">Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="909c1-142">Retrieves or sets the line width used to graph the counter value.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="909c1-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="909c1-143">Remarks</span></span>

<span data-ttu-id="909c1-144">[**Value**](counteritem-value.md) ist die Standard Eigenschaft von **count** Item.</span><span class="sxs-lookup"><span data-stu-id="909c1-144">[**Value**](counteritem-value.md) is the default property of **CounterItem**.</span></span>

## <a name="requirements"></a><span data-ttu-id="909c1-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="909c1-145">Requirements</span></span>



| <span data-ttu-id="909c1-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="909c1-146">Requirement</span></span> | <span data-ttu-id="909c1-147">Wert</span><span class="sxs-lookup"><span data-stu-id="909c1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="909c1-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="909c1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="909c1-149">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="909c1-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="909c1-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="909c1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="909c1-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="909c1-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="909c1-152">Header</span><span class="sxs-lookup"><span data-stu-id="909c1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="909c1-153"><dt>Isysmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="909c1-153"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="909c1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="909c1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="909c1-155"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="909c1-155"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="909c1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="909c1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="909c1-157">Sysmon-Klassen</span><span class="sxs-lookup"><span data-stu-id="909c1-157">SYSMON Classes</span></span>](sysmon-classes.md)
</dt> </dl>

 

 





