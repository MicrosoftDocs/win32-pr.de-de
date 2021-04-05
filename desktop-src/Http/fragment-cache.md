---
title: Fragmentcache
description: Die HTTP-Server-API stellt Funktionen bereit, mit denen Benutzerdaten Fragmente in einem Cache für die schnelle Bildung von HTTP-Antworten speichern können.
ms.assetid: 0f9a768e-723c-4c7b-a746-6b817441409c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3979fb03c4f8898644329fd27eafb7007adbcc9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947504"
---
# <a name="fragment-cache"></a>Fragmentcache

Die HTTP-Server-API stellt Funktionen bereit, mit denen Benutzerdaten Fragmente in einem Cache für die schnelle Bildung von HTTP-Antworten speichern können.

Fragmente können dem Cache hinzugefügt werden, indem die [**httpaddfragmenttocache**](/windows/desktop/api/Http/nf-http-httpaddfragmenttocache) -Funktion aufgerufen wird. Ein Fragment wird durch eine URL identifiziert, die im *purlprefix* -Parameter enthalten ist. Ein Aufrufen dieser Funktion mit der URL eines vorhandenen Fragments überschreibt das vorhandene Fragment.

Ein Fragment kann vom Besitzer der Anforderungs Warteschlange gelöscht oder überschrieben werden, die anfänglich das Fragment hinzugefügt hat. Die [**httpflushresponsecache**](/windows/desktop/api/Http/nf-http-httpflushresponsecache) -Funktion, die mit einem URLPrefix aufgerufen wird, löscht alle Fragmente innerhalb dieses Präfixes sowie die hierarchischen Nachfolger dieses URLPrefix. Die [**httpreadfragmentfromcache**](/windows/desktop/api/Http/nf-http-httpreadfragmentfromcache) -Funktion liest das gesamte Fragment oder einen angegebenen Byte Bereich innerhalb des Fragments.

> [!Note]  
> Durch das Hinzufügen eines Fragments zum Cache wird nicht garantiert, dass es für zukünftige Aufrufe verfügbar ist, um eine Antwort zu senden. Fragment-Cache Einträge können jederzeit nicht mehr verfügbar sein. Ein-Befehl, der ein nicht verfügbares Fragment verwendet, schlägt fehl. Anwendungen, die den Fragmentcache verwenden, müssen darauf vorbereitet sein, diesen Fehler zu behandeln.

 

## <a name="sending-a-response-with-a-fragment"></a>Senden einer Antwort mit einem Fragment

Fragmente können verwendet werden, um alle-oder-Teile eines HTTP-Antwort-Entitäts Texts zu bilden. Sie können eine Antwort und einen Entitäts Text in einem-Rückruf an die [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) -Funktion senden, indem Sie ein Array von [**http- \_ Daten \_**](/windows/desktop/api/Http/ns-http-http_data_chunk) Block Strukturen in der [**http- \_ Antwort**](http-response.md) Struktur angeben.

Ein [**http \_ - \_ Daten**](/windows/desktop/api/Http/ns-http-http_data_chunk) Block kann einen Speicherblock angeben, ein Handle für eine bereits geöffnete Datei oder einen fragmentcacheeintrag. Diese entsprechen den **http- \_ Daten \_** Segmenttypen: **httpdatachunkfrommemory**, **httpdatachunkfromfilehandle**, bzw. **httpdatachunkfromfragmentcache**. Vollständige Antworten im HTTP-Cache können auch als Fragmente in der [**http- \_ Antwort**](http-response.md) Struktur verwendet werden, obwohl diese Vorgehensweise nicht empfohlen wird.

Die [**http- \_ Antwort**](http-response.md) Struktur enthält einen Zeiger auf ein Array von [**http- \_ Daten \_**](/windows/desktop/api/Http/ns-http-http_data_chunk) Block Strukturen, die den Entitäts Text der Antwort bilden. Die **http- \_ Antwort** Struktur enthält auch eine übereinstimmende Anzahl, die die Dimension des Arrays von **http- \_ Daten \_** Block Strukturen angibt. Der httpdatachunkfromfragmentcache-Wert in der **http- \_ Daten \_** Segmentstruktur gibt den fragmentcachetyp des Datensegments an. Die **http \_ - \_ Daten** Segmentstruktur gibt auch den fragmentnamen an.

Eine Antwort, die ein zwischengespeichertes Fragment enthält, schlägt fehl, und \_ \_ es wird kein Fehler Pfad \_ gefunden, wenn eine der Fragmente-Cache Einträge nicht verfügbar ist. Da es nicht garantiert wird, dass die Fragmentcache Einträge verfügbar sind, müssen Anwendungen darauf vorbereitet sein, diesen Fall zu verarbeiten. Eine Möglichkeit, diesen Fall zu behandeln, besteht darin, den Fragment-Cache Eintrag erneut hinzuzufügen und die Antwort erneut zu senden. Wenn wiederholte Fehler auftreten, kann die Anwendung Datenblöcke verwenden, die in Arbeitsspeicher Puffern gespeichert sind, anstelle von Fragment-Cache Einträgen.

Fragment-Cache Einträge können auch in der [**httpsendresponlentitybody**](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody) -Funktion angegeben werden. Das Fragment wird dem Entitäts Text in der [**http- \_ Daten \_**](/windows/desktop/api/Http/ns-http-http_data_chunk) Segmentstruktur hinzugefügt, wie oben beschrieben. Auch hier kann der Sendevorgang fehlschlagen, wenn eine der angegebenen Fragmente des Fragmentcaches nicht verfügbar ist.

 

 




