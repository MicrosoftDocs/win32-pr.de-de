---
description: Ein Netzwerkanbieter ist eine DLL, die dem Windows-Betriebssystem die Unterstützung eines bestimmten Netzwerk Protokolls ermöglicht.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementieren eines Netzwerk Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128308"
---
# <a name="implementing-a-network-provider"></a>Implementieren eines Netzwerk Anbieters

Ein Netzwerkanbieter ist eine DLL, die dem Windows-Betriebssystem die Unterstützung eines bestimmten Netzwerk Protokolls ermöglicht. Hierzu wird die Netzwerkanbieter-API implementiert. Diese API ist eine Reihe von Funktionen, die der [*mehrere Anbieter Router*](../secgloss/m-gly.md) (MPR) aufruft, um mit dem Netzwerk zu kommunizieren. Der Netzwerkanbieter übersetzt diese Aufrufe dann in Netzwerk spezifische API-Aufrufe, um die von MPR angegebene Aktion auszuführen. Auf diese Weise kann das Windows-Betriebssystem mit neuen Netzwerkprotokollen interagieren, ohne die Netzwerk spezifischen APIs kennen zu müssen.

Zum Erstellen eines Netzwerk Anbieters schreiben Sie eine DLL, die die [**NPgetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) -Funktion exportiert.

Die Unterstützung der anderen Funktionen in der Netzwerkanbieter-API ist optional. Wenn Ihr Netzwerkanbieter keine Funktion erfordert, muss Sie von Ihrer dll nicht implementiert oder eine Stubimplementierung bereitgestellt werden. Weitere Informationen finden Sie in den Themen zu den einzelnen Funktionen in [Netzwerkanbieter Funktionen](authentication-functions.md).

Eine Ausnahme besteht darin, dass Sie, wenn Sie eine der folgenden Enumerationsfunktionen unterstützen, die anderen beiden Funktionen ebenfalls unterstützen müssen: [**npopenum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**npoumresource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)und [**npcloseenum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

In den folgenden Richtlinien wird beschrieben, wie Sie einen Netzwerkanbieter schreiben, der gut mit dem MPR und dem Windows-Betriebssystem interagiert. Wenn möglich, sollte Ihr Anbieter die folgenden Richtlinien für Geschwindigkeit, Validierung und Routing einhalten.

## <a name="speed"></a>Geschwindigkeit

Ein Netzwerkanbieter sollte schnell ermitteln, ob es sich um eine Netzwerkressource handelt. Dies liegt daran, dass die MPR möglicherweise viele Anbieter durchlaufen muss, um den Besitzer einer Ressource zu finden.

Wenn der Netzwerkanbieter nicht Besitzer der Ressource ist, sollte er sofort den ungültigen \_ NetName-Statuscode "wn" zurückgeben \_ .

Außerdem ist es wichtig, dass Anbieter, die [**npgetdirectorytype**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) unterstützen, Ergebnisse für diese Funktion schnell zurückgeben, da Sie aufgerufen werden, während winfile die Verzeichnisstruktur erstellt.

## <a name="validation"></a>Überprüfen

Die Reihenfolge der Überprüfung ist wichtig. Ein Netzwerkanbieter sollte zunächst ermitteln, ob das Netzwerk gestartet wurde, und dann ermitteln, ob der Netzwerk-und Netzwerkanbieter den Vorgang unterstützen. Wenn der Netzwerkanbieter nach diesen Überprüfungen Netzwerkressourcen erhält, sollte er ermitteln, ob er die Netzwerkressourcen besitzt. Zum Schluss sollten andere Parameter überprüft werden.

## <a name="routing"></a>Routing

Wenn die MPR Netzwerkanbieter durchlaufen muss, versucht Sie, alle Anbieter zu testen, bis Sie von einem akzeptiert werden. Das heißt, die MPR versucht immer, einen Netzwerkanbieter zu finden.

Der erste signifikante, von einem Anbieter gemeldete Fehler wird jedoch berücksichtigt. Fehler, wie z. b. fehlerhaft \_ \_ netpath, fehlerhafter \_ \_ \_ Netzwerkname, \_ ungültiger \_ Parameter, \_ ungültige Fehler \_ Stufe werden als unbedeutend angesehen, da Sie einfach bedeuten, dass der Anbieter die Ressource nicht verwaltet. Wenn der Anbieter jedoch mit dem fehlerhaften \_ \_ Kennwort oder einem anderen signifikanten Fehler fehlschlägt, wird dieser Fehler von MPR aufgezeichnet und die Netzwerkanbieter werden fortgesetzt. Wenn beim Routing kein Anbieter den-Befehl annimmt, meldet die MPR im Allgemeinen den ersten signifikanten Fehler, der beim Durchlaufen der Netzwerkanbieter auftritt.

Der Netzwerkanbieter sollte dieses Verhalten der MPR berücksichtigen, wenn Sie entscheiden, welche Fehlermeldung zurückgegeben werden soll.

## <a name="implementation-note"></a>Implementierungs Hinweis

Beim Implementieren von Netzwerkanbieter-dll darf der Anbieter keine anderen Windows- [Netzwerkfunktionen](../wnet/windows-networking-functions.md), [Shell-APIs](../shell/samples-usingthumbnailproviders.md)oder anderen UNC-Pfad basierten Abfragen anrufen, die zu einem erneuten Einstieg in das MPR-Subsystem führen könnten. Wenn Sie solche Aufrufe von einer Netzwerkanbieter-dll durchführen, treten bei der Anwendung oder anderen Betriebssystemkomponenten möglicherweise Konflikte, schlechte Leistung oder Deadlocks im MPR-Subsystem auf.

 

 
