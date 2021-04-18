---
description: Client-Side Fehler
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: Client-Side Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef309858d1527fdcabe0f487de87df19d20635c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344948"
---
# <a name="client-side-errors"></a>Client-Side Fehler

Client seitige Fehler werden ähnlich wie serverseitige Fehler behandelt. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) können eine Nachricht in die Ziel Warteschlange verschieben, wenn Sie z. b. nicht vom Client zum Server verschoben werden kann. In diesem Fall wird die Nachricht in die Client seitige Warteschlange für unzustellbare Nachrichten verschoben.

Der Dienst "com+-Warteschlangen Komponenten" überwacht die Warteschlange für unzustellbare Meldungen Wenn Nachrichten verschoben wurden, erstellt der in der Warteschlange befindliche Komponenten Dienst eine Instanz der Ausnahme Klasse und ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)anzufordern. Wenn dies erfolgreich ist, ruft der Monitor für die Warteschlange für unzustellbare Nachrichten [**IPlaybackControl:: FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)auf.

Das-Objekt kann einige Maßnahmen ergreifen, um die Auswirkungen einer vorherigen Transaktion umzukehren. Wenn bei der Wiedergabe ein Commit ausgeführt wird, wird die Nachricht aus der Warteschlange für unzustellbare Nachrichten des Wenn die Wiedergabe fehlschlägt oder die erforderliche CLSID und Schnittstelle nicht verfügbar sind, verbleibt die Nachricht in der Warteschlange für unzustellbare Nachrichten.

Wenn Sie in den oben beschriebenen Prozess eingreifen müssen oder eine nicht verarbeitbare Nachricht aus der letzten ruhenden Warteschlange verschieben müssen, verwenden Sie das Hilfsprogramm Nachrichten Verschiebung. Weitere Informationen zum Hilfsprogramm für den Nachrichten Verschiebungsvorgang finden Sie unter [Behandeln von Fehlern](handling-errors-in-queued-components.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Persistente Client-Side Fehler](persistent-client-side-failures.md)
</dt> <dt>

[Server seitige Fehler](server-side-errors.md)
</dt> </dl>

 

 
