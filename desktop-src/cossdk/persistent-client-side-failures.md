---
description: Persistente Client-Side Fehler
ms.assetid: f991db71-8319-414d-8a25-2d02bc7c8b51
title: Persistente Client-Side Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d303e712257d62e4ae42497cb4463e782cfbb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393106"
---
# <a name="persistent-client-side-failures"></a>Persistente Client-Side Fehler

In einigen Fällen kann [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) eine Nachricht in die Ziel Warteschlange verschieben. Wenn z. b. die Warteschlangen Zugriffs Steuerung nicht zulässt, dass die Nachricht vom Client auf den Server verschoben wird, wird die problematische Nachricht in die Client seitige Warteschlange für unzustellbare Nachrichten verschoben. In diesem Fall kann der in der Warteschlange befindliche Komponenten Dienst eine Ausnahme Klasse einer Komponente zugeordnet werden. Um die Ausnahme Klasse der Komponente zuzuordnen, verwenden Sie die Registerkarte **erweitert** auf der Seite Komponenteneigenschaften des Verwaltungs Tools Komponenten Dienste. Sie können die Ausnahme Klasse auch Programm gesteuert zuordnen, indem Sie das Attribut "exceptionclass Catalog Component" der com+-Verwaltungsfunktionen verwenden.

Die Exception-Klasse wird entweder als ProgID oder als CLSID einer Komponente definiert, die [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)implementiert. Der Dienst für in der Warteschlange befindliche Komponenten verfügt über eine Warteschlange für unzustellbare Nachrichten, die die XACT-Warteschlange Wenn eine Nachricht in der Warteschlange vorhanden ist, instanziiert der Monitor für unzustellbare Nachrichten den Ausnahmehandler, der der Zielkomponente zugeordnet ist, und ruft [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)auf, was darauf hinweist, dass ein Client seitiger, nicht BEHEB barer Fehler aufgetreten ist.

Zusätzlich zu [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)sollte der Ausnahmehandler denselben Satz von Schnittstellen implementieren wie die Serverkomponente, für die er Ausnahmen behandelt. Wenn [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) aufgerufen wird, gibt die Laufzeit der in der Warteschlange befindlichen Komponenten die fehlerhafte Nachricht an den Ausnahmehandler zurück. Dies ermöglicht es dem Ausnahmehandler, ein alternatives Verhalten für Nachrichten zu implementieren, die nicht auf den Server verschoben werden können, z. –. durch das Erstellen einer kompensierenden Transaktion.

Wenn der Ausnahmehandler alle wiedergegebenen Methodenaufrufe abschließt, wird die Nachricht aus der Warteschlange für unzustellbare Nachrichten von XACT entfernt und verworfen. Wenn der Ausnahmehandler jedoch die Nachricht abbricht, indem er einen Fehlerstatus von einem der Methodenaufrufe zurückgibt, wird die Nachricht an die XACT-Warteschlange für unzustellbare Nachrichten zurückgegeben. Die folgende Abfolge von Ereignissen zeigt, wie Client seitige Ausnahmen behandelt werden:

1.  Message Queuing kann keine Nachricht an den Server übermitteln und die Nachricht in die Warteschlange für unzustellbare Nachrichten von XACT versetzen.
2.  Der Warteschlangen Listener für unzustellbare Nachrichten (dlql) sucht eine Nachricht in der Warteschlange für unzustellbare Nachrichten.
3.  Der dlql Ruft die CLSID der Zielkomponente aus der Nachricht ab und überprüft, ob eine Ausnahme Klasse besteht.
4.  Dlql instanziiert die Exception-Klasse.
5.  Die dlql-Abfragen für [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol) für die Exception-Klasse.
6.  Dlql Ruft die [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry) -Methode in der Ausnahme Klasse auf.
7.  Dlql gibt alle Eigenschafts-und Methodenaufrufe von der Nachricht an die Exception-Klasse zurück.
8.  Der dlql löscht die Nachricht, wenn der Ausnahmehandler die Transaktion erfolgreich abgeschlossen hat. Der Ausnahmehandler gibt möglicherweise [**IObjectContext:: abtabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)aus, und die Nachricht verbleibt in der Warteschlange für unzustellbare Nachrichten.

Wenn einer der vorangegangenen Schritte fehlschlägt, wird die Nachricht in der Warteschlange für unzustellbare Nachrichten von XACT belassen.

Beim Start liest dlql jede Nachricht in der Message Queuing Transaktions Warteschlange für unzustellbare Nachrichten und instanziiert die Exception-Klasse für jede Nachricht in der Warteschlange. Nach dem Durchlaufen der Warteschlange wartet Sie auf neue Nachrichten. Anschließend werden alle neuen Warteschlangen Nachrichten für unzustellbare Nachrichten verarbeitet, sobald sie eintreffen.

Wenn Sie in den hier beschriebenen Prozess eingreifen müssen oder eine nicht verarbeitbare Nachricht aus der letzten ruhenden Warteschlange verschieben müssen, verwenden Sie das Hilfsprogramm Nachrichten Verschiebung. Weitere Informationen zum Hilfsprogramm für den Nachrichten Verschiebungsvorgang finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Client seitige Fehler](client-side-errors.md)
</dt> <dt>

[Server seitige Fehler](server-side-errors.md)
</dt> </dl>

 

 



