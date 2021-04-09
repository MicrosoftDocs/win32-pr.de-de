---
title: Unabhängigkeit von anderen Komponenten
description: Erweiterte Fehler Daten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übermittelt wurde, erweiterte Fehler Daten nicht erkennt oder Sie nicht nutzt. Empfohlene Vorgehensweisen für derartige Situationen werden am Ende dieses Abschnitts bereitgestellt.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Unabhängigkeit von anderen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948005"
---
# <a name="independence-from-other-components"></a>Unabhängigkeit von anderen Komponenten

Erweiterte Fehler Daten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übermittelt wurde, erweiterte Fehler Daten nicht erkennt oder Sie nicht nutzt. Empfohlene Vorgehensweisen für derartige Situationen werden am Ende dieses Abschnitts bereitgestellt.

Erweiterte Fehler Daten sind besonders nützlich, wenn Anwendungen oder Server, die RPC verwenden, erweiterte Fehlerinformationen nutzen. Wenn Sie einen RPC \_ \_ \* -Fehlercode untersuchen und die beteiligten Server oder Anwendungen keine erweiterten Fehler Daten verfügbar machen, sollten Sie die folgenden Ansätze beachten:

-   Nehmen Sie einen Sniff vor.

    Reproduzieren Sie das Szenario, während Sie den Sniff ausführen. Der Ausspionieren der Verbindung enthält die erweiterten Fehler Daten.

-   Überprüfen Sie diese im Debugger.

    Wenn das Erstellen eines Problems mit dem Problem nicht funktioniert, weil der Aufruf lokal erfolgt oder weil der Fehler lokal auftritt, fügen Sie einen Debugger an den Prozess an, der den Fehler zurückgibt, und platzieren Sie unmittelbar nach dem RPC-Aufruf, der den Fehler erzeugt, einen Haltepunkt. RPC weist häufig auf Fehler hin, indem Ausnahmen ausgelöst werden. Wenn Sie also nach Fehler 1825 (RPC \_ S S \_ \_ pkg- \_ Fehler) suchen, aktivieren Sie Exception 1825, und wenn der Debugger bei dieser Ausnahme anhält, überprüfen Sie die erweiterten Fehlerinformationen für den Thread.

 

 




