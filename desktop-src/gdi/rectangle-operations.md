---
description: Die SetRect-Funktion erstellt ein Rechteck, die copyrect-Funktion erstellt eine Kopie eines angegebenen Rechtecks, und die Funktion setrectempty erstellt ein leeres Rechteck.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Rechteck Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344639"
---
# <a name="rectangle-operations"></a><span data-ttu-id="3d789-103">Rechteck Vorgänge</span><span class="sxs-lookup"><span data-stu-id="3d789-103">Rectangle Operations</span></span>

<span data-ttu-id="3d789-104">Die [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) -Funktion erstellt ein Rechteck, die [**copyrect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) -Funktion erstellt eine Kopie eines angegebenen Rechtecks, und die Funktion [**setrectempty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) erstellt ein leeres Rechteck.</span><span class="sxs-lookup"><span data-stu-id="3d789-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="3d789-105">Ein leeres Rechteck ist ein beliebiges Rechteck, das eine Breite, eine Höhe von 0 (null) oder beides aufweist.</span><span class="sxs-lookup"><span data-stu-id="3d789-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="3d789-106">Die [**isrectempty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) -Funktion bestimmt, ob ein bestimmtes Rechteck leer ist.</span><span class="sxs-lookup"><span data-stu-id="3d789-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="3d789-107">Die [**equalrect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) -Funktion bestimmt, ob zwei Rechtecke identisch sind, d. h., ob Sie die gleichen Koordinaten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3d789-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="3d789-108">Die [**inflaterect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) -Funktion vergrößert oder verringert die Breite oder Höhe eines Rechtecks oder beides.</span><span class="sxs-lookup"><span data-stu-id="3d789-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="3d789-109">Sie kann die Breite von beiden Enden des Rechtecks hinzufügen oder entfernen. die Höhe kann dem oberen und unteren Rand des Rechtecks hinzugefügt oder daraus entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3d789-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="3d789-110">Die [**offsetrect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) -Funktion verschiebt ein Rechteck um einen angegebenen Betrag.</span><span class="sxs-lookup"><span data-stu-id="3d789-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="3d789-111">Er verschiebt das Rechteck durch Hinzufügen der angegebenen x-Amount-, y-Amount-oder x-und y-Beträge zu den Eckkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="3d789-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="3d789-112">Die [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) -Funktion bestimmt, ob ein angegebener Punkt innerhalb eines angegebenen Rechtecks liegt.</span><span class="sxs-lookup"><span data-stu-id="3d789-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="3d789-113">Der Punkt befindet sich im Rechteck, wenn er auf der linken oder oberen Seite liegt oder sich vollständig innerhalb des Rechtecks befindet.</span><span class="sxs-lookup"><span data-stu-id="3d789-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="3d789-114">Der Punkt befindet sich nicht im Rechteck, wenn er sich auf der rechten oder unteren Seite befindet.</span><span class="sxs-lookup"><span data-stu-id="3d789-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="3d789-115">Die [**intersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) -Funktion erstellt ein neues Rechteck, bei dem es sich um die Schnittmenge zweier bestehender Rechtecke handelt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3d789-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="3d789-116">Abbildung mit zwei überlappenden Rechtecke, mit dunkler Schattierung zum Angeben der Schnittmenge</span><span class="sxs-lookup"><span data-stu-id="3d789-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="3d789-117">Die [**unionrect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) -Funktion erstellt ein neues Rechteck, das die Union zweier bestehender Rechtecke darstellt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3d789-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![Abbildung von zwei überlappenden Rechtecke mit dunkler Schattierung, die Bereiche innerhalb der Union, aber nicht innerhalb eines der beiden Rechtecks anzeigt](images/csrec-02.png)

<span data-ttu-id="3d789-119">Informationen zu Funktionen, die Ellipsen und Polygone zeichnen, finden Sie unter [gefüllte Formen](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="3d789-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



