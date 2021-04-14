---
title: Idlesettings-Objekt
description: Skript Objekt, das angibt, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.
ms.assetid: d303596a-0a84-4056-9f7a-5a9512852002
keywords:
- Idlesettings-Objekt Taskplaner
- Idlesettings-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- IdleSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 819ff226386f30483de96fac6213b35d7dd51a52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391766"
---
# <a name="idlesettings-object"></a><span data-ttu-id="2d76e-105">Idlesettings-Objekt</span><span class="sxs-lookup"><span data-stu-id="2d76e-105">IdleSettings object</span></span>

<span data-ttu-id="2d76e-106">Ein Skript Objekt, das angibt, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="2d76e-106">A scripting object that specifies how the Task Scheduler performs tasks when the computer is in an idle condition.</span></span> <span data-ttu-id="2d76e-107">Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="2d76e-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="2d76e-108">Member</span><span class="sxs-lookup"><span data-stu-id="2d76e-108">Members</span></span>

<span data-ttu-id="2d76e-109">Das **idlesettings** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2d76e-109">The **IdleSettings** object has these types of members:</span></span>

- [<span data-ttu-id="2d76e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d76e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d76e-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2d76e-111">Properties</span></span>

<span data-ttu-id="2d76e-112">Das **idlesettings** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2d76e-112">The **IdleSettings** object has these properties.</span></span>

> [!NOTE]
> <span data-ttu-id="2d76e-113">Die Einstellungen *idleduration* und *WaitTimeout* sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="2d76e-113">The *IdleDuration* and *WaitTimeout* settings are deprecated.</span></span> <span data-ttu-id="2d76e-114">Sie sind weiterhin in der Taskplaner-Benutzeroberfläche vorhanden, und ihre Schnittstellen Methoden geben möglicherweise weiterhin gültige Werte zurück, aber Sie werden nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d76e-114">They're still present in the Task Scheduler user interface, and their interface methods may still return valid values, but they're no longer used.</span></span>

| <span data-ttu-id="2d76e-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d76e-115">Property</span></span>                                                       | <span data-ttu-id="2d76e-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="2d76e-116">Access type</span></span>           | <span data-ttu-id="2d76e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d76e-117">Description</span></span>                                                                                                                                                     |
|:---------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d76e-118">**Neustartondle**</span><span class="sxs-lookup"><span data-stu-id="2d76e-118">**RestartOnIdle**</span></span>](idlesettings-restartonidle.md)<br/> | <span data-ttu-id="2d76e-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d76e-119">Read/write</span></span><br/> | <span data-ttu-id="2d76e-120">Ruft einen booleschen Wert ab, der angibt, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="2d76e-120">Gets or sets a Boolean value that indicates whether the task is restarted when the computer cycles into an idle condition more than once.</span></span><br/>            |
| [<span data-ttu-id="2d76e-121">**Stoponidleend**</span><span class="sxs-lookup"><span data-stu-id="2d76e-121">**StopOnIdleEnd**</span></span>](idlesettings-stoponidleend.md)<br/> | <span data-ttu-id="2d76e-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d76e-122">Read/write</span></span><br/> | <span data-ttu-id="2d76e-123">Ruft einen booleschen Wert ab, der angibt, dass die Taskplaner die Aufgabe beendet, wenn die Leerlauf Bedingung endet, bevor die Aufgabe abgeschlossen wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="2d76e-123">Gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span><br/> |
| <span data-ttu-id="2d76e-124">**Veraltet**: [ **idleduration**](idlesettings-idleduration.md)</span><span class="sxs-lookup"><span data-stu-id="2d76e-124">**Deprecated**: [**IdleDuration**](idlesettings-idleduration.md)</span></span><br/>   | <span data-ttu-id="2d76e-125">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d76e-125">Read/write</span></span><br/> | <span data-ttu-id="2d76e-126">Ruft einen Wert ab, der angibt, wie lange sich der Computer im Leerlauf befinden muss, bevor der Task ausgeführt wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="2d76e-126">Gets or sets a value that indicates the amount of time that the computer must be in an idle state before the task is run.</span></span><br/>                            |
| <span data-ttu-id="2d76e-127">**Veraltet**: [ **WaitTimeout**](idlesettings-waittimeout.md)</span><span class="sxs-lookup"><span data-stu-id="2d76e-127">**Deprecated**: [**WaitTimeout**](idlesettings-waittimeout.md)</span></span><br/>     | <span data-ttu-id="2d76e-128">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="2d76e-128">Read/write</span></span><br/> | <span data-ttu-id="2d76e-129">Ruft einen Wert ab oder legt einen Wert fest, der die Zeitspanne angibt, die der Taskplaner auf das Eintreten einer Leerlauf Bedingung wartet.</span><span class="sxs-lookup"><span data-stu-id="2d76e-129">Gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span><br/>                             |

## <a name="remarks"></a><span data-ttu-id="2d76e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d76e-130">Remarks</span></span>

<span data-ttu-id="2d76e-131">Beim Lesen oder Schreiben von XML für eine Aufgabe wird diese Einstellung im [**idlesettings**](taskschedulerschema-idlesettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d76e-131">When reading or writing XML for a task, this setting is specified in the [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="2d76e-132">Wenn eine Aufgabe durch einen Leerlauf Trigger ausgelöst wird, wird die [**idlesettings. WaitTimeout**](idlesettings-waittimeout.md) -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2d76e-132">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

> [!NOTE]
> <span data-ttu-id="2d76e-133">*Idlesettings. idleduration* und *idlesettings. WaitTimeout* sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="2d76e-133">*IdleSettings.IdleDuration* and *IdleSettings.WaitTimeout* are deprecated.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d76e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d76e-134">Requirements</span></span>

| <span data-ttu-id="2d76e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d76e-135">Requirement</span></span> | <span data-ttu-id="2d76e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2d76e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d76e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d76e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2d76e-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d76e-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2d76e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d76e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2d76e-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d76e-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d76e-141">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2d76e-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d76e-142"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2d76e-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2d76e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2d76e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d76e-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d76e-144"><dt>Taskschd.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="2d76e-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d76e-145">See also</span></span>

[<span data-ttu-id="2d76e-146">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="2d76e-146">Task Scheduler Objects</span></span>](task-scheduler-objects.md)

[<span data-ttu-id="2d76e-147">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="2d76e-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
