---
title: Systemmonitor. showtimeaxislabels (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob die horizontale Achse (X) der Diagramm Ansicht Bezeichnungen enthält, oder legt ihn fest.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Showtimeaxislabels-Eigenschaft (Sysmon)
- Showtimeaxislabels-Eigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", showtimeaxislabels (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337306"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a><span data-ttu-id="a83dc-106">Systemmonitor. showtimeaxislabels (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a83dc-106">SystemMonitor.ShowTimeAxisLabels property</span></span>

<span data-ttu-id="a83dc-107">Ruft einen Wert ab, der bestimmt, ob die horizontale Achse (X) der Diagramm Ansicht Bezeichnungen enthält, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="a83dc-107">Retrieves or sets a value that determines if the horizontal (X) axis of the graph view contains labels.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83dc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a83dc-108">Syntax</span></span>


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a83dc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="a83dc-109">Property value</span></span>

<span data-ttu-id="a83dc-110">Mit dem Wert true werden Bezeichnungen auf die x-Achse angewendet.</span><span class="sxs-lookup"><span data-stu-id="a83dc-110">A value of True will apply labels to the x-axis.</span></span> <span data-ttu-id="a83dc-111">Der Wert false ist nicht.</span><span class="sxs-lookup"><span data-stu-id="a83dc-111">A value of False will not.</span></span> <span data-ttu-id="a83dc-112">Die Standardeinstellung lautet „false“.</span><span class="sxs-lookup"><span data-stu-id="a83dc-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="a83dc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a83dc-113">Remarks</span></span>

<span data-ttu-id="a83dc-114">Sysmon ignoriert diese Eigenschaft für Balkendiagramme, Berichte und Histogramme.</span><span class="sxs-lookup"><span data-stu-id="a83dc-114">SYSMON ignores this property for bar graphs, reports and histograms.</span></span>

<span data-ttu-id="a83dc-115">Bei Linien Diagrammen verwendet sysmon die Zeit, in der der Wert des Leistungs Zählers als Bezeichnung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="a83dc-115">For line graphs, SYSMON uses the time that the counter value was sampled as the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83dc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a83dc-116">Requirements</span></span>



| <span data-ttu-id="a83dc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a83dc-117">Requirement</span></span> | <span data-ttu-id="a83dc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a83dc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a83dc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a83dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a83dc-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a83dc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a83dc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a83dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a83dc-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a83dc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a83dc-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a83dc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a83dc-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="a83dc-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





