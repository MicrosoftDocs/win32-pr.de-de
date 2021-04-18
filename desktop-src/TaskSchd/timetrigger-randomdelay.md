---
title: Timeauslöst. randomdelay-Eigenschaft
description: Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest. | Timeauslöst. randomdelay-Eigenschaft
ms.assetid: ee55dd85-9696-4872-8670-f919fca7481d
keywords:
- Randomdelay-Eigenschaft Taskplaner
- Randomdelay-Eigenschaft Taskplaner, Time-Auslöserobjekt
- Time-Auslöserobjekt Taskplaner, randomdelay-Eigenschaft
topic_type:
- apiref
api_name:
- TimeTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39c4acf4f38670332e723ac0824276695919cb1d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365260"
---
# <a name="timetriggerrandomdelay-property"></a><span data-ttu-id="80491-107">Timeauslöst. randomdelay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="80491-107">TimeTrigger.RandomDelay property</span></span>

<span data-ttu-id="80491-108">Ruft bei der Skripterstellung eine Verzögerungszeit ab, die der Startzeit des Auslösers zufällig hinzugefügt wird, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="80491-108">For scripting, gets or sets a delay time that is randomly added to the start time of the trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="80491-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="80491-109">Syntax</span></span>


```VB
TimeTrigger.RandomDelay As String
```



## <a name="property-value"></a><span data-ttu-id="80491-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="80491-110">Property value</span></span>

<span data-ttu-id="80491-111">Die Verzögerungszeit, die der Startzeit des Auslösers nach dem Zufallsprinzip hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="80491-111">The delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="80491-112">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="80491-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="80491-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80491-113">Requirements</span></span>



| <span data-ttu-id="80491-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80491-114">Requirement</span></span> | <span data-ttu-id="80491-115">Wert</span><span class="sxs-lookup"><span data-stu-id="80491-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80491-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80491-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80491-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80491-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="80491-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80491-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80491-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80491-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80491-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="80491-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="80491-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="80491-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="80491-122">DLL</span><span class="sxs-lookup"><span data-stu-id="80491-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80491-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80491-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





