---
title: Taskfolder. kreatefolder-Methode
description: Erstellt bei der Skripterstellung einen Ordner für Verwandte Aufgaben.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Taskplaner der Methode "kreatefolder"
- Methode der Methode "Taskplaner", "taskfolder"-Objekt
- Task Folder-Objekt Taskplaner, Methode "kreatefolder"
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341812"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="44ca6-106">Taskfolder. kreatefolder-Methode</span><span class="sxs-lookup"><span data-stu-id="44ca6-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="44ca6-107">Erstellt bei der Skripterstellung einen Ordner für Verwandte Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="44ca6-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ca6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="44ca6-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="44ca6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="44ca6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ca6-110">*FolderName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44ca6-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44ca6-111">Der Name, der zum Identifizieren des Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44ca6-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="44ca6-112">Wenn "FolderName \\ Unterordner1 \\ SubFolder2" angegeben wird, wird die gesamte Ordnerstruktur erstellt, wenn die Ordner nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="44ca6-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="44ca6-113">Dieser Parameter kann ein relativer Pfad zur aktuellen [**Task Folder**](taskfolder.md) -Instanz sein.</span><span class="sxs-lookup"><span data-stu-id="44ca6-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="44ca6-114">Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) .</span><span class="sxs-lookup"><span data-stu-id="44ca6-114">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="44ca6-115">Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder.</span><span class="sxs-lookup"><span data-stu-id="44ca6-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="44ca6-116">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="44ca6-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="44ca6-117">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="44ca6-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="44ca6-118">*SDDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44ca6-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44ca6-119">Die Sicherheits Beschreibung, die dem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="44ca6-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ca6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44ca6-120">Return value</span></span>

<span data-ttu-id="44ca6-121">Ein [**taskfolder**](taskfolder.md) -Objekt, das den neuen Unterordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="44ca6-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ca6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44ca6-122">Requirements</span></span>



| <span data-ttu-id="44ca6-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44ca6-123">Requirement</span></span> | <span data-ttu-id="44ca6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="44ca6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44ca6-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44ca6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44ca6-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ca6-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="44ca6-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44ca6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44ca6-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44ca6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44ca6-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="44ca6-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="44ca6-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="44ca6-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="44ca6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="44ca6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44ca6-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ca6-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ca6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44ca6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ca6-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="44ca6-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





