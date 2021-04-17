---
title: Principal. logontype (Eigenschaft)
description: Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: ac6fd7a1-00ef-4478-920f-de391a5a2c8c
keywords:
- Logontype-Eigenschaft Taskplaner
- Logontype-Eigenschaft Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, logontype-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.LogonType
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4455fd273144b2d6abd81c78be31a1b037cd889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477199"
---
# <a name="principallogontype-property"></a><span data-ttu-id="d08dd-106">Principal. logontype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d08dd-106">Principal.LogonType property</span></span>

<span data-ttu-id="d08dd-107">Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d08dd-107">For scripting, gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08dd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d08dd-108">Syntax</span></span>


```VB
Principal.LogonType As Integer
```



## <a name="property-value"></a><span data-ttu-id="d08dd-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d08dd-109">Property value</span></span>

<span data-ttu-id="d08dd-110">Legen Sie auf eine der folgenden Enumerationskonstanten für den [**\_ Anmeldetyp der Aufgabe**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) fest.</span><span class="sxs-lookup"><span data-stu-id="d08dd-110">Set to one of the following [**TASK\_LOGON TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) enumeration constants.</span></span>



| <span data-ttu-id="d08dd-111">Wert</span><span class="sxs-lookup"><span data-stu-id="d08dd-111">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="d08dd-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d08dd-112">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="d08dd-113"><dt>**Aufgabe \_ Login \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-113"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="d08dd-114">Die Anmelde Methode ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="d08dd-114">The logon method is not specified.</span></span> <span data-ttu-id="d08dd-115">Wird für nicht-NT-Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d08dd-115">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="d08dd-116"><dt>**Aufgabe \_ Anmelde \_ Kennwort**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-116"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="d08dd-117">Verwenden Sie ein Kennwort für die Anmeldung für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d08dd-117">Use a password for logging on the user.</span></span> <span data-ttu-id="d08dd-118">Das Kennwort muss beim Registrierungs Zeitpunkt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d08dd-118">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="d08dd-119"><dt>**Aufgabe \_ Anmeldung \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-119"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="d08dd-120">Verwenden Sie ein vorhandenes interaktives Token, um eine Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d08dd-120">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="d08dd-121">Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden.</span><span class="sxs-lookup"><span data-stu-id="d08dd-121">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="d08dd-122">Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.</span><span class="sxs-lookup"><span data-stu-id="d08dd-122">When an S4U logon is used, no password is stored by the system and there is no access to either the network or encrypted files.</span></span><br/>                                                |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="d08dd-123"><dt>**Aufgabe \_ \_Interaktives Anmelde \_ Token**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-123"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="d08dd-124">Der Benutzer muss bereits angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="d08dd-124">User must already be logged on.</span></span> <span data-ttu-id="d08dd-125">Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d08dd-125">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="d08dd-126"><dt>**Aufgabe \_ Anmelde \_ Gruppe**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-126"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="d08dd-127">Gruppen Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="d08dd-127">Group activation.</span></span> <span data-ttu-id="d08dd-128">Das Feld "UserID" gibt die Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="d08dd-128">The userId field specifies the group.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="d08dd-129"><dt>**Aufgabe \_ Anmelde \_ Dienst \_ Konto**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-129"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="d08dd-130">Gibt an, dass ein lokales System, ein lokaler Dienst oder ein Netzwerkdienst Konto als Sicherheitskontext zum Ausführen des Tasks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d08dd-130">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="d08dd-131"><dt>**Aufgabe \_ \_Interaktives \_ Token \_ oder \_ Kennwort**</dt> für die Anmeldung <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-131"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="d08dd-132">Verwenden Sie zuerst das interaktive Token.</span><span class="sxs-lookup"><span data-stu-id="d08dd-132">First use the interactive token.</span></span> <span data-ttu-id="d08dd-133">Wenn der Benutzer nicht angemeldet ist (kein interaktives Token verfügbar), wird das Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="d08dd-133">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="d08dd-134">Das Kennwort muss angegeben werden, wenn ein Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="d08dd-134">The password must be specified when a task is registered.</span></span> <span data-ttu-id="d08dd-135">Dieses Flag wird für neue Aufgaben nicht empfohlen, da es weniger zuverlässig ist als das Kennwort für die Task \_ Anmeldung \_ .</span><span class="sxs-lookup"><span data-stu-id="d08dd-135">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d08dd-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d08dd-136">Remarks</span></span>

<span data-ttu-id="d08dd-137">Diese Eigenschaft ist nur gültig, wenn eine Benutzer-ID von der [**UserID**](principal-userid.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d08dd-137">This property is valid only when a user identifier is specified by the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="d08dd-138">Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Anmeldetyp im- [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="d08dd-138">When reading or writing XML for a task, the logon type is specified in the [**<LogonType>**](taskschedulerschema-logontype-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="d08dd-139">Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="d08dd-139">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="d08dd-140">Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der **logontype** -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von [**taskfolder. RegisterTask**](taskfolder-registertask.md) oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_\*\*\*\*\_ \_**</span><span class="sxs-lookup"><span data-stu-id="d08dd-140">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the **LogonType** property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d08dd-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d08dd-141">Requirements</span></span>



| <span data-ttu-id="d08dd-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d08dd-142">Requirement</span></span> | <span data-ttu-id="d08dd-143">Wert</span><span class="sxs-lookup"><span data-stu-id="d08dd-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08dd-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d08dd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d08dd-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d08dd-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d08dd-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d08dd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d08dd-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d08dd-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d08dd-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d08dd-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d08dd-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d08dd-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d08dd-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08dd-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d08dd-151"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08dd-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d08dd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08dd-153">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="d08dd-153">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="d08dd-154">**Prinzipal**</span><span class="sxs-lookup"><span data-stu-id="d08dd-154">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





