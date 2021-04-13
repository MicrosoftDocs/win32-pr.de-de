---
title: Logonauslöst. UserId-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner des Benutzers ab oder legt ihn fest.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserID-Eigenschaft Taskplaner
- UserID-Eigenschaft Taskplaner, LOGON-Auslöserobjekt
- Logon-Auslöserobjekt Taskplaner, UserID-Eigenschaft
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391636"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="ec4a6-106">Logonauslöst. UserId-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ec4a6-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="ec4a6-107">Ruft bei der Skripterstellung den Bezeichner des Benutzers ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec4a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec4a6-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="ec4a6-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ec4a6-109">Property value</span></span>

<span data-ttu-id="ec4a6-110">Der Bezeichner des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-110">The identifier of the user.</span></span> <span data-ttu-id="ec4a6-111">Beispiel: "mydomain \\ myname" oder für ein lokales Konto "Administrator".</span><span class="sxs-lookup"><span data-stu-id="ec4a6-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="ec4a6-112">Diese Eigenschaft kann in einem der folgenden Formate vorliegen:</span><span class="sxs-lookup"><span data-stu-id="ec4a6-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="ec4a6-113">Benutzername oder SID: der Task wird gestartet, wenn sich der Benutzer am Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="ec4a6-114">NULL: der Task wird gestartet, wenn sich ein Benutzer am Computer anmeldet.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec4a6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec4a6-115">Remarks</span></span>

<span data-ttu-id="ec4a6-116">Wenn ein Task ausgelöst werden soll, wenn sich ein Mitglied einer Gruppe beim Computer anmeldet, anstatt sich zu anmelden, wenn sich ein bestimmter Benutzer anmeldet, weisen Sie der **logontrigger. UserID** -Eigenschaft keinen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="ec4a6-117">Erstellen Sie stattdessen einen LOGON-und eine leere **logonauslöst. UserID** -Eigenschaft, und weisen Sie dem Prinzipal für die Aufgabe mithilfe der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft einen Wert zu.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="ec4a6-118">Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Anmelde Benutzer-ID mit dem [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="ec4a6-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec4a6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec4a6-119">Requirements</span></span>



| <span data-ttu-id="ec4a6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec4a6-120">Requirement</span></span> | <span data-ttu-id="ec4a6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ec4a6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec4a6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec4a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec4a6-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ec4a6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec4a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec4a6-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec4a6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec4a6-126">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="ec4a6-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec4a6-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec4a6-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec4a6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ec4a6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec4a6-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec4a6-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec4a6-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec4a6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec4a6-131">**Logonauslöst**</span><span class="sxs-lookup"><span data-stu-id="ec4a6-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="ec4a6-132">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="ec4a6-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





