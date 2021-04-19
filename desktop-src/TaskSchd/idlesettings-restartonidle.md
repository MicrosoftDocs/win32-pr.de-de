---
title: Idlesettings. restartondle (Eigenschaft)
description: Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.
ms.assetid: c77b6f5f-659c-4aa0-a5f7-39c01e5ca65e
keywords:
- Restartondle-Eigenschaft Taskplaner
- Restartondle-Eigenschaft Taskplaner, idlesettings-Objekt
- Idlesettings-Objekt Taskplaner, restartondle-Eigenschaft
topic_type:
- apiref
api_name:
- IdleSettings.RestartOnIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e80b2e523f2f19222292eac7752847a72291c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342216"
---
# <a name="idlesettingsrestartonidle-property"></a><span data-ttu-id="f473c-106">Idlesettings. restartondle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f473c-106">IdleSettings.RestartOnIdle property</span></span>

<span data-ttu-id="f473c-107">Ruft bei der Skripterstellung einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="f473c-107">For scripting, gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

## <a name="syntax"></a><span data-ttu-id="f473c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f473c-108">Syntax</span></span>


```VB
IdleSettings.RestartOnIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="f473c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f473c-109">Property value</span></span>

<span data-ttu-id="f473c-110">Ein boolescher Wert, der angibt, ob die Aufgabe neu gestartet werden muss, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.</span><span class="sxs-lookup"><span data-stu-id="f473c-110">A Boolean value that indicates whether the task must be restarted when the computer cycles into an idle condition more than once.</span></span> <span data-ttu-id="f473c-111">Die Standardeinstellung lautet „false“.</span><span class="sxs-lookup"><span data-stu-id="f473c-111">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="f473c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f473c-112">Remarks</span></span>

<span data-ttu-id="f473c-113">Diese Eigenschaft wird nur verwendet, wenn die [**idlesettings. stoponidleend**](idlesettings-stoponidleend.md) -Eigenschaft auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f473c-113">This property is only used if the [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md) property is set to True.</span></span>

<span data-ttu-id="f473c-114">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**restartondle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="f473c-114">When reading or writing XML for a task, this setting is specified in the [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f473c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f473c-115">Requirements</span></span>



| <span data-ttu-id="f473c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f473c-116">Requirement</span></span> | <span data-ttu-id="f473c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f473c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f473c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f473c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f473c-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f473c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f473c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f473c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f473c-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f473c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f473c-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f473c-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="f473c-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f473c-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f473c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f473c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f473c-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f473c-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f473c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f473c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f473c-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="f473c-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f473c-128">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="f473c-128">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





