---
title: Aufzählen von Aufgaben und Anzeigen von Aufgabeninformationen
description: Das Anzeigen von Informationen zu einem Task, z. B. Aufgabenname, Status oder zeitpunkt der letzten Ausführung des Tasks, erfolgt durch Aufzählen von ausgeführten Tasks oder aufgaben in einem Aufgabenordner und Anzeigen der gewünschten Informationen.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Aufzählen von Aufgaben Taskplaner
- Taskplaner Beispiele Taskplaner , Aufzählen von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4859122218ead4d18c1f9e83de0f55ce9373306cd2762e5608cf4d1841019b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002448"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Aufzählen von Aufgaben und Anzeigen von Aufgabeninformationen

Das Anzeigen von Informationen zu einem Task, z. B. Aufgabenname, Status oder zeitpunkt der letzten Ausführung des Tasks, erfolgt durch Aufzählen von ausgeführten Tasks oder aufgaben in einem Aufgabenordner und Anzeigen der gewünschten Informationen.

## <a name="accessing-properties-of-registered-tasks"></a>Zugreifen auf Eigenschaften von registrierten Aufgaben

Um den Eigenschaftswert einer registrierten Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Instanz des Aufgabenordners abrufen, der die Tasks enthält, zu denen Sie Informationen benötigen. Anschließend erhalten Sie eine Sammlung aller registrierten Aufgaben im Aufgabenordner. Anschließend durchlaufen Sie jede registrierte Aufgabe und erhalten und zeigen einen Eigenschaftswert für jede Aufgabe an.

## <a name="accessing-properties-of-running-tasks"></a>Zugreifen auf Eigenschaften von ausgeführten Aufgaben

Um den -Eigenschaftswert einer ausgeführten Aufgabe anzuzeigen, müssen Sie eine Verbindung mit dem Taskplaner-Dienst herstellen und dann eine Sammlung aller ausgeführten Aufgaben abrufen (einschließlich oder ausschließen von ausgeblendeten Aufgaben). Anschließend durchlaufen Sie die einzelnen ausgeführten Aufgaben und erhalten und zeigen einen Eigenschaftswert für jede Aufgabe an.

## <a name="example"></a>Beispiel

In den folgenden Beispielen werden Tasks aufzählt und der Name und Status der Aufgaben angezeigt:

-   [Anzeigen von Aufgabennamen und -zuständen (Skripterstellung)](displaying-task-names-and-state--scripting-.md)
-   [Anzeigen von Aufgabennamen und -zuständen (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




