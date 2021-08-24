---
description: Eintragung einer Ressource in eine Transaktion
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Eintragung einer Ressource in eine Transaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef1ab34d32853be0ca7d4641958b4f57ab55577865aad8612821e98882c71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858960"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Eintragung einer Ressource in eine Transaktion

Nachdem eine Ressource zugeordnet wurde, aber kurz vor der Rückgabe der Ressource an den Ressourcensender, überprüft der Versender-Manager mit COM+, ob das aufrufende Objekt innerhalb einer Transaktion ausgeführt wird. Wenn das aufrufende Objekt innerhalb einer Transaktion ausgeführt wird, ruft der Versendermanager den Ressourcensender zurück und fordert ihn auf, die Ressource in die Transaktion einträgt. Anschließend wird die Ressource an den Ressourcenausgaber zurückgegeben, der sie dann an die aufrufende Instanz zurückgibt.

Der Ressourcensender muss in der Lage sein, sich bei einer OLE-Transaktion mit dem Distributed Transaction Coordinator (DTC) zu eintragungen.

> [!Note]  
> Die Transaktionsinlistung ist optional, wenn ein Ressourcenverzehrer nicht transaktionale Ressourcen wie Arbeitsspeicher oder Threads aus gibt.

 

Wenn eine Transaktion abgeschlossen ist, benachrichtigt COM+ den Versender-Manager darüber, ob ein Committed oder ein Abbruch ausgeführt wurde. Anschließend benachrichtigt der Versendermanager den Besitzer jedes Ressourcensenders, dass alle in dieser Transaktion eingetragenen Ressourcen jetzt in den allgemeinen Bestand verschoben werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KONZEPTE DES COM+-Ressourcensenders](com--resource-dispenser-concepts.md)
</dt> <dt>

[Poolressourcenzustände, die für com+-Ressourcenspender verfügbar sind](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Ressourcenzuordnungsprozess des Ressourcensenders](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



