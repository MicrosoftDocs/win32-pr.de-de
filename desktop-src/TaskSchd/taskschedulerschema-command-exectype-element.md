---
title: Command (exectype)-Element
description: Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Command-Element Taskplaner
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392121"
---
# <a name="command-exectype-element"></a><span data-ttu-id="8e5cf-104">Command (exectype)-Element</span><span class="sxs-lookup"><span data-stu-id="8e5cf-104">Command (execType) Element</span></span>

<span data-ttu-id="8e5cf-105">Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="8e5cf-106">Das **Command** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8e5cf-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="8e5cf-107">Parent element</span></span>



| <span data-ttu-id="8e5cf-108">Element</span><span class="sxs-lookup"><span data-stu-id="8e5cf-108">Element</span></span>                                                      | <span data-ttu-id="8e5cf-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="8e5cf-109">Derived from</span></span>                                                 | <span data-ttu-id="8e5cf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e5cf-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="8e5cf-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="8e5cf-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="8e5cf-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="8e5cf-113">Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="8e5cf-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8e5cf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e5cf-114">Remarks</span></span>

<span data-ttu-id="8e5cf-115">Informationen zur C++-Entwicklung finden Sie unter der [**Arguments-Eigenschaft von IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="8e5cf-116">Informationen zur Skript Entwicklung finden Sie unter [**execaction. Arguments**](execaction-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e5cf-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e5cf-117">Examples</span></span>

<span data-ttu-id="8e5cf-118">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die eine ausführbare Aktion verwendet, finden Sie unter [time-triggerbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="8e5cf-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e5cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e5cf-119">Requirements</span></span>



| <span data-ttu-id="8e5cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e5cf-120">Requirement</span></span> | <span data-ttu-id="8e5cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8e5cf-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8e5cf-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5cf-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e5cf-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8e5cf-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e5cf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5cf-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e5cf-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8e5cf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e5cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e5cf-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="8e5cf-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





