---
title: Registeredtaskcollection-Objekt
description: Skript Objekt, das alle registrierten Tasks enthält.
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- Registeredtaskcollection-Objekt Taskplaner
- Registeredtaskcollection-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040285"
---
# <a name="registeredtaskcollection-object"></a><span data-ttu-id="fc99e-105">Registeredtaskcollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="fc99e-105">RegisteredTaskCollection object</span></span>

<span data-ttu-id="fc99e-106">Skript Objekt, das alle registrierten Tasks enthält.</span><span class="sxs-lookup"><span data-stu-id="fc99e-106">Scripting object that contains all the tasks that are registered.</span></span>

## <a name="members"></a><span data-ttu-id="fc99e-107">Member</span><span class="sxs-lookup"><span data-stu-id="fc99e-107">Members</span></span>

<span data-ttu-id="fc99e-108">Das **registeredtaskcollection** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fc99e-108">The **RegisteredTaskCollection** object has these types of members:</span></span>

-   [<span data-ttu-id="fc99e-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc99e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc99e-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fc99e-110">Properties</span></span>

<span data-ttu-id="fc99e-111">Das **registeredtaskcollection** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fc99e-111">The **RegisteredTaskCollection** object has these properties.</span></span>



| <span data-ttu-id="fc99e-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fc99e-112">Property</span></span>                                                   | <span data-ttu-id="fc99e-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="fc99e-113">Access type</span></span>          | <span data-ttu-id="fc99e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc99e-114">Description</span></span>                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="fc99e-115">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="fc99e-115">**Count**</span></span>](registeredtaskcollection-count.md)<br/> | <span data-ttu-id="fc99e-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc99e-116">Read-only</span></span><br/> | <span data-ttu-id="fc99e-117">Ruft die Anzahl der registrierten Tasks in der-Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="fc99e-117">Gets the number of registered tasks in the collection.</span></span><br/>  |
| [<span data-ttu-id="fc99e-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc99e-118">**Item**</span></span>](registeredtaskcollection-item.md)<br/>   | <span data-ttu-id="fc99e-119">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="fc99e-119">Read-only</span></span><br/> | <span data-ttu-id="fc99e-120">Ruft die angegebene registrierte Aufgabe aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="fc99e-120">Gets the specified registered task from the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="fc99e-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc99e-121">Examples</span></span>

<span data-ttu-id="fc99e-122">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [Anzeigen von Aufgaben Namen und Zuständen (Skripterstellung)](displaying-task-names-and-state--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="fc99e-122">For more information and example code for this scripting object, see [Displaying Task Names and States (Scripting)](displaying-task-names-and-state--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc99e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc99e-123">Requirements</span></span>



| <span data-ttu-id="fc99e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc99e-124">Requirement</span></span> | <span data-ttu-id="fc99e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fc99e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc99e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fc99e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc99e-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc99e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fc99e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fc99e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc99e-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fc99e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc99e-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="fc99e-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc99e-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc99e-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc99e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fc99e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc99e-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc99e-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc99e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc99e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc99e-135">**Taskfolder. GetTasks**</span><span class="sxs-lookup"><span data-stu-id="fc99e-135">**TaskFolder.GetTasks**</span></span>](taskfolder-gettasks.md)
</dt> </dl>

 

 





