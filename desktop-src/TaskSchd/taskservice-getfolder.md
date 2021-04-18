---
title: TaskService. GetFolder-Methode
description: Ruft bei der Skripterstellung einen Ordner registrierter Tasks ab.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder-Methode Taskplaner
- GetFolder-Methode Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, GetFolder-Methode
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341038"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="66b01-106">TaskService. GetFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="66b01-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="66b01-107">Ruft bei der Skripterstellung einen Ordner registrierter Tasks ab.</span><span class="sxs-lookup"><span data-stu-id="66b01-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="66b01-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="66b01-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="66b01-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="66b01-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66b01-110">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="66b01-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66b01-111">Der Pfad zu dem Ordner, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="66b01-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="66b01-112">Verwenden Sie keinen umgekehrten Schrägstrich nach dem letzten Ordnernamen im Pfad.</span><span class="sxs-lookup"><span data-stu-id="66b01-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="66b01-113">Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) .</span><span class="sxs-lookup"><span data-stu-id="66b01-113">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="66b01-114">Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder.</span><span class="sxs-lookup"><span data-stu-id="66b01-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="66b01-115">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="66b01-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="66b01-116">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="66b01-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66b01-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66b01-117">Return value</span></span>

<span data-ttu-id="66b01-118">Ein [**taskfolder**](taskfolder.md) -Objekt für den angeforderten Ordner.</span><span class="sxs-lookup"><span data-stu-id="66b01-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="66b01-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66b01-119">Requirements</span></span>



| <span data-ttu-id="66b01-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66b01-120">Requirement</span></span> | <span data-ttu-id="66b01-121">Wert</span><span class="sxs-lookup"><span data-stu-id="66b01-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66b01-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66b01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="66b01-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66b01-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="66b01-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66b01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="66b01-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66b01-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="66b01-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="66b01-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="66b01-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="66b01-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="66b01-128">DLL</span><span class="sxs-lookup"><span data-stu-id="66b01-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66b01-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66b01-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66b01-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66b01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66b01-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="66b01-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





