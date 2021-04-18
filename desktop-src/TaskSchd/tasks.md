---
title: Aufgaben
description: Eine Aufgabe ist die geplante Arbeit, die der Taskplaner-Dienst ausführt.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- Aufgaben Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337390"
---
# <a name="tasks"></a>Aufgaben

Eine Aufgabe ist die geplante Arbeit, die der Taskplaner-Dienst ausführt. Eine Aufgabe besteht aus verschiedenen Komponenten, aber eine Aufgabe muss einen-Triggern enthalten, den der Taskplaner verwendet, um die Aufgabe zu starten, und eine Aktion, die beschreibt, welche Arbeit der Taskplaner ausführt.

Wenn eine Aufgabe erstellt wird, wird Sie in einem Aufgaben Ordner gespeichert. Auf Aufgaben Ordner kann über die [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) -Schnittstelle ([**taskfolder**](taskfolder.md) für die Skripterstellung) zugegriffen werden, und auf Aufgaben kann über die [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) -Schnittstelle ([**registeredtask**](registeredtask.md) für die Skripterstellung) zugegriffen werden, wenn Sie erstellt werden. Sie können Zugriffs Steuerungs Listen (Access Control Lists, ACLs) für Aufgaben und Aufgaben Ordner ändern, um bestimmten Benutzern und Gruppen den Zugriff auf einen Task-oder Aufgaben Ordner zu gewähren oder zu verweigern. Dies kann mithilfe der [**IRegisteredTask:: SETSECURITYDESCRIPTOR**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) -Methode, der [**ITaskFolder:: SETSECURITYDESCRIPTOR**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) -Methode oder durch Angeben einer Sicherheits Beschreibung erfolgen, wenn eine Aufgabe mithilfe der [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode oder der [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode registriert wird.

> [!Note]  
> Wenn dem lokalen System Konto der Zugriff auf eine Aufgaben Datei oder einen Aufgaben Ordner verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.

 

## <a name="components-of-a-task"></a>Komponenten einer Aufgabe

In der folgenden Abbildung sind die Aufgaben Komponenten dargestellt.

![Task Komponenten](images/taskcomponents.png)

Die folgende Liste enthält eine kurze Beschreibung der einzelnen Aufgaben Komponenten:

-   Trigger: Taskplaner verwendet Ereignis-oder zeitbasierte Trigger, um zu erfahren, wann eine Aufgabe gestartet werden soll. Jeder Task kann einen oder mehrere Trigger zum Starten der Aufgabe angeben.

    Weitere Informationen zu Triggern finden Sie unter [Task Trigger](task-triggers.md).

-   Aktionen: Dies sind die Aktionen, die von der Aufgabe durchgeführt werden. Jeder Task kann eine oder mehrere Aktionen angeben, um seine Arbeit abzuschließen.

    Weitere Informationen zu Aktionen finden Sie unter [Task Actions](task-actions.md).

-   Prinzipale: Prinzipale definieren den Sicherheitskontext, in dem die Aufgabe ausgeführt wird. Ein Prinzipal könnte z. b. einen bestimmten Benutzer oder eine Benutzergruppe definieren, die die Aufgabe ausführen kann.

    Weitere Informationen zu Prinzipale finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).

-   Einstellungen: Dies sind die Einstellungen, die von der Taskplaner verwendet werden, um die Aufgabe in Bezug auf Bedingungen auszuführen, die sich außerhalb der Aufgabe selbst befinden. Diese Einstellungen können z. b. die Priorität der Aufgabe in Bezug auf andere Aufgaben angeben, unabhängig davon, ob mehrere Instanzen der Aufgabe ausgeführt werden können, wie die Aufgabe behandelt wird, wenn sich der Computer in einem Leerlaufzustand befindet, und andere Bedingungen.

    Weitere Informationen zu Aufgaben Einstellungen finden Sie unter [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**tasksettings**](tasksettings.md) für Skripterstellung).

    > [!Note]  
    > Standardmäßig wird eine Aufgabe 72 Stunden nach dem Start angehalten. Sie können dies ändern, indem Sie die Einstellung [**executiontimelimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) ändern.

     

-   Registrierungsinformationen: Hierbei handelt es sich um administrative Informationen, die gesammelt werden, wenn der Task registriert wird. Diese Informationen beschreiben beispielsweise den Autor der Aufgabe, das Datum, an dem die Aufgabe registriert wurde, eine XML-Beschreibung des Tasks und weitere Informationen.

    Weitere Informationen zu Aufgaben Registrierungsinformationen finden Sie unter [Aufgaben Registrierungsinformationen](task-registration-information.md).

-   Daten: Dies ist eine zusätzliche Dokumentation zu der Aufgabe, die vom Autor der Aufgabe bereitgestellt wird. Diese Daten können z. b. XML-Hilfe enthalten, die von Benutzern verwendet werden kann, wenn Sie die Aufgabe ausführen.

