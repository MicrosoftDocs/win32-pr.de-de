---
title: Systemmonitor. MaximumScale (Eigenschaft)
description: Ruft den maximalen Wert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- MaximumScale-Eigenschaft (Sysmon)
- MaximumScale-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, MaximumScale (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37740802fac4d89bbcbe9d5c105e357b55ab481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949745"
---
# <a name="systemmonitormaximumscale-property"></a><span data-ttu-id="78a92-106">Systemmonitor. MaximumScale (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="78a92-106">SystemMonitor.MaximumScale property</span></span>

<span data-ttu-id="78a92-107">Ruft den maximalen Wert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="78a92-107">Retrieves or sets the maximum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="78a92-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="78a92-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a92-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="78a92-109">Syntax</span></span>


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="78a92-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="78a92-110">Property value</span></span>

<span data-ttu-id="78a92-111">Positiver maximaler Wert der vertikalen Achse des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="78a92-111">Positive maximum value of the vertical axis of the graph.</span></span> <span data-ttu-id="78a92-112">Der maximale Standardwert für die vertikale Skala beträgt 100.</span><span class="sxs-lookup"><span data-stu-id="78a92-112">The default maximum value of the vertical scale is 100.</span></span> <span data-ttu-id="78a92-113">Der niedrigste Wert, auf den Sie den maximalen Wert festlegen können, ist ein Wert, der größer als der [**MinimumScale**](systemmonitor-minimumscale.md) -Wert ist.</span><span class="sxs-lookup"><span data-stu-id="78a92-113">The lowest value that you can set the maximum value to is one more than the [**MinimumScale**](systemmonitor-minimumscale.md) value.</span></span> <span data-ttu-id="78a92-114">Der höchste Wert, auf den Sie den maximalen Wert festlegen können, ist 999.999.999.</span><span class="sxs-lookup"><span data-stu-id="78a92-114">The highest value that you can set the maximum value to is 999,999,999.</span></span>

## <a name="remarks"></a><span data-ttu-id="78a92-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78a92-115">Remarks</span></span>

<span data-ttu-id="78a92-116">Das-Steuerelement passt automatisch die Position der Skalierungs Nummern an, die auf der vertikalen Skala entsprechend der Größe des angezeigten Steuer Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="78a92-116">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="78a92-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78a92-117">Requirements</span></span>



| <span data-ttu-id="78a92-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78a92-118">Requirement</span></span> | <span data-ttu-id="78a92-119">Wert</span><span class="sxs-lookup"><span data-stu-id="78a92-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78a92-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78a92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78a92-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78a92-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="78a92-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78a92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78a92-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78a92-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78a92-124">DLL</span><span class="sxs-lookup"><span data-stu-id="78a92-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78a92-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="78a92-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78a92-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78a92-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78a92-127">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="78a92-127">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="78a92-128">**Systemmonitor. MinimumScale**</span><span class="sxs-lookup"><span data-stu-id="78a92-128">**SystemMonitor.MinimumScale**</span></span>](systemmonitor-minimumscale.md)
</dt> <dt>

[<span data-ttu-id="78a92-129">**Systemmonitor. showscalelabels**</span><span class="sxs-lookup"><span data-stu-id="78a92-129">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





