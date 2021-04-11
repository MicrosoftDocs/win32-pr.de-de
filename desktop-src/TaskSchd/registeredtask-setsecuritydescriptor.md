---
title: Registeredtask. SETSECURITYDESCRIPTOR-Methode
description: Bei der Skripterstellung wird die Sicherheits Beschreibung festgelegt, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- SETSECURITYDESCRIPTOR-Methode Taskplaner
- SETSECURITYDESCRIPTOR-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, SETSECURITYDESCRIPTOR-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105686"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="21e23-106">Registeredtask. SETSECURITYDESCRIPTOR-Methode</span><span class="sxs-lookup"><span data-stu-id="21e23-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="21e23-107">Bei der Skripterstellung wird die Sicherheits Beschreibung festgelegt, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21e23-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e23-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="21e23-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="21e23-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="21e23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e23-110">*SDDL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21e23-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e23-111">Die Sicherheits Beschreibung, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="21e23-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="21e23-112">Wenn dem lokalen System Konto der Zugriff auf eine Aufgabe verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.</span><span class="sxs-lookup"><span data-stu-id="21e23-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="21e23-113">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21e23-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e23-114">Flags, die angeben, wie die Sicherheits Beschreibung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="21e23-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="21e23-115">Der Task \_ " \_ \_ Prinzipal- \_ ACE-Flag (0x10)" aus der [**\_ Taskerstellungs**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) -Enumeration kann nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="21e23-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e23-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21e23-116">Return value</span></span>

<span data-ttu-id="21e23-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="21e23-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e23-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21e23-118">Remarks</span></span>

<span data-ttu-id="21e23-119">Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für eine Aufgabe angeben, um bestimmten Benutzern und Gruppen den Zugriff auf eine Aufgabe zu gewähren oder zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="21e23-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e23-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21e23-120">Requirements</span></span>



| <span data-ttu-id="21e23-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21e23-121">Requirement</span></span> | <span data-ttu-id="21e23-122">Wert</span><span class="sxs-lookup"><span data-stu-id="21e23-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21e23-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21e23-123">Minimum supported client</span></span><br/> | <span data-ttu-id="21e23-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21e23-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="21e23-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21e23-125">Minimum supported server</span></span><br/> | <span data-ttu-id="21e23-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21e23-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21e23-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="21e23-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="21e23-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21e23-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21e23-129">DLL</span><span class="sxs-lookup"><span data-stu-id="21e23-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21e23-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e23-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e23-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21e23-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e23-132">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="21e23-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="21e23-133">**Taskfolder. getsecuritydescriptor**</span><span class="sxs-lookup"><span data-stu-id="21e23-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="21e23-134">**Registeredtask. SETSECURITYDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="21e23-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





