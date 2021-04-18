---
title: Monthly-Eigenschaft. randomdelay (Eigenschaft)
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Monthly-Eigenschaft. randomdelay (Eigenschaft)
ms.assetid: 5334356f-fef1-4d0e-9879-6ec996b75dff
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, Monthly-Auslöserobjekt
- Monthly-Auslöserobjekt Taskplaner, randomdelay-Eigenschaft
topic_type:
- apiref
api_name:
- MonthlyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b290e3a0bae1f8032b19d4d07203a64e1d1686
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365030"
---
# <a name="monthlytriggerrandomdelay-property"></a><span data-ttu-id="c455a-107">Monthly-Eigenschaft. randomdelay (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c455a-107">MonthlyTrigger.RandomDelay property</span></span>

<span data-ttu-id="c455a-108">Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c455a-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="c455a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c455a-109">Syntax</span></span>


```VB
MonthlyTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="c455a-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c455a-110">Property value</span></span>

<span data-ttu-id="c455a-111">Die Verzögerungszeit, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c455a-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="c455a-112">Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).</span><span class="sxs-lookup"><span data-stu-id="c455a-112">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span>

## <a name="requirements"></a><span data-ttu-id="c455a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c455a-113">Requirements</span></span>



| <span data-ttu-id="c455a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c455a-114">Requirement</span></span> | <span data-ttu-id="c455a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c455a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c455a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c455a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c455a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c455a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c455a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c455a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c455a-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c455a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c455a-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c455a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="c455a-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c455a-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c455a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c455a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c455a-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c455a-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c455a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c455a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c455a-125">**Monthly-auslöst**</span><span class="sxs-lookup"><span data-stu-id="c455a-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
</dt> </dl>

 

 





