---
title: Tasksettings. allowdemandstart (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task entweder mit dem Befehl ausführen oder mit dem Kontextmenü gestartet werden kann, oder legt diesen fest.
ms.assetid: 1eae19ae-3b4d-4eb2-82d0-685ef2729f36
keywords:
- Allowdemandstart-Eigenschaft Taskplaner
- Allowdemandstart-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, allowdemandstart-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.AllowDemandStart
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657ba45e0809b74803e27de70fae52576fcf2a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391628"
---
# <a name="tasksettingsallowdemandstart-property"></a><span data-ttu-id="70113-106">Tasksettings. allowdemandstart (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="70113-106">TaskSettings.AllowDemandStart property</span></span>

<span data-ttu-id="70113-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, dass der Task entweder mit dem Befehl ausführen oder mit dem Kontextmenü gestartet werden kann, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="70113-107">For scripting, gets or sets a Boolean value that indicates that the task can be started by using either the Run command or the Context menu.</span></span>

<span data-ttu-id="70113-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="70113-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="70113-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="70113-109">Syntax</span></span>


```VB
TaskSettings.AllowDemandStart As Boolean
```



## <a name="property-value"></a><span data-ttu-id="70113-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="70113-110">Property value</span></span>

<span data-ttu-id="70113-111">True gibt an, dass der Task mithilfe des Befehls ausführen oder des Kontextmenüs ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="70113-111">If True, the task can be run by using the Run command or the Context menu.</span></span> <span data-ttu-id="70113-112">Wenn der Wert false ist, kann der Task nicht mit dem Befehl ausführen oder dem Kontextmenü ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70113-112">If False, the task cannot be run using the Run command or the Context menu.</span></span> <span data-ttu-id="70113-113">Der Standardwert ist True.</span><span class="sxs-lookup"><span data-stu-id="70113-113">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="70113-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70113-114">Remarks</span></span>

<span data-ttu-id="70113-115">Wenn diese Eigenschaft auf true festgelegt ist, kann der Task unabhängig von gestartet werden, wenn ein Trigger den Task startet.</span><span class="sxs-lookup"><span data-stu-id="70113-115">When this property is set to True, the task can be started independent of when any triggers start the task.</span></span>

<span data-ttu-id="70113-116">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [allowstartondemand](taskschedulerschema-allowstartondemand-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="70113-116">When reading or writing XML for a task, this setting is specified in the [AllowStartOnDemand](taskschedulerschema-allowstartondemand-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="70113-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70113-117">Requirements</span></span>



| <span data-ttu-id="70113-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70113-118">Requirement</span></span> | <span data-ttu-id="70113-119">Wert</span><span class="sxs-lookup"><span data-stu-id="70113-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70113-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="70113-120">Minimum supported client</span></span><br/> | <span data-ttu-id="70113-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70113-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="70113-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="70113-122">Minimum supported server</span></span><br/> | <span data-ttu-id="70113-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="70113-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70113-124">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="70113-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="70113-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70113-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70113-126">DLL</span><span class="sxs-lookup"><span data-stu-id="70113-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70113-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70113-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70113-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70113-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70113-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="70113-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





