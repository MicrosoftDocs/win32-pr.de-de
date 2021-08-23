---
title: Out-of-Context-Hookfunktionen
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: Weitere Informationen finden Sie unter Out-of-Context Hook Functions (Hookfunktionen ohne Kontext).
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e41e9a6bba1f705c3c5dc8781b2663be22086955f5dee45f07022504d0ccbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133743"
---
# <a name="out-of-context-hook-functions"></a>Out-of-Context-Hookfunktionen

In der folgenden Liste werden die wichtigsten Aspekte von Hookfunktionen ohne Kontext beschrieben:

-   Hookfunktionen außerhalb des Kontexts befinden sich im Adressraum des Clients, unabhängig davon, ob sie sich im Codekörper oder in einer DLL befinden.
-   Hookfunktionen ohne Kontext werden nicht dem Adressraum des Servers zugeordnet.
-   Wenn ein Ereignis ausgelöst wird, werden die Parameter für die Hookfunktion über Prozessgrenzen hinweg gemarshallt.
-   Hookfunktionen ohne Kontext sind aufgrund von Marshalling deutlich langsamer als Kontexthookfunktionen.
-   Das System reiht die Ereignisbenachrichtigungen in die Warteschlange ein, sodass sie asynchron eintreffen (aufgrund der Zeit, die zum Ausführen des Marshallings erforderlich ist).

Obwohl die Ereignisbenachrichtigungen asynchron sind, stellt Microsoft Active Accessibility sicher, dass die Rückruffunktion alle Ereignisse in der Reihenfolge empfängt, in der sie generiert werden.

Die USER-Komponente des Betriebssystems weist Arbeitsspeicher für Ereignisse zu, die von Hookfunktionen ohne Kontext verarbeitet werden. Der Arbeitsspeicher wird frei, wenn die Hookfunktionen zurückgeben. Wenn eine Hookfunktion Ereignisse nicht schnell genug verarbeiten kann, werden BENUTZERressourcen gesenkt, was letztendlich zu einem Fehler oder extrem langsamen Antwortzeiten führt. Diese Probleme können auftreten, wenn:

-   Ereignisse werden sehr schnell ausgelöst.
-   Das System ist langsam.
-   Die Hookfunktion verarbeitet Ereignisse langsam.
-   Der Client wird auf Windows 9x ausgeführt.

 

 




