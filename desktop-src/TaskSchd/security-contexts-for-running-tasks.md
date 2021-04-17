---
title: Sicherheits Kontexte für Tasks
description: Tasks werden registriert und in einem bestimmten Sicherheitskontext ausgeführt.
ms.assetid: be86eb9f-f6ec-4dce-afe8-e3314a74062a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329f354518daeb11a5f330ae3fdc2c332b66d5c3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389948"
---
# <a name="security-contexts-for-tasks"></a>Sicherheits Kontexte für Tasks

Tasks werden registriert und in einem bestimmten Sicherheitskontext ausgeführt. Benutzer können Anwendungen erstellen, die Aufgaben erfolgreich registrieren, aktualisieren, löschen oder ausführen, aber der Benutzer muss die richtigen Anmelde Informationen angeben, wenn ein Task registriert wird und die Anwendung in einem Prozess mit den richtigen Berechtigungen ausgeführt werden muss.

## <a name="specifying-credentials"></a>Angeben von Anmelde Informationen

Sie können den Sicherheitskontext für eine Aufgabe angeben, indem Sie die Anmelde Informationen in den Methoden [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) oder [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ([**taskfolder. RegisterTask**](taskfolder-registertask.md) oder [**taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) für Scripting) angeben oder indem Sie der [**Principal-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) ([**Taskdefinition. Principal**](taskdefinition-principal.md) für Scripting) einen Prinzipal zuweisen. Wenn ein Prinzipal für eine Aufgabendefinition erstellt wird und die Aufgabendefinition mithilfe der **RegisterTaskDefinition** -Methode mit anderen Anmelde Informationen registriert wird, die in den Methoden Parametern angegeben sind, überschreiben die in der **RegisterTaskDefinition** -Methode angegebenen Anmelde Informationen die Anmelde Informationen im Prinzipal. Wenn ein Prinzipal für eine Aufgabendefinition mithilfe von XML erstellt wird und dann der XML-Code für die Aufgabe mithilfe der **RegisterTask** -Methode mit anderen Anmelde Informationen registriert wird, die in den Methoden Parametern angegeben sind, überschreiben die in der **RegisterTask** -Methode angegebenen Anmelde Informationen die Anmelde Informationen im Prinzipal.

Sie geben ein Benutzerkonto oder eine Gruppe an, wenn Sie eine Aufgabe registrieren oder das Prinzip für eine Aufgabe angeben. Der Sicherheitskontext des Benutzerkontos oder der Gruppe wird für den Sicherheitskontext der Aufgabe verwendet. In diesen Methoden und Eigenschaften definieren Sie außerdem den Anmeldetyp. Der Anmeldetyp wird durch eine der Konstanten in der [**\_ \_ Aufgabentyp**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type) -Enumeration der Aufgabe definiert.

Aufgaben, die mit dem Kennzeichen Task \_ Logon \_ Password oder Task \_ Logon \_ S4U registriert werden, werden nur gestartet, wenn für den angegebenen Benutzer die Berechtigung Anmelden als Batch aktiviert ist. Administratoren und die Gruppe der Sicherungs Operatoren, in denen Benutzer diese Berechtigung standardmäßig aktiviert haben.

Wenn Sie die [**ITaskService:: Connect**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect) ([**TaskService. Connect**](taskservice-connect.md) for Scripting)-Methode aufrufen, werden alle nachfolgenden Methodenaufrufe an den Taskplaner-Dienst die Anmelde Informationen verwenden, die an die **Connect** -Methode übermittelt wurden. Dies ist wichtig zu beachten, wenn Sie Aufgaben mit einem interaktiven Anmeldetyp registrieren. Wenn Sie einen Task mit dem Anmeldetyp registrieren, der mit dem interaktiven Token der Aufgaben Anmeldung identisch ist \_ \_ \_ , und für den Task keine Anmelde Informationen in der [**Principal**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal) -Eigenschaft der Aufgabendefinition angegeben sind, die in den Parametern für die Register Task [**Definition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)angegeben sind oder in der XML-Datei angegeben sind **, die** an [**Register Task**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask)weitergegeben wird, wird die Aufgabe mit den Anmelde Informationen des Benutzers registriert,

## <a name="user-account-control-uac-security-for-tasks"></a>Sicherheit der Benutzerkontensteuerung (User Account Control, UAC) für Tasks

Mithilfe der [Benutzerkontensteuerung (User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) , UAC) können Benutzer allgemeine Funktionen, z. b. das Ausführen von Programmen, das Speichern und Ändern von Daten, ohne Standardmäßig wird eine Aufgabe mit Low-Level-Berechtigungen ausgeführt, wenn UAC aktiviert ist. Tasks können angeben, dass Sie mit erhöhten Rechten oder niedrigen Berechtigungen ausgeführt werden, indem Sie für die [**Runlevel-Eigenschaft von IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) ([**Principal. Runlevel**](principal-runlevel.md) für Scripting) eine Berechtigungsebene aus der Aufgabentyp-Enumeration der [**Aufgabe \_ \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type) festlegen. Der Wert der **Runlevel** -Eigenschaft bestimmt die Berechtigungsstufe, unter der die Aktionen einer Aufgabe ausgeführt werden. Wenn für die Ausführung einer Aufgabe erhöhte Rechte erforderlich sind, müssen Sie die **Runlevel** -Eigenschaft auf " **Task \_ Runlevel \_** Most" festlegen. Wenn eine Aufgabe mithilfe der Gruppe "Administratoren" für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie die **Runlevel** -Eigenschaft auch auf " **Task \_ Runlevel \_** " festlegen, wenn Sie die Aufgabe ausführen möchten. Wenn ein Task mit dem integrierten \\ Administrator Konto oder dem lokalen System Konto oder dem lokalen Dienst Konto registriert wird, wird die **Runlevel** -Eigenschaft ignoriert. Der Eigenschafts Wert wird auch ignoriert, wenn die Benutzerkontensteuerung (User Account Control, UAC) ausgeschaltet ist. Der Wert der **Runlevel** -Eigenschaft wirkt sich nicht auf die Berechtigungen aus, die zum Ausführen oder Löschen einer Aufgabe erforderlich sind.

> [!Note]  
> Nach dem Upgrade eines Betriebssystems von Windows XP auf Windows Vista wird für Aufgaben, die mit dem integrierten \\ Administrator Konto unter Windows XP registriert wurden, die [**Runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) -Eigenschaft **auf \_ taskrunlevel \_ Lua** festgelegt. Dies kann dazu führen, dass einige Aufgaben fehlschlagen. Sie können diese Eigenschaft manuell aktualisieren, um sicherzustellen, dass alle Tasks ausgeführt werden.

 

Bei einem Prozess mit niedriger Berechtigung können Sie einen Task nicht mit der [**Runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) -Eigenschaft gleich **dem \_ \_ höchsten Task Runlevel** registrieren, Sie können jedoch eine Aufgabe mit der **Runlevel** -Eigenschaft registrieren, die gleich der **Aufgabe " \_ Runlevel \_ Lua**" ist. Die Aufgaben Aktionen werden mit niedrigen Berechtigungen ausgeführt. Sie sind nicht berechtigt, den Task als "Builtin/Administrator", "Lokales System" oder für eine Gruppe zu registrieren.

Bei einem Prozess mit erweiterten Berechtigungen können Sie eine Aufgabe mit der [**Runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) -Eigenschaft gleich der **Aufgabe \_ Runlevel " \_ hoch** " oder " **Task \_ Runlevel \_ Lua**" registrieren. Der Task wird mit einer Berechtigungsstufe ausgeführt, die von der **Runlevel** -Eigenschaft festgelegt wird, es sei denn, Sie verwenden das Administrator Konto. in diesem Fall wird der Task mit erhöhten Rechten ausgeführt.

Von einem erweiterten Prozess aus können Sie eine Taskplaner 1,0-Aufgabe registrieren. Der Taskplaner-Dienst legt die Ausführungs Ebene der Aufgabe auf "Task \_ Runlevel hoch" fest, \_ und der Task wird mit erhöhten Rechten ausgeführt.

Bei einem Prozess mit niedriger Berechtigung können Sie auch einen Taskplaner 1,0-Task registrieren. Der Taskplaner-Dienst legt die Ausführungs Ebene der Aufgabe auf Task \_ Runlevel \_ Lua fest, und der Task wird mit niedrigen Berechtigungen ausgeführt. Wenn diese Aufgabe von einem Prozess mit erhöhten Rechten aktualisiert wird, bleibt die Ausführungs Ebene der Aufgabe in der Task Ausführung \_ \_ Lua erhalten.

## <a name="security-for-registering-tasks"></a>Sicherheit für das Registrieren von Tasks

Wenn Sie einen Task von einem Konto registrieren, das Mitglied der Gruppe "Administratoren" ist, müssen Sie nur ein Kennwort angeben, wenn Sie den Task in den folgenden Situationen registrieren:

-   Wenn Sie die Aufgabe für die unter Verwendung des Sicherheits Kontexts Ihres Kontos oder eines anderen Benutzerkontos registrieren und Sie das Kennzeichen \_ \_ Kennwort für die Aufgabe in der [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode oder der [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode verwenden.
-   Wenn Sie die Aufgabe registrieren, um Sie im Sicherheitskontext eines anderen Benutzerkontos auszuführen, und Sie das Flag "Task \_ Logon \_ S4U" in der Methode " [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) " oder " [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) " verwenden.

Eine Benutzergruppe kann nicht als Sicherheitskontext einer Aufgabe verwendet werden, wenn Sie den Task mithilfe des Task \_ Logon \_ S4U-Flags oder des Kennworts für den Task \_ Anmelde \_ Kennwort in der [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode oder der [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode registrieren.

Wenn Sie einen Task von einem Benutzerkonto registrieren, das kein Mitglied der Gruppe "Administratoren" ist, müssen Sie beim Registrieren des Tasks kein Kennwort angeben, wenn Sie die Aufgabe registrieren, um Sie im Sicherheitskontext Ihres Kontos auszuführen, und Sie den Anmeldetyp S4U oder Interactive verwenden. Andernfalls müssen Sie beim Registrieren der Aufgabe ein Kennwort angeben. Außerdem können Sie den Task nicht mithilfe des lokalen Dienst Kontos oder mithilfe einer Gruppe für den Sicherheitskontext des Tasks registrieren.

## <a name="security-for-reading-updating-deleting-and-running-tasks"></a>Sicherheit zum Lesen, aktualisieren, löschen und Ausführen von Aufgaben

Standardmäßig kann ein Benutzer, der einen Task erstellt, den Task lesen, aktualisieren, löschen und ausführen. Ein Benutzer muss über die Berechtigung zum Schreiben von Dateien für eine Task Datei verfügen, um eine Aufgabe zu aktualisieren, die Berechtigung Datei lesen für eine Task Datei zum Lesen eines Tasks, die [**delete-Berechtigung**](registeredtask-run.md) für eine Aufgaben Datei zum Löschen eines Tasks und die EXECUTE-Berechtigung für eine Aufgabe zum Ausführen einer Aufgabe mit der [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) [**-Methode**](registeredtask-runex.md) oder der [**RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) -Methode zu verwenden Mitglieder der Gruppe "Administratoren" oder des System Kontos können beliebige Aufgaben lesen, aktualisieren, löschen und ausführen. Mitglieder der Benutzergruppe, das LocalService-Konto und das Network Service-Konto können nur die von Ihnen erstellten Aufgaben lesen, aktualisieren, löschen und ausführen. Dieses Standardverhalten wird geändert, wenn die DACL der Task Datei geändert wird. in diesem Fall definiert die DACL, welche Benutzer über die Berechtigung zum Schreiben, lesen, ausführen und Löschen verfügen. Um Berechtigungen für eine Aufgaben Datei festzulegen, verwenden Sie die IRegisteredTask. SETSECURITYDESCRIPTOR-Methode (registeredtask. SETSECURITYDESCRIPTOR für die Skripterstellung), oder legen Sie die Sicherheits Beschreibung fest, wenn Sie die Aufgabe mithilfe der [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode oder der [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode registrieren.

Ein Benutzer muss zusätzlich zu den Lese-/Schreibberechtigungen zum Aktualisieren einer Aufgabe über die Berechtigung "schreiben" verfügen, wenn für die Task Aktualisierung eine Änderung an der DACL für den Task erforderlich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben Registrierungsinformationen](task-registration-information.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Sicherheitshärtung der Aufgabe](task-security-hardening.md)
</dt> <dt>

[**Taskfolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md)
</dt> <dt>

[**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)
</dt> <dt>

[**Principal-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)
</dt> <dt>

[**Task \_ \_ Anmeldetyp**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)
</dt> </dl>

 

 




