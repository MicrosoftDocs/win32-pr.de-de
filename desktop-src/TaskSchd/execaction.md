---
title: Execaction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Aktion Taskplaner ausführen, Schnittstelle
- Execaction-Objekt Taskplaner
- Taskplaner des execaction-Objekts, beschrieben
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105692"
---
# <a name="execaction-object"></a><span data-ttu-id="31e22-106">Execaction-Objekt</span><span class="sxs-lookup"><span data-stu-id="31e22-106">ExecAction object</span></span>

<span data-ttu-id="31e22-107">Skript Objekt, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="31e22-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="31e22-108">Member</span><span class="sxs-lookup"><span data-stu-id="31e22-108">Members</span></span>

<span data-ttu-id="31e22-109">Das **execaction** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="31e22-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="31e22-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31e22-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31e22-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="31e22-111">Properties</span></span>

<span data-ttu-id="31e22-112">Das **execaction** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="31e22-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="31e22-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="31e22-113">Property</span></span>                                                            | <span data-ttu-id="31e22-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="31e22-114">Access type</span></span>           | <span data-ttu-id="31e22-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31e22-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31e22-116">**Argumente**</span><span class="sxs-lookup"><span data-stu-id="31e22-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="31e22-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e22-117">Read/write</span></span><br/> | <span data-ttu-id="31e22-118">Ruft die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="31e22-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="31e22-119">**Name**</span><span class="sxs-lookup"><span data-stu-id="31e22-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="31e22-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e22-120">Read/write</span></span><br/> | <span data-ttu-id="31e22-121">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="31e22-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="31e22-122">Ruft den Bezeichner der Aktion ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="31e22-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="31e22-123">**ADS**</span><span class="sxs-lookup"><span data-stu-id="31e22-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="31e22-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e22-124">Read/write</span></span><br/> | <span data-ttu-id="31e22-125">Ruft den Pfad zu einer ausführbaren Datei ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="31e22-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="31e22-126">**type**</span><span class="sxs-lookup"><span data-stu-id="31e22-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="31e22-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="31e22-127">Read-only</span></span><br/>  | <span data-ttu-id="31e22-128">Wird vom [**Action**](action.md) -Objekt geerbt.</span><span class="sxs-lookup"><span data-stu-id="31e22-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="31e22-129">Ruft den Typ der Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="31e22-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="31e22-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="31e22-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="31e22-131">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="31e22-131">Read/write</span></span><br/> | <span data-ttu-id="31e22-132">Ruft das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="31e22-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="31e22-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31e22-133">Remarks</span></span>

<span data-ttu-id="31e22-134">Wenn Umgebungsvariablen in den [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)-, [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)-oder [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) -Eigenschaften verwendet werden, werden die Werte der Umgebungsvariablen zwischengespeichert und verwendet, wenn die Taskeng.exe (Task-Engine) gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="31e22-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="31e22-135">Änderungen an den Umgebungsvariablen, die nach dem Start der Task-Engine auftreten, werden von der Task-Engine nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="31e22-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="31e22-136">Diese Aktion führt einen Befehlszeilen Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="31e22-136">This action performs a command-line operation.</span></span> <span data-ttu-id="31e22-137">Beispielsweise könnte die Aktion ein Skript ausführen oder eine ausführbare Datei starten.</span><span class="sxs-lookup"><span data-stu-id="31e22-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="31e22-138">Beim Lesen oder Schreiben von XML wird im [**exec**](taskschedulerschema-exec-actiongroup-element.md) -Element des Taskplaner Schemas eine Ausführungs Aktion angegeben.</span><span class="sxs-lookup"><span data-stu-id="31e22-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="31e22-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31e22-139">Examples</span></span>

<span data-ttu-id="31e22-140">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="31e22-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31e22-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31e22-141">Requirements</span></span>



| <span data-ttu-id="31e22-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31e22-142">Requirement</span></span> | <span data-ttu-id="31e22-143">Wert</span><span class="sxs-lookup"><span data-stu-id="31e22-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31e22-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31e22-144">Minimum supported client</span></span><br/> | <span data-ttu-id="31e22-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31e22-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="31e22-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31e22-146">Minimum supported server</span></span><br/> | <span data-ttu-id="31e22-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31e22-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31e22-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="31e22-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="31e22-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31e22-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31e22-150">DLL</span><span class="sxs-lookup"><span data-stu-id="31e22-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31e22-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31e22-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





