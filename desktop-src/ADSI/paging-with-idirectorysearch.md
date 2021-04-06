---
title: Paging mit idirector ysearch
description: Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947336"
---
# <a name="paging-with-idirectorysearch"></a>Paging mit idirector ysearch

Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt. Eine Seite kann durch die Anzahl von Zeilen oder ein Zeitlimit definiert werden. Das ADSI COM-Objekt ruft jede Ergebnisseite auf Grundlage der in der folgenden Tabelle aufgeführten Werte ab. Der Aufrufer ruft [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) auf, wenn er das Seiten Ende erreicht hat, und das ADSI COM-Objekt ruft die nächste Seite ab.



| Wert                                   | BESCHREIBUNG                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anzeigen von \_ searchpref \_ Page Size**           | Gibt die maximale Anzahl von Zeilen an, die auf einer Seite zurückgegeben werden sollen.                                                                                                                                                                                            |
| **Auslagerungszeit- \_ \_ \_ \_ Limit für Werbeeinblendungen** | Gibt die maximale Zeit in Sekunden an, die der Server zum Sammeln einer Ergebnisseite aufwenden soll, bevor die Seite an den Client zurückgegeben wird. Wenn der Grenzwert erreicht wird, beendet der Server die Suche und gibt die bereits für die Seite abgerufenen Zeilen zurück. |



 

Wenn keine dieser Sucheinstellungen festgelegt ist, ist der Standardwert kein Paging. Suchen der Active Directory, die ohne Paging ausgeführt werden, sind auf die Rückgabe von maximal den ersten 1000 Datensätzen beschränkt. Daher müssen Sie eine seitenweise Suche verwenden, wenn die Möglichkeit besteht, dass das Resultset mehr als 1000 Elemente enthält.

Ein Suchvorgang kann dazu führen, dass eine große Anzahl von Objekten zurückgegeben wird. Wenn der Server das Ergebnis in einem Satz zurückgibt, kann dies die Leistung des Clients und des Servers verringern und die Netzwerk Auslastung beeinträchtigen. Eine auslagerbare Suche kann verwendet werden, um dies zu verhindern. In einer auslagerenen Suche kann der Client Ergebnisse in kleineren Paketen akzeptieren. Die Größe eines Pakets wird als Suchseiten Größe bezeichnet.

Auslagerbare Suchvorgänge bieten sowohl dem Client als auch dem Server Vorteile. Der Client kann bei der Darstellung der Ergebnisse für Benutzer reaktionsfähiger sein. Dies ist besonders wichtig für grafische Benutzeroberflächen Tools, die den Fenster Anzeige Prozess starten können, während der andere Thread gleichzeitig die Daten empfängt.

Auf Serverseite wird der Vorgang durch seitenweise Suchen skalierbar. Wenn z. b. 100 Clients Suchanforderungen gleichzeitig ausgeben und im Durchschnitt jeder Client 200 Objekte empfängt. Wenn keine Seitengröße angegeben ist, muss der Server im ungünstigsten Fall über ausreichend Arbeitsspeicher verfügen, um 20.000 Objekte zu speichern. Wenn hingegen jeder Client eine Seitengröße angibt (z. b. zehn Objekte), wird die Arbeitsspeicher Anforderung auf dem Server um den Faktor 20 reduziert.

Außerdem kann ein Client mit einer auslagerungssuche den Vorgang abbrechen, der gerade ausgeführt wird. Im Gegensatz dazu empfängt der Client in einer nicht Auslagerungs Suche ein Resultset in einem Paket. Dadurch kann die Netzwerkleistung verringert werden.

ADSI behandelt die Seitengröße für den Client. Der Client muss die Anzahl der aktuell ausgeführten Objekte nicht zählen. ADSI kapselt die Server Interaktion für den Client. Aus Sicht des Clients gibt die Suche ein umfassendes Resultset zurück.

Es wird empfohlen, Paging zu verwenden.

Wenn Sie eine maximale Seitengröße angeben möchten, legen Sie die Suchoption **ADS \_ searchpref \_ PageSize** mit einem **\_ ganzzahligen adstype** -Wert fest, der auf die maximale Anzahl von Zeilen pro Seite in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden ADS festgelegt ist. [**\_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)

Im folgenden Codebeispiel wird gezeigt, wie die maximale Seitengröße festgelegt wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Um einen Seiten Zeitraum anzugeben, legen Sie die Suchoption für das Auslagerungs **\_ \_ \_ Zeit \_ Limit für Werbe** Einblendungen auf einen Wert vom Typ " **adstype \_** " fest, der auf die maximale Anzahl von Sekunden festgelegt ist, die der Server für das Abrufen einer Seite im [**ADS- \_ \_ infoarray**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) mit der [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode aufwenden soll.

Im folgenden Codebeispiel wird gezeigt, wie die Seiten Zeit angegeben wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




