---
title: TaskService.GetFolder-Methode
description: Ruft für die Skripterstellung einen Ordner mit registrierten Tasks ab.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- GetFolder-Taskplaner
- GetFolder-Methode Taskplaner , TaskService-Objekt
- TaskService-Taskplaner , GetFolder-Methode
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
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387099"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="aa5f4-106">TaskService.GetFolder-Methode</span><span class="sxs-lookup"><span data-stu-id="aa5f4-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="aa5f4-107">Ruft für die Skripterstellung einen Ordner mit registrierten Tasks ab.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5f4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5f4-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="aa5f4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5f4-110">*pfad* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5f4-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5f4-111">Der Pfad zum abzurufenden Ordner.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="aa5f4-112">Verwenden Sie keinen zurücken Schrägstrich nach dem Namen des letzten Ordners im Pfad.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="aa5f4-113">Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="aa5f4-114">Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="aa5f4-115">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Taskordner und "." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="aa5f4-116">-Zeichen können nicht verwendet werden, um den übergeordneten Taskordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5f4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa5f4-117">Return value</span></span>

<span data-ttu-id="aa5f4-118">Ein [**TaskFolder-Objekt**](taskfolder.md) für den angeforderten Ordner.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa5f4-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-119">Requirements</span></span>



| <span data-ttu-id="aa5f4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa5f4-120">Requirement</span></span> | <span data-ttu-id="aa5f4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="aa5f4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5f4-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5f4-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5f4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="aa5f4-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5f4-125">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5f4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa5f4-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="aa5f4-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa5f4-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f4-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="aa5f4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5f4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5f4-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f4-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5f4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa5f4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5f4-131">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="aa5f4-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





