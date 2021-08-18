---
description: Eine Ellipse ist eine geschlossene Kurve, die durch zwei feste Punkte (f1 und f2) definiert wird, sodass die Summe der Entfernungen (d1 +d2 ) von jedem Punkt in der Kurve zu den beiden festen Punkten konstant ist.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Informationen zu Ellipsen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0892bfd2a8aa6fad43d18ead65eb92d260150ab31ca9057177c33af2cb8d4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117888551"
---
# <a name="about-ellipses"></a>Informationen zu Ellipsen

Eine Ellipse ist eine geschlossene Kurve, die durch zwei feste Punkte (f1 und f2) definiert wird, sodass die Summe der Entfernungen (d1 +d2 ) von jedem Punkt in der Kurve zu den beiden festen Punkten konstant ist. Die folgende Abbildung zeigt eine Ellipse, die mit der [**Ellipse-Funktion gezeichnet**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) wurde.

![Abbildung mit einer Ellipse, zwei festen Punkten, zwei Entfernungen und einem umgrenzten Rechteck](images/csfsh-01.png)

Beim Aufrufen von [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)stellt eine Anwendung die Koordinaten der oberen linken und unteren rechten Ecken des umgrenzten Rechtecks der Ellipse zur Verfügung. Ein *umschließendes Rechteck* ist das kleinste Rechteck, das die Ellipse vollständig umgibt. Wenn das System die Ellipse zeichnet, schließt es die rechte und untere Seite aus, wenn keine Welttransformationen festgelegt sind. Daher misst die zugeordnete Ellipse für jedes Rechteck, das x Einheiten breit um y Einheiten hoch misst, x1 Einheiten breit und y1 Einheiten hoch. Wenn die Anwendung eine Welttransformation durch Aufrufen der [**SetWorldTransform-**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) oder [**ModifyWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) festlegt, schließt das System die rechte und untere Seite ein.

 

 



