---
description: Eintragen einer Ressource in eine Transaktion
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Eintragen einer Ressource in eine Transaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393229"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Eintragen einer Ressource in eine Transaktion

Nachdem eine Ressource zugewiesen wurde, aber kurz vor der Rückgabe der Ressource an den Ressourcen Verteiler, prüft der Dispenser-Manager mit com+, ob das aufrufende Objekt innerhalb einer Transaktion ausgeführt wird. Wenn das Aufruf Objekt innerhalb einer Transaktion ausgeführt wird, ruft der Dispenser-Manager den Ressourcen Verteiler zurück und fordert ihn auf, die Ressource in der Transaktion einzutragen. Anschließend wird die Ressource an den Ressourcen Verteiler zurückgegeben, der Sie an die aufrufenden Instanz zurückgibt.

Der Ressourcen Verteiler muss in der Lage sein, sich in einer OLE-Transaktion mit dem Distributed Transaction Coordinator (DTC) anzumelden.

> [!Note]  
> Die Transaktions Eintragung ist optional, wenn ein Ressourcen Spender nicht transaktionale Ressourcen (z. b. Arbeitsspeicher oder Threads) ausgibt.

 

Wenn eine Transaktion abgeschlossen ist, benachrichtigt com+ den Verteiler-Manager darüber, ob er zugesichert oder abgebrochen wurde. Anschließend benachrichtigt der Dispenser Manager den Besitzer jedes Ressourcen Verteilers, dass alle in dieser Transaktion eingetragenen Ressourcen nun in den allgemeinen bestand verschoben werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte des com+-Ressourcen Verteilers](com--resource-dispenser-concepts.md)
</dt> <dt>

[In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Ressourcen Zuordnungs Prozess Ressourcen Verteiler](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



