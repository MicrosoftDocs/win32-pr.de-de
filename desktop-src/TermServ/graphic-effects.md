---
title: Grafische Effekte
description: Eine Liste der Funktionen, die beim Ausführen als Remote Sitzung in einer Remotedesktopdienste Umgebung deaktiviert werden sollten.
ms.assetid: 229a1058-acba-4d4b-ba52-824dda4f91a5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f850b8bac5d084419b1f15c2e0efe619da5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947759"
---
# <a name="graphic-effects"></a>Grafische Effekte

Ein Remotedesktopdienste Server verwendet das Netzwerk, um alle Eingaben und Ausgaben an seine Client Terminals zu übertragen. Folglich können Anwendungen, die eine übermäßige Nutzung von grafischen Effekten machen, die Leistung für alle Remotedesktopdienste Clients beeinträchtigen, indem Sie das Netzwerk verlangsamen. Außerdem kann die langsamere Übertragungsgeschwindigkeit über ein Netzwerk dazu führen, dass diese besonderen Effekte weniger ansprechend erscheinen als in einer lokalen Video Umgebung.

Insbesondere sollten Anwendungen die Verwendung der folgenden Features deaktivieren oder minimieren, wenn Sie in einer Remotedesktopdienste Umgebung als Remote Sitzung ausgeführt werden:

-   Begrüßungs Bildschirme – grafische Produkt-oder Unternehmensinformationen, die angezeigt werden, während eine Anwendung gestartet wird. Das übertragen eines Begrüßungs Bildschirms an einen Remotedesktopverbindung-Client (RDC) beansprucht zusätzliche Netzwerkbandbreite und zwingt den Benutzer zu warten, bevor er auf die Anwendung zugreift.
-   Animationen, die CPU-Zeit und Netzwerkbandbreite verbrauchen.
-   Leiten Sie die Eingabe oder Ausgabe an den Bildschirm weiter. Wenn Sie Bits vom Bildschirm lesen müssen, warten Sie eine separate Kopie des Video Puffers auf dem Bildschirm ab. Wenn Sie eine aufwändige Bildschirmausgabe ausführen müssen – z. b. mehrere Bilder zu überlagern, um Sie auf einem abschließenden zusammengesetzten Bildschirm zu erreichen – tun Sie dies in einem Offscreen-Puffer, und senden Sie die Ergebnisse dann an den eigentlichen Video Puffer.

Weitere Informationen zum Erkennen von Remote Sitzungen finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md).

Verwenden Sie nach Möglichkeit die Microsoft Foundation Class-Bibliothek oder MFC. Der MFC verfügt über eine lange Liste von bewährten Klassen, um eine Vielzahl von Aufgaben auszuführen. Die meisten dieser Klassen funktionieren gut in einer Remotedesktopdienste Umgebung – in der Regel viel besser als neu entwickelte Lösungen. Ein gutes Beispiel ist die-Klasse, die kontextbezogenen Hilfe Text bereitstellt – Hilfetext, der auf dem Bildschirm angezeigt wird, wenn der Mauszeiger über eine Schaltfläche oder ein Menü Element bewegt wird. Wenn eine Anwendung die MFC-Implementierung verwendet, um diese Funktion bereitzustellen, funktioniert Sie auf dem Desktop System in angemessener Weise. Wenn die Anwendung diese Funktion jedoch mithilfe von Dialogfeldern oder einem alternativen Ansatz implementiert, funktioniert das Endergebnis möglicherweise nicht auch in einer Remotedesktopdienste Umgebung.

 

 




