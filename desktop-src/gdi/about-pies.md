---
description: Ein Kreis ist ein Bereich, der durch die Schnittmenge einer Ellipse und zwei Radials begrenzt ist. Die folgende Abbildung zeigt einen Kreis, der mithilfe der Kreis Funktion gezeichnet wurde.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informationen zu Torten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041982"
---
# <a name="about-pies"></a><span data-ttu-id="45517-104">Informationen zu Torten</span><span class="sxs-lookup"><span data-stu-id="45517-104">About Pies</span></span>

<span data-ttu-id="45517-105">Ein *Kreis ist ein* Bereich, der durch die Schnittmenge einer Ellipse und zwei Radials begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="45517-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="45517-106">Die folgende Abbildung zeigt einen Kreis, der mithilfe der [**Kreis Funktion gezeichnet**](/windows/desktop/api/Wingdi/nf-wingdi-pie) wurde.</span><span class="sxs-lookup"><span data-stu-id="45517-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![Abbildung, die eine Ellipse mit schattiertem Kreis zeigt](images/csfsh-03.png)

<span data-ttu-id="45517-108">Beim Aufrufen von " [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie)" stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten bereit, die zwei radiale definieren.</span><span class="sxs-lookup"><span data-stu-id="45517-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="45517-109">Wenn das System den gekrümmten Teil des Kreises zeichnet, wird die aktuelle Bogen Richtung für den angegebenen Gerätekontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="45517-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="45517-110">Die Standard-Bogen Richtung ist gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="45517-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="45517-111">Eine Anwendung kann die Richtung des Bogens zurücksetzen, indem die [**setarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="45517-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
