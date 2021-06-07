---
title: TaskFolder.Path (Eigenschaft)
description: Ruft für die Skripterstellung den Pfad zum Ort ab, in dem der Ordner gespeichert ist.
ms.assetid: a0b28527-4875-4fe4-b2dd-08abbdc87ccc
keywords:
- Path-Taskplaner
- Path-Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , Path-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c917a7f03a28f7b5c379673229976897af9b5f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387009"
---
# <a name="taskfolderpath-property"></a><span data-ttu-id="82501-106">TaskFolder.Path (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="82501-106">TaskFolder.Path property</span></span>

<span data-ttu-id="82501-107">Ruft für die Skripterstellung den Pfad zum Ort ab, in dem der Ordner gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="82501-107">For scripting, gets the path to where the folder is stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="82501-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="82501-108">Syntax</span></span>


```VB
TaskFolder.Path As String
```



## <a name="property-value"></a><span data-ttu-id="82501-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="82501-109">Property value</span></span>

<span data-ttu-id="82501-110">Der Pfad, in dem der Ordner gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="82501-110">The path to where the folder is stored.</span></span> <span data-ttu-id="82501-111">Der Stammordner des Task wird mit einem schrägen Schrägstrich () \\ angegeben.</span><span class="sxs-lookup"><span data-stu-id="82501-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="82501-112">Ein Beispiel für einen Taskordnerpfad unter dem Stammaufgabenordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="82501-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="82501-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="82501-113">Requirements</span></span>



| <span data-ttu-id="82501-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82501-114">Requirement</span></span> | <span data-ttu-id="82501-115">Wert</span><span class="sxs-lookup"><span data-stu-id="82501-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82501-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82501-116">Minimum supported client</span></span><br/> | <span data-ttu-id="82501-117">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82501-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82501-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82501-118">Minimum supported server</span></span><br/> | <span data-ttu-id="82501-119">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="82501-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82501-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="82501-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="82501-121"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="82501-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="82501-122">DLL</span><span class="sxs-lookup"><span data-stu-id="82501-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82501-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82501-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82501-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82501-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82501-125">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="82501-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





