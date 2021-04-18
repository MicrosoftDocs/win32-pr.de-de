---
title: Tasksettings. restartcount (Eigenschaft)
description: Ruft bei der Skripterstellung ab oder legt fest, wie oft das Taskplaner versucht, den Task neu zu starten.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Restartcount-Eigenschaft Taskplaner
- Restartcount-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, restartcount-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391755"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="8b990-106">Tasksettings. restartcount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b990-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="8b990-107">Ruft bei der Skripterstellung ab oder legt fest, wie oft das Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="8b990-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="8b990-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8b990-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b990-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b990-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="8b990-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8b990-110">Property value</span></span>

<span data-ttu-id="8b990-111">Gibt an, wie oft der Taskplaner versucht, den Task neu zu starten.</span><span class="sxs-lookup"><span data-stu-id="8b990-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b990-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b990-112">Remarks</span></span>

<span data-ttu-id="8b990-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**count**](taskschedulerschema-count-restarttype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="8b990-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b990-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b990-114">Requirements</span></span>



| <span data-ttu-id="8b990-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b990-115">Requirement</span></span> | <span data-ttu-id="8b990-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8b990-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b990-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b990-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8b990-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b990-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8b990-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b990-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8b990-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b990-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b990-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8b990-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b990-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b990-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b990-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8b990-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b990-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b990-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b990-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b990-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b990-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="8b990-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





