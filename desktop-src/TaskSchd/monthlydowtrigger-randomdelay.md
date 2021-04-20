---
title: MonthlyDOWTrigger.RandomDelay-Eigenschaft
description: Ruft für die Skripterstellung eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest. | MonthlyDOWTrigger.RandomDelay-Eigenschaft
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- RandomDelay-Eigenschaft Taskplaner
- RandomDelay-Eigenschaft Taskplaner , MonthlyDOWTrigger-Objekt
- MonthlyDOWTrigger-Objekt Taskplaner , RandomDelay-Eigenschaft
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e781941e927547a4ea25935fb21299777c34b3ea
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734125"
---
# <a name="monthlydowtriggerrandomdelay-property"></a><span data-ttu-id="62678-107">MonthlyDOWTrigger.RandomDelay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="62678-107">MonthlyDOWTrigger.RandomDelay property</span></span>

<span data-ttu-id="62678-108">Ruft für die Skripterstellung eine Verzögerungszeit ab, die zufällig zur Startzeit des Triggers hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="62678-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="62678-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="62678-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="62678-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="62678-110">Property value</span></span>

<span data-ttu-id="62678-111">Die Verzögerungszeit, die zufällig zur Startzeit des Triggers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="62678-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="62678-112">Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (p2DT5S ist z. B. eine Verzögerung von 2 Tagen und 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="62678-112">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="62678-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62678-113">Requirements</span></span>



| <span data-ttu-id="62678-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62678-114">Requirement</span></span> | <span data-ttu-id="62678-115">Wert</span><span class="sxs-lookup"><span data-stu-id="62678-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62678-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62678-116">Minimum supported client</span></span><br/> | <span data-ttu-id="62678-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62678-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="62678-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62678-118">Minimum supported server</span></span><br/> | <span data-ttu-id="62678-119">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62678-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62678-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="62678-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="62678-121"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62678-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62678-122">DLL</span><span class="sxs-lookup"><span data-stu-id="62678-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62678-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62678-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62678-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62678-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62678-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="62678-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="62678-126">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="62678-126">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> </dl>

 

 





