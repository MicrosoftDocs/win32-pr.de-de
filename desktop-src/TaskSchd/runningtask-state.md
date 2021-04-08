---
title: Runningtask. State (Eigenschaft)
description: Ruft für die Skripterstellung einen Bezeichner für den Zustand der aktuell laufenden Aufgabe ab.
ms.assetid: 048863f4-b80b-42ab-bd74-ec761a8f03aa
keywords:
- State-Eigenschaft Taskplaner
- State-Eigenschaft Taskplaner, runningtask-Objekt
- Runningtask-Objekt Taskplaner, State-Eigenschaft
topic_type:
- apiref
api_name:
- RunningTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b962de116eef1301be209828181147dfe03273e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740856"
---
# <a name="runningtaskstate-property"></a><span data-ttu-id="cf801-106">Runningtask. State (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cf801-106">RunningTask.State property</span></span>

<span data-ttu-id="cf801-107">Ruft für die Skripterstellung einen Bezeichner für den Zustand der aktuell laufenden Aufgabe ab.</span><span class="sxs-lookup"><span data-stu-id="cf801-107">For scripting, gets an identifier for the state of the running task.</span></span>

<span data-ttu-id="cf801-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cf801-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf801-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf801-109">Syntax</span></span>


```VB
RunningTask.State As String
```



## <a name="property-value"></a><span data-ttu-id="cf801-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cf801-110">Property value</span></span>

<span data-ttu-id="cf801-111">Ein Bezeichner für den Zustand der laufenden Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="cf801-111">An identifier for the state of the running task.</span></span>



| <span data-ttu-id="cf801-112">Wert</span><span class="sxs-lookup"><span data-stu-id="cf801-112">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="cf801-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cf801-113">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="cf801-114"><dt>**Aufgabe \_ \_Unbekannter Status**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-114"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="cf801-115">Der Task Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="cf801-115">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="cf801-116"><dt>**Aufgabe \_ Status \_ deaktiviert**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-116"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="cf801-117">Der Task ist registriert, aber deaktiviert, und es werden keine Instanzen der Aufgabe in die Warteschlange eingereiht oder ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf801-117">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="cf801-118">Der Task kann erst ausgeführt werden, wenn er aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cf801-118">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="cf801-119"><dt>**Aufgabe \_ Status in \_ Warteschlange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-119"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="cf801-120">Instanzen der Aufgabe werden in die Warteschlange eingereiht.</span><span class="sxs-lookup"><span data-stu-id="cf801-120">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="cf801-121"><dt>**Aufgabe \_ Status \_ bereit**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-121"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="cf801-122">Der Task ist für die Ausführung bereit, aber es werden keine Instanzen in die Warteschlange eingereiht oder ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf801-122">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="cf801-123"><dt>**Aufgabe \_ Status \_**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-123"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="cf801-124">Eine oder mehrere Instanzen der Aufgabe werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf801-124">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="cf801-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf801-125">Remarks</span></span>

<span data-ttu-id="cf801-126">Die [**runningtask. Refresh**](runningtask-refresh.md) -Methode wird aufgerufen, bevor der-Eigenschafts Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cf801-126">The [**RunningTask.Refresh**](runningtask-refresh.md) method is called before the property value is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf801-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf801-127">Requirements</span></span>



| <span data-ttu-id="cf801-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf801-128">Requirement</span></span> | <span data-ttu-id="cf801-129">Wert</span><span class="sxs-lookup"><span data-stu-id="cf801-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf801-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf801-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cf801-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf801-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cf801-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf801-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cf801-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf801-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf801-134">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cf801-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf801-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf801-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cf801-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf801-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf801-137"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





