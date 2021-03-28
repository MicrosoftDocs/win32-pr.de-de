---
description: Die Abmessungen eines kosmetischen Stifts werden in Geräte Einheiten angegeben.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Kosmetische Stifte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754465"
---
# <a name="cosmetic-pens"></a>Kosmetische Stifte

Die Abmessungen eines kosmetischen Stifts werden in Geräte Einheiten angegeben. Daher haben Zeilen, die mit einem kosmetischen Stift gezeichnet werden, immer eine festgelegte Breite. Zeilen, die mit einem kosmetischen Stift gezeichnet werden, werden in der Regel 3 bis 10 mal schneller als mit einem geometrischen Stift gezeichnete Linien gezeichnet. Kosmetische Stifte haben drei Attribute: "width", "Style" und "Color". Weitere Informationen zu diesen Attributen finden Sie unter [Pen-Attribute](pen-attributes.md).

Verwenden Sie zum Erstellen eines kosmetischen Stifts die Funktion " [**kreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)", " [**kreatepenindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)" oder " [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) ". Verwenden Sie die [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion, um einen der drei durch das System verwalteten, mit dem Kurs verwalteten Kosmetik Stifte abzurufen.

Nachdem Sie einen Stift erstellt (oder ein Handle für einen der Aktien Stifte abgerufen haben), wählen Sie den Stift mithilfe der [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion in den Gerätekontext der Anwendung aus. Ab diesem Zeitpunkt wird dieser Stift von der Anwendung für alle Zeilen Zeichnungsvorgänge im Client Bereich verwendet.

 

 



