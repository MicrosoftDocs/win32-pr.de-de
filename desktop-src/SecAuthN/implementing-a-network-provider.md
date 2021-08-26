---
description: Ein Netzwerkanbieter ist eine DLL, die es dem Windows ermöglicht, ein bestimmtes Netzwerkprotokoll zu unterstützen.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementieren eines Netzwerkanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4776bd97b9528bd04bbda25b88e0ff45a8f911429bb573e62dbbb8581abdfbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015980"
---
# <a name="implementing-a-network-provider"></a>Implementieren eines Netzwerkanbieters

Ein Netzwerkanbieter ist eine DLL, die es dem Windows ermöglicht, ein bestimmtes Netzwerkprotokoll zu unterstützen. Hierzu wird die Netzwerkanbieter-API implementieren. Bei dieser API handelt es sich um eine Reihe von [*Funktionen,*](../secgloss/m-gly.md) die der Multiple Provider Router (MPR) aufruft, um mit dem Netzwerk zu kommunizieren. Der Netzwerkanbieter übersetzt diese Aufrufe dann in netzwerkspezifische API-Aufrufe, um die vom MPR angegebene Aktion durchzuführen. Auf diese Weise kann das Windows mit neuen Netzwerkprotokollen interagieren, ohne seine netzwerkspezifischen APIs verstehen zu müssen.

Um einen Netzwerkanbieter zu erstellen, schreiben Sie eine DLL, die die [**NPGetCaps-Funktion**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) exportiert.

Die Unterstützung der anderen Funktionen in der Netzwerkanbieter-API ist optional. Wenn Ihr Netzwerkanbieter keine Funktion erfordert, muss Ihre DLL sie nicht implementieren oder eine Stubimplementierung bereitstellen. Weitere Informationen finden Sie in den Einzelnen Funktionsthemen unter [Netzwerkanbieterfunktionen.](authentication-functions.md)

Die Ausnahme ist, dass Sie, wenn Sie eine der folgenden Enumerationsfunktionen unterstützen, auch die anderen beiden Funktionen unterstützen müssen: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)und [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

In den folgenden Richtlinien wird beschrieben, wie Sie einen Netzwerkanbieter schreiben, der gut mit dem MPR und dem Windows interagiert. Wenn möglich, sollte Ihr Anbieter die folgenden Richtlinien für Geschwindigkeit, Validierung und Routing einhalten.

## <a name="speed"></a>Geschwindigkeit

Ein Netzwerkanbieter sollte schnell bestimmen, ob es sich um eine eigene Netzwerkressource handelt. Dies liegt daran, dass die MPR möglicherweise viele Anbieter durchzyklen muss, um den Besitzer einer Ressource zu finden.

Wenn der Netzwerkanbieter die Ressource nicht besitzt, sollte er sofort den WN \_ BAD \_ NETNAME-Statuscode zurückgeben.

Es ist auch wichtig, dass Anbieter, die [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) unterstützen, schnell Ergebnisse für diese Funktion zurückgeben, da sie aufgerufen wird, während WinFile die Verzeichnisstruktur malt.

## <a name="validation"></a>Überprüfung

Die Reihenfolge der Überprüfung ist wichtig. Ein Netzwerkanbieter sollte zuerst bestimmen, ob sein Netzwerk gestartet wird, und dann bestimmen, ob das Netzwerk und der Netzwerkanbieter den Vorgang unterstützen. Wenn der Netzwerkanbieter nach diesen Überprüfungen Netzwerkressourcen empfängt, sollte er bestimmen, ob er diese besitzt. Schließlich sollten andere Parameter überprüft werden.

## <a name="routing"></a>Routing

Wenn der MPR Netzwerkanbieter durchzyklen muss, versucht er alle Anbieter, bis einer den Aufruf akzeptiert. Das heißt, die MPR versucht immer weiterhin, einen Netzwerkanbieter zu finden.

Sie notieren jedoch den ersten signifikanten Fehler, der von einem Anbieter gemeldet wird. Fehler wie ERROR \_ BAD \_ NETPATH, ERROR \_ BAD NET \_ \_ NAME, ERROR INVALID \_ PARAMETER, ERROR INVALID \_ \_ \_ LEVEL werden als nicht signifikant angesehen, da sie lediglich bedeuten, dass der Anbieter die Ressource nicht verwaltet. Wenn der Anbieter jedoch mit dem Fehler ERROR INVALID PASSWORD oder einem anderen signifikanten Fehler ausfällt, zeichnet MPR diesen Fehler auf und durchfing weiterhin die \_ \_ Netzwerkanbieter. Wenn beim Routing kein Anbieter den Aufruf akzeptiert, meldet der MPR im Allgemeinen den ersten signifikanten Fehler, der beim Durchfahren der Netzwerkanbieter auftritt.

Ihr Netzwerkanbieter sollte dieses Verhalten der MPR berücksichtigen, wenn er entscheidet, welche Fehlermeldung zurückgegeben werden soll.

## <a name="implementation-note"></a>Implementierungshinweis

Bei der Implementierung von Netzwerkanbieter-DLLs darf der Anbieter keine anderen [Windows-Netzwerkfunktionen,](../wnet/windows-networking-functions.md) [Shell-APIs](../shell/samples-usingthumbnailproviders.md)oder andere UNC-pfadbasierte Abfragen aufrufen, die einen erneuten Versuch im MPR-Subsystem verursachen könnten. Wenn Sie solche Aufrufe von einer Netzwerkanbieter-DLL aus tätigen, kann es bei der Anwendung oder anderen Betriebssystemkomponenten zu Problemen, leistungsschläftiger Leistung oder Deadlocks innerhalb des MPR-Subsystems kommen.

 

 
