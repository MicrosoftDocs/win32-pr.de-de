---
title: Taskfolder. GetFolder (Eigenschaft)
description: Ruft bei der Skripterstellung einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder-Eigenschaft Taskplaner
- GetFolder-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, GetFolder-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103186"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="9ad43-106">Taskfolder. GetFolder (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="9ad43-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="9ad43-107">Ruft bei der Skripterstellung einen Ordner ab, der Tasks an einem angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="9ad43-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad43-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ad43-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="9ad43-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="9ad43-109">Property value</span></span>

<span data-ttu-id="9ad43-110">Der Pfad (Speicherort) zum Ordner.</span><span class="sxs-lookup"><span data-stu-id="9ad43-110">The path (location) to the folder.</span></span> <span data-ttu-id="9ad43-111">Verwenden Sie keinen umgekehrten Schrägstrich nach dem letzten Ordnernamen im Pfad.</span><span class="sxs-lookup"><span data-stu-id="9ad43-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="9ad43-112">Der Stamm Aufgaben Ordner wird mit einem umgekehrten Schrägstrich () angegeben \) .</span><span class="sxs-lookup"><span data-stu-id="9ad43-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="9ad43-113">Ein Beispiel für einen Aufgaben Ordner Pfad unter dem Stamm Aufgaben Ordner ist \\ mytaskfolder.</span><span class="sxs-lookup"><span data-stu-id="9ad43-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="9ad43-114">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ad43-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="9ad43-115">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ad43-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9ad43-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="9ad43-116">Error codes</span></span>

<span data-ttu-id="9ad43-117">Der Ordner am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="9ad43-117">The folder at the specified location.</span></span> <span data-ttu-id="9ad43-118">Der Ordner ist ein [**Task Folder**](taskfolder.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9ad43-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad43-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ad43-119">Requirements</span></span>



| <span data-ttu-id="9ad43-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ad43-120">Requirement</span></span> | <span data-ttu-id="9ad43-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9ad43-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad43-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ad43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ad43-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ad43-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9ad43-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ad43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ad43-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9ad43-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ad43-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9ad43-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ad43-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ad43-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ad43-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9ad43-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ad43-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ad43-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





