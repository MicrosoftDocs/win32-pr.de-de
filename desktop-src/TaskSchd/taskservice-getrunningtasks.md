---
title: TaskService. getrunningtasks-Methode
description: Ruft bei der Skripterstellung eine Auflistung von laufenden Tasks ab.
ms.assetid: bae3c035-a6b2-4ca5-970b-d4bc808068ad
keywords:
- Getrunningtasks-Methode Taskplaner
- Getrunningtasks-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, getrunningtasks-Methode
topic_type:
- apiref
api_name:
- TaskService.GetRunningTasks
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec585b9ed46af9a283e337c8f200687c512cd36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743737"
---
# <a name="taskservicegetrunningtasks-method"></a><span data-ttu-id="a4473-106">TaskService. getrunningtasks-Methode</span><span class="sxs-lookup"><span data-stu-id="a4473-106">TaskService.GetRunningTasks method</span></span>

<span data-ttu-id="a4473-107">Ruft bei der Skripterstellung eine Auflistung von laufenden Tasks ab.</span><span class="sxs-lookup"><span data-stu-id="a4473-107">For scripting, gets a collection of running tasks.</span></span>

> [!Note]  
> <span data-ttu-id="a4473-108">**TaskService. getrunningtasks** gibt nur eine Auflistung von ausgeführte Tasks zurück, die unter oder unterhalb des Sicherheits Kontexts eines Benutzers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a4473-108">**TaskService.GetRunningTasks** will only return a collection of running tasks that are running at or below a user's security context.</span></span> <span data-ttu-id="a4473-109">Für Mitglieder der Gruppe "Administratoren" gibt **getrunningtasks** beispielsweise eine Sammlung aller ausgelaufenden Aufgaben zurück, aber für Mitglieder der Gruppe "Benutzer" gibt **getrunningtasks** nur eine Auflistung von Aufgaben zurück, die unter dem Sicherheitskontext der Benutzergruppe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a4473-109">For example, for members of the Administrators group, **GetRunningTasks** will return a collection of all running tasks, but for members of the Users group, **GetRunningTasks** will only return a collection of tasks that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a4473-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4473-110">Syntax</span></span>


```VB
TaskService.GetRunningTasks( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a4473-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4473-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4473-112">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4473-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4473-113">Übergeben Sie 1, um alle laufenden Tasks, einschließlich ausgeblendeter Tasks, zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="a4473-113">Pass in 1 to return all running tasks, including hidden tasks.</span></span> <span data-ttu-id="a4473-114">Übergeben Sie 0, um eine Auflistung von Aufgaben zurückzugeben, die keine ausgeblendeten Tasks sind.</span><span class="sxs-lookup"><span data-stu-id="a4473-114">Pass in 0 to return a collection of running tasks that are not hidden tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4473-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4473-115">Return value</span></span>

<span data-ttu-id="a4473-116">Ein [**runningtaskcollection**](runningtaskcollection.md) -Objekt, das die derzeit laufenden Tasks enthält.</span><span class="sxs-lookup"><span data-stu-id="a4473-116">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains the currently running tasks.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4473-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4473-117">Requirements</span></span>



| <span data-ttu-id="a4473-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4473-118">Requirement</span></span> | <span data-ttu-id="a4473-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a4473-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4473-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4473-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a4473-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4473-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a4473-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4473-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a4473-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4473-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a4473-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a4473-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="a4473-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a4473-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a4473-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a4473-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4473-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4473-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4473-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4473-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4473-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="a4473-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





