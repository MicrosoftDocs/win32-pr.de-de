---
title: Aufgaben
description: Eine Aufgabe ist die geplante Arbeit, die vom Taskplaner Dienst ausgeführt wird.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tasks Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f6122bcf32e0c3e242b6dce119432a9014718d4b65d19c613ce27794355491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517105"
---
# <a name="tasks"></a>Aufgaben

Eine Aufgabe ist die geplante Arbeit, die vom Taskplaner Dienst ausgeführt wird. Eine Aufgabe besteht aus verschiedenen Komponenten, aber eine Aufgabe muss einen Trigger enthalten, den der Taskplaner zum Starten der Aufgabe verwendet, und eine Aktion, die beschreibt, welche Arbeit die Taskplaner ausführt.

Wenn eine Aufgabe erstellt wird, wird sie in einem Aufgabenordner gespeichert. Auf Taskordner kann über die [**ITaskFolder-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) [**(TaskFolder**](taskfolder.md) für Skripterstellung) zugegriffen werden, und auf Aufgaben kann über die [**IRegisteredTask-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) [**(RegisteredTask**](registeredtask.md) für Skripterstellung) zugegriffen werden, wenn sie erstellt werden. Sie können Zugriffssteuerungslisten (ACCESS Control Lists, ACLs) für Tasks und Aufgabenordner ändern, um bestimmten Benutzern und Gruppen den Zugriff auf einen Task- oder Aufgabenordner zu gewähren oder zu verweigern. Hierzu können Sie die [**IRegisteredTask::SetSecurityDescriptor-Methode,**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) die [**ITaskFolder::SetSecurityDescriptor-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) oder einen Sicherheitsdeskriptor angeben, wenn eine Aufgabe mithilfe der [**RegisterTaskDefinition-**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) oder [**RegisterTask-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) registriert wird.

> [!Note]  
> Wenn dem lokalen Systemkonto der Zugriff auf eine Taskdatei oder einen Aufgabenordner verweigert wird, kann der Taskplaner Dienst zu unerwarteten Ergebnissen führen.

 

## <a name="components-of-a-task"></a>Komponenten eines Tasks

Die folgende Abbildung zeigt die Aufgabenkomponenten.

![Taskkomponenten](images/taskcomponents.png)

Die folgende Liste enthält eine kurze Beschreibung der einzelnen Aufgabenkomponenten:

-   Trigger: Taskplaner verwendet ereignis- oder zeitbasierte Trigger, um zu wissen, wann eine Aufgabe gestartet werden soll. Jede Aufgabe kann einen oder mehrere Trigger angeben, um die Aufgabe zu starten.

    Weitere Informationen zu Triggern finden Sie unter [Tasktrigger.](task-triggers.md)

-   Aktionen: Dies sind die Aktionen, die eigentliche Arbeit, die von der Aufgabe ausgeführt wird. Jede Aufgabe kann eine oder mehrere Aktionen angeben, um ihre Arbeit abzuschließen.

    Weitere Informationen zu Aktionen finden Sie unter [Aufgabenaktionen.](task-actions.md)

-   Prinzipale: Prinzipale definieren den Sicherheitskontext, in dem der Task ausgeführt wird. Beispielsweise kann ein Prinzipal einen bestimmten Benutzer oder eine Bestimmte Benutzergruppe definieren, der bzw. die die Aufgabe ausführen kann.

    Weitere Informationen zu Prinzipalen finden Sie unter [Sicherheitskontexte für Tasks.](security-contexts-for-running-tasks.md)

-   Einstellungen: Dies sind die Einstellungen, die der Taskplaner verwendet, um den Task in Bezug auf Bedingungen auszuführen, die außerhalb der Aufgabe selbst liegen. Diese Einstellungen können z. B. die Priorität des Tasks in Bezug auf andere Tasks angeben, ob mehrere Instanzen des Tasks ausgeführt werden können, wie der Task behandelt wird, wenn sich der Computer in einer Leerlaufbedingung befindet, und andere Bedingungen.

    Weitere Informationen zu Taskeinstellungen finden Sie unter [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) for scripting).

    > [!Note]  
    > Standardmäßig wird eine Aufgabe 72 Stunden nach beginn der Ausführung beendet. Sie können dies ändern, indem Sie die [**Einstellung ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) ändern.

     

-   Registrierungsinformationen: Dies sind Administrative Informationen, die bei der Registrierung des Tasks gesammelt werden. Diese Informationen beschreiben z. B. den Ersteller der Aufgabe, das Datum, an dem der Task registriert wurde, eine XML-Beschreibung der Aufgabe und andere Informationen.

    Weitere Informationen zur Aufgabenregistrierung finden Sie unter [Informationen zur Aufgabenregistrierung.](task-registration-information.md)

