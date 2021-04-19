---
title: Taskfolder. getsecuritydescriptor (Eigenschaft)
description: Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner abgerufen.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Getsecuritydescriptor-Eigenschaft Taskplaner
- Getsecuritydescriptor-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, getsecuritydescriptor-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346744"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a><span data-ttu-id="ff810-106">Taskfolder. getsecuritydescriptor (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ff810-106">TaskFolder.GetSecurityDescriptor property</span></span>

<span data-ttu-id="ff810-107">Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ff810-107">For scripting, gets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff810-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff810-108">Syntax</span></span>


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a><span data-ttu-id="ff810-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ff810-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ff810-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff810-110">Requirements</span></span>



| <span data-ttu-id="ff810-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff810-111">Requirement</span></span> | <span data-ttu-id="ff810-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ff810-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff810-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff810-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ff810-114">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff810-114">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ff810-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff810-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ff810-116">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff810-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff810-117">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ff810-117">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff810-118"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ff810-118"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ff810-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ff810-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff810-120"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff810-120"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff810-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff810-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff810-122">**Taskfolder. SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="ff810-122">**TaskFolder.SetSecurityDescriptor**</span></span>](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="ff810-123">**Registeredtask. SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="ff810-123">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





