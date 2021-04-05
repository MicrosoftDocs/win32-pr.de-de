---
title: Systemmonitor. hervorzuheben (Eigenschaft)
description: Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben sind, oder legt diesen fest.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Eigenschaften-sysmon hervorheben
- Eigenschaften-sysmon, Systemmonitor-Klasse hervorheben
- Systemmonitor-Klasse (Sysmon), Eigenschaft hervorheben
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858916"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="17a01-106">Systemmonitor. hervorzuheben (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="17a01-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="17a01-107">Ruft einen Wert ab, der angibt, ob die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben sind, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="17a01-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="17a01-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="17a01-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="17a01-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="17a01-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="17a01-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="17a01-110">Property value</span></span>

<span data-ttu-id="17a01-111">True gibt an, dass die Werte der ausgewählten Indikatoren im Diagramm hervorgehoben werden. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="17a01-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="17a01-112">Der Standardwert ist False.</span><span class="sxs-lookup"><span data-stu-id="17a01-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="17a01-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17a01-113">Remarks</span></span>

<span data-ttu-id="17a01-114">Wenn Sie einen oder mehrere Leistungsindikatoren auswählen möchten, können [**Sie als "true" festlegen,**](counteritem-selected.md) oder der Benutzer kann die Indikatoren aus der Liste der in der Legende angezeigten Indikatoren auswählen.</span><span class="sxs-lookup"><span data-stu-id="17a01-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="17a01-115">**Vor Windows Vista:** Leistungsindikatoren können nicht Programm gesteuert ausgewählt werden, und der Benutzer kann nur einen Indikator aus der Liste der in der Legende angezeigten Indikatoren auswählen.</span><span class="sxs-lookup"><span data-stu-id="17a01-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="17a01-116">Die Hervorhebung kann abhängig vom Wert der [**BackColor**](systemmonitor-backcolor.md) -Eigenschaft schwarz oder weiß sein.</span><span class="sxs-lookup"><span data-stu-id="17a01-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="17a01-117">Die Hervorhebung wird automatisch auf die Farbe festgelegt, die einen ausreichenden Kontrast zwischen Hervorhebungs Farbe und Hintergrundfarbe bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="17a01-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="17a01-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17a01-118">Requirements</span></span>



| <span data-ttu-id="17a01-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17a01-119">Requirement</span></span> | <span data-ttu-id="17a01-120">Wert</span><span class="sxs-lookup"><span data-stu-id="17a01-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17a01-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17a01-121">Minimum supported client</span></span><br/> | <span data-ttu-id="17a01-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17a01-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="17a01-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17a01-123">Minimum supported server</span></span><br/> | <span data-ttu-id="17a01-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17a01-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17a01-125">DLL</span><span class="sxs-lookup"><span data-stu-id="17a01-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17a01-126"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="17a01-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17a01-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17a01-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17a01-128">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="17a01-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="17a01-129">**"Zählelement. ausgewählt"**</span><span class="sxs-lookup"><span data-stu-id="17a01-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





