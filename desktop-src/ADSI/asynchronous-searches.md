---
title: Asynchrone Suchvorgänge
description: Das Aktivieren der asynchronen (asynchronen) Suche führt zu einem Aufruf von GetFirstRow oder zum ersten Aufruf von GetNextRow blockiert, bis der erste Eintrag vom Server zurückgegeben wird.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Asynchrone Suchvorgänge ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082784"
---
# <a name="asynchronous-searches"></a>Asynchrone Suchvorgänge

Das Aktivieren der asynchronen (asynchronen) Suche führt zu einem Aufruf von **GetFirstRow** oder zum ersten Aufruf von **GetNextRow** blockiert, bis der erste Eintrag vom Server zurückgegeben wird. Das heißt, wenn die Suche auf dem Server viel Zeit erfordert, werden die ersten Ergebnisse schnell zurückgegeben. Dies kann beim Auflisten eines Listenfelds mit Suchergebnissen helfen. Suchergebnisse werden angezeigt, sobald sie zurückgegeben werden.

Wenn async deaktiviert ist, wird der erste Aufruf von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server das gesamte Ergebnisset berechnet und zurückgibt. Nur dann wird die erste Zeile zurückgegeben. Dies wird nicht empfohlen, wenn erwartet wird, dass das Resultset groß ist.

Wenn paging und async aktiviert sind, wird der erste Aufruf von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server die erste Ergebnisseite generiert und sendet. Wenn eine angemessene Seitengröße festgelegt wurde, werden die Ergebnisse sofort angezeigt. Wichtiger noch: Wenn die Suchergebnisse sehr groß sein sollen und Sie nach einem bestimmten Eintrag suchen, ist es nicht erforderlich, dass Sie mehr Ergebnisse vom Server anfordern, nachdem Sie die für Sie wichtigen Einträge gefunden haben.

Eine asynchrone Suche mit Seiten bietet eine gute Kontrolle über eine Suche. Dies ist nützlich, wenn die Suchergebnisse sehr groß sein können und viel Zeit vom Server erfordern.

Weitere Informationen zur Verwendung von asynchronen Suchvorgängen mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Synchrone und asynchrone Suchvorgänge mit IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




