---
title: Such Timeout
description: Ein Client kann auch ein Zeitlimit erzwingen, das auf das Zurückgeben des Resultsets durch einen Server gewartet wird.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Such Timeout ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309220"
---
# <a name="search-time-out"></a>Such Timeout

Ein Client kann auch ein Zeitlimit erzwingen, das auf das Zurückgeben des Resultsets durch einen Server gewartet wird. Der Wert der Option "Timeout suchen" gibt diesen Grenzwert an. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche beenden und den Vorgang später wiederholen.

Die Timeout-Eigenschaft ist nützlich, wenn ein Client eine asynchrone Suche anfordert. Bei einer asynchronen Suche sendet der Client eine Anforderung und fährt dann mit anderen Tasks fort, während er darauf wartet, dass der Server die Ergebnisse zurückgibt. Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen. In diesem Fall kann der Client nicht erkennen, dass der Server die Abfrage noch verarbeitet oder nicht mehr aktiv ist. Die Timeout-Eigenschaft stellt dem Client ein Steuerelement in solchen Instanzen bereit.

Weitere Informationen zur Verwendung der Such Timeout Option mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Client Zeit Limit mit idirector ysearch](client-time-limit-with-idirectorysearch.md)
-   [Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




