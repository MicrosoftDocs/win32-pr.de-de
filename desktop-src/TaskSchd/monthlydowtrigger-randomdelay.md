---
title: Monthlydowauslöst. randomdelay-Eigenschaft
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Monthlydowauslöst. randomdelay-Eigenschaft
ms.assetid: e5cb6c1d-8003-43f4-bf35-da490a6097f0
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, monthlydowauslöserobjekt
- Monthlydowauslöst-Objekt Taskplaner, randomdelay-Eigenschaft
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
ms.openlocfilehash: d6fbdcab3b3f20d32e67b5b4e3e27b890b6bc902
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961462"
---
# <a name="monthlydowtriggerrandomdelay-property"></a><span data-ttu-id="c0ec3-107">Monthlydowauslöst. randomdelay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c0ec3-107">MonthlyDOWTrigger.RandomDelay property</span></span>

<span data-ttu-id="c0ec3-108">Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c0ec3-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0ec3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0ec3-109">Syntax</span></span>


```VB
MonthlyDOWTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="c0ec3-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c0ec3-110">Property value</span></span>

<span data-ttu-id="c0ec3-111">Die Verzögerungszeit, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c0ec3-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="c0ec3-112">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="c0ec3-112">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ec3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0ec3-113">Requirements</span></span>



| <span data-ttu-id="c0ec3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0ec3-114">Requirement</span></span> | <span data-ttu-id="c0ec3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c0ec3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0ec3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0ec3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ec3-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0ec3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c0ec3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0ec3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ec3-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0ec3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0ec3-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c0ec3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0ec3-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0ec3-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0ec3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c0ec3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0ec3-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0ec3-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ec3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0ec3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ec3-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="c0ec3-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="c0ec3-126">**Monthlydowlöst**</span><span class="sxs-lookup"><span data-stu-id="c0ec3-126">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
</dt> </dl>

 

 





