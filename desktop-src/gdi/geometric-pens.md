---
description: Die Abmessungen eines geometrischen Stifts werden in logischen Einheiten angegeben.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Geometrische Stifte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993998"
---
# <a name="geometric-pens"></a><span data-ttu-id="556be-103">Geometrische Stifte</span><span class="sxs-lookup"><span data-stu-id="556be-103">Geometric Pens</span></span>

<span data-ttu-id="556be-104">Die Abmessungen eines geometrischen Stifts werden in logischen Einheiten angegeben.</span><span class="sxs-lookup"><span data-stu-id="556be-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="556be-105">Daher können Linien, die mit einem geometrischen Stift gezeichnet werden, skaliert werden, d. h., Sie können je nach aktueller Welt Transformation breiter oder schmaler erscheinen.</span><span class="sxs-lookup"><span data-stu-id="556be-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="556be-106">Weitere Informationen zur weltweiten Transformation finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="556be-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="556be-107">Zusätzlich zu den drei Attributen, die mit den kosmetischen stiften (Breite, Format und Farbe) gemeinsam genutzt werden, besitzen geometrische Stifte die folgenden vier Attribute: Muster, optionale Schraffur, Endstil und joinstil.</span><span class="sxs-lookup"><span data-stu-id="556be-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="556be-108">Weitere Informationen zu diesen Attributen finden Sie unter [Pen-Attribute](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="556be-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="556be-109">Zum Erstellen eines geometrischen Stifts verwendet eine Anwendung die [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="556be-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="556be-110">Wie bei den kosmetischen stiften wählt die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion einen geometrischen Stift in den DC der Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="556be-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 



