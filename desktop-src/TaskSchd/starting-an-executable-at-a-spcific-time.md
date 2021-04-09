---
title: Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt
description: Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeit Auslösers und einer ausführbaren Aktion.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Taskplaner Beispiele Taskplaner, Zeit Auslösung
- Taskplaner Beispiele Taskplaner, Starten einer ausführbaren Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856500"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt

Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeit Auslösers und einer ausführbaren Aktion.

## <a name="start-boundary"></a>Start Grenze

Es ist wichtig zu beachten, dass ein Zeit Trigger von anderen zeitbasierten Triggern abweicht, dass er ausgelöst wird, wenn der Trigger durch seine Start Grenze aktiviert wird. Andere Zeitbasierte Trigger werden über die Start Grenze aktiviert, aber Sie beginnen nicht mit der Ausführung ihrer Aktionen (in diesem Fall das Starten einer ausführbaren Datei), bis ein geplantes Datum erreicht ist.

## <a name="time-trigger-examples"></a>Beispiele für Zeit Beispiele

In den folgenden Beispielen wird der Editor 30 Sekunden nach der Aktivierung der Aufgabe gestartet:

-   [Beispiel für Zeit Auslösung (C++)](time-trigger-example--c---.md)
-   [Beispiel für Zeit Auslösung (Skripterstellung)](time-trigger-example--scripting-.md)
-   [Beispiel für Zeit Auslösung (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




