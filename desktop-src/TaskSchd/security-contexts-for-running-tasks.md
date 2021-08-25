---
title: Sicherheitskontexte für Aufgaben
description: Aufgaben werden registriert und unter einem bestimmten Sicherheitskontext ausgeführt.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6f49ef07818b1fe729fa96a2b5e0712979a17f300e4f411f96cefd2f3917f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738250"
---
# <a name="security-contexts-for-tasks"></a>Sicherheitskontexte für Aufgaben

Aufgaben werden registriert und unter einem bestimmten Sicherheitskontext ausgeführt. Benutzer können Anwendungen erstellen, die Aufgaben erfolgreich registrieren, aktualisieren, löschen oder ausführen. Der Benutzer muss jedoch beim Registrieren eines Tasks die richtigen Anmeldeinformationen bereitstellen, und die Anwendung muss in einem Prozess mit den richtigen Berechtigungen ausgeführt werden.

## <a name="specifying-credentials"></a>Angeben von Anmeldeinformationen

Sie können den Sicherheitskontext für eine Aufgabe angeben, indem Sie Anmeldeinformationen in den [**Methoden ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**TaskFolder.RegisterTask**](taskfolder-registertask.md) oder [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) für Skripterstellung) angeben oder der [**Principal-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**TaskDefinition.Principal**](taskdefinition-principal.md) für Skripterstellung) einen Prinzipal zuweisen. Wenn ein Prinzipal für eine Aufgabendefinition erstellt wird und die Taskdefinition mithilfe der **RegisterTaskDefinition-Methode** mit unterschiedlichen Anmeldeinformationen registriert wird, die in den Methodenparametern angegeben sind, überschreiben die in der **RegisterTaskDefinition-Methode** angegebenen Anmeldeinformationen die Anmeldeinformationen im Prinzipal. Wenn ein Prinzipal für eine Aufgabendefinition mitHILFE von XML erstellt wird und der XML-Code für den Task mithilfe der **RegisterTask-Methode** mit anderen Anmeldeinformationen registriert wird, die in den Methodenparametern angegeben sind, überschreiben die in der **RegisterTask-Methode** angegebenen Anmeldeinformationen die Anmeldeinformationen im Prinzipal.

Sie geben ein Benutzerkonto oder eine Gruppe an, wenn Sie eine Aufgabe registrieren oder das Prinzip für eine Aufgabe angeben. Der Sicherheitskontext des Benutzerkontos oder der Gruppe wird für den Sicherheitskontext der Aufgabe verwendet. In diesen Methoden und Eigenschaften definieren Sie auch den Anmeldetyp. Der Anmeldetyp wird durch eine der Konstanten in der [**TASK \_ LOGON \_ TYPE-Enumeration**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) definiert.

Aufgaben, die mit dem Flag TASK \_ LOGON \_ PASSWORD oder TASK \_ LOGON S4U registriert \_ sind, werden nur gestartet, wenn für den angegebenen Benutzer die Berechtigung Anmelden als Batch aktiviert ist. Administratoren und Gruppenbenutzer von Sicherungsoperatoren haben diese Berechtigung standardmäßig aktiviert.

Wenn Sie die [**ITaskService::Verbinden**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) [**(TaskService.Verbinden**](taskservice-connect.md) for scripting)-Methode aufrufen, verwenden alle nachfolgenden Methodenaufrufe des Taskplaner-Diensts die Anmeldeinformationen, die an die **Verbinden-Methode** übergeben wurden. Dies ist wichtig, wenn Sie Aufgaben mit einem interaktiven Anmeldetyp registrieren. Wenn Sie eine Aufgabe mit dem Anmeldetyp "TASK \_ LOGON INTERACTIVE TOKEN" registrieren und die Aufgabe keine \_ \_ Anmeldeinformationen enthält, die in der [**Principal-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) der Taskdefinition angegeben sind, in den Parametern [**für RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)oder im XML-Code angegeben sind, der an [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)übergeben wird, wird die Aufgabe mit den Anmeldeinformationen des Benutzers registriert, der die **Verbinden-Methode** aufgerufen hat.

## <a name="user-account-control-uac-security-for-tasks"></a>Sicherheit der Benutzerkontensteuerung (User Account Control, UAC) für Tasks

