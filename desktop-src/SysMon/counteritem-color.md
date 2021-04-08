---
title: Count. Color-Eigenschaft
description: Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.
ms.assetid: 73630efc-3128-4db5-b64c-ebb2f5e7611a
keywords:
- Color-Eigenschaft (Sysmon)
- Color-Eigenschaft (Sysmon), ratteritem-Klasse
- Namteritem Class sysmon, Color-Eigenschaft
topic_type:
- apiref
api_name:
- CounterItem.Color
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ada0a2266c4cf53e9706f1330e2336e6a38386b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741920"
---
# <a name="counteritemcolor-property"></a><span data-ttu-id="df075-106">Count. Color-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="df075-106">CounterItem.Color property</span></span>

<span data-ttu-id="df075-107">Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df075-107">Retrieves or sets the color used to graph the counter value.</span></span>

<span data-ttu-id="df075-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="df075-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="df075-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="df075-109">Syntax</span></span>


```VB
Property Color As stdole.OLE_COLOR
```



## <a name="property-value"></a><span data-ttu-id="df075-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="df075-110">Property value</span></span>

<span data-ttu-id="df075-111">Die zum Diagramm des Leistungs Zählers verwendete Farbe.</span><span class="sxs-lookup"><span data-stu-id="df075-111">Color used to graph the counter value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df075-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df075-112">Remarks</span></span>

<span data-ttu-id="df075-113">Wenn Sie die zu verwendende Farbe nicht angeben, wählt sysmon Farben für die ersten 16 Indikatoren aus.</span><span class="sxs-lookup"><span data-stu-id="df075-113">If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="df075-114">Wenn Sie mehr als sechzehn Zähler angeben, werden die gleichen Farben von sysmon von den ersten 16 Leistungsindikatoren wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="df075-114">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="df075-115">Um die Indikatoren voneinander zu unterscheiden, ändert sysmon den [**Linienstil**](counteritem-linestyle.md) , der für jedes Vielfache von sechzehn Leistungsindikatoren verwendet wird, bis zu den ersten 80-Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="df075-115">To help distinguish the counters from one another, SYSMON changes the [**line style**](counteritem-linestyle.md) used for each multiple of sixteen counters up to the first 80 counters.</span></span> <span data-ttu-id="df075-116">Beispielsweise verwenden die ersten 16 Indikatoren eine solide Linienart, die nächsten sechzehn einen Strich Linienstil usw.</span><span class="sxs-lookup"><span data-stu-id="df075-116">For example, the first sixteen counters use a solid line style, the next sixteen use a dash line style, and so on.</span></span> <span data-ttu-id="df075-117">Sysmon legt dann die [**Linien**](counteritem-width.md) Stärke auf 2 für die Leistungsindikatoren 81-96 und auf 3 für die Zähler 96-112 fest.</span><span class="sxs-lookup"><span data-stu-id="df075-117">SYSMON then sets the [**line width**](counteritem-width.md) to 2 for counters 81 - 96 and to 3 for counters 96 - 112.</span></span> <span data-ttu-id="df075-118">Wenn die Sammlung mehr als 112 Leistungsindikatoren enthält, enthalten die Indikatoren doppelte Werte für Farbe, Linienart und Breite.</span><span class="sxs-lookup"><span data-stu-id="df075-118">If the collection contains more than 112 counters, the counters will contain duplicate color, line style, and width values.</span></span>

<span data-ttu-id="df075-119">**Vor Windows Vista:** Wenn Sie die zu verwendende Farbe nicht angeben, wählt sysmon Farben für die ersten 16 Indikatoren aus.</span><span class="sxs-lookup"><span data-stu-id="df075-119">**Prior to Windows Vista:** If you do not specify the color to use, SYSMON selects colors for the first sixteen counters.</span></span> <span data-ttu-id="df075-120">Wenn Sie mehr als sechzehn Zähler angeben, werden die gleichen Farben von sysmon von den ersten 16 Leistungsindikatoren wieder verwendet.</span><span class="sxs-lookup"><span data-stu-id="df075-120">If you specify more than sixteen counters, SYSMON will reuse the same colors from the first sixteen counters.</span></span> <span data-ttu-id="df075-121">Zur besseren Unterscheidung der Leistungsindikatoren erhöht sysmon die [**Linien**](counteritem-width.md) Stärke der ersten drei Leistungsindikatoren, die die gleiche Farb Zuweisung erhalten.</span><span class="sxs-lookup"><span data-stu-id="df075-121">To help distinguish the counters from one another, SYSMON increases the [**line width**](counteritem-width.md) of the first three counters that receive the same color assignment.</span></span> <span data-ttu-id="df075-122">Wenn mehr als drei Leistungsindikatoren dieselbe Farbe verwenden, wählt sysmon die für den Indikator zu verwendende Linienbreite nach dem Zufallsprinzip aus.</span><span class="sxs-lookup"><span data-stu-id="df075-122">If more than three counters use the same color, SYSMON randomly chooses the line width to use for the counter.</span></span>

## <a name="requirements"></a><span data-ttu-id="df075-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df075-123">Requirements</span></span>



| <span data-ttu-id="df075-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df075-124">Requirement</span></span> | <span data-ttu-id="df075-125">Wert</span><span class="sxs-lookup"><span data-stu-id="df075-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df075-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df075-126">Minimum supported client</span></span><br/> | <span data-ttu-id="df075-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df075-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="df075-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df075-128">Minimum supported server</span></span><br/> | <span data-ttu-id="df075-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df075-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df075-130">DLL</span><span class="sxs-lookup"><span data-stu-id="df075-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df075-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="df075-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df075-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df075-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df075-133">**Ratteritem**</span><span class="sxs-lookup"><span data-stu-id="df075-133">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





