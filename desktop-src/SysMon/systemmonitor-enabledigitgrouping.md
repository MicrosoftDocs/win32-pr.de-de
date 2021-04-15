---
title: Systemmonitor. enabledigitgruppierung (Eigenschaft)
description: Ruft einen Wert ab, der bestimmt, ob sysmon eine Ziffern Gruppierung verwendet, wenn numerische Werte angezeigt werden, oder legt ihn fest.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Enabledigitgruppierung-Eigenschaft (Sysmon)
- Enabledigitgruppierungseigenschaft (Sysmon), Systemmonitor-Objekt
- Systemmonitor-Objekt "sysmon", enabledigitgruppierung (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391941"
---
# <a name="systemmonitorenabledigitgrouping-property"></a><span data-ttu-id="e5725-106">Systemmonitor. enabledigitgruppierung (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e5725-106">SystemMonitor.EnableDigitGrouping property</span></span>

<span data-ttu-id="e5725-107">Ruft einen Wert ab, der bestimmt, ob sysmon eine Ziffern Gruppierung verwendet, wenn numerische Werte angezeigt werden, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e5725-107">Retrieves or sets a value that determines if SYSMON uses digit grouping when displaying numeric values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5725-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5725-108">Syntax</span></span>


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e5725-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e5725-109">Property value</span></span>

<span data-ttu-id="e5725-110">True gibt an, dass sysmon Ziffern beim Anzeigen numerischer Werte gruppiert, z. b. 1.214.</span><span class="sxs-lookup"><span data-stu-id="e5725-110">If True, SYSMON will group digits when displaying numeric values, for example, 1,214.</span></span> <span data-ttu-id="e5725-111">False gibt an, dass numerische Werte nicht gruppiert werden, z. b. 1214.</span><span class="sxs-lookup"><span data-stu-id="e5725-111">If False, numeric values are not grouped, for example, 1214.</span></span> <span data-ttu-id="e5725-112">Der Standardwert ist "true".</span><span class="sxs-lookup"><span data-stu-id="e5725-112">True is the default.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5725-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5725-113">Remarks</span></span>

<span data-ttu-id="e5725-114">Das Ziffern Gruppierungs Symbol ist lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="e5725-114">The digit grouping symbol is localized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5725-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5725-115">Requirements</span></span>



| <span data-ttu-id="e5725-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5725-116">Requirement</span></span> | <span data-ttu-id="e5725-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e5725-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e5725-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5725-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e5725-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5725-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e5725-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5725-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e5725-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e5725-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e5725-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e5725-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5725-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e5725-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





