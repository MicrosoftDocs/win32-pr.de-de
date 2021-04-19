---
title: Restartondle (idlesettingstype)-Element
description: Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Restartondle-Element Taskplaner
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec1d20798b7ceb6ad6ebe2c3a92896600e36eec1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346539"
---
# <a name="restartonidle-idlesettingstype-element"></a><span data-ttu-id="dff82-104">Restartondle (idlesettingstype)-Element</span><span class="sxs-lookup"><span data-stu-id="dff82-104">RestartOnIdle (idleSettingsType) Element</span></span>

<span data-ttu-id="dff82-105">Gibt an, ob der Task neu gestartet wird, wenn der Computer mehrmals in eine Leerlauf Bedingung wechselt.</span><span class="sxs-lookup"><span data-stu-id="dff82-105">Specifies whether the task is restarted when the computer cycles into an idle condition more than once.</span></span>

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

<span data-ttu-id="dff82-106">Das **restartondle** -Element wird durch den komplexen [**idlesettingstype**](taskschedulerschema-idlesettingstype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="dff82-106">The **RestartOnIdle** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="dff82-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="dff82-107">Parent element</span></span>



| <span data-ttu-id="dff82-108">Element</span><span class="sxs-lookup"><span data-stu-id="dff82-108">Element</span></span>                                                                       | <span data-ttu-id="dff82-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="dff82-109">Derived from</span></span>                                                                 | <span data-ttu-id="dff82-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dff82-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dff82-111">**Idlesettings**</span><span class="sxs-lookup"><span data-stu-id="dff82-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="dff82-112">**idlesettingstype**</span><span class="sxs-lookup"><span data-stu-id="dff82-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="dff82-113">Gibt an, wie die Taskplaner Aufgaben ausführt, wenn sich der Computer im Leerlauf befindet.</span><span class="sxs-lookup"><span data-stu-id="dff82-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="dff82-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dff82-114">Remarks</span></span>

<span data-ttu-id="dff82-115">Dieses Element wird nur verwendet, wenn das [**terminateonidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) -Element auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dff82-115">This element is used only if the [**TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element is set to True.</span></span>

<span data-ttu-id="dff82-116">Bei der Skript Entwicklung werden diese Aufgaben Einstellungen mithilfe der [**idlesettings. restartondle**](idlesettings-restartonidle.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="dff82-116">For script development, this task settings is specified using the [**IdleSettings.RestartOnIdle**](idlesettings-restartonidle.md) property.</span></span>

<span data-ttu-id="dff82-117">Bei der C++-Entwicklung werden diese Aufgaben Einstellungen mithilfe der [**iidlesettings:: restartondle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="dff82-117">For C++ development, this task settings is specified using the [**IIdleSettings::RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) property.</span></span>

## <a name="examples"></a><span data-ttu-id="dff82-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dff82-118">Examples</span></span>

<span data-ttu-id="dff82-119">Der folgende XML-Code definiert eine Leerlauf Einstellung, die angibt, dass die Aufgabe nicht neu gestartet werden soll, wenn die Leerlauf Bedingung nicht erfüllt ist.</span><span class="sxs-lookup"><span data-stu-id="dff82-119">The following XML defines an idle setting that indicates that the task should not be restarted when the idle condition cycles.</span></span>


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="dff82-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dff82-120">Requirements</span></span>



| <span data-ttu-id="dff82-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dff82-121">Requirement</span></span> | <span data-ttu-id="dff82-122">Wert</span><span class="sxs-lookup"><span data-stu-id="dff82-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dff82-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dff82-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dff82-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dff82-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dff82-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dff82-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dff82-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dff82-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dff82-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dff82-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff82-128">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="dff82-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="dff82-129">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="dff82-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





