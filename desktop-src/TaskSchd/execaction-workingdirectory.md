---
title: Execaction. WorkingDirectory-Eigenschaft
description: Ruft bei der Skripterstellung das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- WorkingDirectory-Eigenschaft Taskplaner
- WorkingDirectory-Eigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, WorkingDirectory-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337309"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="7c993-106">Execaction. WorkingDirectory-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7c993-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="7c993-107">Ruft bei der Skripterstellung das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="7c993-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c993-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c993-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="7c993-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7c993-109">Property value</span></span>

<span data-ttu-id="7c993-110">Das Verzeichnis, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c993-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c993-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c993-111">Remarks</span></span>

<span data-ttu-id="7c993-112">Beim Lesen oder Schreiben von XML wird das Arbeitsverzeichnis der Anwendung im [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="7c993-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="7c993-113">Der Pfad wird geprüft, um sicherzustellen, dass er gültig ist, wenn die Aufgabe registriert wird, und nicht, wenn diese Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7c993-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c993-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c993-114">Requirements</span></span>



| <span data-ttu-id="7c993-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c993-115">Requirement</span></span> | <span data-ttu-id="7c993-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7c993-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c993-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c993-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7c993-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c993-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7c993-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c993-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7c993-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c993-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c993-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7c993-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c993-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c993-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c993-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7c993-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c993-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c993-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c993-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c993-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c993-126">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="7c993-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="7c993-127">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="7c993-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





