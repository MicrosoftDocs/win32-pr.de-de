---
title: Paging mit IDirectorySearch
description: Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paging mit IDirectorySearch ADSI
- ADSI, Suchen, IDirectorySearch, Andere Suchoptionen, Paging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838940"
---
# <a name="paging-with-idirectorysearch"></a>Paging mit IDirectorySearch

Paging gibt an, wie viele Zeilen der Server an den Client zurückgibt. Eine Seite kann durch die Anzahl der Zeilen oder ein Zeitlimit definiert werden. Das ADSI COM-Objekt ruft jede Seite der Ergebnisse basierend auf den in der folgenden Tabelle aufgeführten Werten ab. Der Aufrufer ruft [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) auf, wenn er das Seitenende erreicht hat und das ADSI COM-Objekt die nächste Seite abruft.



| Wert                                   | Beschreibung                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ SEARCHPREF \_ PAGESIZE**           | Gibt die maximale Anzahl von Zeilen an, die auf einer Seite zurückgegeben werden sollen.                                                                                                                                                                                            |
| **ADS \_ SEARCHPREF \_ PAGED \_ TIME \_ LIMIT** | Gibt die maximale Zeit in Sekunden an, die der Server für das Sammeln einer Seite mit Ergebnissen aufwenden soll, bevor die Seite an den Client zurückgegeben wird. Wenn der Grenzwert erreicht ist, beendet der Server die Suche und gibt die Zeilen zurück, die bereits für die Seite abgerufen wurden. |



 

Wenn keine dieser Sucheinstellungen festgelegt ist, wird standardmäßig kein Paging verwendet. Suchvorgänge in Active Directory, die ohne Auslagerung ausgeführt werden, sind auf die Rückgabe von maximal 1.000 Datensätzen beschränkt. Daher müssen Sie eine ausgelagerungte Suche verwenden, wenn die Möglichkeit besteht, dass das Resultset mehr als 1.000 Elemente enthält.

Ein Suchvorgang kann dazu führen, dass eine große Anzahl von Objekten zurückgegeben wird. Wenn der Server das Ergebnis in einem Satz zurückgibt, kann dies die Leistung von Client und Server beeinträchtigen und sich auf die Netzwerklast auswirken. Seitensuchen können verwendet werden, um dies zu verhindern. Bei einer ausgelagerungten Suche kann der Client Ergebnisse in kleineren Paketen akzeptieren. Die Größe eines Pakets wird als Größe der Suchseite bezeichnet.

Ausgelagerungssuchen bieten sowohl für den Client als auch für den Server Vorteile. Der Client kann reaktionsfähiger sein, wenn die Ergebnisse Benutzern präsentiert werden. Dies ist besonders relevant für grafische Benutzeroberflächentools, die den Fensteranzeigeprozess starten können, während der andere Thread die Daten gleichzeitig empfängt.

Auf serverseitiger Seite wird der Vorgang durch ausgelagerungte Suchvorgänge skalierbar. Wenn z. B. 100 Clients gleichzeitig Suchanforderungen ausstellen und im Durchschnitt jeder Client zwei hundert Objekte empfängt. Wenn keine Seitengröße angegeben wird, muss der Server im schlimmsten Fall über ausreichend Arbeitsspeicher für 20.000 Objekte verfügen. Wenn dagegen jeder Client eine Seitengröße angibt, z. B. zehn Objekte, wird der Arbeitsspeicherbedarf auf dem Server um den Faktor 20 reduziert.

Darüber hinaus kann ein Client mithilfe einer ausgelagerungten Suche den ausgeführten Vorgang abbrechen. Im Gegensatz dazu empfängt der Client bei einer nicht ausgelagerungten Suche ein Resultset in einem Paket. Dies kann die Netzwerkleistung beeinträchtigen.

ADSI verarbeitet die Seitengröße für den Client. Der Client muss die Anzahl der ausgeführten Objekte nicht zählen. ADSI kapselt die Serverinteraktion für den Client. Aus Clientsicht gibt die Suche ein vollständiges Resultset zurück.

Es wird empfohlen, paging zu verwenden.

Um eine maximale Seitengröße anzugeben, legen Sie eine **ADS \_ SEARCHPREF \_ PAGESIZE-Suchoption** mit einem **ADSTYPE \_ INTEGER-Wert** auf die maximale Anzahl von Zeilen pro Seite im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) fest, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird.

Im folgenden Codebeispiel wird veranschaulicht, wie die maximale Seitengröße festgelegt wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Um eine Seitenzeit anzugeben, legen Sie eine **ADS \_ SEARCHPREF \_ PAGED \_ TIME \_ LIMIT-Suchoption** mit einem **ADSTYPE \_ INTEGER-Wert** fest, der auf die maximale Anzahl von Sekunden festgelegt ist, die der Server für das Abrufen einer Seite im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) aufwenden soll, die an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird.

Im folgenden Codebeispiel wird gezeigt, wie Die Seitenzeit angegeben wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




