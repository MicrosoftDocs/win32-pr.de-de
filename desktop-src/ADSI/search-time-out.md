---
title: Time out bei der Suche
description: Ein Client kann auch eine Zeitbeschränkung festlegen, die darauf wartet, dass ein Server das Ergebnis zurück gibt.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Search Time Out ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99b287c1bc0ba0da5e39b579c4a454eae821cf2c443930a5ae0376412e2c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082304"
---
# <a name="search-time-out"></a>Time out bei der Suche

Ein Client kann auch eine Zeitbeschränkung festlegen, die darauf wartet, dass ein Server das Ergebnis zurück gibt. Der Wert der Option "Suchzeitlimit" gibt diesen Grenzwert an. Wenn der Server innerhalb des angegebenen Zeitraums nicht auf eine Abfrage antwortet, kann der Client die Suche beenden und es später erneut versuchen.

Die Time out-Eigenschaft ist nützlich, wenn ein Client eine asynchrone Suche an fordert. Bei einer asynchronen Suche sendet der Client eine Anforderung und geht dann mit anderen Aufgaben fort, während auf die Rückgabe der Ergebnisse durch den Server gewartet wird. Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen. In diesem Fall kann der Client nicht erkennen, dass der Server die Abfrage noch verarbeitet oder nicht mehr live ist. Die time-out-Eigenschaft bietet dem Client ein gewisses Steuerelement in solchen Instanzen.

Weitere Informationen zur Verwendung der Option "Time out" für die Suche mit einer bestimmten Suchschnittstelle finden Sie unter:

-   [Clientzeitlimit mit IDirectorySearch](client-time-limit-with-idirectorysearch.md)
-   [Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
-   [Suchen mit OLE DB](searching-with-ole-db.md)

 

 