-   Daten: Dies ist eine zusätzliche Dokumentation zu der Aufgabe, die vom Ersteller der Aufgabe bereitgestellt wird. Diese Daten können z. B. XML-Hilfe enthalten, die von Benutzern beim Ausführen der Aufgabe verwendet werden kann.

## <a name="task-apis"></a>Aufgaben-APIs

Taskplaner 2.0 bietet zwei APIs: eine Reihe von Skriptobjekten und Schnittstellen für Taskplaner 2.0. Weitere Informationen finden Sie unter [Taskplaner Referenz.](task-scheduler-reference.md)

Taskkompatibilität, die über die [**Compatibility-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) festgelegt wird, sollte nur auf TASK COMPATIBILITY V1 festgelegt werden, wenn auf \_ einen Task von einem Windows \_ XP-, Windows Server 2003- oder Windows 2000-Computer zugegriffen oder geändert werden muss. Andernfalls wird empfohlen, Taskplaner 2.0-Kompatibilität zu verwenden, da sie über mehr Features verfügt.

Ab Taskplaner 2.0 wird die [**ITaskService-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) [**(TaskService**](taskservice.md) für Skripterstellung) als Ausgangspunkt zum Erstellen von Aufgaben in angegebenen Ordnern verwendet. Die [**ITaskDefinition-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) [**(TaskDefinition**](taskdefinition.md) für Skripts) wird verwendet, um alle Komponenten einer Aufgabe zu speichern, z. B. einstellungen, aktionen und trigger. Die [**APIs ITaskTrigger,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)und [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) stellen Eigenschaften bereit, die dann zum Definieren der anderen Komponenten des Tasks verwendet werden. Taskplaner 1.0 stellt die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) bereit, die nur aus Gründen der Abwärtskompatibilität unterstützt wird.

Für die Skripterstellung werden die Taskplaner Schnittstellen Skriptobjekten zugeordnet, die ähnliche Namen, Eigenschaften und Methoden aufweisen. Beispielsweise verfügt das [**TaskService-Skriptobjekt**](taskservice.md) über die gleichen Eigenschaften und Methoden wie die [**ITaskService-Schnittstelle.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skriptobjekte und XML finden Sie unter [Verwenden der Taskplaner](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Taskplaner 1.0 Tasks

Eine Taskplaner 1.0-Aufgabe ist jede Anwendung oder jeder Dateityp, die bzw. der vom Taskplaner ausgeführt werden kann. Dies kann eine der folgenden Optionen umfassen (wie vom Betriebssystem unterstützt, unter dem der Task ausgeführt wird): Win32-Anwendungen, Win16-Anwendungen, Betriebssystem-/2-Anwendungen, MS-DOS-Anwendungen, Batchdateien ( \*.bat), Befehlsdateien ( \* CMD) oder alle ordnungsgemäß registrierten Dateitypen.

Daten, die eine Aufgabe beschreiben, werden in einer Taskdatei gespeichert, die im Ordner Geplante Aufgaben gespeichert ist. Weitere Informationen finden Sie unter [*Scheduled Tasks folder (Ordner*](s.md)für geplante Aufgaben). Der Name dieser Taskdateien enthält den Namen der Aufgabe, gefolgt von der Dateierweiterung .job.

Weitere Informationen zum Hinzufügen von Taskplaner 1.0-Aufgaben finden Sie unter [Hinzufügen von Arbeitselementen.](adding-work-items.md)

Weitere Informationen zum Aufzählen von Taskplaner 1.0-Tasks finden Sie unter [Aufzählen von Tasks.](enumerating-tasks.md)

Damit ein Windows Server 2003-, Windows XP- oder Windows 2000-Computer Aufgaben auf einem Windows Vista-Computer erstellen, überwachen oder steuern kann, müssen die folgenden Vorgänge auf dem computer Windows Vista ausgeführt werden, und der Benutzer, der die [**ITaskScheduler::SetTargetComputer-Methode**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) aufruft, muss Mitglied der Gruppe Administratoren auf dem Remotecomputer Windows Vista sein.

**So aktivieren Sie die Ausnahme "Datei und Drucker freigeben" in Windows Firewall**

1.  Klicken Sie auf **Start** und dann auf **Systemsteuerung**.
2.  Klicken Sie **in Systemsteuerung** auf **Klassische Ansicht,** und doppelklicken Sie dann auf das **Windows Firewallsymbol.**
3.  Klicken Sie im **fenster Windows Firewall** auf die Registerkarte **Ausnahmen,** und aktivieren Sie das **Kontrollkästchen Datei- und Druckerfreigabeausnahme.**

**So aktivieren Sie den Dienst "Remoteregistrierung"**

-   Öffnen Sie ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl ein: **net start "Remote Registry".**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> <dt>

[Aufgabenaktionen](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




