---
title: Wiederholen einer Aufgabe
description: Taskplaner kann eine Aufgabe nach dem Auslösen eines Triggers mehrmals ausführen.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- Wiederholungsmuster Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039b57bdc6cc7f53125e74b8a6fda7d017106cd44c66d2535f7fdf27505a960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759355"
---
# <a name="repeating-a-task"></a>Wiederholen einer Aufgabe

Taskplaner kann eine Aufgabe nach dem Auslösen eines Triggers mehrmals ausführen. Zu diesem Grund definiert der Trigger ein Wiederholungsmuster, Taskplaner, wie lange der Task wiederholt werden soll und wie lange zwischen jeder Aufgabenwiederholung ein Zeitintervall liegen soll.

## <a name="repetition-pattern"></a>Wiederholungsmuster

Die folgende Abbildung zeigt ein Wiederholungsmuster mit einer Dauer von 60 Minuten und einem Intervall von 25 Minuten. Beachten Sie, dass Taskplaner in diesem Fall die Aufgabe bei Auslösung des Triggers nach 25 Minuten erneut ausführen und die Aufgabe dann nach 50 Minuten erneut ausführen kann. Dies hängt von der Einstellung der [**StopAtDurationEnd-Eigenschaft von IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) für Skripts) ab. Wenn die **StopAtDurationEnd-Eigenschaft** auf True festgelegt ist, Taskplaner die letzte Instanz der Aufgabe beendet, wenn sie nach 60 Minuten noch ausgeführt wird. Wenn die **StopAtDurationEnd-Eigenschaft** auf False festgelegt ist, wird die letzte Instanz der Aufgabe unabhängig von der Dauer ausgeführt.

![Triggerwiederholungsmuster](images/repetition-pattern.png)

Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird die Aufgabe fünfmal gestartet. Die fünf Wiederholungen können nach folgendem Muster definiert werden:

1.  Eine Aufgabe beginnt am Anfang der ersten Minute.
2.  Die nächste Aufgabe beginnt am Ende der ersten Minute.
3.  Die nächste Aufgabe beginnt am Ende der zweiten Minute.
4.  Die nächste Aufgabe beginnt am Ende der dritten Minute.
5.  Die nächste Aufgabe beginnt am Ende der vierten Minute.

**Windows Server 2003, Windows XP und Windows 2000:** Wenn Sie eine Aufgabe registrieren, die einen Trigger mit einem Wiederholungsintervall von einer Minute und einer Wiederholungsdauer von vier Minuten enthält, wird die Aufgabe viermal gestartet.

## <a name="objects-interfaces-and-xml-elements"></a>Objekte, Schnittstellen und XML-Elemente

Für die Skriptentwicklung wird das Wiederholungsmuster mithilfe des [**RepetitionPattern-Objekts**](repetitionpattern.md) definiert.

Für die C++-Entwicklung wird das Wiederholungsmuster durch die [**IRepetitionPattern-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) definiert.

Beim Lesen oder Schreiben von XML für eine Aufgabe wird das Wiederholungsmuster im [**Wiederholungselement**](taskschedulerschema-repetition-triggerbasetype-element.md) angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabentrigger](task-triggers.md)
</dt> </dl>

 

 




