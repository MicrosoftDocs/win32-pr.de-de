---
title: Informationen zur Aufgabenregistrierung
description: Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren. Beispielsweise kann ein Task vom Autor identifiziert werden, wie er erstellt wurde (als Taskquelle bezeichnet) und das Datum der Registrierung.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- Registrierungsinformationen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12e3dc9163b1074eff12be6b872780184b112b6c8a2512e3a68901d083f9c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139283"
---
# <a name="task-registration-information"></a>Informationen zur Aufgabenregistrierung

Registrierungsinformationen bieten eine Möglichkeit, eine Aufgabe auf verschiedene Weise zu identifizieren. Beispielsweise kann ein Task vom Autor identifiziert werden, wie er erstellt wurde (als Taskquelle bezeichnet) und das Datum der Registrierung.

## <a name="using-registration-information"></a>Verwenden von Registrierungsinformationen

Registrierungsinformationen werden in der Regel angegeben, wenn der Task erstellt und dann auf folgende Weise verwendet wird:

-   Wird von der Taskplaner Benutzeroberfläche angezeigt.
-   Abrufen oder Festlegen durch C++-Anwendungen oder -Skripts.
-   In einer Unternehmensumgebung, die als Suchkriterien beim Aufzählen aller registrierten Aufgaben verwendet wird.

## <a name="types-of-registration-information"></a>Typen von Registrierungsinformationen

Informationen zur Aufgabenregistrierung werden durch die Eigenschaften des [**RegistrationInfo-Objekts**](registrationinfo.md) für Skriptanwendungen, die Eigenschaften der [**IRegistrationInfo-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) für C++-Anwendungen und die untergeordneten Elemente des [**RegistrationInfo -Elements (taskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) zum Lesen oder Schreiben von XML definiert.

Diese Eigenschaften ermöglichen den Zugriff auf die folgenden Arten von Registrierungsinformationen:

-   Taskautor

    Taskplaner legt den Ersteller der Aufgabe fest, wenn sie erstellt wird.

-   Datum der Aufgabenregistrierung

    Taskplaner legt dieses Datum fest, wenn der Task registriert wird.

-   Taskbeschreibung

    Eine benutzerdefinierte Beschreibung, die möglicherweise enthält, welche Trigger zum Starten der Aufgabe verwendet werden oder welche Aktionen der Task ausführt.

-   Aufgabendokumentation

    Vom Benutzer bereitgestellte Dokumentation, die von der Aufgabe benötigt wird.

-   Tasksicherheitsdeskriptor

    Ein vom Benutzer bereitgestellter Sicherheitsdeskriptor.

-   Taskquelle

    Vom Benutzer bereitgestellte Informationen, die beschreiben, woher die Aufgabe stammt. Beispielsweise kann eine Aufgabe von einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.

-   Aufgaben-URI

    Ein Uniform Resource Identifier (URI) für den Task.

-   Taskversion

    Vom Benutzer bereitgestellte Informationen, die verwendet werden, wenn mehrere Versionen einer Aufgabe vorhanden sind.

-   XML-Text

    Eine XML-formatierte Version der Registrierungsinformationen. Beachten Sie, dass Sie die Registrierungsinformationen direkt über diesen XML-Code festlegen oder ändern können. Die entsprechenden Objekt- und Schnittstelleneigenschaften werden entsprechend aktualisiert.

## <a name="registering-tasks"></a>Registrieren von Aufgaben

Eine Aufgabe kann registriert werden, nachdem die Taskdefinitionen erstellt wurden und Registrierungsinformationen und Einstellungswerte vom Benutzer bereitgestellt werden. Eine Aufgabe wird mithilfe der [**TaskFolder.RegisterTaskDefinition-Methode**](taskfolder-registertaskdefinition.md) für die Skripterstellung von Anwendungen oder der [**ITaskFolder::RegisterTaskDefinition-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) für C++-Anwendungen registriert. Wenn Sie eine Aufgabe mit XML registrieren möchten, um den Task zu definieren, verwenden Sie die [**TaskFolder.RegisterTask-Methode**](taskfolder-registertask.md) zum Erstellen von Skripts für Anwendungen und die [**ITaskFolder::RegisterTask-Methode**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) für C++-Anwendungen.

In den oben erwähnten Methoden können Sie den Sicherheitskontext angeben, um die Aufgabe auszuführen. Sie müssen ein Administrator auf dem System sein, um die Ausführung von Aufträgen in anderen Kontexten als Ihren eigenen zu planen. Weitere Informationen zu den Sicherheitskontexten zum Ausführen von Aufgaben finden Sie unter [Sicherheitskontexte für ausgeführte Aufgaben.](security-contexts-for-running-tasks.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 




