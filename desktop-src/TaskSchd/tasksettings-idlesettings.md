---
title: Tasksettings. idlesettings-Eigenschaft
description: Ruft bei der Skripterstellung die Informationen ab, die angeben, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese Informationen fest.
ms.assetid: 5205db6d-668e-498a-bbd5-edfcf66eec7f
keywords:
- Idlesettings-Eigenschaft Taskplaner
- Idlesettings-Eigenschaft Taskplaner, tasksettings-Objekt
- Tasksettings-Objekt Taskplaner, idlesettings-Eigenschaft
topic_type:
- apiref
api_name:
- TaskSettings.IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972d341d205ff5719f94a9c0a3b44f64c5678495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344482"
---
# <a name="tasksettingsidlesettings-property"></a><span data-ttu-id="3ff58-106">Tasksettings. idlesettings-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3ff58-106">TaskSettings.IdleSettings property</span></span>

<span data-ttu-id="3ff58-107">Ruft bei der Skripterstellung die Informationen ab, die angeben, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet, oder legt diese Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="3ff58-107">For scripting, gets or sets the information that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="3ff58-108">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="3ff58-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

<span data-ttu-id="3ff58-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3ff58-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ff58-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ff58-110">Syntax</span></span>


```VB
TaskSettings.IdleSettings As IdleSettings
```



## <a name="property-value"></a><span data-ttu-id="3ff58-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3ff58-111">Property value</span></span>

<span data-ttu-id="3ff58-112">Ein [**idlesettings**](idlesettings.md) -Objekt, das angibt, wie die Taskplaner den Task verarbeitet, wenn der Computer in einen Leerlaufzustand wechselt.</span><span class="sxs-lookup"><span data-stu-id="3ff58-112">An [**IdleSettings**](idlesettings.md) object that specifies how the Task Scheduler handles the task when the computer goes into an idle condition.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ff58-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ff58-113">Remarks</span></span>

<span data-ttu-id="3ff58-114">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="3ff58-114">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ff58-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3ff58-115">Requirements</span></span>



| <span data-ttu-id="3ff58-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ff58-116">Requirement</span></span> | <span data-ttu-id="3ff58-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3ff58-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff58-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ff58-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ff58-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ff58-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3ff58-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ff58-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ff58-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ff58-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ff58-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3ff58-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ff58-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ff58-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ff58-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3ff58-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ff58-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ff58-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ff58-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ff58-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff58-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="3ff58-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





