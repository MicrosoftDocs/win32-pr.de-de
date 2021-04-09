---
title: Count. Width-Eigenschaft
description: Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest
ms.assetid: 1f5c1e74-18d4-4005-b83f-bf7265d356cb
keywords:
- Width-Eigenschaft (Sysmon)
- Width-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Width-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Width
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e67892f9e4cf6799f1b9311bb2cd47ec02744cb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741785"
---
# <a name="counteritemwidth-property"></a><span data-ttu-id="61bc5-106">Count. Width-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="61bc5-106">CounterItem.Width property</span></span>

<span data-ttu-id="61bc5-107">Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest</span><span class="sxs-lookup"><span data-stu-id="61bc5-107">Retrieves or sets the line width used to graph the counter value.</span></span>

<span data-ttu-id="61bc5-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="61bc5-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="61bc5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="61bc5-109">Syntax</span></span>


```VB
Property Width As Long
```



## <a name="property-value"></a><span data-ttu-id="61bc5-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="61bc5-110">Property value</span></span>

<span data-ttu-id="61bc5-111">In einem Liniendiagramm verwendete Linienstärke.</span><span class="sxs-lookup"><span data-stu-id="61bc5-111">Line width used in a line graph.</span></span> <span data-ttu-id="61bc5-112">Gültige Werte reichen von 1 bis 3, wobei 1 (der Standardwert) die enge Breite ist.</span><span class="sxs-lookup"><span data-stu-id="61bc5-112">Valid values range from 1 to 3, where 1 (the default value) is the narrowest width.</span></span>

<span data-ttu-id="61bc5-113">**Vor Windows Vista:** Gültige Werte liegen zwischen 1 und 9.</span><span class="sxs-lookup"><span data-stu-id="61bc5-113">**Prior to Windows Vista:** Valid values range from 1 to 9.</span></span> <span data-ttu-id="61bc5-114">Verwenden Sie keinen Wert für die Breite, der größer als 3 ist, wenn Ihre Anwendung unter Windows Vista ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61bc5-114">Do not use a width value greater than 3 if your application will be run on Windows Vista.</span></span>

## <a name="exceptions"></a><span data-ttu-id="61bc5-115">Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="61bc5-115">Exceptions</span></span>



| <span data-ttu-id="61bc5-116">Ausnahmetyp</span><span class="sxs-lookup"><span data-stu-id="61bc5-116">Exception type</span></span>               | <span data-ttu-id="61bc5-117">Bedingung</span><span class="sxs-lookup"><span data-stu-id="61bc5-117">Condition</span></span>                              |
|------------------------------|----------------------------------------|
| <span data-ttu-id="61bc5-118">**System.ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="61bc5-118">**System.ArgumentException**</span></span> | <span data-ttu-id="61bc5-119">Die angegebene Zeilenbreite ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61bc5-119">The specified line width is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="61bc5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61bc5-120">Remarks</span></span>

<span data-ttu-id="61bc5-121">Die Standardlinien Stärke für die ersten 16 Leistungsindikatoren, die Sie hinzufügen, ist 1.</span><span class="sxs-lookup"><span data-stu-id="61bc5-121">The default line width for the first sixteen counters that you add is 1.</span></span> <span data-ttu-id="61bc5-122">Die Standardlinienbreite für die nächsten 16 Leistungsindikatoren (Zähler 17-32), die Sie hinzufügen, ist 2.</span><span class="sxs-lookup"><span data-stu-id="61bc5-122">The default line width for the next sixteen counters (counters 17 - 32) that you add is 2.</span></span> <span data-ttu-id="61bc5-123">Die Standardlinienbreite für die nächsten 16 Leistungsindikatoren (Zähler 33-48), die Sie hinzufügen, ist 3.</span><span class="sxs-lookup"><span data-stu-id="61bc5-123">The default line width for the next sixteen counters (counters 33 - 48) that you add is 3.</span></span> <span data-ttu-id="61bc5-124">Danach wählt sysmon die Linienbreite nach dem Zufallsprinzip aus.</span><span class="sxs-lookup"><span data-stu-id="61bc5-124">After that, SYSMON randomly chooses the line width.</span></span> <span data-ttu-id="61bc5-125">Weitere Informationen finden Sie unter " [**ratteritem. Color**](counteritem-color.md)".</span><span class="sxs-lookup"><span data-stu-id="61bc5-125">For details, see [**CounterItem.Color**](counteritem-color.md).</span></span>

<span data-ttu-id="61bc5-126">Um einen anderen [**Linienstil**](counteritem-linestyle.md) als Solid anzugeben, muss die Breite 1 lauten.</span><span class="sxs-lookup"><span data-stu-id="61bc5-126">To specify a [**line style**](counteritem-linestyle.md) other than solid, the width must be 1.</span></span> <span data-ttu-id="61bc5-127">Wenn Sie einen Wert größer als 1 angeben und einen nicht einstufigen Linienstil angeben, ignoriert sysmon die angegebene Linienbreite.</span><span class="sxs-lookup"><span data-stu-id="61bc5-127">If you specify a value greater than 1 and specify a non-solid line style, SYSMON ignores the specified line width.</span></span>

## <a name="requirements"></a><span data-ttu-id="61bc5-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61bc5-128">Requirements</span></span>



| <span data-ttu-id="61bc5-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61bc5-129">Requirement</span></span> | <span data-ttu-id="61bc5-130">Wert</span><span class="sxs-lookup"><span data-stu-id="61bc5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61bc5-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61bc5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="61bc5-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61bc5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61bc5-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61bc5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="61bc5-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="61bc5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61bc5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="61bc5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61bc5-136"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="61bc5-136"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61bc5-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61bc5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61bc5-138">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="61bc5-138">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





