---
title: TaskService. highestversion (Eigenschaft)
description: Gibt für die Skripterstellung die höchste Version von Taskplaner an, die von einem Computer unterstützt wird.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Highestversion-Eigenschaft Taskplaner
- Highestversion-Eigenschaft Taskplaner, Task Service-Objekt
- TaskService-Objekt Taskplaner, highestversion-Eigenschaft
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743736"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="76c7b-106">TaskService. highestversion (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="76c7b-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="76c7b-107">Gibt für die Skripterstellung die höchste Version von Taskplaner an, die von einem Computer unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="76c7b-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c7b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="76c7b-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="76c7b-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="76c7b-109">Property value</span></span>

<span data-ttu-id="76c7b-110">Die höchste Version von Taskplaner, die ein Computer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76c7b-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="76c7b-111">Die höchste Version ist ein Wert, der in MajorVersion/MinorVersion an der 16-Bit-Grenze aufgeteilt ist.</span><span class="sxs-lookup"><span data-stu-id="76c7b-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="76c7b-112">Der Taskplaner-Dienst gibt 1 für die Hauptversion und 2 für die neben Version zurück.</span><span class="sxs-lookup"><span data-stu-id="76c7b-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="76c7b-113">Verwenden Sie die [CLng](/previous-versions//ck4c5842(v=vs.85)) -Funktion, um den ganzzahligen Wert der Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76c7b-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="76c7b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76c7b-114">Examples</span></span>

<span data-ttu-id="76c7b-115">Der folgende Code zeigt, wie die [CLng](/previous-versions//ck4c5842(v=vs.85)) -Funktion verwendet wird, um den Wert der **highestversion** -Eigenschaft zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="76c7b-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="76c7b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76c7b-116">Requirements</span></span>



| <span data-ttu-id="76c7b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76c7b-117">Requirement</span></span> | <span data-ttu-id="76c7b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="76c7b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76c7b-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76c7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="76c7b-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76c7b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="76c7b-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76c7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="76c7b-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76c7b-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="76c7b-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="76c7b-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="76c7b-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="76c7b-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="76c7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="76c7b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76c7b-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76c7b-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

