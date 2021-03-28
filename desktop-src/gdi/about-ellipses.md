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
# <a name="about-ellipses"></a><span data-ttu-id="9c7ed-103">Informationen zu Ellipsen</span><span class="sxs-lookup"><span data-stu-id="9c7ed-103">About Ellipses</span></span>

<span data-ttu-id="9c7ed-104">Eine Ellipse ist eine geschlossene Kurve, die durch zwei festgelegte Punkte (F1 und F2) definiert wird, sodass die Summe der Entfernungen (D1 + D2) von einem beliebigen Punkt in der Kurve zu den zwei festgelegten Punkten konstant ist.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="9c7ed-105">Die folgende Abbildung zeigt eine Ellipse, die mithilfe der [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) -Funktion gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![Abbildung: eine Ellipse, zwei fixierte Punkte, zwei Entfernungen und ein Begrenzungs Rechteck](images/csfsh-01.png)

<span data-ttu-id="9c7ed-107">Beim Aufrufen der [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse bereit.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="9c7ed-108">Ein umschließendes *Rechteck* ist das kleinste Rechteck, das die Ellipse vollständig umgibt.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="9c7ed-109">Wenn das System die Ellipse zeichnet, werden die Rechte und die untere Seite ausgeschlossen, wenn keine globalen Transformationen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="9c7ed-110">Aus diesem Grund misst die zugeordnete Ellipse bei allen Rechtecks, die x-Einheiten nach y-Einheiten breit sind, eine Breite von x1 y1 Einheiten.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="9c7ed-111">Wenn die Anwendung eine globale Transformation durch Aufrufen der [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -oder der [**modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) -Funktion festlegt, schließt das System die Rechte und die untere Seite ein.</span><span class="sxs-lookup"><span data-stu-id="9c7ed-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



