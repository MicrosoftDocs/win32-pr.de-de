---
title: Registeredtask. getinhaltungen-Methode
description: Gibt für die Skripterstellung alle zurzeit auf dem registrierten Task aktuell laufenden Instanzen zurück.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Die getinhaltungen-Methode Taskplaner
- Getinhaltungen-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getinhaltungen-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105243"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="095bb-106">Registeredtask. getinhaltungen-Methode</span><span class="sxs-lookup"><span data-stu-id="095bb-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="095bb-107">Gibt für die Skripterstellung alle zurzeit auf dem registrierten Task aktuell laufenden Instanzen zurück.</span><span class="sxs-lookup"><span data-stu-id="095bb-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="095bb-108">**Registeredtask. getinhaltungen** gibt nur Instanzen der aktuell registrierten Aufgabe zurück, die unter oder unterhalb des Sicherheits Kontexts eines Benutzers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="095bb-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="095bb-109">Bei Mitgliedern der Gruppe "Administratoren" gibt " **getinhaltungen** " z. b. alle Instanzen der aktuell registrierten Aufgabe zurück. für Mitglieder der Gruppe "Benutzer" gibt " **getinhaltungen** " jedoch nur Instanzen der aktuell registrierten Aufgabe zurück, die im Sicherheitskontext der Benutzergruppe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="095bb-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="095bb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="095bb-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="095bb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="095bb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095bb-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="095bb-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="095bb-113">Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="095bb-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="095bb-114">*runningtasks* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="095bb-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="095bb-115">Ein [**runningtaskcollection**](runningtaskcollection.md) -Objekt, das alle derzeit aktuell aktuell laufenden Instanzen der Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="095bb-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="095bb-116">Return value</span></span>

<span data-ttu-id="095bb-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="095bb-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="095bb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="095bb-118">Requirements</span></span>



| <span data-ttu-id="095bb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="095bb-119">Requirement</span></span> | <span data-ttu-id="095bb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="095bb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="095bb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="095bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="095bb-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="095bb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="095bb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="095bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="095bb-124">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="095bb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="095bb-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="095bb-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="095bb-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="095bb-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="095bb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="095bb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="095bb-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="095bb-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="095bb-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="095bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095bb-130">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="095bb-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="095bb-131">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="095bb-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





