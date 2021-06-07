---
title: TaskFolder.DeleteFolder-Methode
description: Für die Skripterstellung löscht einen Unterordner aus dem übergeordneten Ordner.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- DeleteFolder-Taskplaner
- DeleteFolder-Methode Taskplaner , TaskFolder-Objekt
- TaskFolder-Taskplaner , DeleteFolder-Methode
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
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387039"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="99a08-106">TaskFolder.DeleteFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="99a08-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="99a08-107">Für die Skripterstellung löscht einen Unterordner aus dem übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="99a08-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a08-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="99a08-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="99a08-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="99a08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a08-110">*folderName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="99a08-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a08-111">Der Name des zu entfernenden Unterordners.</span><span class="sxs-lookup"><span data-stu-id="99a08-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="99a08-112">Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben.</span><span class="sxs-lookup"><span data-stu-id="99a08-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="99a08-113">Dieser Parameter kann ein relativer Pfad zu dem Ordner sein, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="99a08-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="99a08-114">Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="99a08-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="99a08-115">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und "." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="99a08-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="99a08-116">-Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="99a08-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="99a08-117">*Flags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="99a08-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99a08-118">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99a08-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a08-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99a08-119">Return value</span></span>

<span data-ttu-id="99a08-120">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="99a08-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a08-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="99a08-121">Requirements</span></span>



| <span data-ttu-id="99a08-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99a08-122">Requirement</span></span> | <span data-ttu-id="99a08-123">Wert</span><span class="sxs-lookup"><span data-stu-id="99a08-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99a08-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99a08-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99a08-125">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99a08-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="99a08-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99a08-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99a08-127">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99a08-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99a08-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="99a08-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="99a08-129"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99a08-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99a08-130">DLL</span><span class="sxs-lookup"><span data-stu-id="99a08-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99a08-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99a08-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a08-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99a08-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99a08-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="99a08-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="99a08-134">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="99a08-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





