---
title: Abrufen von großen Resultsets
description: Wenn die Möglichkeit besteht, dass das Resultset, das zurückgegeben wird, mehr als 1000 Elemente enthält, müssen Sie eine auslagerbare Suche verwenden.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Abrufen von großen Resultsets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340402"
---
# <a name="retrieving-large-results-sets"></a>Abrufen von großen Resultsets

Wenn die Möglichkeit besteht, dass das Resultset, das zurückgegeben wird, mehr als 1000 Elemente enthält, müssen Sie eine auslagerbare Suche verwenden. Suchen nach Active Directory, die ohne Paging ausgeführt werden, sind auf die Rückgabe von maximal den ersten 1000-Datensätzen beschränkt. Bei einer seitenweise Suche wird das Resultset als einzelne Seiten dargestellt, die jeweils eine vorgegebene Anzahl von Ergebnis Einträgen enthalten. Bei dieser Art von Suche werden neue Seiten von Ergebnis Einträgen zurückgegeben, bis das Ende des Resultsets erreicht ist.

Standardmäßig berechnet der Server, der auf eine Abfrage Anforderung antwortet, ein Resultset vollständig, bevor Daten zurückgegeben werden. In einem großen Resultset erfordert dies den Server Arbeitsspeicher, wenn das Resultset abgerufen wird, und die Netzwerkbandbreite, wenn das große Ergebnis zurückgegeben wird. Wenn Sie eine Seitengröße festlegen, kann der Server die Daten beim Erstellen der Seiten auf Seiten senden. Der Client speichert dann diese Daten zwischen und stellt einen Cursor für den Code auf Anwendungsebene bereit. Paging wird festgelegt, indem definiert wird, wie viele Zeilen der Server berechnet, bevor die Daten über das Netzwerk an den Client zurückgegeben werden.

Das auslagerbare suchen bietet sowohl für den Client als auch den Server Vorteile. Beispielsweise kann der Client bei der Darstellung der Ergebnisse für Endbenutzer reaktionsfähiger sein. Dies ist besonders für grafische Benutzeroberflächen Tools relevant, die Daten anzeigen können, während ein anderer Thread gleichzeitig weitere Daten vom Server empfängt.

Wenn Sie die Abfrage einrichten und eine Sortierreihenfolge für das Resultset angeben, muss der Server das Resultset vollständig berechnen, bevor die Daten an den Client zurückgegeben werden. Dies wirkt sich auf die Antwortzeit für die Abfrage aus.

Auf der Serverseite wird durch die seitenweise Suche der Vorgang skalierbar. Wenn z. b. 100 Clients Suchanforderungen gleichzeitig ausgeben und im Durchschnitt von jedem Client 200 Objekte zurückgegeben werden, muss der Server über genügend Arbeitsspeicher verfügen, um das gesamte Resultset von 20.000 Einträgen aufzunehmen, wenn die Seitengröße nicht angegeben ist. Wenn jeder Client beispielsweise eine Seitengröße von zehn Objekten angegeben hat, werden die Arbeitsspeicher Anforderungen auf dem Server um den Faktor 20 reduziert.

> [!Note]  
> Nicht alle Verzeichnisdienste unterstützen auslagerbare Suchvorgänge. Active Directory implementiert die Architektur der Seitengröße.

 

Viele Verzeichnisserver geben eine administrative Beschränkung für die maximale Anzahl von Objekten an, die zurückgegeben werden können, wenn ein Client die Seitengröße nicht angibt. Wenn das Verwaltungs Limit erreicht ist, generiert ADSI den **Fehler \_ DS \_ Admin \_ Limit \_ überschritten** Win32.

Auf der Clientseite ermöglicht eine seitenweise Suche einem Client, den Vorgang anzuhalten, während er noch ausgeführt wird. Im Gegensatz dazu wird der Client in einer nicht auslagerungssuche blockiert, bis die Daten vollständig zurückgegeben werden, oder es tritt ein Fehler auf. Dies kann sich auf die Netzwerkleistung auswirken, wenn sich das Resultset als größer erweist und mehr Zeit als erwartet dauert.

Im Auftrag des Clients behandelt ADSI die Seitengröße transparent. Der Client muss die Anzahl der aktuell ausgeführten Objekte nicht zählen. ADSI kapselt die Server Interaktion für den Client. Aus Sicht des Clients gibt die Suche ein umfassendes Resultset zurück.

Weitere Informationen zur Verwendung der Such Timeout Option mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Paging mit idirector ysearch](paging-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

Eine seitenweise Suche ist für Ihre Anwendung transparent, da ADSI automatisch weitere Ergebnisseiten abruft, bis das Ende des Resultsets oder das Ende des festgelegten Zeitraums erreicht ist. Wenn Sie eine seitenweise Suche verwenden, wird die Seitengröße durch die Größenbeschränkung nicht überschrieben. Das Größenlimit kann nur verwendet werden, wenn Sie ein Resultset abrufen, das weniger als 1000 Einträge enthält.

 

 




