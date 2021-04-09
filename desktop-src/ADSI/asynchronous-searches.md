---
title: Asynchrone Suchvorgänge
description: Das Aktivieren der asynchronen Suche (Async) führt zum Aufrufen von "GetFirstRow" oder zum ersten Aufrufen von "GetNextRow", bis der erste Eintrag vom Server zurückgegeben wird.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Asynchrone Suchvorgänge ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947360"
---
# <a name="asynchronous-searches"></a>Asynchrone Suchvorgänge

Das Aktivieren der asynchronen Suche (Async) führt zum Aufrufen von " **GetFirstRow** " oder zum ersten Aufrufen von " **GetNextRow** ", bis der erste Eintrag vom Server zurückgegeben wird. Das heißt, wenn die Suche auf dem Server viel Zeit erfordert, werden die ersten Ergebnisse schnell zurückgegeben. Dies kann hilfreich sein, wenn Sie ein Listenfeld mit Suchergebnissen auffüllen. Suchergebnisse werden angezeigt, sobald Sie zurückgegeben werden.

Wenn async deaktiviert ist, wird der erste Aufrufen von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server das gesamte Resultset berechnet und zurückgibt. Nur dann ist die erste zurückgegebene Zeile. Dies wird nicht empfohlen, wenn das Resultset als groß erwartet wird.

Wenn sowohl Paging als auch Async aktiviert sind, wird der erste Aufrufen von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server die erste Seite der Ergebnisse generiert und sendet. Wenn eine angemessene Seitengröße festgelegt wurde, werden die Ergebnisse sofort angezeigt. Noch wichtiger ist: Wenn die Suchergebnisse sehr groß werden und Sie nach einem bestimmten Eintrag suchen, ist es nicht erforderlich, dass Sie weitere Ergebnisse vom Server anfordern, nachdem Sie die für Sie interessanten Einträge gefunden haben.

Eine auslagerbare asynchrone Suche bietet eine gute Kontrolle über eine Suche. Dies ist hilfreich, wenn die Suchergebnisse sehr groß sein können und eine lange Zeit auf dem Server erforderlich ist.

Weitere Informationen zur Verwendung von asynchronen Such Vorgängen mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Synchrone und asynchrone Suchvorgänge mit idirector ysearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




