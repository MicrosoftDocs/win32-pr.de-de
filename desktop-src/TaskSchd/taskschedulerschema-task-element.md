---
title: Task-Element
description: Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- Task-Element Taskplaner
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858736"
---
# <a name="task-element"></a><span data-ttu-id="67e3b-104">Task-Element</span><span class="sxs-lookup"><span data-stu-id="67e3b-104">Task Element</span></span>

<span data-ttu-id="67e3b-105">Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67e3b-105">Defines the task that is performed by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="67e3b-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="67e3b-106">Child elements</span></span>



| <span data-ttu-id="67e3b-107">Element</span><span class="sxs-lookup"><span data-stu-id="67e3b-107">Element</span></span>                                                                           | <span data-ttu-id="67e3b-108">type</span><span class="sxs-lookup"><span data-stu-id="67e3b-108">Type</span></span>                                                                                 | <span data-ttu-id="67e3b-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="67e3b-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67e3b-110">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="67e3b-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="67e3b-111">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="67e3b-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="67e3b-112">Gibt die Aktionen an, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="67e3b-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="67e3b-113">**Daten**</span><span class="sxs-lookup"><span data-stu-id="67e3b-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="67e3b-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="67e3b-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="67e3b-115">Gibt zusätzliche Daten an, die dem Task zugeordnet sind, wird aber vom Taskplaner-Dienst anderweitig nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="67e3b-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="67e3b-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="67e3b-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="67e3b-117">**principalstype**</span><span class="sxs-lookup"><span data-stu-id="67e3b-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="67e3b-118">Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="67e3b-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="67e3b-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="67e3b-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="67e3b-120">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="67e3b-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="67e3b-121">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="67e3b-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="67e3b-122">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="67e3b-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="67e3b-123">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="67e3b-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="67e3b-124">Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67e3b-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="67e3b-125">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="67e3b-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="67e3b-126">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="67e3b-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="67e3b-127">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="67e3b-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="remarks"></a><span data-ttu-id="67e3b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67e3b-128">Remarks</span></span>

<span data-ttu-id="67e3b-129">Informationen zur C++-Entwicklung finden Sie unter [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span><span class="sxs-lookup"><span data-stu-id="67e3b-129">For C++ development, see [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).</span></span>

<span data-ttu-id="67e3b-130">Informationen zur Skript Entwicklung finden Sie unter [**Task Definition**](taskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="67e3b-130">For script development, see [**TaskDefinition**](taskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67e3b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67e3b-131">Requirements</span></span>



| <span data-ttu-id="67e3b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67e3b-132">Requirement</span></span> | <span data-ttu-id="67e3b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="67e3b-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67e3b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67e3b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="67e3b-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e3b-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67e3b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67e3b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="67e3b-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67e3b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





