---
title: Exec (aktiongroup)-Element
description: Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Exec-Element Taskplaner
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106364296"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="e042e-104">Exec (aktiongroup)-Element</span><span class="sxs-lookup"><span data-stu-id="e042e-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="e042e-105">Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="e042e-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="e042e-106">Das **exec** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="e042e-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="e042e-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="e042e-107">Parent element</span></span>



| <span data-ttu-id="e042e-108">Element</span><span class="sxs-lookup"><span data-stu-id="e042e-108">Element</span></span>                                                         | <span data-ttu-id="e042e-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="e042e-109">Derived from</span></span>                                                       | <span data-ttu-id="e042e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e042e-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e042e-111">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="e042e-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="e042e-112">**Aktions sType**</span><span class="sxs-lookup"><span data-stu-id="e042e-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="e042e-113">Enthält die Aktionen, die vom Task ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e042e-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e042e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e042e-114">Child elements</span></span>



| <span data-ttu-id="e042e-115">Element</span><span class="sxs-lookup"><span data-stu-id="e042e-115">Element</span></span>                                                                           | <span data-ttu-id="e042e-116">type</span><span class="sxs-lookup"><span data-stu-id="e042e-116">Type</span></span>       | <span data-ttu-id="e042e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e042e-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e042e-118">**Argumente**</span><span class="sxs-lookup"><span data-stu-id="e042e-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="e042e-119">**string**</span><span class="sxs-lookup"><span data-stu-id="e042e-119">**string**</span></span> | <span data-ttu-id="e042e-120">Gibt die Argumente an, die dem Befehlszeilen Vorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e042e-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="e042e-121">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="e042e-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="e042e-122">**string**</span><span class="sxs-lookup"><span data-stu-id="e042e-122">**string**</span></span> | <span data-ttu-id="e042e-123">Gibt die ausführbare Datei oder das Dokument an, das ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e042e-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="e042e-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="e042e-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="e042e-125">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e042e-125">string</span></span>     | <span data-ttu-id="e042e-126">Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e042e-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="e042e-127">Attributes</span><span class="sxs-lookup"><span data-stu-id="e042e-127">Attributes</span></span>



| <span data-ttu-id="e042e-128">Name</span><span class="sxs-lookup"><span data-stu-id="e042e-128">Name</span></span> | <span data-ttu-id="e042e-129">type</span><span class="sxs-lookup"><span data-stu-id="e042e-129">Type</span></span>       | <span data-ttu-id="e042e-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e042e-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="e042e-131">id</span><span class="sxs-lookup"><span data-stu-id="e042e-131">id</span></span>   | <span data-ttu-id="e042e-132">**string**</span><span class="sxs-lookup"><span data-stu-id="e042e-132">**string**</span></span> | <span data-ttu-id="e042e-133">Der Bezeichner der Aktion, die von der Aufgabe ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e042e-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e042e-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e042e-134">Remarks</span></span>

<span data-ttu-id="e042e-135">Die oben aufgeführten untergeordneten Elemente werden durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e042e-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="e042e-136">Bei der Skript Entwicklung wird eine Ausführungs Aktion vom [**execaction**](execaction.md) -Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="e042e-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="e042e-137">Bei der C++-Entwicklung wird eine Ausführungs Aktion von der [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="e042e-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="e042e-138">Wenn Umgebungsvariablen in den Elementen [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md)oder [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) verwendet werden, werden die Werte der Umgebungsvariablen zwischengespeichert und verwendet, wenn die Taskeng.exe (Task-Engine) gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e042e-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="e042e-139">Änderungen an den Umgebungsvariablen, die nach dem Start der Task-Engine auftreten, werden von der Task-Engine nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e042e-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="e042e-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e042e-140">Examples</span></span>

<span data-ttu-id="e042e-141">Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers verwendet, finden Sie unter [time-auslöserbeispiel (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e042e-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e042e-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e042e-142">Requirements</span></span>



| <span data-ttu-id="e042e-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e042e-143">Requirement</span></span> | <span data-ttu-id="e042e-144">Wert</span><span class="sxs-lookup"><span data-stu-id="e042e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e042e-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e042e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e042e-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e042e-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e042e-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e042e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e042e-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e042e-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e042e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e042e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e042e-150">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="e042e-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





