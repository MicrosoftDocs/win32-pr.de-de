---
description: Komponenten Fehler in der Warteschlange
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Komponenten Fehler in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346447"
---
# <a name="queued-components-errors"></a>Komponenten Fehler in der Warteschlange

Wenn ein Aufruf an eine in der Warteschlange befindliche Komponente fehlschlägt, weil Sie entweder nicht an den Server übertragen werden konnte (ein Client seitiger Fehler) oder weil Sie beim Eintreffen (serverseitiger Fehler) nicht ausgeführt werden konnte, wird die entsprechende [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Meldung als nicht verarbeitbare *Nachricht* bezeichnet.

Der Dienst "com+-Warteschlangen Komponenten" verarbeitet nicht verarbeitbare Nachrichten mithilfe einer Reihe von Wiederholungs Warteschlangen. Nach mehreren Wiederholungs versuchen wird die Nachricht in eine letzte Warteschlange verschoben. Nachrichten bleiben in der ruhenden Warteschlange, bis Sie manuell mithilfe des Nachrichten verschiebungshilfsprogramms in der Warteschlange eingereiht werden. Weitere Informationen zur Verwendung des Nachrichten Verschiebungsvorgangs finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).

Ausführliche Beschreibungen der Ereignis Sequenz, die für verschiedene Arten von Fehlern auftritt, finden Sie in den Themen, die in der folgenden Tabelle beschrieben werden.



| Thema                                                                             | BESCHREIBUNG                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Server seitige Fehler](server-side-errors.md)<br/>                           | Beschreibt ausführlich die Antwort des Dienstanbieter der com+-Warteschlange auf einen serverseitigen Fehler.<br/>             |
| [Client seitige Fehler](client-side-errors.md)<br/>                           | Beschreibt ausführlich die Antwort des Dienstanbieter der com+-Warteschlange auf einen Client seitigen Fehler.<br/>             |
| [Persistente Client-Side Fehler](persistent-client-side-failures.md)<br/> | Beschreibt im Detail die Antwort des com+-Dienstanbieter für die Warteschlange auf wiederholte Client seitige Fehler.<br/> |



 

 

 