## <a name="task-apis"></a>Task-APIs

Taskplaner 2,0 stellt zwei Sätze von APIs bereit: einen Satz von Skript Objekten und Schnittstellen für Taskplaner 2,0. Weitere Informationen finden Sie unter [Taskplaner Referenz](task-scheduler-reference.md).

Die mit der [**Compatibility**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) -Eigenschaft festgelegte Task Kompatibilität sollte nur auf Task Kompatibilität v1 festgelegt werden, \_ \_ Wenn ein Task auf einen Computer unter Windows XP, Windows Server 2003 oder Windows 2000 zugegriffen werden muss oder geändert werden muss. Andernfalls empfiehlt es sich, die Kompatibilität mit Taskplaner 2,0 zu verwenden, da Sie mehr Features hat.

Ab Taskplaner 2,0 wird die [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Schnittstelle ([**Task Service**](taskservice.md) für die Skripterstellung) als Ausgangspunkt zum Erstellen von Aufgaben in den angegebenen Ordnern verwendet. Die [**itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) -Schnittstelle ([**Task Definition**](taskdefinition.md) für die Skripterstellung) wird verwendet, um alle Komponenten einer Aufgabe (z. b. Einstellungen, Aktionen und Trigger) zu speichern. Die [**itasktrigger-**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)-und [**itasksettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) -APIs stellen Eigenschaften bereit, die dann verwendet werden, um die anderen Komponenten der Aufgabe zu definieren. Taskplaner 1,0 stellt die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle bereit, die nur aus Gründen der Abwärtskompatibilität unterstützt wird.

Bei der Skripterstellung werden die Taskplaner Schnittstellen Skript Objekten mit ähnlichen Namen, Eigenschaften und Methoden zugeordnet. Das [**TaskService**](taskservice.md) -Skript Objekt hat z. b. die gleichen Eigenschaften und Methoden wie die [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) -Schnittstelle.

Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Taskplaner 1,0 Tasks

Eine Taskplaner 1,0-Aufgabe ist jede Anwendung oder jeder Dateityp, die von der Taskplaner ausgeführt werden kann. Diese können Folgendes umfassen (wie von dem Betriebssystem unterstützt, auf dem der Task ausgeführt wird): Win32-Anwendungen, Win16-Anwendungen, OS/2-Anwendungen, MS-DOS-Anwendungen, Batch Dateien ( \* bat), Befehls Dateien ( \* . cmd) oder ein beliebiger ordnungsgemäß registrierter Dateityp.

Daten, die eine Aufgabe beschreiben, werden in einer Aufgaben Datei gespeichert, die im Ordner "geplante Aufgaben" gespeichert ist. Weitere Informationen finden Sie im [*Ordner "geplante Aufgaben*](s.md)". Der Name dieser Aufgaben Dateien enthält den Namen der Aufgabe, gefolgt von der Dateinamenerweiterung. Job.

Weitere Informationen zum Hinzufügen von Taskplaner 1,0-Tasks finden Sie unter [Hinzufügen von Arbeits Elementen](adding-work-items.md).

Weitere Informationen zum Auflisten von Taskplaner 1,0-Tasks finden Sie unter Auflisten von [Tasks](enumerating-tasks.md).

Für einen Computer mit Windows Server 2003, Windows XP oder Windows 2000 zum Erstellen, überwachen oder Steuern von Aufgaben auf einem Computer mit Windows Vista müssen die folgenden Vorgänge auf dem Computer mit Windows Vista ausgeführt werden, und der Benutzer, der die [**itaskscheduler:: settargetcomputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) -Methode aufgerufen hat, muss ein Mitglied der Gruppe "Administratoren" auf dem Windows Vista-Remote Computer sein.

**So aktivieren Sie die Ausnahme "Datei und Drucker freigeben" in der Windows-Firewall**

1.  Klicken Sie auf **Start** und dann auf **Systemsteuerung**.
2.  Klicken Sie in der **Systemsteuerung** auf **klassische Ansicht** , und doppelklicken Sie dann auf das Symbol **Windows-Firewall** .
3.  Klicken Sie im Fenster **Windows-Firewall** auf die Registerkarte **Ausnahmen** , und aktivieren Sie das Kontrollkästchen **Datei-und Druckerfreigabe Ausnahme** .

**So aktivieren Sie den Dienst "Remote Registrierung"**

-   Öffnen Sie ein Eingabe Aufforderungs Fenster, und geben Sie den folgenden Befehl ein: **net Start "Remote Registry"**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Task Trigger](task-triggers.md)
</dt> <dt>

[Task Aktionen](task-actions.md)
</dt> <dt>

[**Itaskdefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**Task Definition**](taskdefinition.md)
</dt> <dt>

[**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**Task Service**](taskservice.md)
</dt> </dl>

 

 




