---
title: TaskFolder.CreateFolder-Methode
description: Erstellt für die Skripterstellung einen Ordner für verwandte Aufgaben.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- CreateFolder-Methode Taskplaner
- CreateFolder-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , CreateFolder-Methode
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
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387078"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="43b4e-106">TaskFolder.CreateFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="43b4e-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="43b4e-107">Erstellt für die Skripterstellung einen Ordner für verwandte Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="43b4e-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b4e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="43b4e-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="43b4e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="43b4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b4e-110">*folderName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b4e-111">Der Name, der zum Identifizieren des Ordners verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43b4e-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="43b4e-112">Wenn "FolderName \\ SubFolder1 \\ SubFolder2" angegeben ist, wird die gesamte Ordnerstruktur erstellt, wenn die Ordner nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="43b4e-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="43b4e-113">Dieser Parameter kann ein relativer Pfad zur aktuellen [**TaskFolder-Instanz**](taskfolder.md) sein.</span><span class="sxs-lookup"><span data-stu-id="43b4e-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="43b4e-114">Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben.</span><span class="sxs-lookup"><span data-stu-id="43b4e-114">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="43b4e-115">Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="43b4e-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="43b4e-116">Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43b4e-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="43b4e-117">-Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="43b4e-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="43b4e-118">*sddl* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b4e-119">Der Sicherheitsdeskriptor, der dem Ordner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="43b4e-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b4e-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43b4e-120">Return value</span></span>

<span data-ttu-id="43b4e-121">Ein [**TaskFolder-Objekt,**](taskfolder.md) das den neuen Unterordner darstellt.</span><span class="sxs-lookup"><span data-stu-id="43b4e-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b4e-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="43b4e-122">Requirements</span></span>



| <span data-ttu-id="43b4e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43b4e-123">Requirement</span></span> | <span data-ttu-id="43b4e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="43b4e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43b4e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43b4e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="43b4e-126">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="43b4e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43b4e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="43b4e-128">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43b4e-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="43b4e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="43b4e-130"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43b4e-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43b4e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="43b4e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43b4e-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b4e-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b4e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43b4e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b4e-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="43b4e-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





