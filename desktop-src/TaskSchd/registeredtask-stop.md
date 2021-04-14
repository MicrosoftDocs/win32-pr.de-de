---
title: Registeredtask. stoppt-Methode
description: Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Taskplaner der Methode wird beendet
- Methode zum Taskplaner Ende, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, Methode "Ende"
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392176"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="d1266-106">Registeredtask. stoppt-Methode</span><span class="sxs-lookup"><span data-stu-id="d1266-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="d1266-107">Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="d1266-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1266-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1266-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d1266-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1266-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1266-110">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1266-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1266-111">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d1266-111">Reserved.</span></span> <span data-ttu-id="d1266-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="d1266-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1266-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1266-113">Return value</span></span>

<span data-ttu-id="d1266-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d1266-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1266-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1266-115">Remarks</span></span>

<span data-ttu-id="d1266-116">Mit der **registeredtask. Stopp** -Funktion werden alle Instanzen der Aufgabe beendet.</span><span class="sxs-lookup"><span data-stu-id="d1266-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="d1266-117">System Kontobenutzer können eine Aufgabe abbrechen, Benutzer mit Administrator Gruppenberechtigungen können eine Aufgabe abbrechen, und wenn ein Benutzer über Rechte zum Ausführen und Lesen einer Aufgabe verfügt, kann der Benutzer die Aufgabe abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d1266-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="d1266-118">Ein Benutzer kann die Task Instanzen, die ausgeführt werden, mit denselben Anmelde Informationen wie das Benutzerkonto abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d1266-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="d1266-119">In allen anderen Fällen wird dem Benutzer der Zugriff verweigert, um den Task zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="d1266-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1266-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1266-120">Requirements</span></span>



| <span data-ttu-id="d1266-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1266-121">Requirement</span></span> | <span data-ttu-id="d1266-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d1266-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1266-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1266-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1266-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1266-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d1266-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1266-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1266-126">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1266-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1266-127">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d1266-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1266-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1266-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1266-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d1266-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1266-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1266-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1266-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1266-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1266-132">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="d1266-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





