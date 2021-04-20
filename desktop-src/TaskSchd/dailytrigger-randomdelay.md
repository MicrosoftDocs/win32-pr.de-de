---
title: DailyTrigger.RandomDelay-Eigenschaft
description: Ruft für die Skripterstellung eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest. | DailyTrigger.RandomDelay-Eigenschaft
ms.assetid: 0494a963-bdaf-4f3f-a2e3-9482409ecda4
keywords:
- RandomDelay-Eigenschaft Taskplaner
- RandomDelay-Eigenschaft Taskplaner , DailyTrigger-Objekt
- DailyTrigger-Objekt Taskplaner , RandomDelay-Eigenschaft
topic_type:
- apiref
api_name:
- DailyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303192d578a2681e250784c1e1eb2831c98482cc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734105"
---
# <a name="dailytriggerrandomdelay-property"></a><span data-ttu-id="67ab2-107">DailyTrigger.RandomDelay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="67ab2-107">DailyTrigger.RandomDelay property</span></span>

<span data-ttu-id="67ab2-108">Ruft für die Skripterstellung eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="67ab2-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ab2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="67ab2-109">Syntax</span></span>


```VB
DailyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="67ab2-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="67ab2-110">Property value</span></span>

<span data-ttu-id="67ab2-111">Die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="67ab2-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="67ab2-112">Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (p2DT5S ist z. B. eine Verzögerung von 2 Tagen und 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="67ab2-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="67ab2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67ab2-113">Requirements</span></span>



| <span data-ttu-id="67ab2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67ab2-114">Requirement</span></span> | <span data-ttu-id="67ab2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="67ab2-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67ab2-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67ab2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67ab2-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67ab2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="67ab2-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67ab2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67ab2-119">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67ab2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="67ab2-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="67ab2-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="67ab2-121"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="67ab2-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="67ab2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="67ab2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67ab2-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ab2-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ab2-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="67ab2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ab2-125">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="67ab2-125">**DailyTrigger**</span></span>](dailytrigger.md)
</dt> <dt>

[<span data-ttu-id="67ab2-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="67ab2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





