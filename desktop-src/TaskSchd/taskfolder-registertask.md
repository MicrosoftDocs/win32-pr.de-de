---
title: Taskfolder. RegisterTask-Methode
description: Bei der Skripterstellung (erstellt) eine neue Aufgabe im Ordner mithilfe von XML zum Definieren der Aufgabe.
ms.assetid: 9bf5c59b-5aa1-42b3-a307-f583cdf59a39
keywords:
- RegisterTask-Methode Taskplaner
- RegisterTask-Methode Taskplaner, taskfolder-Objekt
- Task Folder-Objekt Taskplaner, RegisterTask-Methode
topic_type:
- apiref
api_name:
- TaskFolder.RegisterTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc0ed00ec736a90f716d895199812899d972930
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956925"
---
# <a name="taskfolderregistertask-method"></a><span data-ttu-id="791ae-106">Taskfolder. RegisterTask-Methode</span><span class="sxs-lookup"><span data-stu-id="791ae-106">TaskFolder.RegisterTask method</span></span>

<span data-ttu-id="791ae-107">Bei der Skripterstellung (erstellt) eine neue Aufgabe im Ordner mithilfe von XML zum Definieren der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="791ae-107">For scripting, registers (creates) a new task in the folder using XML to define the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="791ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="791ae-108">Syntax</span></span>


```VB
TaskFolder.RegisterTask( _
  ByVal path, _
  ByVal xmlText, _
  ByVal flags, _
  ByVal userId, _
  ByVal password, _
  ByVal logonType, _
  [ ByVal sddl ], _
  ByRef pTask _
)
```



## <a name="parameters"></a><span data-ttu-id="791ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="791ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791ae-110">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-111">Der Name der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="791ae-111">The name of the task.</span></span> <span data-ttu-id="791ae-112">Wenn dieser Wert auf " **Nothing**" festgelegt ist, wird die Aufgabe im Stamm Aufgaben Ordner registriert, und der TaskName ist ein GUID-Wert, der vom Taskplaner-Dienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-112">If this value is **Nothing**, the task will be registered in the root task folder and the task name will be a GUID value that is created by the Task Scheduler service.</span></span>

<span data-ttu-id="791ae-113">Ein Taskname darf nicht mit einem Leerzeichen beginnen oder enden.</span><span class="sxs-lookup"><span data-stu-id="791ae-113">A task name cannot begin or end with a space character.</span></span> <span data-ttu-id="791ae-114">Das Zeichen "." kann nicht verwendet werden, um den aktuellen Aufgaben Ordner und ".." anzugeben.</span><span class="sxs-lookup"><span data-stu-id="791ae-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="791ae-115">Zeichen können nicht verwendet werden, um den übergeordneten Aufgaben Ordner im Pfad anzugeben.</span><span class="sxs-lookup"><span data-stu-id="791ae-115">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="791ae-116">*XmlText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-116">*xmlText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-117">Eine XML-formatierte Beschreibung der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="791ae-117">An XML-formatted description of the task.</span></span>

<span data-ttu-id="791ae-118">Die folgenden Themen enthalten Aufgaben, die mithilfe von XML definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="791ae-118">The following topics contain tasks defined using XML.</span></span>

