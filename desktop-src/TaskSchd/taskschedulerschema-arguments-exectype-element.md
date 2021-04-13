---
title: Arguments (exectype)-Element
description: Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments-Element Taskplaner
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518194"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="60af5-104">Arguments (exectype)-Element</span><span class="sxs-lookup"><span data-stu-id="60af5-104">Arguments (execType) Element</span></span>

<span data-ttu-id="60af5-105">Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="60af5-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="60af5-106">Das **Arguments** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="60af5-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="60af5-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="60af5-107">Parent element</span></span>



| <span data-ttu-id="60af5-108">Element</span><span class="sxs-lookup"><span data-stu-id="60af5-108">Element</span></span>                                                      | <span data-ttu-id="60af5-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="60af5-109">Derived from</span></span>                                                 | <span data-ttu-id="60af5-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60af5-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="60af5-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="60af5-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="60af5-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="60af5-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="60af5-113">Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="60af5-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="60af5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60af5-114">Remarks</span></span>

<span data-ttu-id="60af5-115">Informationen zur C++-Entwicklung finden Sie unter der [**Arguments-Eigenschaft von IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="60af5-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="60af5-116">Informationen zur Skript Entwicklung finden Sie unter [**execaction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="60af5-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="60af5-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60af5-117">Examples</span></span>

<span data-ttu-id="60af5-118">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine ausführbare Aktion verwendet, finden Sie unter [time-triggerbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="60af5-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60af5-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60af5-119">Requirements</span></span>



| <span data-ttu-id="60af5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60af5-120">Requirement</span></span> | <span data-ttu-id="60af5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="60af5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="60af5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="60af5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="60af5-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60af5-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="60af5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="60af5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="60af5-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="60af5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="60af5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60af5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60af5-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="60af5-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





