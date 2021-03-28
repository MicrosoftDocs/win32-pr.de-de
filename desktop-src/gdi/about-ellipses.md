---
description: Eine Ellipse ist eine geschlossene Kurve, die durch zwei festgelegte Punkte (F1 und F2) definiert wird, sodass die Summe der Entfernungen (D1 + D2) von einem beliebigen Punkt in der Kurve zu den zwei festgelegten Punkten konstant ist.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Informationen zu Ellipsen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560654"
---
# <a name="about-ellipses"></a>Informationen zu Ellipsen

Eine Ellipse ist eine geschlossene Kurve, die durch zwei festgelegte Punkte (F1 und F2) definiert wird, sodass die Summe der Entfernungen (D1 + D2) von einem beliebigen Punkt in der Kurve zu den zwei festgelegten Punkten konstant ist. Die folgende Abbildung zeigt eine Ellipse, die mithilfe der [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) -Funktion gezeichnet wurde.

![Abbildung: eine Ellipse, zwei fixierte Punkte, zwei Entfernungen und ein Begrenzungs Rechteck](images/csfsh-01.png)

Beim Aufrufen der [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse bereit. Ein umschließendes *Rechteck* ist das kleinste Rechteck, das die Ellipse vollständig umgibt. Wenn das System die Ellipse zeichnet, werden die Rechte und die untere Seite ausgeschlossen, wenn keine globalen Transformationen festgelegt sind. Aus diesem Grund misst die zugeordnete Ellipse bei allen Rechtecks, die x-Einheiten nach y-Einheiten breit sind, eine Breite von x1 y1 Einheiten. Wenn die Anwendung eine globale Transformation durch Aufrufen der [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -oder der [**modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) -Funktion festlegt, schließt das System die Rechte und die untere Seite ein.

 

 



