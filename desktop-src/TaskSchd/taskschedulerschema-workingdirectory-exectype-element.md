---
title: WorkingDirectory (exectype)-Element
description: Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- WorkingDirectory-Element Taskplaner
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341039"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="52fbc-104">WorkingDirectory (exectype)-Element</span><span class="sxs-lookup"><span data-stu-id="52fbc-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="52fbc-105">Gibt das Verzeichnis an, in dem die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="52fbc-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="52fbc-106">Das **WorkingDirectory** -Element wird durch den komplexen [**exectype**](taskschedulerschema-exectype-complextype.md) -Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="52fbc-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="52fbc-107">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="52fbc-107">Parent element</span></span>



| <span data-ttu-id="52fbc-108">Element</span><span class="sxs-lookup"><span data-stu-id="52fbc-108">Element</span></span>                                                      | <span data-ttu-id="52fbc-109">Abgeleitet von</span><span class="sxs-lookup"><span data-stu-id="52fbc-109">Derived from</span></span>                                                 | <span data-ttu-id="52fbc-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52fbc-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="52fbc-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="52fbc-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="52fbc-112">**exectype**</span><span class="sxs-lookup"><span data-stu-id="52fbc-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="52fbc-113">Gibt eine Aktion an, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="52fbc-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="52fbc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52fbc-114">Remarks</span></span>

<span data-ttu-id="52fbc-115">Bei der Skript Entwicklung wird das Arbeitsverzeichnis von der [**execaction. WorkingDirectory**](execaction-workingdirectory.md) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="52fbc-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="52fbc-116">Bei der C++-Entwicklung wird das Arbeitsverzeichnis durch die [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="52fbc-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="52fbc-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52fbc-117">Examples</span></span>

<span data-ttu-id="52fbc-118">Der folgende XML-Code definiert eine Ausführungs Aktion.</span><span class="sxs-lookup"><span data-stu-id="52fbc-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="52fbc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52fbc-119">Requirements</span></span>



| <span data-ttu-id="52fbc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52fbc-120">Requirement</span></span> | <span data-ttu-id="52fbc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="52fbc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="52fbc-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52fbc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="52fbc-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52fbc-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="52fbc-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52fbc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="52fbc-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52fbc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52fbc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52fbc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fbc-127">Schema Elemente Taskplaner</span><span class="sxs-lookup"><span data-stu-id="52fbc-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="52fbc-128">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="52fbc-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





