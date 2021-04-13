---
title: Wiederholen einer Aufgabe
description: Taskplaner können eine Aufgabe beliebig oft nach dem Auslösen eines Auslösers ausführen.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- Wiederholungsmuster Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310655"
---
# <a name="repeating-a-task"></a>Wiederholen einer Aufgabe

Taskplaner können eine Aufgabe beliebig oft nach dem Auslösen eines Auslösers ausführen. Zu diesem Zweck definiert der-Vorgang ein Wiederholungsmuster, das angibt, Taskplaner wie lange die Aufgabe fortgesetzt werden soll, und das Zeitintervall zwischen den einzelnen Aufgaben Wiederholungen.

## <a name="repetition-pattern"></a>Wiederholungsmuster

Die folgende Abbildung zeigt ein Wiederholungsmuster mit einer Dauer von 60 Minuten und einem Intervall von 25 Minuten. Beachten Sie, dass Taskplaner in diesem Fall die Aufgabe ausführt, wenn der Triggervorgang ausgelöst wird, die Aufgabe nach 25 Minuten erneut ausführt und dann die Aufgabe nach 50 Minuten erneut ausführt, abhängig von der Einstellung der [**stopatdurationend-Eigenschaft von irepetitionpattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**repetitionpattern. stopatdurationend**](repetitionpattern-stopatdurationend.md) für Scripting). Wenn die **stopatdurationend** -Eigenschaft auf true festgelegt ist, beendet Taskplaner die letzte Instanz der Aufgabe, wenn Sie noch nach 60 Minuten ausgeführt wird. Wenn die **stopatdurationend** -Eigenschaft auf false festgelegt ist, wird die letzte Instanz der Aufgabe unabhängig von der Dauer ausgeführt.

![Wiederholungsmuster für Wiederholung](images/repetition-pattern.png)

Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet. Die fünf Wiederholungen können mithilfe des folgenden Musters definiert werden:

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen-Auslösers mit einem Wiederholungsintervall von einer Minute und einer Wiederholungs Dauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

## <a name="objects-interfaces-and-xml-elements"></a>Objekte, Schnittstellen und XML-Elemente

Bei der Skripterstellung wird das Wiederholungsmuster mithilfe des [**repetitionpattern**](repetitionpattern.md) -Objekts definiert.

Bei der C++-Entwicklung wird das Wiederholungsmuster durch die [**irepetitionpattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) -Schnittstelle definiert.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsmuster im [**Wiederholungs**](taskschedulerschema-repetition-triggerbasetype-element.md) Element angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Task Trigger](task-triggers.md)
</dt> </dl>

 

 




