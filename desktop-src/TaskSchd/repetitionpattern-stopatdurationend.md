---
title: Repetitionpattern. stopatdurationend-Eigenschaft
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.
ms.assetid: 421f2d6f-7c35-44b4-97f2-45f46ca5e40e
keywords:
- Stopatdurationend-Eigenschaft Taskplaner
- Stopatdurationend-Eigenschaft Taskplaner, repetitionpattern-Objekt
- Repetitionpattern-Objekt Taskplaner, stopatdurationend-Eigenschaft
topic_type:
- apiref
api_name:
- RepetitionPattern.StopAtDurationEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b95d7e8941a4249991692dffbd3cac9ad1ca7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742440"
---
# <a name="repetitionpatternstopatdurationend-property"></a><span data-ttu-id="39d56-106">Repetitionpattern. stopatdurationend-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39d56-106">RepetitionPattern.StopAtDurationEnd property</span></span>

<span data-ttu-id="39d56-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="39d56-107">For scripting, gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d56-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39d56-108">Syntax</span></span>


```VB
RepetitionPattern.StopAtDurationEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="39d56-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="39d56-109">Property value</span></span>

<span data-ttu-id="39d56-110">Ein boolescher Wert, der angibt, ob eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="39d56-110">A Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d56-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39d56-111">Remarks</span></span>

<span data-ttu-id="39d56-112">Beim Lesen oder Schreiben von XML für eine Aufgabe werden diese Informationen im [**stopatdurationend**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="39d56-112">When reading or writing XML for a task, this information is specified in the [**StopAtDurationEnd**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d56-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39d56-113">Requirements</span></span>



| <span data-ttu-id="39d56-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39d56-114">Requirement</span></span> | <span data-ttu-id="39d56-115">Wert</span><span class="sxs-lookup"><span data-stu-id="39d56-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39d56-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39d56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="39d56-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39d56-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="39d56-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39d56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="39d56-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39d56-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39d56-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="39d56-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="39d56-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="39d56-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="39d56-122">DLL</span><span class="sxs-lookup"><span data-stu-id="39d56-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d56-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d56-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d56-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39d56-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d56-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="39d56-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





