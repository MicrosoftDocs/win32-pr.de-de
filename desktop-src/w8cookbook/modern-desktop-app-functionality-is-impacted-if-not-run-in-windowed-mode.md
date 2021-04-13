---
title: Die Funktionalität der Desktop-App ist beeinträchtigt, wenn Sie nicht im Fenstermodus ausgeführt wird.
description: In Windows 10 sind Windows-apps nicht mehr standardmäßig voll Bild fähig – stattdessen sind Sie Fenster und Vorgänge wie das minimieren, wiederherstellen, maximieren und Ändern der Größe (und jeder andere Vorgang, den Sie immer in einem anderen klassischen Windows-Anwendungsfenster ausführen konnten) sind jetzt möglich.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388591"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>Die Funktionalität der Desktop-App ist beeinträchtigt, wenn Sie nicht im Fenstermodus ausgeführt wird.

In Windows 10 sind Windows-apps nicht mehr standardmäßig voll Bild fähig – stattdessen sind Sie Fenster und Vorgänge wie das minimieren, wiederherstellen, maximieren und Ändern der Größe (und jeder andere Vorgang, den Sie immer in einem anderen klassischen Windows-Anwendungsfenster ausführen konnten) sind jetzt möglich.

## <a name="manifestations"></a>Kundgebungen

Die auffälligste Änderung ist nun, dass Sie Größe beliebig groß machen können, die nicht nur die Größe des Bildschirms bzw. der Höhe des Bildschirms ist. Ein Benutzer kann die Größe des App-Fensters kontinuierlich anpassen (bis zur minimalen Fenstergröße der APP). Dies unterscheidet sich von Windows 8,0 oder Windows 8.1, bei dem das Ändern der Größe eines Fensters eine diskrete Aktion war (die Benutzer haben eine Miniaturansicht des Fensters geändert, wodurch sich die Größe des Fensters geändert hat, nachdem der Benutzer die Aktion committet hat). Heutzutage ist es eine kontinuierliche Größenänderung, wenn der Benutzer das Fenster in der unteren Ecke (oder an einer anderen Rahmen Position) zieht, und die APP erhält Größen Änderungs Nachrichten in einer Zeile und nicht in einer Größenänderung.

## <a name="mitigations"></a>Gegenmaßnahmen

So mindern Sie dieses Problem für Windows 8,0-und 8,1-apps:

-   Wenn die erwartete Funktion innerhalb der APP-Funktionalität beschädigt ist, besteht die Benutzer Entschärfung darin, die app in den Vollbildmodus zu versetzen (mithilfe der Schaltfläche "Vollbild wechseln" in der oberen rechten Ecke der Titelleiste).
-   Wenn die APP-Start Anleitung davon betroffen ist, dass Sie nicht erwartungsgemäß geöffnet ist, sollte der Benutzer dennoch in der Lage sein, in den Tablet-Modus zu wechseln, um zu erzwingen, dass die APP im Vollbildmodus ohne Benutzereingriff gestartet wird.

Die beste Möglichkeit, dies zu handhaben, besteht darin, die APP so zu ändern, dass Sie die Größe der Größen und Höhen von nicht überwachten Größen (d. h. nicht über eine hart codierte Tabelle mit Höhe/Breite verfügt und diese nur erwartet oder hart codierte Verhältnisse erwartet). App-Entwickler sollten davon ausgehen, dass bei der Größenänderung der App eine andere Nachricht zum Ändern der Größe direkt nach dem übermitteln der aktuellen Größenänderung auftreten kann – wenn die APP während der Größenänderung Animationen startet, kann die APP möglicherweise eine andere Nachricht zum Ändern der Größe erhalten (daher ist es wichtig sicherzustellen, dass diese Art von Situation nicht zum Absturz der APP führt).

 

 




