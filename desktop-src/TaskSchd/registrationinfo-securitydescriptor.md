---
title: RegistrationInfo. securityDescriptor (Eigenschaft)
description: Ruft bei der Skripterstellung die Sicherheits Beschreibung der Aufgabe ab oder legt diese fest.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- SecurityDescriptor-Eigenschaft Taskplaner
- SecurityDescriptor-Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, securityDescriptor-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338114"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="11056-106">RegistrationInfo. securityDescriptor (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="11056-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="11056-107">Ruft bei der Skripterstellung die Sicherheits Beschreibung der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="11056-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="11056-108">Wenn bei der Task Registrierung eine andere Sicherheits Beschreibung angegeben wird, ersetzt Sie den Sicherheits Deskriptor, der durch diese Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="11056-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="11056-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="11056-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="11056-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="11056-110">Property value</span></span>

<span data-ttu-id="11056-111">Die Sicherheits Beschreibung, die der Aufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="11056-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="11056-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11056-112">Remarks</span></span>

<span data-ttu-id="11056-113">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Sicherheits Beschreibung der Aufgabe mit dem [**securityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="11056-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="11056-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11056-114">Requirements</span></span>



| <span data-ttu-id="11056-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11056-115">Requirement</span></span> | <span data-ttu-id="11056-116">Wert</span><span class="sxs-lookup"><span data-stu-id="11056-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11056-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11056-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11056-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11056-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="11056-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11056-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11056-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11056-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11056-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="11056-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="11056-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="11056-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="11056-123">DLL</span><span class="sxs-lookup"><span data-stu-id="11056-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11056-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11056-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11056-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11056-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11056-126">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="11056-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





