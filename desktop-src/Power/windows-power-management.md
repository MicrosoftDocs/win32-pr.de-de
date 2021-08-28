---
description: Windows Energieverwaltung macht Computer für Benutzer sofort über eine Schaltfläche oder einen Schlüssel zugänglich.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows Energieverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7335b521b22b762468d2b542ea3c4fdbfcacb798860d4997f4a512d8135bcf46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032720"
---
# <a name="windows-power-management"></a>Windows Energieverwaltung

Windows Energieverwaltung macht Computer für Benutzer sofort über eine Schaltfläche oder einen Schlüssel zugänglich. Außerdem wird sichergestellt, dass alle Elemente des Systems – Anwendungen, Geräte und Benutzeroberfläche – von den enormen Verbesserungen der Energieverwaltungstechnologie und -funktionen profitieren können.

Das Windows-Betriebssystem verwendet Energieverwaltungshardware, um den Computer  in einen Niedrigen-Energie-Ruhezustand zu bringen, anstatt vollständig heruntergefahren zu werden, sodass das System schnell wieder arbeiten kann. Das Betriebssystem geht automatisch in den Ruhezustand über, wenn sich der Computer im Leerlauf befindet oder wenn der Benutzer eine Schaltfläche drückt, um anzuzeigen, dass die aktuelle Arbeitssitzung beendet ist. Für den Benutzer scheint das System deaktiviert zu sein. Im Ruhezustand wird vom Prozessor des Computers kein Code ausgeführt, und es wird keine Arbeit für den Benutzer ausgeführt. Ereignisse im System können jedoch sowohl von Hardwaregeräten als auch von der Echtzeituhr aktiviert werden, um das System dazu zu bringen, den Ruhezustand (d. h. "Reaktivieren") zu beenden und schnell in den Betriebszustand zurückzukehren.

Wenn sich der Computer im Ruhezustand befindet, müssen die Computerhardware, das System und die anwendungen, die auf dem Computer ausgeführt werden, sofort auf den Netzschalter, Kommunikationsereignisse und andere Aktionen reagieren können. Wenn alle Anwendungen Energiezustandsübergänge ordnungsgemäß verarbeiten, nimmt der Benutzer ein eleganteres und integriertes System wahr. Anwendungen, die diese Übergänge nicht verarbeiten, können fehlschlagen, wenn die Stromversorgung ausgeschaltet und dann eingeschaltet wird, weil Daten verloren gehen oder eine Abhängigkeit von einem Gerät besteht, das möglicherweise entfernt wurde.

Im Folgenden finden Sie die Vorteile Windows Energieverwaltung:

-   Beseitigt Verzögerungen beim Starten und Herunterfahren. Der Computer muss beim Beenden des Ruhezustands oder beim vollständigen Herunterfahren des Systems keinen vollständigen Systemstart ausführen, wenn der Benutzer den Ruhezustand initiiert.
-   Ermöglicht die Ausführung automatisierter Aufgaben, während sich der Computer im Ruhezustand befindet. Die Taskplaner ermöglicht es dem Benutzer, die Ausführung von Anwendungen zu planen. Geplante Ereignisse können auch ausgeführt werden, wenn sich das System im Ruhezustand befindet. Der Taskplaner verwendet [wartebare Timer,](/windows/desktop/Sync/waitable-timer-objects) um sicherzustellen, dass das System bereit ist, wenn die Ausführung der Anwendung geplant ist. Weitere Informationen finden Sie in der Hilfedatei, die im Taskplaner.
-   Aktiviert die Energieverwaltung pro Gerät. Geräte, die nicht verwendet werden, können Energie sparen, indem sie in den Ruhezustand eintreten.
-   Verbessert die Energieeffizienz. Die Energieeffizienz ist auf portablen Computern besonders wichtig. Eine Reduzierung des Systemleistungsverbrauchs führt direkt zu geringeren Energiekosten und längerer Akkulaufzeit.
-   Ermöglicht Es Benutzern, Energieschemas [zu](power-schemes.md)erstellen, Alarme festzulegen und Akkuoptionen über die Energieoptionen anwendung in Systemsteuerung. Das Betriebssystem koordiniert alle Energieverwaltungsaktivitäten basierend auf den Energierichtlinieneinstellungen. Weitere Informationen finden Sie in der Hilfedatei, die in der Energieoptionen enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> <dt>

[Aufgabenplanung](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
