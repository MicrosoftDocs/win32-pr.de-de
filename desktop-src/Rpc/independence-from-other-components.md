---
title: Unabhängig von anderen Komponenten
description: Erweiterte Fehlerdaten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übergeben wurde, keine erweiterten Fehlerdaten erkennt oder sie nicht nutzt. Empfohlene Ansätze für solche Situationen finden Sie am Ende dieses Abschnitts.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Unabhängig von anderen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8174ffa0469550d3a7b274fb28f2f30dd807314e6bd596b75469f717f5924a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020450"
---
# <a name="independence-from-other-components"></a>Unabhängig von anderen Komponenten

Erweiterte Fehlerdaten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übergeben wurde, keine erweiterten Fehlerdaten erkennt oder sie nicht nutzt. Empfohlene Ansätze für solche Situationen finden Sie am Ende dieses Abschnitts.

Erweiterte Fehlerdaten sind besonders nützlich, wenn Anwendungen oder Server, die RPC verwenden, erweiterte Fehlerinformationen nutzen. Wenn Sie einen RPC S-Fehlercode untersuchen und die beteiligten Server oder Anwendungen keine erweiterten Fehlerdaten verfügbar machen, sollten \_ Sie die folgenden Ansätze in Betracht \_ \* ziehen:

-   Nehmen Sie einen Sniff.

    Reproduzieren Sie das Szenario, während Sie den Sniff verwenden. Der Sniff des Kabels enthält die erweiterten Fehlerdaten.

-   Untersuchen Sie sie über den Debugger.

    Wenn eine Problemsniffe nicht funktioniert, weil der Aufruf lokal ist oder der Fehler lokal auftritt, fügen Sie einen Debugger an den Prozess an, der den Fehler zurücksendet, und setzen Sie unmittelbar nach dem RPC-Aufruf, der den Fehler generiert, einen Haltepunkt. RPC weist häufig auf Fehler hin, indem Ausnahmen ausgelöst werden. Wenn Sie also nach Fehler 1825 (RPC S SEC PKG ERROR) suchen, aktivieren Sie Ausnahme \_ \_ \_ 1825, und wenn der Debugger bei dieser Ausnahme unterbricht, überprüfen Sie die erweiterten Fehlerinformationen für den \_ Thread.

 

 