[Mit der Benutzerkontensteuerung](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (User Account Control, UAC) können Benutzer allgemeine Funktionen wie das Ausführen von Programmen und das Speichern und Ändern von Daten ausführen, ohne Administratorrechte verfügbar zu machen. Standardmäßig wird ein Task mit berechtigungen auf niedriger Ebene ausgeführt, wenn die UAC aktiviert ist. Tasks können angeben, dass sie mit erhöhten oder niedrigen Berechtigungen ausgeführt werden, indem sie eine Berechtigungsebene aus der [**TASK \_ RUNLEVEL \_ TYPE-Enumeration**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) für die [**RunLevel-Eigenschaft von IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) festlegen ([**Principal.RunLevel**](principal-runlevel.md) für Skripterstellung). Der Wert der **RunLevel-Eigenschaft** bestimmt die Berechtigungsebene, auf der die Aktionen eines Tasks ausgeführt werden. Wenn die Aktionen eines Tasks über erhöhte Berechtigungen für die Ausführung verfügen müssen, müssen Sie die **RunLevel-Eigenschaft** auf **TASK \_ RUNLEVEL \_ HIGHEST** festlegen. Wenn eine Aufgabe mithilfe der Gruppe Administratoren für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie auch die **RunLevel-Eigenschaft** auf **TASK \_ RUNLEVEL \_ HIGHEST** festlegen, wenn Sie den Task ausführen möchten. Wenn eine Aufgabe mithilfe des integrierten \\ Administratorkontos oder des lokalen Systems oder des lokalen Dienstkontos registriert wird, wird die **RunLevel-Eigenschaft** ignoriert. Der Eigenschaftswert wird auch ignoriert, wenn die Benutzerkontensteuerung (User Account Control, UAC) deaktiviert ist. Der Wert der **RunLevel-Eigenschaft** wirkt sich nicht auf die Berechtigungen aus, die zum Ausführen oder Löschen einer Aufgabe erforderlich sind.

> [!Note]  
> Nach dem Upgrade eines Betriebssystems von Windows XP auf Windows Vista wird für Aufgaben, die mit dem integrierten Administratorkonto auf Windows XP registriert wurden, \\ die [**RunLevel-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) auf **TASK \_ RUNLEVEL \_ LUA** festgelegt. Dies kann dazu führen, dass einige Aufgaben fehlschlagen. Sie können diese Eigenschaft manuell aktualisieren, um sicherzustellen, dass alle Tasks ausgeführt werden.

 

Bei einem Prozess mit geringen Berechtigungen können Sie einen Task nicht mit der [**RunLevel-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) gleich **TASK \_ RUNLEVEL \_ HIGHEST** registrieren, aber Sie können eine Aufgabe mit der **RunLevel-Eigenschaft** registrieren, die **task \_ runlevel \_ LUA** entspricht. Die Taskaktionen werden mit geringen Berechtigungen ausgeführt. Sie dürfen die Aufgabe nicht als "Integriert/Administrator", "Lokales System" oder für eine Gruppe registrieren.

Bei einem Prozess mit erhöhten Rechten können Sie einen Task mit der [**RunLevel-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) registrieren, die **gleich TASK \_ RUNLEVEL \_ HIGHEST** oder **TASK \_ RUNLEVEL \_ LUA** ist. Die Aufgabe wird mit einer Berechtigungsstufe ausgeführt, die von der **RunLevel-Eigenschaft** festgelegt wird, es sei denn, Sie verwenden das Administratorkonto. In diesem Fall wird der Task mit erhöhten Rechten ausgeführt.

Bei einem Prozess mit erhöhten Rechten können Sie eine Taskplaner 1.0-Aufgabe registrieren. Der Taskplaner-Dienst legt die Ausführungsebene des Tasks auf TASK \_ RUNLEVEL \_ HIGHEST fest, und der Task wird mit erhöhten Rechten ausgeführt.

Bei einem Prozess mit geringen Rechten können Sie auch eine Taskplaner 1.0-Aufgabe registrieren. Der Taskplaner-Dienst legt die Ausführungsebene des Tasks auf TASK \_ RUNLEVEL \_ LUA fest, und der Task wird mit geringen Berechtigungen ausgeführt. Wenn dieser Task von einem Prozess mit erhöhten Rechten aktualisiert wird, bleibt die Ausführungsebene des Tasks TASK \_ RUNLEVEL \_ LUA.

## <a name="security-for-registering-tasks"></a>Sicherheit beim Registrieren von Aufgaben

Wenn Sie eine Aufgabe über ein Konto registrieren, das Mitglied der Gruppe Administratoren ist, müssen Sie beim Registrieren der Aufgabe nur in den folgenden Situationen ein Kennwort angeben:

-   Wenn Sie die Aufgabe für die Ausführung im Sicherheitskontext Ihres Kontos oder eines anderen Benutzerkontos registrieren und das FLAG TASK \_ LOGON \_ PASSWORD in der [**RegisterTask-**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**RegisterTaskDefinition-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) verwenden.
-   Wenn Sie die Aufgabe für die Ausführung im Sicherheitskontext eines anderen Benutzerkontos registrieren und das FLAG TASK \_ LOGON \_ S4U in der [**RegisterTask-**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**RegisterTaskDefinition-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) verwenden.

Sie können eine Benutzergruppe nicht als Sicherheitskontext einer Aufgabe verwenden, wenn Sie die Aufgabe mit dem TASK \_ LOGON \_ S4U-Flag oder dem TASK \_ LOGON \_ PASSWORD-Flag in der [**RegisterTask-**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**RegisterTaskDefinition-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) registrieren.

Wenn Sie eine Aufgabe über ein Benutzerkonto registrieren, das kein Mitglied der Gruppe Administratoren ist, müssen Sie beim Registrieren der Aufgabe kein Kennwort angeben, wenn Sie die Aufgabe für die Ausführung im Sicherheitskontext Ihres Kontos registrieren und den S4U- oder interaktiven Anmeldetyp verwenden. Andernfalls müssen Sie beim Registrieren der Aufgabe ein Kennwort angeben. Außerdem können Sie den Task nicht mit dem lokalen Dienstkonto oder mithilfe einer Gruppe für den Sicherheitskontext des Tasks registrieren.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Sicherheit beim Lesen, Aktualisieren, Löschen und Ausführen von Aufgaben

Standardmäßig kann ein Benutzer, der eine Aufgabe erstellt, die Aufgabe lesen, aktualisieren, löschen und ausführen. Ein Benutzer muss über die Dateischreibberechtigung für eine Taskdatei verfügen, um eine Aufgabe zu aktualisieren, über die Berechtigung zum Lesen einer Aufgabe für eine Taskdatei, über die Berechtigung zum Löschen einer Taskdatei und über die Berechtigung zum Ausführen von Dateien für eine Aufgabe zum Ausführen eines Tasks mithilfe der Methoden [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) oder [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ([**RegisteredTask.Run**](registeredtask-run.md) und [**RunEx**](registeredtask-runex.md) für Skripterstellung). Mitglieder der Gruppe Administratoren oder des SYSTEM-Kontos können alle Aufgaben lesen, aktualisieren, löschen und ausführen. Mitglieder der Gruppe Benutzer, des LocalService-Kontos und des NetworkService-Kontos können nur die erstellten Aufgaben lesen, aktualisieren, löschen und ausführen. Dieses Standardverhalten wird geändert, wenn die DACL der Taskdatei geändert wird. In diesem Fall definiert die DACL, welche Benutzer über die Berechtigung zum Schreiben, Lesen, Ausführen und Löschen von Dateien verfügen. Verwenden Sie zum Festlegen von Berechtigungen für eine Taskdatei die IRegisteredTask.SetSecurityDescriptor-Methode (RegisteredTask.SetSecurityDescriptor für die Skripterstellung), oder legen Sie den Sicherheitsdeskriptor fest, wenn Sie den Task mithilfe der [**RegisterTask-**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**RegisterTaskDefinition-Methoden**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) registrieren.

Ein Benutzer muss zusätzlich zu den Lese-/Schreibberechtigungen über die WriteDAC-Berechtigung verfügen, um eine Aufgabe zu aktualisieren, wenn das Taskupdate eine Änderung der DACL für den Task erfordert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Aufgabenregistrierung](task-registration-information.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Tasksicherheitshärtung](task-security-hardening.md)
</dt> <dt>

[**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Principal-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**\_TYP DER TASKANMELDUNG \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




