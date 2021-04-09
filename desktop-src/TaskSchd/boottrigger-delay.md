---
title: Boottrigger. Delay (Eigenschaft)
description: Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Start des Systems und dem Start der Aufgabe angibt.
ms.assetid: 4e1c4e6f-640a-4e7d-8197-914c58cfae90
keywords:
- Verzögerte Eigenschaften Taskplaner
- Delay-Eigenschaft Taskplaner, boottrigger-Objekt
- Boottrigger-Objekt Taskplaner, Delay-Eigenschaft
topic_type:
- apiref
api_name:
- BootTrigger.Delay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6be91f00b79f2c2a47235a389b82ffb9255d586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104667"
---
# <a name="boottriggerdelay-property"></a><span data-ttu-id="35eb2-106">Boottrigger. Delay (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35eb2-106">BootTrigger.Delay property</span></span>

<span data-ttu-id="35eb2-107">Ruft bei der Skripterstellung einen Wert ab oder legt einen Wert fest, der die Zeitspanne zwischen dem Start des Systems und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="35eb2-107">For scripting, gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="35eb2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="35eb2-108">Syntax</span></span>


```VB
BootTrigger.Delay As String
```



## <a name="property-value"></a><span data-ttu-id="35eb2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35eb2-109">Property value</span></span>

<span data-ttu-id="35eb2-110">Ein-Wert, der den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe angibt.</span><span class="sxs-lookup"><span data-stu-id="35eb2-110">A value that indicates the amount of time between when the system is booted and when the task is started.</span></span> <span data-ttu-id="35eb2-111">Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z</span><span class="sxs-lookup"><span data-stu-id="35eb2-111">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="35eb2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35eb2-112">Remarks</span></span>

<span data-ttu-id="35eb2-113">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird die Startverzögerung mit dem [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="35eb2-113">When reading or writing your own XML for a task, the boot delay is specified using the [**Delay**](taskschedulerschema-delay-boottriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="35eb2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35eb2-114">Requirements</span></span>



| <span data-ttu-id="35eb2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35eb2-115">Requirement</span></span> | <span data-ttu-id="35eb2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="35eb2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35eb2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35eb2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35eb2-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35eb2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35eb2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35eb2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35eb2-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35eb2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35eb2-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="35eb2-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="35eb2-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35eb2-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35eb2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="35eb2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35eb2-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35eb2-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35eb2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35eb2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35eb2-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="35eb2-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="35eb2-127">**Boottrigger**</span><span class="sxs-lookup"><span data-stu-id="35eb2-127">**BootTrigger**</span></span>](boottrigger.md)
</dt> </dl>

 

 





