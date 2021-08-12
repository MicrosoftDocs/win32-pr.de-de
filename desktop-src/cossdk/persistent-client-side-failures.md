---
description: Persistente Client-Side Fehler
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Persistente Client-Side Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e832ec8339c33263600a1657b8d29ef2d2aecf4ceb3e000666f9db5776b3ac13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305773"
---
# <a name="persistent-client-side-failures"></a>Persistente Client-Side Fehler

In einigen Fällen kann [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) Nachricht in die Zielwarteschlange verschieben. Wenn die Warteschlangenzugriffssteuerungen beispielsweise nicht zulassen, dass die Nachricht vom Client auf den Server verschoben wird, wird die anstärmende Nachricht in die clientseitige Warteschlange für unbende Nachrichten verschoben. In diesem Fall lässt der COM+-Dienst für komponenten in der Warteschlange zu, dass eine Ausnahmeklasse einer Komponente zugeordnet werden kann. Um die Ausnahmeklasse der Komponente zu zuordnen, verwenden Sie die **Registerkarte Erweitert** auf der Eigenschaftenseite der Komponenten des Verwaltungstool Komponentendienste. Sie können die Ausnahmeklasse auch programmgesteuert zuordnen, indem Sie das ExceptionClass-Katalogkomponentenattribut der COM+-Verwaltungsfunktionen verwenden.

Die Ausnahmeklasse wird entweder als ProgID oder CLSID einer Komponente definiert, die [**IPlaybackControl implementieren.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) Der Dienst für Komponenten in der Warteschlange verfügt über einen Monitor für Warteschlangen für unbierte Nachrichten, der die Xact-Warteschlange für unbierte Nachrichten überprüft. Wenn eine Nachricht in der Warteschlange enthalten ist, instanziiert der Warteschlangenmonitor für unzustellbare Nachrichten den Ausnahmehandler, der der Zielkomponente zugeordnet ist, und ruft [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)auf, was darauf hinweist, dass ein clientseitiger, nicht behebbarer Fehler aufgetreten ist.

Zusätzlich zu [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)sollte der Ausnahmehandler denselben Satz von Schnittstellen implementieren wie die Serverkomponente, für die er Ausnahmen verarbeitet. Wenn [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) aufgerufen wird, gibt die Laufzeit der Komponenten in der Warteschlange die fehlerhafte Meldung an den Ausnahmehandler zurück. Dadurch kann der Ausnahmehandler ein alternatives Verhalten für Nachrichten implementieren, die nicht auf den Server verschoben werden können, z. B. durch Generieren einer kompensierenden Transaktion.

Wenn der Ausnahmehandler alle zurückgespielten Methodenaufrufe ab schließt, wird die Nachricht aus der Xact-Warteschlange für unnachrichtierte Nachrichten entfernt und verworfen. Wenn der Ausnahmehandler die Nachricht jedoch abbricht, indem er einen Fehlerstatus von einem der Methodenaufrufe zurücksendet, wird die Nachricht an die Xact-Warteschlange für unbende Nachrichten zurückgegeben. Die folgende Ereignissequenz zeigt, wie clientseitige Ausnahmen behandelt werden:

1.  Message Queuing kann keine Nachricht an den Server senden und die Nachricht in die Xact-Warteschlange für unbnachrichtig stellen.
2.  Der Warteschlangenlistener für unbingte Nachrichten (DEAD LETTER Queue Listener, DLQL) findet eine Nachricht in der Xact-Warteschlange für unblinkte Nachrichten.
3.  Die DLQL ruft die ZIELkomponenten-CLSID aus der Nachricht ab und sucht nach einer Ausnahmeklasse.
4.  Die DLQL instanziiert die Ausnahmeklasse.
5.  Die DLQL fragt [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) für die Ausnahmeklasse ab.
6.  Die DLQL ruft die [**IPlaybackControl::FinalClientRetry-Methode**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) in der Ausnahmeklasse auf.
7.  Die DLQL gibt alle Eigenschaften- und Methodenaufrufe aus der Nachricht an die Ausnahmeklasse zurück.
8.  Die DLQL löscht die Meldung, wenn der Ausnahmehandler die Transaktion erfolgreich abgeschlossen hat. Der Ausnahmehandler gibt möglicherweise [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)aus, und die Nachricht verbleibt in der Warteschlange für unnachrichtliche Nachrichten.

Wenn einer der oben genannten Schritte fehlschlägt, wird die Nachricht in der Xact-Warteschlange für unbende Nachrichten zurückgelassen.

Beim Starten liest die DLQL jede Nachricht in der Message Queuing transaktionalen Warteschlange für unnachrichtliche Nachrichten und instanziiert die Ausnahmeklasse für jede Nachricht der Komponenten in der Warteschlange. Nach dem Passieren der Warteschlange wartet es auf neue Nachrichten. Anschließend verarbeitet er jede neue Warteschlangennachricht für unnachrichtische Nachrichten, sobald sie eintrifft.

Wenn Sie in den hier beschriebenen Prozess eingreifen müssen oder wenn Sie eine nicht verfeinerte Nachricht aus der endgültigen Ruhewarteschlange verschieben müssen, verwenden Sie das Nachrichten-Mover-Hilfsprogramm. Weitere Informationen zum Nachrichten-Mover-Hilfsprogramm finden Sie unter [Behandeln von Fehlern.](handling-errors-in-queued-components.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientseitige Fehler](client-side-errors.md)
</dt> <dt>

[Serverseitige Fehler](server-side-errors.md)
</dt> </dl>

 

 



