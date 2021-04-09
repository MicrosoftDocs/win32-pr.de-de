---
description: Mit der Windows-Energie Verwaltung können Benutzer sofort auf eine Schaltfläche oder einen Schlüssel zugreifen.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows-Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abb3a040f8da8e2deb242a2aa607a9448d31c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865064"
---
# <a name="windows-power-management"></a>Windows-Energie Verwaltung

Mit der Windows-Energie Verwaltung können Benutzer sofort auf eine Schaltfläche oder einen Schlüssel zugreifen. Außerdem wird sichergestellt, dass alle Elemente der System – Anwendungen, Geräte und Benutzeroberflächen – von den umfangreichen Verbesserungen bei der Energie Verwaltungs Technologie und den Funktionen profitieren können.

Das Windows-Betriebssystem verwendet die Energie Verwaltungs Hardware, um den Computer in einen Energiesparmodus zu versetzen *, anstatt ihn* vollständig herunterzufahren, damit das System schnell wieder funktionsfähig ist. Das Betriebssystem wechselt automatisch in den Standbymodus, wenn sich der Computer im Leerlauf befindet oder wenn der Benutzer eine Schaltfläche drückt, um anzugeben, dass die aktuelle Arbeitssitzung vorbei ist. Für den Benutzer scheint das System deaktiviert zu sein. Im Standbymodus führt der Prozessor des Computers keinen Code aus, und es wird keine Arbeit für den Benutzer ausgeführt. Allerdings können Ereignisse im System sowohl von Hardware Geräten als auch von der Echtzeit-Uhr aktiviert werden, damit das System den Ruhezustand verlässt (d. h. "reaktivieren") und schnell zum Arbeitszustand zurückkehrt.

Wenn sich der Computer im Standbymodus befindet, muss die Computer Hardware, das System und die Anwendungen, die auf dem Computer ausgeführt werden, sofort auf den Strom Switch, die Kommunikations Ereignisse und andere Aktionen reagieren können. Wenn alle Anwendungen Energie Zustandsübergänge ordnungsgemäß verarbeiten, wird der Benutzer ein eleganteres und integriertes System betrachten. Anwendungen, die diese Übergänge nicht verarbeiten, können fehlschlagen, wenn die Stromversorgung ausgeschaltet und dann aktiviert wird, weil Daten verloren gehen oder eine Abhängigkeit von einem Gerät entfernt wurde, das möglicherweise entfernt wurde.

Im folgenden sind die Vorteile der Windows-Energie Verwaltung aufgeführt:

-   Beseitigt Verzögerungen beim Starten und Herunterfahren. Der Computer muss keinen vollständigen Systemstart ausführen, wenn der Standbymodus beendet oder ein vollständiges System heruntergefahren wird, wenn der Benutzer den Ruhezustand initiiert.
-   Ermöglicht das Ausführen automatisierter Tasks, während sich der Computer im Ruhezustand befindet. Der Taskplaner ermöglicht dem Benutzer das Planen der Ausführung von Anwendungen. geplante Ereignisse können auch dann ausgeführt werden, wenn sich das System im Ruhezustand befindet. Der Taskplaner verwendet [ausnutzbare Timer](/windows/desktop/Sync/waitable-timer-objects) , um sicherzustellen, dass das System bereit ist, wenn die Ausführung der Anwendung geplant ist. Weitere Informationen finden Sie in der Hilfedatei, die im Taskplaner enthalten ist.
-   Aktiviert die Geräte basierte Energie Verwaltung. Geräte, die nicht verwendet werden, können Energie sparen, indem Sie in den Ruhezustand wechseln.
-   Verbesserung der Energieeffizienz Die Energieeffizienz ist auf tragbaren Computern besonders wichtig. Die Reduzierung des System Stromverbrauchs wird direkt in niedrigere Stromkosten und eine längere Akku Lebensdauer übersetzt.
-   Ermöglicht Benutzern das Erstellen von [Energie Schemas](power-schemes.md), das Festlegen von Alarmen und das Angeben von Akku Optionen über die Anwendung Energieoptionen in der Systemsteuerung. Das Betriebssystem koordiniert alle Energie Verwaltungsaktivitäten basierend auf den Energierichtlinien Einstellungen. Weitere Informationen finden Sie in der Hilfedatei, die in der Power Options-Anwendung enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> <dt>

[Aufgabenplanung](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
