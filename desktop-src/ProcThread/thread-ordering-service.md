---
description: Der Thread Bestell Dienst steuert die Ausführung von mindestens einem Clientthread. Dadurch wird sichergestellt, dass jeder Client Thread innerhalb des angegebenen Zeitraums und in relativer Reihenfolge einmal ausgeführt wird.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Thread Bestell Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350220"
---
# <a name="thread-ordering-service"></a>Thread Bestell Dienst

Der *Thread Bestell Dienst* steuert die Ausführung von mindestens einem Clientthread. Dadurch wird sichergestellt, dass jeder Client Thread innerhalb des angegebenen Zeitraums und in relativer Reihenfolge einmal ausgeführt wird.

**Windows Server 2003 und Windows XP:** Der Thread Bestell Dienst ist ab Windows Vista und Windows Server 2008 verfügbar.

Der Thread Bestell Dienst ist standardmäßig deaktiviert und muss vom Benutzer gestartet werden. Während der Thread Bestell Dienst ausgeführt wird, wird er alle 5 Sekunden aktiviert, um zu überprüfen, ob eine neue Anforderung vorliegt, auch wenn sich das System im Leerlauf befindet. Dadurch wird verhindert, dass das System länger als 5 Sekunden im Ruhezustand ist, was dazu führt, dass das System mehr Leistung beansprucht. Wenn die Energieeffizienz für die Anwendung wichtig ist, ist es besser, den Thread Bestell Dienst zu verwenden und stattdessen zuzulassen, dass der Systemplaner die Ausführung von Threads verwaltet.

Jeder Client Thread gehört zu einer *Thread Reihenfolge Gruppe*. Der über *geordnete Thread* erstellt eine oder mehrere Thread Sortiergruppen, indem er die [**avrtcreatethleorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) -Funktion aufrufen. Der übergeordnete Thread verwendet diese Funktion, um den Zeitraum für die Thread Reihenfolge Gruppe und ein Timeout Intervall anzugeben.

Zusätzliche Clientthreads wenden die [**avrtjointhreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) -Funktion an, um einer vorhandenen Thread Reihenfolge Gruppe beizutreten. Diese Threads geben an, ob es sich um einen Vorgänger oder einen Nachfolger für den übergeordneten Thread in der Ausführungsreihenfolge handelt. Jeder Client Thread wird erwartet, dass jeder Zeitraum eine bestimmte Verarbeitungs Menge ausgeführt wird. Alle Threads innerhalb der Gruppe sollten ihre Ausführung innerhalb des Zeitraums zuzüglich des Timeout Intervalls vervollständigen.

Die Threads einer Thread Sortier Gruppe schließen ihren Verarbeitungs Code in eine Schleife ein, die von der [**avrtwaitonthreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) -Funktion gesteuert wird. Zuerst werden die Vorgänger Threads nacheinander in der Reihenfolge ausgeführt, in der Sie der Gruppe beigetreten sind, während die übergeordneten und die Nachfolger Threads bei ihren Aufrufen von **avrtwaitonthreadorderinggroup** blockiert werden. Wenn jeder Vorgänger Thread seine Verarbeitung abgeschlossen hat, wird die Steuerung der Ausführung an den Anfang der Verarbeitungs Schleife zurückgegeben, und der Thread ruft **avrtwaitonthreadorderinggroup** erneut auf, um bis zum nächsten Ende zu blockieren. Nachdem alle Vorgänger Threads diese Funktion aufgerufen haben, kann der Thread Bestell Dienst den übergeordneten Thread planen. Wenn der übergeordnete Thread schließlich seine Verarbeitung beendet und **avrtwaitonthreadorderinggroup** erneut aufruft, kann der Thread Sortier Dienst die Nachfolger Threads nacheinander in der Reihenfolge planen, in der Sie der Gruppe beigetreten sind. Wenn alle Threads ihre Ausführung vor dem Ende eines Zeitraums abgeschlossen haben, warten alle Threads, bis der restliche Zeitraum verstrichen ist, bevor Sie erneut ausgeführt werden.

Wenn der Client nicht mehr als Teil der Thread Reihenfolge Gruppe ausgeführt werden muss, wird die [**avrtleavethreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) -Funktion aufgerufen, um sich selbst aus der Gruppe zu entfernen. Beachten Sie, dass der übergeordnete Thread sich nicht selbst aus einer Thread Reihenfolge Gruppe entfernen darf. Wenn ein Thread seine Ausführung vor dem Zeitraum und dem Timeout Intervall nicht vollständig abschließt, wird er aus der Gruppe gelöscht.

Der übergeordnete Thread ruft die [**avrtdeletethreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) -Funktion auf, um die Thread Sortier Gruppe zu löschen. Die Thread Reihenfolge Gruppe wird ebenfalls zerstört, wenn der übergeordnete Thread seine Ausführung vor dem Zeitraum und dem Timeout Intervall nicht vollständig beendet. Wenn die Thread Sortier Gruppe zerstört wird, tritt bei allen Aufrufen von [**avrtwaitonthreadorderinggroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) aus Threads dieser Gruppe ein Fehler oder ein Timeout auf.

 

 



