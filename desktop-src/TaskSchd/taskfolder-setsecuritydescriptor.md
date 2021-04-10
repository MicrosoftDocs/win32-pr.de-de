---
title: Taskfolder. SETSECURITYDESCRIPTOR (Eigenschaft)
description: Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner festgelegt.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- SETSECURITYDESCRIPTOR-Eigenschaft Taskplaner
- SETSECURITYDESCRIPTOR-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, SETSECURITYDESCRIPTOR-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949645"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a><span data-ttu-id="7252f-106">Taskfolder. SETSECURITYDESCRIPTOR (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7252f-106">TaskFolder.SetSecurityDescriptor property</span></span>

<span data-ttu-id="7252f-107">Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7252f-107">For scripting, sets the security descriptor for the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7252f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7252f-108">Syntax</span></span>


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a><span data-ttu-id="7252f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7252f-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7252f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7252f-110">Remarks</span></span>

<span data-ttu-id="7252f-111">Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für einen Aufgaben Ordner angeben, um bestimmten Benutzern und Gruppen den Zugriff auf einen Aufgaben Ordner zu gewähren oder zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="7252f-111">You can specify the access control list (ACL) in the security descriptor for a task folder in order to allow or deny certain users and groups access to a task folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="7252f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7252f-112">Requirements</span></span>



| <span data-ttu-id="7252f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7252f-113">Requirement</span></span> | <span data-ttu-id="7252f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7252f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7252f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7252f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7252f-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7252f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7252f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7252f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7252f-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7252f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7252f-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7252f-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="7252f-120"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7252f-120"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7252f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7252f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7252f-122"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7252f-122"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7252f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7252f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7252f-124">**Registeredtask. SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="7252f-124">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="7252f-125">**Taskfolder. getsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="7252f-125">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





