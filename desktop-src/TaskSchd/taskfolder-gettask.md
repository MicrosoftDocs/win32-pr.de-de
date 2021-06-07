---
title: TaskFolder.GetTask-Eigenschaft
description: Ruft für die Skripterstellung eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- GetTask-Eigenschaft Taskplaner
- GetTask-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , GetTask-Eigenschaft
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387676"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="d0d91-106">TaskFolder.GetTask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d0d91-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="d0d91-107">Ruft für die Skripterstellung eine Aufgabe an einem angegebenen Speicherort in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="d0d91-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0d91-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0d91-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="d0d91-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d0d91-109">Property value</span></span>

<span data-ttu-id="d0d91-110">Der Pfad (Speicherort) der Aufgabe in einem Ordner.</span><span class="sxs-lookup"><span data-stu-id="d0d91-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="d0d91-111">Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben.</span><span class="sxs-lookup"><span data-stu-id="d0d91-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="d0d91-112">Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="d0d91-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="d0d91-113">Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0d91-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d0d91-114">-Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d0d91-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d0d91-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="d0d91-115">Error codes</span></span>

<span data-ttu-id="d0d91-116">Die Aufgabe an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="d0d91-116">The task at the specified location.</span></span> <span data-ttu-id="d0d91-117">Der Task ist ein [**RegisteredTask-Objekt.**](registeredtask.md)</span><span class="sxs-lookup"><span data-stu-id="d0d91-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0d91-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d0d91-118">Requirements</span></span>



| <span data-ttu-id="d0d91-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0d91-119">Requirement</span></span> | <span data-ttu-id="d0d91-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d0d91-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0d91-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0d91-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d0d91-122">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0d91-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d0d91-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0d91-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d0d91-124">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d0d91-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d0d91-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d0d91-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0d91-126"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d0d91-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d0d91-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d0d91-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0d91-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0d91-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





