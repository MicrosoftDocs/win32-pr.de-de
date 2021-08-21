---
title: Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt
description: Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeittriggers und einer ausführbaren Aktion.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Taskplaner Beispiele Taskplaner , Zeittrigger
- Taskplaner Beispielen Taskplaner , Starten einer ausführbaren Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62276568f7c626935d8c5c518d51f58ad0a58b5c313e780ec5651067af625068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059958"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Starten einer ausführbaren Datei zu einem bestimmten Zeitpunkt

Das Schreiben einer Aufgabe, die eine ausführbare Datei zu einem bestimmten Zeitpunkt startet, erfolgt durch Definieren eines Zeittriggers und einer ausführbaren Aktion.

## <a name="start-boundary"></a>Startgrenze

Es ist wichtig zu beachten, dass sich ein Zeittrigger von anderen zeitbasierten Triggern abgrenzt, da er ausgelöst wird, wenn der Trigger durch seine Startgrenze aktiviert wird. Andere zeitbasierte Trigger werden durch ihre Startgrenze aktiviert, aber sie beginnen nicht mit der Ausführung ihrer Aktionen (in diesem Fall dem Starten einer ausführbaren Datei), bis ein geplantes Datum erreicht ist.

## <a name="time-trigger-examples"></a>Beispiele für Zeittrigger

Die folgenden Beispiele beginnen Editor 30 Sekunden nach der Aktivierung der Aufgabe:

-   [Beispiel für Zeittrigger (C++)](time-trigger-example--c---.md)
-   [Beispiel für Zeittrigger (Skripterstellung)](time-trigger-example--scripting-.md)
-   [Beispiel für Zeittrigger (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




