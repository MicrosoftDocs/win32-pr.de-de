---
title: Fragmentcache
description: Die HTTP-Server-API bietet Benutzern Funktionen zum Speichern von Datenfragmenten in einem Cache für die schnelle Bildung von HTTP-Antworten.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659ead1139bd1b35a466a56c44357dd1f7f30cbac5fad8669445208be0e5136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047250"
---
# <a name="fragment-cache"></a>Fragmentcache

Die HTTP-Server-API bietet Benutzern Funktionen zum Speichern von Datenfragmenten in einem Cache für die schnelle Bildung von HTTP-Antworten.

Fragmente können dem Cache durch Aufrufen der [**HttpAddFragmentToCache-Funktion hinzugefügt**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) werden. Ein Fragment wird durch eine URL identifiziert, die im *pUrlPrefix-Parameter* enthalten ist. Ein Aufruf dieser Funktion mit der URL eines vorhandenen Fragments überschreibt das vorhandene Fragment.

Ein Fragment kann vom Besitzer der Anforderungswarteschlange, die das Fragment ursprünglich hinzugefügt hat, gelöscht oder überschrieben werden. Die [**HttpFlushResponseCache-Funktion,**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) die mit einem UrlPrefix aufgerufen wird, löscht alle Fragmente innerhalb dieses Präfixes sowie die hierarchischen Nachfolger dieses UrlPrefix. Die [**HttpReadFragmentFromCache-Funktion**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) liest das gesamte Fragment oder einen angegebenen Bytebereich innerhalb des Fragments ein.

> [!Note]  
> Das Hinzufügen eines Fragments zum Cache garantiert nicht, dass es für zukünftige Aufrufe zum Senden einer Antwort verfügbar ist. Fragmentcacheeinträge können jederzeit nicht mehr verfügbar sein. Ein Aufruf, der ein nicht verfügbares Fragment verwendet, schlägt fehl. Anwendungen, die den Fragmentcache verwenden, müssen darauf vorbereitet sein, diesen Fehler zu behandeln.

 

## <a name="sending-a-response-with-a-fragment"></a>Senden einer Antwort mit einem Fragment

Fragmente können verwendet werden, um den entitätskörper einer HTTP-Antwort ganz oder einen Teil davon zu bilden. Sie können eine Antwort und einen Entitätskörper in einem Aufruf an die [**HttpSendHttpResponse-Funktion**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) senden, indem Sie ein Array von [**HTTP DATA \_ \_ CHUNK-Strukturen**](/windows/desktop/api/Http/ns-http-http_data_chunk) in der [**HTTP \_ RESPONSE-Struktur**](http-response.md) angeben.

Ein [**HTTP \_ DATA \_ CHUNK**](/windows/desktop/api/Http/ns-http-http_data_chunk) kann einen Speicherblock, ein Handle für eine bereits geöffnete Datei oder einen Fragmentcacheeintrag angeben. Diese entsprechen den **HTTP \_ DATA \_ CHUNK-Typen:** **HttpDataChunkFromMemory**, **HttpDataChunkFromFileHandle** bzw. **HttpDataChunkFromFragmentCache.** Vollständige Antworten im HTTP-Cache können auch als Fragmente in der [**HTTP \_ RESPONSE-Struktur**](http-response.md) verwendet werden, obwohl diese Vorgehensweise nicht empfohlen wird.

Die [**HTTP \_ RESPONSE-Struktur**](http-response.md) enthält einen Zeiger auf ein Array von [**HTTP DATA \_ \_ CHUNK-Strukturen,**](/windows/desktop/api/Http/ns-http-http_data_chunk) die den Entitätskörper der Antwort bilden. Die **HTTP \_ RESPONSE-Struktur** enthält auch eine übereinstimmende Anzahl, die die Dimension des Arrays von **HTTP DATA \_ \_ CHUNK-Strukturen angibt.** Der HttpDataChunkFromFragmentCache-Wert in der **HTTP \_ DATA \_ CHUNK-Struktur** gibt den Fragmentcachetyp des Daten chunks an. Die **HTTP \_ DATA \_ CHUNK-Struktur** gibt auch den Fragmentnamen an.

Eine Antwort, die ein zwischengespeichertes Fragment enthält, schlägt mit dem Fehler PATH NOT FOUND fehl, wenn keines der \_ \_ \_ Fragmentcacheeinträge verfügbar ist. Da die Fragmentcacheeinträge nicht garantiert verfügbar sind, müssen Anwendungen darauf vorbereitet sein, diesen Fall zu behandeln. Eine Möglichkeit, diesen Fall zu behandeln, besteht im Versuch, den Fragmentcacheeintrag erneut hinzuzufügen und die Antwort erneut zu senden. Wenn wiederholte Fehler auftreten, kann die Anwendung in Speicherpuffern gespeicherte Datenfragmente anstelle von Fragmentcacheeinträgen verwenden.

Fragmentcacheeinträge können auch in der [**HttpSendResponseEntityBody-Funktion angegeben**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) werden. Das Fragment wird dem Entitätskörper in der [**HTTP \_ DATA \_ CHUNK-Struktur**](/windows/desktop/api/Http/ns-http-http_data_chunk) wie oben beschrieben hinzugefügt. Auch hier kann das Senden fehlschlagen, wenn einer der angegebenen Fragmentcacheeinträge nicht verfügbar ist.

 

 




