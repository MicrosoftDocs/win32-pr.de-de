---
title: Aufgaben Registrierungsinformationen
description: Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren. Beispielsweise kann eine Aufgabe vom Autor identifiziert werden, wie Sie erstellt wurde (als Aufgaben Quelle bezeichnet) und das Datum der Registrierung.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Registrierungsinformationen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309195"
---
# <a name="task-registration-information"></a>Aufgaben Registrierungsinformationen

Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren. Beispielsweise kann eine Aufgabe vom Autor identifiziert werden, wie Sie erstellt wurde (als Aufgaben Quelle bezeichnet) und das Datum der Registrierung.

## <a name="using-registration-information"></a>Verwenden von Registrierungsinformationen

Registrierungsinformationen werden in der Regel angegeben, wenn die Aufgabe erstellt und dann auf folgende Weise verwendet wird:

-   Wird von der Taskplaner Benutzeroberfläche angezeigt.
-   Get oder Set by C++ Applications or Scripts.
-   In einer Unternehmensumgebung, die als Suchkriterium verwendet wird, wenn alle registrierten Tasks aufgezählt werden.

## <a name="types-of-registration-information"></a>Typen von Registrierungsinformationen

Aufgaben Registrierungsinformationen werden durch die Eigenschaften des [**RegistrationInfo**](registrationinfo.md) -Objekts für Skript Anwendungen, die Eigenschaften der [**iregistrationinfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) -Schnittstelle für C++-Anwendungen und die untergeordneten Elemente des [**RegistrationInfo-Elements (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) zum Lesen oder Schreiben von XML definiert.

Diese Eigenschaften ermöglichen den Zugriff auf die folgenden Typen von Registrierungsinformationen:

-   Aufgaben Autor

    Taskplaner legt den Autor der Aufgabe fest, wenn diese erstellt wird.

-   Registrierungsdatum der Aufgabe

    Taskplaner legt dieses Datum fest, wenn der Task registriert wird.

-   Taskbeschreibung

    Eine benutzerdefinierte Beschreibung, die möglicherweise einschließt, welche Trigger verwendet werden, um den Task zu starten oder welche Aktionen der Task ausführt.

-   Task Dokumentation

    Vom Benutzer bereitgestellte Dokumentation, die von der Aufgabe benötigt wird.

-   Task Sicherheits Beschreibung

    Ein vom Benutzer bereitgestellter Sicherheits Deskriptor.

-   Task Quelle

    Vom Benutzer bereitgestellte Informationen, die den Ursprung der Aufgabe von beschreiben. Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.

-   Task-URI

    Ein URI (Uniform Resource Identifier) für den Task.

-   Taskversion

    Vom Benutzer bereitgestellte Informationen, die verwendet werden, wenn mehrere Versionen einer Aufgabe vorhanden sind.

-   XML-Text

    Eine XML-formatierte Version der Registrierungsinformationen. Beachten Sie, dass Sie die Registrierungsinformationen direkt über diesen XML-Code festlegen oder ändern können, und die entsprechenden Objekt-und Schnittstelleneigenschaften werden entsprechend aktualisiert.

## <a name="registering-tasks"></a>Registrieren von Aufgaben

Eine Aufgabe kann registriert werden, nachdem die Aufgaben Definitionen erstellt wurden, und Registrierungsinformationen und Einstellungs Werte werden vom Benutzer bereitgestellt. Eine Aufgabe wird mithilfe der [**Task Folder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) -Methode für Skript Anwendungen oder der [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) -Methode für C++-Anwendungen registriert. Wenn Sie eine Aufgabe mithilfe von XML zum Definieren der Aufgabe registrieren möchten, verwenden Sie die [**Task Folder. RegisterTask**](taskfolder-registertask.md) -Methode für Skript Anwendungen und die [**ITaskFolder:: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) -Methode für C++-Anwendungen.

In den oben erwähnten Methoden können Sie den Sicherheitskontext angeben, um den Task auszuführen. Sie müssen ein Administrator im System sein, um die Ausführung von Aufträgen in anderen Kontexten als ihren eigenen zu planen. Weitere Informationen zu den Sicherheits Kontexten zum Ausführen von Tasks finden Sie unter [Sicherheits Kontexte zum](security-contexts-for-running-tasks.md)Ausführen von Tasks.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 




