---
title: TaskFolder.GetFolder-Eigenschaft
description: Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- GetFolder-Eigenschaft Taskplaner
- GetFolder-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , GetFolder-Eigenschaft
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
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387029"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="ce4a5-106">TaskFolder.GetFolder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce4a5-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="ce4a5-107">Ruft für die Skripterstellung einen Ordner ab, der Aufgaben an einem angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce4a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce4a5-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="ce4a5-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ce4a5-109">Property value</span></span>

<span data-ttu-id="ce4a5-110">Der Pfad (Speicherort) zum Ordner.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-110">The path (location) to the folder.</span></span> <span data-ttu-id="ce4a5-111">Verwenden Sie keinen umgekehrten Schrägstrich, der auf den Namen des letzten Ordners im Pfad folgt.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="ce4a5-112">Der Stammtaskordner wird mit einem umgekehrten Schrägstrich \\ () angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="ce4a5-113">Ein Beispiel für einen Taskordnerpfad im Stammtaskordner ist \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="ce4a5-114">Das Zeichen "." kann nicht zum Angeben des aktuellen Aufgabenordners und des "."-Zeichens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="ce4a5-115">-Zeichen können nicht verwendet werden, um den übergeordneten Aufgabenordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce4a5-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="ce4a5-116">Error codes</span></span>

<span data-ttu-id="ce4a5-117">Der Ordner am angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="ce4a5-117">The folder at the specified location.</span></span> <span data-ttu-id="ce4a5-118">Der Ordner ist ein [**TaskFolder-Objekt.**](taskfolder.md)</span><span class="sxs-lookup"><span data-stu-id="ce4a5-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce4a5-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ce4a5-119">Requirements</span></span>



| <span data-ttu-id="ce4a5-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce4a5-120">Requirement</span></span> | <span data-ttu-id="ce4a5-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ce4a5-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4a5-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce4a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4a5-123">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce4a5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ce4a5-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce4a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4a5-125">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce4a5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce4a5-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ce4a5-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce4a5-127"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce4a5-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce4a5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ce4a5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce4a5-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce4a5-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





