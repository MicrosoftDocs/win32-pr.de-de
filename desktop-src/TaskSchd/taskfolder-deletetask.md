---
title: Taskfolder. DeleteTask-Methode
description: Löscht bei der Skripterstellung eine Aufgabe aus dem Ordner.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- DeleteTask-Methode Taskplaner
- DeleteTask-Methode Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, DeleteTask-Methode
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742176"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="adb8d-106">Taskfolder. DeleteTask-Methode</span><span class="sxs-lookup"><span data-stu-id="adb8d-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="adb8d-107">Löscht bei der Skripterstellung eine Aufgabe aus dem Ordner.</span><span class="sxs-lookup"><span data-stu-id="adb8d-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb8d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="adb8d-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="adb8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="adb8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adb8d-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adb8d-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb8d-111">Der Name der Aufgabe, die beim Registrieren der Aufgabe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="adb8d-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="adb8d-112">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="adb8d-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="adb8d-113">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="adb8d-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="adb8d-114">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="adb8d-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adb8d-115">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adb8d-115">Not supported.</span></span> <span data-ttu-id="adb8d-116">Der Wert ist 0.</span><span class="sxs-lookup"><span data-stu-id="adb8d-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adb8d-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="adb8d-117">Return value</span></span>

<span data-ttu-id="adb8d-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="adb8d-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="adb8d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adb8d-119">Requirements</span></span>



| <span data-ttu-id="adb8d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adb8d-120">Requirement</span></span> | <span data-ttu-id="adb8d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="adb8d-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adb8d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="adb8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="adb8d-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb8d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="adb8d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="adb8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="adb8d-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="adb8d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="adb8d-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="adb8d-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="adb8d-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="adb8d-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="adb8d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="adb8d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adb8d-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adb8d-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adb8d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adb8d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adb8d-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="adb8d-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





