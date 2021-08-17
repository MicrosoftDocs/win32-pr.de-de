---
description: fehler Client-Side
ms.assetid: 95fb2ef1-eec2-4c74-891a-617450098160
title: fehler Client-Side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c27c73cd2be39d98c881021e1a042f15dc623766af0d52a578c6cd49c30e0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129362"
---
# <a name="client-side-errors"></a>fehler Client-Side

Clientseitige Fehler werden in einer Weise behandelt, die serverseitigen Ausfällen ähnelt. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) können eine Nachricht in die Zielwarteschlange verschieben, wenn die Nachricht z. B. nicht vom Client auf den Server verschoben werden kann. In diesem Fall wird die Nachricht in die clientseitige Warteschlange für unzugestellte Nachrichten verschoben.

Der COM+-Komponentendienst in der Warteschlange überwacht die Warteschlange für un tote Briefe. Wenn Nachrichten verschoben wurden, erstellt der Komponentendienst in der Warteschlange eine Instanz der Ausnahmeklasse und ruft [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um [**IPlaybackControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iplaybackcontrol)anzufordern. Wenn dies erfolgreich ist, ruft der Monitor für die Warteschlange für ungebundene Nachrichten [**IPlaybackControl::FinalClientRetry**](/windows/desktop/api/ComSvcs/nf-comsvcs-iplaybackcontrol-finalclientretry)auf.

Das -Objekt kann einige Maßnahmen ergreifen, um die Auswirkung einer vorherigen Transaktion umzukehren. Wenn der Wiedergabecommit erfolgt, wird die Nachricht aus der Xact-Warteschlange für ungenaue Nachrichten entfernt. Wenn die Wiedergabe fehlschlägt oder die erforderliche CLSID und Schnittstelle nicht verfügbar sind, verbleibt die Nachricht in der Xact-Warteschlange für ungenaue Nachrichten.

Wenn Sie in den oben beschriebenen Prozess eingreifen müssen oder eine nicht verarbeitete Nachricht aus der endgültigen Ruhewarteschlange verschieben müssen, verwenden Sie das Hilfsprogramm zum Verschieben von Nachrichten. Weitere Informationen zum Hilfsprogramm zum Verschieben von Nachrichten finden Sie unter [Behandeln von Fehlern.](handling-errors-in-queued-components.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Persistente Client-Side Fehler](persistent-client-side-failures.md)
</dt> <dt>

[Serverseitige Fehler](server-side-errors.md)
</dt> </dl>

 

 
