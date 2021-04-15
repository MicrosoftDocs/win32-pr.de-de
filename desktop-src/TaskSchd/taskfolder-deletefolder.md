---
title: Taskfolder. DeleteFolder-Methode
description: Bei der Skripterstellung wird ein Unterordner aus dem übergeordneten Ordner gelöscht.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder-Methode Taskplaner
- DeleteFolder-Methode Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, DeleteFolder-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477481"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="4d673-106">Taskfolder. DeleteFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="4d673-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="4d673-107">Bei der Skripterstellung wird ein Unterordner aus dem übergeordneten Ordner gelöscht.</span><span class="sxs-lookup"><span data-stu-id="4d673-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d673-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d673-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="4d673-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d673-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d673-110">*FolderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d673-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d673-111">Der Name des unter Ordners, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d673-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="4d673-112">Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) .</span><span class="sxs-lookup"><span data-stu-id="4d673-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="4d673-113">Dieser Parameter kann ein relativer Pfad zu dem Ordner sein, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="4d673-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="4d673-114">Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder.</span><span class="sxs-lookup"><span data-stu-id="4d673-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="4d673-115">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4d673-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="4d673-116">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4d673-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="4d673-117">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d673-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d673-118">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d673-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d673-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d673-119">Return value</span></span>

<span data-ttu-id="4d673-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4d673-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d673-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d673-121">Requirements</span></span>



| <span data-ttu-id="4d673-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d673-122">Requirement</span></span> | <span data-ttu-id="4d673-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4d673-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d673-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d673-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4d673-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d673-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4d673-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d673-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4d673-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d673-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d673-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4d673-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="4d673-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d673-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d673-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4d673-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d673-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d673-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d673-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d673-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d673-133">**Task Folder**</span><span class="sxs-lookup"><span data-stu-id="4d673-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="4d673-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="4d673-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





