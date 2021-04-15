---
title: Systemmonitor. MinimumScale (Eigenschaft)
description: Ruft den Mindestwert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- MinimumScale-Eigenschaft (Sysmon)
- MinimumScale-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse "sysmon", MinimumScale-Eigenschaft
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476575"
---
# <a name="systemmonitorminimumscale-property"></a><span data-ttu-id="f86b9-106">Systemmonitor. MinimumScale (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f86b9-106">SystemMonitor.MinimumScale property</span></span>

<span data-ttu-id="f86b9-107">Ruft den Mindestwert der vertikalen Achse (Y-Achse) des Diagramms ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f86b9-107">Retrieves or sets the minimum value of the vertical (Y) axis of the graph.</span></span>

<span data-ttu-id="f86b9-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f86b9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86b9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f86b9-109">Syntax</span></span>


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a><span data-ttu-id="f86b9-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f86b9-110">Property value</span></span>

<span data-ttu-id="f86b9-111">Positiver Minimalwert der vertikalen Achse des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="f86b9-111">Positive minimum value of the vertical axis of the graph.</span></span> <span data-ttu-id="f86b9-112">Der Standard Minimalwert der vertikalen Skala ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f86b9-112">The default minimum value of the vertical scale is 0.</span></span> <span data-ttu-id="f86b9-113">Der höchste Wert, auf den der minimale Wert festgelegt werden kann, ist ein Wert kleiner als [**MaximumScale**](systemmonitor-maximumscale.md) .</span><span class="sxs-lookup"><span data-stu-id="f86b9-113">The highest value that you can set the minimum value to is one less than [**MaximumScale**](systemmonitor-maximumscale.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f86b9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f86b9-114">Remarks</span></span>

<span data-ttu-id="f86b9-115">Das-Steuerelement passt automatisch die Position der Skalierungs Nummern an, die auf der vertikalen Skala entsprechend der Größe des angezeigten Steuer Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f86b9-115">The control automatically adjusts the position of the scale numbers displayed on the vertical scale according to the size of the displayed control.</span></span>

## <a name="requirements"></a><span data-ttu-id="f86b9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f86b9-116">Requirements</span></span>



| <span data-ttu-id="f86b9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f86b9-117">Requirement</span></span> | <span data-ttu-id="f86b9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f86b9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f86b9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f86b9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f86b9-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f86b9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f86b9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f86b9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f86b9-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f86b9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f86b9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f86b9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f86b9-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="f86b9-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f86b9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f86b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f86b9-126">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="f86b9-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="f86b9-127">**Systemmonitor. MaximumScale**</span><span class="sxs-lookup"><span data-stu-id="f86b9-127">**SystemMonitor.MaximumScale**</span></span>](systemmonitor-maximumscale.md)
</dt> <dt>

[<span data-ttu-id="f86b9-128">**Systemmonitor. showscalelabels**</span><span class="sxs-lookup"><span data-stu-id="f86b9-128">**SystemMonitor.ShowScaleLabels**</span></span>](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





