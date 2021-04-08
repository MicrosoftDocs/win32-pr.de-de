---
title: Sessionstatechangeauslöst. StateChange (Eigenschaft)
description: Ruft bei der Skripterstellung die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt diese fest.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- StateChange-Eigenschaft Taskplaner
- StateChange-Eigenschaft Taskplaner, sessionstatechange-Objekt
- Sessionstatechange-Objekt Taskplaner, StateChange-Eigenschaft
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740616"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="b1973-106">Sessionstatechangeauslöst. StateChange (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1973-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="b1973-107">Ruft bei der Skripterstellung die Art der Sitzungs Änderung für Terminal Server ab, die einen Task Start auslöst, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="b1973-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1973-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1973-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="b1973-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b1973-109">Property value</span></span>

<span data-ttu-id="b1973-110">Die Art der Sitzungs Änderung für Terminal Server, die das Starten einer Aufgabe auslöst.</span><span class="sxs-lookup"><span data-stu-id="b1973-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="b1973-111">Die möglichen Werte stammen aus der Enumeration der [**\_ \_ \_ \_ statusänderungsart des Aufgaben Sitzungs Zustands**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="b1973-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="b1973-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b1973-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="b1973-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b1973-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="b1973-114"><dt>**Aufgabe \_ Konsolen \_ Verbindung**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="b1973-115">Statusänderung der Terminal Server-Konsolen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b1973-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="b1973-116">Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie die Benutzer auf dem Computer wechseln.</span><span class="sxs-lookup"><span data-stu-id="b1973-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="b1973-117"><dt>**Aufgabe \_ Konsolen \_ Trennung**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b1973-118">Statusänderung der Terminal Server Konsole wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="b1973-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="b1973-119">Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln.</span><span class="sxs-lookup"><span data-stu-id="b1973-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="b1973-120"><dt>**Aufgabe \_ Remote \_ Verbindung**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="b1973-121">Statusänderung für Terminal Server-Remote Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b1973-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="b1973-122">Dies ist beispielsweise der Fall, wenn ein Benutzer mithilfe des Remotedesktopverbindung Programms von einem Remote Computer aus eine Verbindung mit einer Benutzersitzung herstellt.</span><span class="sxs-lookup"><span data-stu-id="b1973-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="b1973-123"><dt>**Aufgabe \_ Remote \_**</dt> Verbindung <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="b1973-124">Statusänderung des Terminal Server-Remote Verbindungs Wechsels.</span><span class="sxs-lookup"><span data-stu-id="b1973-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="b1973-125">Dies ist beispielsweise der Fall, wenn ein Benutzer die Verbindung mit einer Benutzersitzung trennt, während das Remotedesktopverbindung Programm von einem Remote Computer aus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1973-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="b1973-126"><dt>**Aufgabe \_ Sitzungs \_ Sperre**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="b1973-127">Statusänderung für Terminal Server Sitzung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="b1973-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="b1973-128">Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="b1973-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="b1973-129"><dt>**Aufgabe \_ Aufheben \_ der Sitzung**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="b1973-130">Die Statusänderung der Terminal Server Sitzung wurde aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="b1973-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="b1973-131">Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="b1973-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="b1973-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1973-132">Requirements</span></span>



| <span data-ttu-id="b1973-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1973-133">Requirement</span></span> | <span data-ttu-id="b1973-134">Wert</span><span class="sxs-lookup"><span data-stu-id="b1973-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1973-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1973-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b1973-136">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1973-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b1973-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1973-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b1973-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1973-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1973-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b1973-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1973-140"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1973-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b1973-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1973-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1973-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





