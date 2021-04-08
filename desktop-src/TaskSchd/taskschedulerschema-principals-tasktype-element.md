---
title: Principals (TaskType)-Element
description: Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Principals-Element Taskplaner
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949516"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="fbf8d-104">Principals (TaskType)-Element</span><span class="sxs-lookup"><span data-stu-id="fbf8d-104">Principals (taskType) Element</span></span>

<span data-ttu-id="fbf8d-105">Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="fbf8d-106">Das **Principals** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fbf8d-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="fbf8d-107">Parent element</span></span>



| <span data-ttu-id="fbf8d-108">Element</span><span class="sxs-lookup"><span data-stu-id="fbf8d-108">Element</span></span>                                          | <span data-ttu-id="fbf8d-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="fbf8d-109">Derived from</span></span>                                                 | <span data-ttu-id="fbf8d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbf8d-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="fbf8d-111">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="fbf8d-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="fbf8d-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="fbf8d-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="fbf8d-113">Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="fbf8d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf8d-114">Child elements</span></span>



| <span data-ttu-id="fbf8d-115">Element</span><span class="sxs-lookup"><span data-stu-id="fbf8d-115">Element</span></span>                                                                  | <span data-ttu-id="fbf8d-116">type</span><span class="sxs-lookup"><span data-stu-id="fbf8d-116">Type</span></span>                                                                   | <span data-ttu-id="fbf8d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbf8d-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="fbf8d-118">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="fbf8d-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="fbf8d-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="fbf8d-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="fbf8d-120">Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fbf8d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbf8d-121">Remarks</span></span>

<span data-ttu-id="fbf8d-122">Sie können bis zu 32 Prinzipale für eine Aufgabe angeben.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="fbf8d-123">Bei der Skripterstellung werden die Prinzipale einer Aufgabe mithilfe der [**Taskdefinition. Principal**](taskdefinition-principal.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="fbf8d-124">Bei der C++-Entwicklung werden die Prinzipale einer Aufgabe mithilfe der [**Principal-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)angegeben.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="fbf8d-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbf8d-125">Examples</span></span>

<span data-ttu-id="fbf8d-126">Der folgende XML-Code definiert zwei Prinzipale: eine Benutzer-ID und einen gruppenbezeichnerprinzipal für die Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="fbf8d-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="fbf8d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbf8d-127">Requirements</span></span>



| <span data-ttu-id="fbf8d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbf8d-128">Requirement</span></span> | <span data-ttu-id="fbf8d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="fbf8d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fbf8d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fbf8d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf8d-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf8d-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fbf8d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fbf8d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf8d-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fbf8d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbf8d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbf8d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf8d-135">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="fbf8d-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fbf8d-136">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="fbf8d-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





