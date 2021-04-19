---
title: Systemmonitor. EnableToolTips (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger über einen Leistungsindikators in einer der Diagramm Ansichten bewegt wird (wird für die Berichtsansicht nicht unterstützt).
ms.assetid: af9a78ea-a9de-4343-8978-4316769a5f30
keywords:
- EnableToolTips-Eigenschaft (Sysmon)
- EnableToolTips-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", EnableToolTips (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.EnableToolTips
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 757cdd8a54bf6e5ae6e70b82dfc30865c796f944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342212"
---
# <a name="systemmonitorenabletooltips-property"></a><span data-ttu-id="2b189-106">Systemmonitor. EnableToolTips (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2b189-106">SystemMonitor.EnableToolTips property</span></span>

<span data-ttu-id="2b189-107">Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine QuickInfo angezeigt wird, wenn der Mauszeiger über einen Leistungsindikators in einer der Diagramm Ansichten bewegt wird (wird für die Berichtsansicht nicht unterstützt).</span><span class="sxs-lookup"><span data-stu-id="2b189-107">Retrieves or sets a value that determines if a tool tip is shown when the mouse hovers over a counter in one of the graph views (not supported for report view).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b189-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b189-108">Syntax</span></span>


```VB
Property EnableToolTips As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2b189-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2b189-109">Property value</span></span>

<span data-ttu-id="2b189-110">True zeigt eine QuickInfo mit den darin angezeigten Informationen zum Gegenstand an. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="2b189-110">True displays a tool tip with the counter information in it; otherwise, False.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b189-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b189-111">Remarks</span></span>

<span data-ttu-id="2b189-112">Bei Linien Diagrammen ist die QuickInfo an dem Datenpunkt verankert, der der Maus am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="2b189-112">For line graphs, the tool tip is anchored to the data point that is closest to the mouse.</span></span> <span data-ttu-id="2b189-113">Bei Balkendiagrammen und Histogrammen stellt die QuickInfo den gesamten Datenwert des Balkens dar, nicht einen Punkt innerhalb des Balkens.</span><span class="sxs-lookup"><span data-stu-id="2b189-113">For bar charts and histograms, the tool tip represents the total data value of the bar, not a point within the bar.</span></span>

<span data-ttu-id="2b189-114">Die QuickInfo enthält verschiedene Informationen, die auf der Datenquelle basieren.</span><span class="sxs-lookup"><span data-stu-id="2b189-114">The tool tip contains different information based upon the data source.</span></span> <span data-ttu-id="2b189-115">Für Protokolldateien enthält die QuickInfo den Wert für den Leistungswert, den Leistungswert, den Zeitstempel, die Anzahl der Daten Stichproben, die im Datenpunkt enthalten sind, sowie die minimalen und maximalen Datenwerte.</span><span class="sxs-lookup"><span data-stu-id="2b189-115">For log files, the tool tip contains the counter path, counter value, time stamp, number of data samples included in the data point, and the minimum and maximum data values.</span></span>

<span data-ttu-id="2b189-116">Für echt Zeit Aktivität enthält die QuickInfo den Wert für den Leistungswert, den Leistungswert und den Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="2b189-116">For real time activity, the tool tip contains the counter path, counter value, and time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b189-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b189-117">Requirements</span></span>



| <span data-ttu-id="2b189-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b189-118">Requirement</span></span> | <span data-ttu-id="2b189-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2b189-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b189-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b189-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b189-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b189-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b189-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b189-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b189-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b189-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b189-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b189-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b189-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2b189-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





