---
title: Die Desktop-App-Funktionalität ist eingeschränkt, wenn sie nicht im Fenstermodus ausgeführt wird.
description: In Windows 10 werden Windows-Apps standardmäßig nicht mehr im Vollbildmodus angezeigt. Stattdessen werden sie in einem Fenster angezeigt, und Vorgänge wie Minimieren, Wiederherstellen, Maximieren, Ändern der Größe (und alle anderen Vorgänge, die Sie immer für ein anderes klassisches Windows-Anwendungsfenster durchgeführt haben) sind jetzt möglich.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79b7db00eb2bab422adaa22d798c373ece7adf061faff43a67e13ee07528a2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028818"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>Die Desktop-App-Funktionalität ist eingeschränkt, wenn sie nicht im Fenstermodus ausgeführt wird.

In Windows 10 werden Windows-Apps standardmäßig nicht mehr im Vollbildmodus angezeigt. Stattdessen werden sie in einem Fenster angezeigt, und Vorgänge wie Minimieren, Wiederherstellen, Maximieren, Ändern der Größe (und alle anderen Vorgänge, die Sie immer für ein anderes klassisches Windows-Anwendungsfenster durchgeführt haben) sind jetzt möglich.

## <a name="manifestations"></a>Manifestationen

Die deutlichste Änderung besteht jetzt in der Größenänderung, die nicht nur die Größe des Bildschirms bzw. der Bildschirmhöhe ist. Ein Benutzer kann die Größe des App-Fensters kontinuierlich an seine Eigenen ändern (bis hin zur minimalen Fenstergröße der App). Dies ist anders als Windows 8.0 oder Windows 8.1, bei dem das Ändern der Fenstergröße eine diskrete Aktion war (Benutzer haben die Größe einer Miniaturansicht des Fensters geändert, wodurch sich die Größe des Fensters geändert hat, nachdem der Benutzer die Aktion abgeschlossen hat). Wenn der Benutzer das Fenster stattdessen durch die untere Ecke (oder eine andere Rahmenposition) zieht, handelt es sich um eine kontinuierliche Größenänderung, und die App empfängt Nachrichten zur Größenänderung in einer Zeile, anstatt die Größe zu ändern.

## <a name="mitigations"></a>Gegenmaßnahmen

So verringern Sie dies für Windows 8.0- und 8.1-Apps:

-   Wenn die erwartete Funktion innerhalb der App-Funktionalität nicht mehr unterstützt wird, besteht die Entschärfung durch den Benutzer in der Anwendung im Vollbildmodus (mithilfe der Schaltfläche "Vollbildschaltfläche" in der oberen rechten Ecke der Titelleiste).
-   Wenn das Starten der App davon abhing, dass sie nicht wie erwartet geöffnet wird, sollte der Benutzer weiterhin in den Tablet-Modus wechseln können, um zu erzwingen, dass die App ohne Benutzereingriff im Vollbildmodus gestartet wird.

Die beste Möglichkeit, dies zu behandeln, besteht in der Änderung der App, um sich der Tatsache bewusst zu sein, dass sie auf nicht überwachte Orte/Höhen dimensioniert werden kann (d. h. keine hartcodierte Tabelle mit Höhe/Breite haben und nur diese erwarten oder auch hartcodierte Verhältnisse erwarten). App-Entwickler sollten davon ausgehen, dass während der Größenvergrößerung der App direkt nach dem Senden der aktuellen Größenvergrößerungsnachricht eine weitere Nachricht zur Größenvergrößerung angezeigt werden kann. Daher ist es möglich, dass die App beim Starten von Animationen während der Größenvergrößerung direkt danach eine weitere Nachricht zur Größenvergrößerung erhält (daher ist es wichtig sicherzustellen, dass diese Art von Situation nicht zu einem Absturz der App führt).

 

 




