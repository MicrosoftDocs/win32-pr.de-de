---
title: Sessionstatechangeauslöst. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde, oder legt diesen Wert fest.
ms.assetid: 3a17884f-fd74-491a-99dc-dce300a2cc77
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, sessionstatechange-Objekt
- Sessionstatechange-Objekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd5afde8ebd2884aee19fbdafb785355b9fedb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103190"
---
# <a name="sessionstatechangetriggerdelay-property"></a><span data-ttu-id="627a6-106">Sessionstatechangeauslöst. Delay (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="627a6-106">SessionStateChangeTrigger.Delay property</span></span>

<span data-ttu-id="627a6-107">Ruft bei der Skripterstellung einen Wert ab, der angibt, wie lange eine Verzögerung stattfindet, bevor eine Aufgabe gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="627a6-107">For scripting, gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span> <span data-ttu-id="627a6-108">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="627a6-108">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="syntax"></a><span data-ttu-id="627a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="627a6-109">Syntax</span></span>


```VB
SessionStateChangeTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="627a6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="627a6-110">Property value</span></span>

<span data-ttu-id="627a6-111">Die Verzögerung, die durchgeführt wird, bevor ein Task gestartet wird, nachdem eine Terminal Server-Sitzungs Zustandsänderung erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="627a6-111">The delay that takes place before a task is started after a Terminal Server session state change is detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="627a6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="627a6-112">Requirements</span></span>



| <span data-ttu-id="627a6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="627a6-113">Requirement</span></span> | <span data-ttu-id="627a6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="627a6-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="627a6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="627a6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="627a6-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="627a6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="627a6-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="627a6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="627a6-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="627a6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="627a6-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="627a6-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="627a6-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="627a6-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="627a6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="627a6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="627a6-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="627a6-122"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





