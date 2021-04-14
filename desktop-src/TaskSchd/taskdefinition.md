---
title: Taskdefinition-Objekt
description: Skript Objekt, das alle Komponenten einer Aufgabe definiert, z. b. die Aufgaben Einstellungen, Trigger, Aktionen und Registrierungsinformationen.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Taskdefinition-Objekt Taskplaner
- Task Definition-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518077"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="02127-105">Taskdefinition-Objekt</span><span class="sxs-lookup"><span data-stu-id="02127-105">TaskDefinition object</span></span>

<span data-ttu-id="02127-106">Skript Objekt, das alle Komponenten einer Aufgabe definiert, z. b. die Aufgaben Einstellungen, Trigger, Aktionen und Registrierungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="02127-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="02127-107">Member</span><span class="sxs-lookup"><span data-stu-id="02127-107">Members</span></span>

<span data-ttu-id="02127-108">Das **Taskdefinition** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02127-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="02127-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02127-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02127-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02127-110">Properties</span></span>

<span data-ttu-id="02127-111">Das **Taskdefinition** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02127-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="02127-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="02127-112">Property</span></span>                                                               | <span data-ttu-id="02127-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="02127-113">Access type</span></span>           | <span data-ttu-id="02127-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02127-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02127-115">**Aktionen**</span><span class="sxs-lookup"><span data-stu-id="02127-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="02127-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-116">Read/write</span></span><br/> | <span data-ttu-id="02127-117">Ruft eine Auflistung von Aktionen ab, die vom Task ausgeführt werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02127-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="02127-118">**Daten**</span><span class="sxs-lookup"><span data-stu-id="02127-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="02127-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-119">Read/write</span></span><br/> | <span data-ttu-id="02127-120">Ruft die Daten ab, die der Aufgabe zugeordnet sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02127-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="02127-121">Diese Daten werden vom Taskplaner-Dienst ignoriert, aber von Drittanbietern verwendet, die das Aufgaben Format erweitern möchten.</span><span class="sxs-lookup"><span data-stu-id="02127-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="02127-122">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="02127-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="02127-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-123">Read/write</span></span><br/> | <span data-ttu-id="02127-124">Ruft den Prinzipal für die Aufgabe ab, die die Sicherheits Anmelde Informationen für den Task bereitstellt, oder legt ihn fest</span><span class="sxs-lookup"><span data-stu-id="02127-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="02127-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="02127-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="02127-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-126">Read/write</span></span><br/> | <span data-ttu-id="02127-127">Ruft die Registrierungsinformationen ab, die zum Beschreiben einer Aufgabe verwendet werden, z. b. die Beschreibung der Aufgabe, den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02127-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="02127-128">**Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="02127-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="02127-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-129">Read/write</span></span><br/> | <span data-ttu-id="02127-130">Ruft die Einstellungen ab, die definieren, wie der Taskplaner-Dienst die Aufgabe ausführt, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02127-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="02127-131">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="02127-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="02127-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-132">Read/write</span></span><br/> | <span data-ttu-id="02127-133">Ruft eine Auflistung von Triggern ab, die zum Starten einer Aufgabe verwendet werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="02127-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="02127-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="02127-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="02127-135">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="02127-135">Read/write</span></span><br/> | <span data-ttu-id="02127-136">Ruft die XML-formatierte Definition der Aufgabe ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="02127-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="02127-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02127-137">Remarks</span></span>

<span data-ttu-id="02127-138">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe wird eine Aufgabendefinition mithilfe des [**Task**](taskschedulerschema-task-element.md) -Elements des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="02127-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="02127-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02127-139">Examples</span></span>

<span data-ttu-id="02127-140">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md) , [Ereignis auslöserbeispiel (Skripterstellung)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), Beispiel für den täglichen Auslösung [(Skripterstellung)](daily-trigger-example--scripting-.md), Registrierungs- [auslöserbeispiel (Skripterstellung)](registration-trigger-example--scripting-.md), Beispiel für einen wöchentlichen Aufruf [(](weekly-trigger-example--scripting-.md)Skripterstellung), Beispiel für LOGON-Beispiel [(Skript](logon-trigger-example--scripting-.md)Erstellung) oder [Beispiel](boot-trigger-example--scripting-.md)für</span><span class="sxs-lookup"><span data-stu-id="02127-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02127-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02127-141">Requirements</span></span>



| <span data-ttu-id="02127-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02127-142">Requirement</span></span> | <span data-ttu-id="02127-143">Wert</span><span class="sxs-lookup"><span data-stu-id="02127-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02127-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02127-144">Minimum supported client</span></span><br/> | <span data-ttu-id="02127-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02127-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="02127-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02127-146">Minimum supported server</span></span><br/> | <span data-ttu-id="02127-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02127-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02127-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="02127-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="02127-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="02127-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="02127-150">DLL</span><span class="sxs-lookup"><span data-stu-id="02127-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02127-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02127-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





