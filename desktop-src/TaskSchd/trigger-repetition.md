---
title: "\"\"-Eigenschaft von \"\""
description: Ruft bei der Skripterstellung einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.
ms.assetid: f90b935c-8b69-4c82-ac4b-6b049e7b9703
keywords:
- Wiederholungs Eigenschaft Taskplaner
- Wiederholungs Eigenschaft Taskplaner, Auslöserobjekt
- Objekt Taskplaner, Wiederholungs Eigenschaft des Auslösers
topic_type:
- apiref
api_name:
- Trigger.Repetition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611c7e42a14de06a8777333a6dc640781943ba06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339139"
---
# <a name="triggerrepetition-property"></a><span data-ttu-id="8d424-106">""-Eigenschaft von ""</span><span class="sxs-lookup"><span data-stu-id="8d424-106">Trigger.Repetition property</span></span>

<span data-ttu-id="8d424-107">Ruft bei der Skripterstellung einen Wert ab, der angibt, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster nach dem Start der Aufgabe wiederholt wird, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="8d424-107">For scripting, gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d424-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d424-108">Syntax</span></span>


```VB
Trigger.Repetition As RepetitionPattern
```



## <a name="property-value"></a><span data-ttu-id="8d424-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8d424-109">Property value</span></span>

<span data-ttu-id="8d424-110">Ein [**wiederholungpattern**](repetitionpattern.md) -Objekt, das definiert, wie oft die Aufgabe ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem die Aufgabe gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="8d424-110">A [**RepetitionPattern**](repetitionpattern.md) object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d424-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d424-111">Remarks</span></span>

<span data-ttu-id="8d424-112">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird das Wiederholungsmuster für einen-Vorgang im [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="8d424-112">When reading or writing your own XML for a task, the repetition pattern for a trigger is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d424-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d424-113">Requirements</span></span>



| <span data-ttu-id="8d424-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d424-114">Requirement</span></span> | <span data-ttu-id="8d424-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8d424-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d424-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d424-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8d424-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d424-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8d424-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d424-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8d424-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d424-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8d424-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8d424-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="8d424-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8d424-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8d424-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8d424-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d424-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d424-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d424-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d424-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d424-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8d424-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="8d424-126">**Repetitionpattern**</span><span class="sxs-lookup"><span data-stu-id="8d424-126">**RepetitionPattern**</span></span>](repetitionpattern.md)
</dt> </dl>

 

 





