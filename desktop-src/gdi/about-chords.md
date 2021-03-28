---
description: Ein Akkord ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines als "Secant" bezeichneten Linien Segments begrenzt ist. Die folgende Abbildung zeigt einen mit der Funktion "Chord" gezeichneten Akkord.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informationen zu Akkorden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527704"
---
# <a name="about-chords"></a><span data-ttu-id="00501-104">Informationen zu Akkorden</span><span class="sxs-lookup"><span data-stu-id="00501-104">About Chords</span></span>

<span data-ttu-id="00501-105">Ein *Akkord* ist ein Bereich, der durch die Schnittmenge einer Ellipse und eines als " *Sekans*" bezeichneten Linien Segments begrenzt ist.</span><span class="sxs-lookup"><span data-stu-id="00501-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="00501-106">Die folgende Abbildung zeigt einen mit der Funktion " [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) " gezeichneten Akkord.</span><span class="sxs-lookup"><span data-stu-id="00501-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![Abbildung einer Elipse, die zwei radiale, eine Secant und einen Akkord anzeigt](images/csfsh-02.png)

<span data-ttu-id="00501-108">Beim Aufrufen von " [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord)" stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten bereit, die zwei radiale definieren.</span><span class="sxs-lookup"><span data-stu-id="00501-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="00501-109">Ein radiales ist eine Linie, die aus der Mitte des umgebenden Rechtecks einer Ellipse bis zu einem Punkt auf der Ellipse gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="00501-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="00501-110">Wenn das System den gekrümmten Teil des Akkords zeichnet, erfolgt dies mithilfe der aktuellen Bogen Richtung für den angegebenen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="00501-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="00501-111">Die Standard-Bogen Richtung ist gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="00501-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="00501-112">Sie können festlegen, dass die Anwendung die Bogen Richtung zurücksetzen soll, indem Sie die [**setarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="00501-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
