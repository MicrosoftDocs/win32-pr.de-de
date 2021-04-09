---
title: Taskfolder. gettask-Eigenschaft
description: Ruft bei der Skripterstellung eine Aufgabe an einer angegebenen Position in einem Ordner ab.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Gettask-Eigenschaft Taskplaner
- Gettask-Eigenschaft Taskplaner, taskfolder-Objekt
- Task Folder-Objekt Taskplaner, gettask-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740600"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="3e52c-106">Taskfolder. gettask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e52c-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="3e52c-107">Ruft bei der Skripterstellung eine Aufgabe an einer angegebenen Position in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="3e52c-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e52c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e52c-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="3e52c-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3e52c-109">Property value</span></span>

<span data-ttu-id="3e52c-110">Der Pfad (Speicherort) für die Aufgabe in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="3e52c-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="3e52c-111">Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) .</span><span class="sxs-lookup"><span data-stu-id="3e52c-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="3e52c-112">Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder.</span><span class="sxs-lookup"><span data-stu-id="3e52c-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="3e52c-113">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3e52c-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="3e52c-114">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3e52c-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e52c-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3e52c-115">Error codes</span></span>

<span data-ttu-id="3e52c-116">Die Aufgabe an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="3e52c-116">The task at the specified location.</span></span> <span data-ttu-id="3e52c-117">Der Task ist ein [**registeredtask**](registeredtask.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e52c-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e52c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e52c-118">Requirements</span></span>



| <span data-ttu-id="3e52c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e52c-119">Requirement</span></span> | <span data-ttu-id="3e52c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3e52c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e52c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e52c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3e52c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3e52c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e52c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3e52c-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e52c-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3e52c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e52c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e52c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3e52c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e52c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





