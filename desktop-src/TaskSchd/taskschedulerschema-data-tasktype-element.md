---
title: Data (TaskType)-Element
description: Definiert Additions Daten, die dem Task zugeordnet sind, aber anderweitig vom Taskplaner Dienst nicht verwendet werden.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
keywords:
- Datenelement Taskplaner
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740825"
---
# <a name="data-tasktype-element"></a><span data-ttu-id="5002b-104">Data (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="5002b-104">Data (taskType) Element</span></span>

<span data-ttu-id="5002b-105">Definiert Additions Daten, die dem Task zugeordnet sind, aber anderweitig vom Taskplaner Dienst nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5002b-105">Defines addition data that is associated with the task, but is otherwise unused by the Task Scheduler service.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="5002b-106">Das **Data** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="5002b-106">The **Data** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5002b-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="5002b-107">Parent element</span></span>



| <span data-ttu-id="5002b-108">Element</span><span class="sxs-lookup"><span data-stu-id="5002b-108">Element</span></span>                                          | <span data-ttu-id="5002b-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="5002b-109">Derived from</span></span>                                                 | <span data-ttu-id="5002b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5002b-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5002b-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="5002b-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="5002b-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="5002b-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="5002b-113">Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5002b-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5002b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5002b-114">Remarks</span></span>

<span data-ttu-id="5002b-115">Als Beispiel für diese Art von Daten verwendet der Leistungsprotokolle und-Warnungen-Dienst diese Eigenschaft als Speicher Container für die einem Task zugeordnete Leistungs-Leistungs Zählers-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5002b-115">As an example of this type of data, the Performance Logs and Alerts service uses this property as a storage container for the perf counter query associated with a task.</span></span>

<span data-ttu-id="5002b-116">Bei der C++-Entwicklung werden die Daten einer Aufgabe mithilfe der [**Data-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data)angegeben.</span><span class="sxs-lookup"><span data-stu-id="5002b-116">For C++ development, the data of a task is specified using the [**Data property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data).</span></span>

<span data-ttu-id="5002b-117">Bei der Skripterstellung werden die Daten einer Aufgabe mithilfe der [**Taskdefinition. Data**](taskdefinition-data.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="5002b-117">In scripting development, the data of a task is specified using the [**TaskDefinition.Data**](taskdefinition-data.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5002b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5002b-118">Requirements</span></span>



| <span data-ttu-id="5002b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5002b-119">Requirement</span></span> | <span data-ttu-id="5002b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5002b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5002b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5002b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5002b-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5002b-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5002b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5002b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5002b-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5002b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5002b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5002b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5002b-126">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="5002b-126">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5002b-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="5002b-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





