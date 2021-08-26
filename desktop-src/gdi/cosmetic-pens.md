---
description: Die Abmessungen eines optischen Stifts werden in Geräteeinheiten angegeben.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Plastische Stifte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65f875ce5873b5f53cba19b5440751b8ac7683df99765ea7e8e6eec813ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966070"
---
# <a name="cosmetic-pens"></a>Plastische Stifte

Die Abmessungen eines optischen Stifts werden in Geräteeinheiten angegeben. Daher weisen Linien, die mit einem stiftierten Stift gezeichnet werden, immer eine feste Breite auf. Linien, die mit einem geometrischen Stift gezeichnet werden, werden in der Regel 3 bis 10 Mal schneller gezeichnet als Linien, die mit einem geometrischen Stift gezeichnet werden. Farbige Stifte verfügen über drei Attribute: Breite, Stil und Farbe. Weitere Informationen zu diesen Attributen finden Sie unter [Pen Attributes](pen-attributes.md).

Verwenden Sie die Funktion [**CreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)oder [**ExtCreatePen,**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) um einen plastischen Stift zu erstellen. Verwenden Sie die [**GetStockObject-Funktion,**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) um einen der drei vom System verwalteten Stock-Pens abzurufen.

Nachdem Sie einen Stift erstellt haben (oder ein Handle für einen der Stockstifte erhalten haben), wählen Sie den Stift mithilfe der [**SelectObject-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) in den Gerätekontext (DC) der Anwendung aus. Ab diesem Zeitpunkt verwendet die Anwendung diesen Stift für alle Strichzeichnungsvorgänge im Clientbereich.

 

 



