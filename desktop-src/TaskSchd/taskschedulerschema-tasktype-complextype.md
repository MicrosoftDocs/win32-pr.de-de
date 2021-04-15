---
title: komplexer TaskType-Typ (Taskplaner)
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Task-Element.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- komplexer TaskType-Typ Taskplaner
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477775"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="9bec4-104">komplexer TaskType-Typ</span><span class="sxs-lookup"><span data-stu-id="9bec4-104">taskType Complex Type</span></span>

<span data-ttu-id="9bec4-105">Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Task**](taskschedulerschema-task-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="9bec4-105">Defines the child elements and sequencing information for the [**Task**](taskschedulerschema-task-element.md) element.</span></span>

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="9bec4-106">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9bec4-106">Child elements</span></span>



| <span data-ttu-id="9bec4-107">Element</span><span class="sxs-lookup"><span data-stu-id="9bec4-107">Element</span></span>                                                                           | <span data-ttu-id="9bec4-108">type</span><span class="sxs-lookup"><span data-stu-id="9bec4-108">Type</span></span>                                                                                 | <span data-ttu-id="9bec4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bec4-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bec4-110">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="9bec4-110">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)                   | [<span data-ttu-id="9bec4-111">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="9bec4-111">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md)                   | <span data-ttu-id="9bec4-112">Gibt die Aktionen an, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9bec4-112">Specifies the actions performed by the task.</span></span><br/>                                                                             |
| [<span data-ttu-id="9bec4-113">**Daten**</span><span class="sxs-lookup"><span data-stu-id="9bec4-113">**Data**</span></span>](taskschedulerschema-data-tasktype-element.md)                         | [<span data-ttu-id="9bec4-114">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9bec4-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md)                         | <span data-ttu-id="9bec4-115">Gibt zusätzliche Daten an, die dem Task zugeordnet sind, wird aber vom Taskplaner-Dienst anderweitig nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bec4-115">Specifies addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span><br/>         |
| [<span data-ttu-id="9bec4-116">**Principals**</span><span class="sxs-lookup"><span data-stu-id="9bec4-116">**Principals**</span></span>](taskschedulerschema-principals-tasktype-element.md)             | [<span data-ttu-id="9bec4-117">**principalstype**</span><span class="sxs-lookup"><span data-stu-id="9bec4-117">**principalsType**</span></span>](taskschedulerschema-principalstype-complextype.md)             | <span data-ttu-id="9bec4-118">Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9bec4-118">Specifies the security contexts that can be used to run the task.</span></span><br/>                                                        |
| [<span data-ttu-id="9bec4-119">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="9bec4-119">**RegistrationInfo**</span></span>](taskschedulerschema-registrationinfo-tasktype-element.md) | [<span data-ttu-id="9bec4-120">**registrationinfotype**</span><span class="sxs-lookup"><span data-stu-id="9bec4-120">**registrationInfoType**</span></span>](taskschedulerschema-registrationinfotype-complextype.md) | <span data-ttu-id="9bec4-121">Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9bec4-121">Specifies administrative information about the task, such as the author of the task and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="9bec4-122">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="9bec4-122">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md)                 | [<span data-ttu-id="9bec4-123">**settingstype**</span><span class="sxs-lookup"><span data-stu-id="9bec4-123">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md)                 | <span data-ttu-id="9bec4-124">Gibt die Einstellungen an, die vom Taskplaner zum Ausführen der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bec4-124">Specifies the settings that the Task Scheduler uses to perform the task.</span></span><br/>                                                 |
| [<span data-ttu-id="9bec4-125">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="9bec4-125">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md)                 | [<span data-ttu-id="9bec4-126">**triggerstype**</span><span class="sxs-lookup"><span data-stu-id="9bec4-126">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md)                 | <span data-ttu-id="9bec4-127">Gibt die Trigger an, die den Task starten.</span><span class="sxs-lookup"><span data-stu-id="9bec4-127">Specifies the triggers that start the task.</span></span><br/>                                                                              |



## <a name="attributes"></a><span data-ttu-id="9bec4-128">Attributes</span><span class="sxs-lookup"><span data-stu-id="9bec4-128">Attributes</span></span>



| <span data-ttu-id="9bec4-129">Name</span><span class="sxs-lookup"><span data-stu-id="9bec4-129">Name</span></span>    | <span data-ttu-id="9bec4-130">type</span><span class="sxs-lookup"><span data-stu-id="9bec4-130">Type</span></span>                                                              | <span data-ttu-id="9bec4-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bec4-131">Description</span></span>                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="9bec4-132">version</span><span class="sxs-lookup"><span data-stu-id="9bec4-132">version</span></span> | [<span data-ttu-id="9bec4-133">**versiontype**</span><span class="sxs-lookup"><span data-stu-id="9bec4-133">**versionType**</span></span>](taskschedulerschema-versiontype-simpletype.md) | <span data-ttu-id="9bec4-134">Gibt die Version der Aufgabe an.</span><span class="sxs-lookup"><span data-stu-id="9bec4-134">Specifies the version of the task.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="9bec4-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bec4-135">Requirements</span></span>



| <span data-ttu-id="9bec4-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bec4-136">Requirement</span></span> | <span data-ttu-id="9bec4-137">Wert</span><span class="sxs-lookup"><span data-stu-id="9bec4-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9bec4-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bec4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="9bec4-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bec4-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9bec4-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bec4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="9bec4-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bec4-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9bec4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bec4-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bec4-143">Komplexe Typen von Taskplaner Schemas</span><span class="sxs-lookup"><span data-stu-id="9bec4-143">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9bec4-144">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="9bec4-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





