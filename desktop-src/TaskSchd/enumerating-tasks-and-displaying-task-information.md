---
title: Auflisten von Aufgaben und Anzeigen von Aufgabeninformationen
description: Zum Anzeigen von Informationen zu einer Aufgabe, z. b. Aufgaben Name, Status oder Zeitpunkt der letzten Ausführung der Aufgabe, werden die ausgeführten Tasks oder die Tasks in einem Aufgaben Ordner aufgelistet und die gewünschten Informationen angezeigt.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Aufzählen von Aufgaben Taskplaner
- Taskplaner Beispiele Taskplaner, Auflisten von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707278"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Auflisten von Aufgaben und Anzeigen von Aufgabeninformationen

Zum Anzeigen von Informationen zu einer Aufgabe, z. b. Aufgaben Name, Status oder Zeitpunkt der letzten Ausführung der Aufgabe, werden die ausgeführten Tasks oder die Tasks in einem Aufgaben Ordner aufgelistet und die gewünschten Informationen angezeigt.

## <a name="accessing-properties-of-registered-tasks"></a>Zugreifen auf Eigenschaften registrierter Tasks

Um den Eigenschafts Wert einer registrierten Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Instanz des Aufgaben Ordners mit den Tasks, über die Sie Informationen erhalten möchten, erhalten. Anschließend erhalten Sie eine Sammlung aller registrierten Tasks im Aufgaben Ordner. Anschließend durchlaufen Sie jede registrierte Aufgabe und erhalten und zeigen einen Eigenschafts Wert für jede Aufgabe an.

## <a name="accessing-properties-of-running-tasks"></a>Zugreifen auf Eigenschaften von laufenden Tasks

Um den Eigenschafts Wert einer ausgewerenden Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Auflistung aller ausgelaufenden Tasks (einschließlich oder ausschließen ausgeblendeter Tasks) erhalten. Anschließend durchlaufen Sie jede ausgestellte Aufgabe und erhalten und zeigen einen Eigenschafts Wert für jede Aufgabe an.

## <a name="example"></a>Beispiel

In den folgenden Beispielen werden Aufgaben aufgelistet und der Name und der Zustand der Aufgaben angezeigt:

-   [Anzeigen von Aufgaben Namen und-Zuständen (Skripterstellung)](displaying-task-names-and-state--scripting-.md)
-   [Anzeigen von Aufgaben Namen und-Status (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




