---
title: Registeredtask. getruntimes-Methode
description: Ruft bei der Skripterstellung die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Getruntimes-Methode Taskplaner
- Getruntimes-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getruntimes-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518503"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="50554-106">Registeredtask. getruntimes-Methode</span><span class="sxs-lookup"><span data-stu-id="50554-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="50554-107">Ruft bei der Skripterstellung die Zeiten ab, zu denen die Ausführung der registrierten Aufgabe innerhalb eines angegebenen Zeitraums geplant ist.</span><span class="sxs-lookup"><span data-stu-id="50554-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="50554-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="50554-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="50554-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="50554-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50554-110">*Anfang* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50554-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50554-111">Die Startzeit für die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="50554-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="50554-112">*Ende* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50554-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50554-113">Die Endzeit für die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="50554-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="50554-114">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50554-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50554-115">Die Anzahl der geplanten Zeiten, zu denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50554-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="50554-116">*rgsttasktimes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50554-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50554-117">Die geplanten Zeiten, zu denen der Task ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50554-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50554-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50554-118">Return value</span></span>

<span data-ttu-id="50554-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50554-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50554-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50554-120">Remarks</span></span>

<span data-ttu-id="50554-121">Wenn die registrierte Aufgabe einzeln deaktivierte Trigger enthält, wirken sich diese Trigger weiterhin auf die nächste geplante Laufzeit aus, die zurückgegeben wird, auch wenn Sie deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="50554-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="50554-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50554-122">Requirements</span></span>



| <span data-ttu-id="50554-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50554-123">Requirement</span></span> | <span data-ttu-id="50554-124">Wert</span><span class="sxs-lookup"><span data-stu-id="50554-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50554-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50554-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50554-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50554-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="50554-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50554-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50554-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50554-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50554-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="50554-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="50554-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50554-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50554-131">DLL</span><span class="sxs-lookup"><span data-stu-id="50554-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50554-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50554-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50554-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50554-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50554-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="50554-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="50554-135">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="50554-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