-   [<span data-ttu-id="791ae-119">Beispiel für Zeit Auslösung (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-119">Time Trigger Example (XML)</span></span>](time-trigger-example--xml-.md)
-   <span data-ttu-id="791ae-120">[Ereignis auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="791ae-120">[Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85))</span></span>
-   [<span data-ttu-id="791ae-121">Beispiel für das tägliche Beispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-121">Daily Trigger Example (XML)</span></span>](daily-trigger-example--xml-.md)
-   [<span data-ttu-id="791ae-122">Registrierungs auslöserbeispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-122">Registration Trigger Example (XML)</span></span>](registration-trigger-example--xml-.md)
-   [<span data-ttu-id="791ae-123">Beispiel für einen wöchentlichen Beispiel (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-123">Weekly Trigger Example (XML)</span></span>](weekly-trigger-example--xml-.md)
-   [<span data-ttu-id="791ae-124">Beispiel eines LOGON-Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-124">Logon Trigger Example (XML)</span></span>](logon-trigger-example--xml-.md)
-   [<span data-ttu-id="791ae-125">Beispiel für einen Start Auslösers (XML)</span><span class="sxs-lookup"><span data-stu-id="791ae-125">Boot Trigger Example (XML)</span></span>](boot-trigger-example--xml-.md)

</dd> <dt>

<span data-ttu-id="791ae-126">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-126">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-127">Eine [**Aufgaben \_ Erstellungs**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) Konstante.</span><span class="sxs-lookup"><span data-stu-id="791ae-127">A [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) constant.</span></span>



| <span data-ttu-id="791ae-128">Wert</span><span class="sxs-lookup"><span data-stu-id="791ae-128">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="791ae-129">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="791ae-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_VALIDATE_ONLY"></span><span id="task_validate_only"></span><dl> <span data-ttu-id="791ae-130"><dt>**Aufgabe \_ \_Nur**</dt> <dt>0x1</dt> validieren</span><span class="sxs-lookup"><span data-stu-id="791ae-130"><dt>**TASK\_VALIDATE\_ONLY**</dt> <dt>0x1</dt></span></span> </dl>                                                | <span data-ttu-id="791ae-131">Der Taskplaner überprüft die Syntax des XML-Codes, der den Task beschreibt, registriert jedoch nicht den Task.</span><span class="sxs-lookup"><span data-stu-id="791ae-131">The Task Scheduler checks the syntax of the XML that describes the task but does not register the task.</span></span> <span data-ttu-id="791ae-132">Diese Konstante kann nicht **mit den Werten Create \_ ,** **Task \_ Update** oder **Task \_ Create \_ oder \_ Update** kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="791ae-132">This constant cannot be combined with the **TASK\_CREATE**, **TASK\_UPDATE**, or **TASK\_CREATE\_OR\_UPDATE** values.</span></span><br/>                                                                                                                  |
| <span id="TASK_CREATE"></span><span id="task_create"></span><dl> <span data-ttu-id="791ae-133"><dt>**Aufgabe \_**</dt> <dt>0x2</dt> erstellen</span><span class="sxs-lookup"><span data-stu-id="791ae-133"><dt>**TASK\_CREATE**</dt> <dt>0x2</dt></span></span> </dl>                                                                      | <span data-ttu-id="791ae-134">Der Taskplaner die den Task als neue Aufgabe registriert.</span><span class="sxs-lookup"><span data-stu-id="791ae-134">The Task Scheduler registers the task as a new task.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="TASK_UPDATE"></span><span id="task_update"></span><dl> <span data-ttu-id="791ae-135"><dt>**Aufgabe \_ Update**</dt> <dt>0x4</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-135"><dt>**TASK\_UPDATE**</dt> <dt>0x4</dt></span></span> </dl>                                                                      | <span data-ttu-id="791ae-136">Der Taskplaner registriert den Task als aktualisierte Version eines vorhandenen Tasks.</span><span class="sxs-lookup"><span data-stu-id="791ae-136">The Task Scheduler registers the task as an updated version of an existing task.</span></span> <span data-ttu-id="791ae-137">Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="791ae-137">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span><br/>                                                                                                                                                            |
| <span id="TASK_CREATE_OR_UPDATE"></span><span id="task_create_or_update"></span><dl> <span data-ttu-id="791ae-138"><dt>**Aufgabe \_ 0x6 erstellen \_ oder \_ Aktualisieren**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="791ae-138"><dt>**TASK\_CREATE\_OR\_UPDATE**</dt> <dt>0x6</dt></span></span> </dl>                                      | <span data-ttu-id="791ae-139">Der Taskplaner registriert den Task entweder als neue Aufgabe oder als aktualisierte Version, wenn der Task bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="791ae-139">The Task Scheduler either registers the task as a new task or as an updated version if the task already exists.</span></span> <span data-ttu-id="791ae-140">Entspricht der Aufgabe zum \_ Erstellen von \| Aufgaben \_ Aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="791ae-140">Equivalent to TASK\_CREATE \| TASK\_UPDATE.</span></span><br/>                                                                                                                                                                                    |
| <span id="TASK_DISABLE"></span><span id="task_disable"></span><dl> <span data-ttu-id="791ae-141"><dt>**Aufgabe \_**</dt> <dt>0x8</dt> deaktivieren</span><span class="sxs-lookup"><span data-stu-id="791ae-141"><dt>**TASK\_DISABLE**</dt> <dt>0x8</dt></span></span> </dl>                                                                   | <span data-ttu-id="791ae-142">Mit dem Taskplaner wird die vorhandene Aufgabe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="791ae-142">The Task Scheduler disables the existing task.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="TASK_DONT_ADD_PRINCIPAL_ACE"></span><span id="task_dont_add_principal_ace"></span><dl> <span data-ttu-id="791ae-143"><dt>**Aufgabe \_ \_ \_ Prinzipal- \_ ACE**</dt> <dt>0x10</dt> nicht hinzufügen</span><span class="sxs-lookup"><span data-stu-id="791ae-143"><dt>**TASK\_DONT\_ADD\_PRINCIPAL\_ACE**</dt> <dt>0x10</dt></span></span> </dl>                  | <span data-ttu-id="791ae-144">Der Taskplaner wird verhindert, dass der ACE (Access Control Entry, ACE) für den Kontext Prinzipal hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-144">The Task Scheduler is prevented from adding the allow access-control entry (ACE) for the context principal.</span></span> <span data-ttu-id="791ae-145">Wenn die **taskfolder. RegisterTask** -Funktion mit diesem Flag aufgerufen wird, um eine Aufgabe zu aktualisieren, fügt der Taskplaner-Dienst nicht den ACE für den neuen Kontext Prinzipal hinzu und entfernt den ACE nicht aus dem alten Kontext Prinzipal.</span><span class="sxs-lookup"><span data-stu-id="791ae-145">When the **TaskFolder.RegisterTask** function is called with this flag to update a task, the Task Scheduler service does not add the ACE for the new context principal and does not remove the ACE from the old context principal.</span></span><br/> |
| <span id="TASK_IGNORE_REGISTRATION_TRIGGERS"></span><span id="task_ignore_registration_triggers"></span><dl> <span data-ttu-id="791ae-146"><dt>**Aufgabe \_ \_Registrierungs \_ Trigger ignorieren**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-146"><dt>**TASK\_IGNORE\_REGISTRATION\_TRIGGERS**</dt> <dt>0x20</dt></span></span> </dl> | <span data-ttu-id="791ae-147">Der Taskplaner erstellt die Aufgabe, ignoriert jedoch die Registrierungs Trigger in der Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="791ae-147">The Task Scheduler creates the task, but ignores the registration triggers in the task.</span></span> <span data-ttu-id="791ae-148">Durch das Ignorieren der Registrierungs Trigger wird die Aufgabe nicht ausgeführt, wenn Sie registriert wird, es sei denn, ein zeitbasierter Trigger führt die Ausführung bei der Registrierung aus.</span><span class="sxs-lookup"><span data-stu-id="791ae-148">By ignoring the registration triggers, the task will not execute when it is registered unless a time-based trigger causes it to execute on registration.</span></span><br/>                                                                                               |



 

</dd> <dt>

<span data-ttu-id="791ae-149">*Benutzer-ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-149">*userId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-150">Die Benutzer Anmelde Informationen, die zum Registrieren der Aufgabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="791ae-150">The user credentials that are used to register the task.</span></span>

> [!Note]  
> <span data-ttu-id="791ae-151">Wenn der Task als Taskplaner 1,0-Aufgabe definiert ist, verwenden Sie in diesem UserID-Parameter keinen Gruppennamen (anstelle eines bestimmten Benutzernamens).</span><span class="sxs-lookup"><span data-stu-id="791ae-151">If the task is defined as a Task Scheduler 1.0 task, then do not use a group name (rather than a specific user name) in this userId parameter.</span></span> <span data-ttu-id="791ae-152">Ein Task wird als Taskplaner 1,0-Aufgabe definiert, wenn das Versions Attribut des Task-Elements im XML-Code der Aufgabe auf 1,1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="791ae-152">A task is defined as a Task Scheduler 1.0 task when the version attribute of the Task element in the task's XML is set to 1.1.</span></span>

 

</dd> <dt>

<span data-ttu-id="791ae-153">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-153">*password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-154">Das Kennwort für die Benutzer-ID, die zum Registrieren der Aufgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-154">The password for the userId that is used to register the task.</span></span> <span data-ttu-id="791ae-155">Wenn der \_ \_ Anmeldetyp für das Anmeldedienst \_ Konto verwendet wird, muss das Kennwort ein leerer **Variant** -Wert wie z. b. **VT \_ null** oder **VT \_ empty** sein.</span><span class="sxs-lookup"><span data-stu-id="791ae-155">When the TASK\_LOGON\_SERVICE\_ACCOUNT logon type is used, the password must be an empty **VARIANT** value such as **VT\_NULL** or **VT\_EMPTY**.</span></span>

</dd> <dt>

<span data-ttu-id="791ae-156">*logontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="791ae-156">*logonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-157">Definiert, welche Anmelde Methode verwendet wird, um die registrierte Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="791ae-157">Defines what logon technique is used to run the registered task.</span></span>



| <span data-ttu-id="791ae-158">Wert</span><span class="sxs-lookup"><span data-stu-id="791ae-158">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="791ae-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="791ae-159">Meaning</span></span>                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_LOGON_NONE"></span><span id="task_logon_none"></span><dl> <span data-ttu-id="791ae-160"><dt>**Aufgabe \_ Login \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-160"><dt>**TASK\_LOGON\_NONE**</dt> <dt>0</dt></span></span> </dl>                                                                               | <span data-ttu-id="791ae-161">Die Anmelde Methode ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="791ae-161">The logon method is not specified.</span></span> <span data-ttu-id="791ae-162">Wird für nicht-NT-Anmelde Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="791ae-162">Used for non-NT credentials.</span></span> <br/>                                                                                                                                                                                                                           |
| <span id="TASK_LOGON_PASSWORD"></span><span id="task_logon_password"></span><dl> <span data-ttu-id="791ae-163"><dt>**Aufgabe \_ Anmelde \_ Kennwort**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-163"><dt>**TASK\_LOGON\_PASSWORD**</dt> <dt>1</dt></span></span> </dl>                                                                   | <span data-ttu-id="791ae-164">Verwenden Sie ein Kennwort für die Anmeldung für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="791ae-164">Use a password for logging on the user.</span></span> <span data-ttu-id="791ae-165">Das Kennwort muss beim Registrierungs Zeitpunkt angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="791ae-165">The password must be supplied at registration time.</span></span><br/>                                                                                                                                                                                                |
| <span id="TASK_LOGON_S4U"></span><span id="task_logon_s4u"></span><dl> <span data-ttu-id="791ae-166"><dt>**Aufgabe \_ Anmeldung \_ S4U**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-166"><dt>**TASK\_LOGON\_S4U**</dt> <dt>2</dt></span></span> </dl>                                                                                  | <span data-ttu-id="791ae-167">Verwenden Sie ein vorhandenes interaktives Token, um eine Aufgabe auszuführen.</span><span class="sxs-lookup"><span data-stu-id="791ae-167">Use an existing interactive token to run a task.</span></span> <span data-ttu-id="791ae-168">Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden.</span><span class="sxs-lookup"><span data-stu-id="791ae-168">The user must log on using a service for user (S4U) logon.</span></span> <span data-ttu-id="791ae-169">Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es gibt keinen Zugriff auf das Netzwerk oder verschlüsselte Dateien.</span><span class="sxs-lookup"><span data-stu-id="791ae-169">When an S4U logon is used, no password is stored by the system and there is no access to either the network or to encrypted files.</span></span><br/>                                             |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN"></span><span id="task_logon_interactive_token"></span><dl> <span data-ttu-id="791ae-170"><dt>**Aufgabe \_ \_Interaktives Anmelde \_ Token**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-170"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN**</dt> <dt>3</dt></span></span> </dl>                                       | <span data-ttu-id="791ae-171">Der Benutzer muss bereits angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="791ae-171">User must already be logged on.</span></span> <span data-ttu-id="791ae-172">Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="791ae-172">The task will be run only in an existing interactive session.</span></span><br/>                                                                                                                                                                                              |
| <span id="TASK_LOGON_GROUP"></span><span id="task_logon_group"></span><dl> <span data-ttu-id="791ae-173"><dt>**Aufgabe \_ Anmelde \_ Gruppe**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-173"><dt>**TASK\_LOGON\_GROUP**</dt> <dt>4</dt></span></span> </dl>                                                                            | <span data-ttu-id="791ae-174">Gruppen Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="791ae-174">Group activation.</span></span> <span data-ttu-id="791ae-175">Das Feld **GroupID** gibt die Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="791ae-175">The **groupId** field specifies the group.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="TASK_LOGON_SERVICE_ACCOUNT"></span><span id="task_logon_service_account"></span><dl> <span data-ttu-id="791ae-176"><dt>**Aufgabe \_ Anmelde \_ Dienst \_ Konto**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-176"><dt>**TASK\_LOGON\_SERVICE\_ACCOUNT**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="791ae-177">Gibt an, dass ein lokales System, ein lokaler Dienst oder ein Netzwerkdienst Konto als Sicherheitskontext zum Ausführen des Tasks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-177">Indicates that a Local System, Local Service, or Network Service account is being used as a security context to run the task.</span></span><br/>                                                                                                                                                              |
| <span id="TASK_LOGON_INTERACTIVE_TOKEN_OR_PASSWORD"></span><span id="task_logon_interactive_token_or_password"></span><dl> <span data-ttu-id="791ae-178"><dt>**Aufgabe \_ \_Interaktives \_ Token \_ oder \_ Kennwort**</dt> für die Anmeldung <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-178"><dt>**TASK\_LOGON\_INTERACTIVE\_TOKEN\_OR\_PASSWORD**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="791ae-179">Verwenden Sie zuerst das interaktive Token.</span><span class="sxs-lookup"><span data-stu-id="791ae-179">First use the interactive token.</span></span> <span data-ttu-id="791ae-180">Wenn der Benutzer nicht angemeldet ist (kein interaktives Token verfügbar), wird das Kennwort verwendet.</span><span class="sxs-lookup"><span data-stu-id="791ae-180">If the user is not logged on (no interactive token is available), then the password is used.</span></span> <span data-ttu-id="791ae-181">Das Kennwort muss angegeben werden, wenn ein Task registriert wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-181">The password must be specified when a task is registered.</span></span> <span data-ttu-id="791ae-182">Dieses Flag wird für neue Aufgaben nicht empfohlen, da es weniger zuverlässig ist als das Kennwort für die Task \_ Anmeldung \_ .</span><span class="sxs-lookup"><span data-stu-id="791ae-182">This flag is not recommended for new tasks because it is less reliable than TASK\_LOGON\_PASSWORD.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="791ae-183">*SDDL* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="791ae-183">*sddl* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-184">Die Sicherheits Beschreibung, die der registrierten Aufgabe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="791ae-184">The security descriptor that is associated with the registered task.</span></span> <span data-ttu-id="791ae-185">Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für eine Aufgabe angeben, um bestimmten Benutzern und Gruppen den Zugriff auf eine Aufgabe zu gewähren oder zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="791ae-185">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

> [!Note]  
> <span data-ttu-id="791ae-186">Wenn dem lokalen System Konto der Zugriff auf eine Aufgabe verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.</span><span class="sxs-lookup"><span data-stu-id="791ae-186">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="791ae-187">*pTask* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="791ae-187">*pTask* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="791ae-188">Ein [**registeredtask**](registeredtask.md) -Objekt, das die neue Aufgabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="791ae-188">A [**RegisteredTask**](registeredtask.md) object that represents the new task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791ae-189">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="791ae-189">Return value</span></span>

<span data-ttu-id="791ae-190">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="791ae-190">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="791ae-191">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="791ae-191">Remarks</span></span>

<span data-ttu-id="791ae-192">Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist.</span><span class="sxs-lookup"><span data-stu-id="791ae-192">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="791ae-193">Wenn Sie den Anmeldetyp für die Aufgabe interaktiv festlegen möchten, geben Sie in der [**logontype**](principal-logontype.md) -Eigenschaft des Task Prinzipals oder im *logontype* -Parameter von **taskfolder. RegisterTask** oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)den Wert 3 an.**\_ \_ \_\*\*\*\*\_ \_**</span><span class="sxs-lookup"><span data-stu-id="791ae-193">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="791ae-194">Nur ein Mitglied der Gruppe "Administratoren" kann eine Aufgabe mit einem Start--Vorgang erstellen.</span><span class="sxs-lookup"><span data-stu-id="791ae-194">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="791ae-195">Sie können eine Aufgabe erfolgreich mit einer Gruppe registrieren, die im *UserID* -Parameter angegeben ist, und 3 (**\_ \_ interaktives Anmelde \_ Token** für die Aufgabe), das im *logontype* -Parameter von **Task Folder. RegisterTask** oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)angegeben ist, die Aufgabe jedoch nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="791ae-195">You can successfully register a task with a group specified in the *userId* parameter and 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) specified in the *logonType* parameter of **TaskFolder.RegisterTask** or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md), but the task will not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="791ae-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="791ae-196">Requirements</span></span>



| <span data-ttu-id="791ae-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="791ae-197">Requirement</span></span> | <span data-ttu-id="791ae-198">Wert</span><span class="sxs-lookup"><span data-stu-id="791ae-198">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="791ae-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="791ae-199">Minimum supported client</span></span><br/> | <span data-ttu-id="791ae-200">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="791ae-200">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="791ae-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="791ae-201">Minimum supported server</span></span><br/> | <span data-ttu-id="791ae-202">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="791ae-202">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="791ae-203">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="791ae-203">Type library</span></span><br/>             | <dl> <span data-ttu-id="791ae-204"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-204"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="791ae-205">DLL</span><span class="sxs-lookup"><span data-stu-id="791ae-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="791ae-206"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="791ae-206"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="791ae-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="791ae-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791ae-208">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="791ae-208">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="791ae-209">**Registeredtask**</span><span class="sxs-lookup"><span data-stu-id="791ae-209">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="791ae-210">**Task Folder**</span><span class="sxs-lookup"><span data-stu-id="791ae-210">**TaskFolder**</span></span>](taskfolder.md)
</dt> </dl>

 

