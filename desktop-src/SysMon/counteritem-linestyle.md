---
title: Count. LineStyle-Eigenschaft
description: Ruft den Linienstil zum Diagramm des Leistungsindikators ab oder legt diesen fest.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- LineStyle-Eigenschaft (Sysmon)
- LineStyle-Eigenschaft "sysmon", "count"-Klasse
- Namteritem Class sysmon, LineStyle-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956429"
---
# <a name="counteritemlinestyle-property"></a><span data-ttu-id="6f4c0-106">Count. LineStyle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6f4c0-106">CounterItem.LineStyle property</span></span>

<span data-ttu-id="6f4c0-107">Ruft den Linienstil zum Diagramm des Leistungsindikators ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-107">Retrieves or sets the line style used to graph the counter value.</span></span>

<span data-ttu-id="6f4c0-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4c0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f4c0-109">Syntax</span></span>


```VB
Property LineStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="6f4c0-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6f4c0-110">Property value</span></span>

<span data-ttu-id="6f4c0-111">Der Linienstil, der zum Diagramm des Leistungs Zählers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-111">The line style used to graph the counter value.</span></span> <span data-ttu-id="6f4c0-112">Die Werte entsprechen den in der folgenden Tabelle dargestellten System Konstanten.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-112">The values correspond to system constants shown in the following table.</span></span>



| <span data-ttu-id="6f4c0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6f4c0-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="6f4c0-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f4c0-114">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <span data-ttu-id="6f4c0-115"><dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-115"><dt>**System.Drawing.Drawing2D.DashStyle.Solid**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="6f4c0-116">Durchgehende Linie.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-116">Solid line.</span></span> <span data-ttu-id="6f4c0-117">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-117">This is the default value.</span></span><br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <span data-ttu-id="6f4c0-118"><dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-118"><dt>**System.Drawing.Drawing2D.DashStyle.Dash**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="6f4c0-119">Gepunktete Linie mit langen Segmenten und schmalen Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-119">Dotted line with long segments and narrow spaces.</span></span><br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <span data-ttu-id="6f4c0-120"><dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-120"><dt>**System.Drawing.Drawing2D.DashStyle.Dot**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="6f4c0-121">Gepunktete Linie mit einheitlichen Segmenten und Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-121">Dotted line with uniform segments and spaces.</span></span><br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <span data-ttu-id="6f4c0-122"><dt>**System. Drawing. Drawing2D. DashStyle. DashDot**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-122"><dt>**System.Drawing.Drawing2D.DashStyle.DashDot**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="6f4c0-123">Gepunktete Linie mit abwechselnden kurzen und langen Segmenten.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-123">Dotted line with alternating short and long segments.</span></span><br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <span data-ttu-id="6f4c0-124"><dt>**System. Drawing. Drawing2D. DashStyle. DashDotDot**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-124"><dt>**System.Drawing.Drawing2D.DashStyle.DashDotDot**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="6f4c0-125">Gepunktete Linie mit abwechselnden Bindestrichen und doppelten Punkten.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-125">Dotted line with alternating dashes and double dots.</span></span><br/>  |



 

## <a name="exceptions"></a><span data-ttu-id="6f4c0-126">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="6f4c0-126">Exceptions</span></span>



| <span data-ttu-id="6f4c0-127">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="6f4c0-127">Exception type</span></span>               | <span data-ttu-id="6f4c0-128">Bedingung</span><span class="sxs-lookup"><span data-stu-id="6f4c0-128">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="6f4c0-129">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="6f4c0-129">**System.ArgumentException**</span></span> | <span data-ttu-id="6f4c0-130">Die angegebene Linienart ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-130">The specified line style is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6f4c0-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f4c0-131">Remarks</span></span>

<span data-ttu-id="6f4c0-132">Um einen anderen Wert als "DashStyle. Solid" anzugeben, muss " [**count. Width**](counteritem-width.md) " auf 1 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-132">To specify a value other than DashStyle.Solid, [**CounterItem.Width**](counteritem-width.md) must be set to 1.</span></span> <span data-ttu-id="6f4c0-133">Wenn die Breite größer als 1 ist, ignoriert sysmon die angegebene Linienart und verwendet DashStyle. Solid.</span><span class="sxs-lookup"><span data-stu-id="6f4c0-133">If the width is greater than 1, SYSMON ignores the specified line style and uses DashStyle.Solid.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f4c0-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f4c0-134">Requirements</span></span>



| <span data-ttu-id="6f4c0-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f4c0-135">Requirement</span></span> | <span data-ttu-id="6f4c0-136">Wert</span><span class="sxs-lookup"><span data-stu-id="6f4c0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f4c0-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f4c0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6f4c0-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f4c0-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6f4c0-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f4c0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6f4c0-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f4c0-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f4c0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4c0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f4c0-142"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6f4c0-142"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f4c0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f4c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f4c0-144">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="6f4c0-144">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





