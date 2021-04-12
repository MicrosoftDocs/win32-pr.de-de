---
title: TaskService. TargetServer (Eigenschaft)
description: Ruft bei der Skripterstellung den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- TargetServer-Eigenschaft Taskplaner
- TargetServer-Eigenschaft Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, TargetServer-Eigenschaft
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519095"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="222f3-106">TaskService. TargetServer (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="222f3-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="222f3-107">Ruft bei der Skripterstellung den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="222f3-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="222f3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="222f3-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="222f3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="222f3-109">Property value</span></span>

<span data-ttu-id="222f3-110">Der Name des Computers, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="222f3-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="222f3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="222f3-111">Remarks</span></span>

<span data-ttu-id="222f3-112">Diese Eigenschaft gibt eine leere Zeichenfolge zurück, wenn der Benutzer eine IP-Adresse, einen localhost oder "." als Parameter übergibt, und gibt den Namen des Computers zurück, auf dem der Taskplaner-Dienst ausgeführt wird, wenn der Benutzer keinen Parameterwert übergibt.</span><span class="sxs-lookup"><span data-stu-id="222f3-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="222f3-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="222f3-113">Requirements</span></span>



| <span data-ttu-id="222f3-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="222f3-114">Requirement</span></span> | <span data-ttu-id="222f3-115">Wert</span><span class="sxs-lookup"><span data-stu-id="222f3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="222f3-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="222f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="222f3-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="222f3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="222f3-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="222f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="222f3-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="222f3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="222f3-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="222f3-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="222f3-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="222f3-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="222f3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="222f3-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="222f3-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="222f3-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





