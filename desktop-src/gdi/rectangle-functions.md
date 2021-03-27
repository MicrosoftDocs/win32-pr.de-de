---
description: Die folgenden Funktionen werden mit Rechtecke verwendet.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Rechteck Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215176"
---
# <a name="rectangle-functions"></a><span data-ttu-id="5d608-103">Rechteck Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d608-103">Rectangle Functions</span></span>

<span data-ttu-id="5d608-104">Die folgenden Funktionen werden mit Rechtecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d608-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="5d608-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="5d608-105">Function</span></span>                               | <span data-ttu-id="5d608-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d608-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d608-107">**Copyrect**</span><span class="sxs-lookup"><span data-stu-id="5d608-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="5d608-108">Kopiert die Koordinaten eines Rechtecks in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="5d608-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="5d608-109">**Equalrect**</span><span class="sxs-lookup"><span data-stu-id="5d608-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="5d608-110">Bestimmt, ob die beiden angegebenen Rechtecke gleich sind, indem die Koordinaten ihrer oberen linken und unteren rechten Ecke verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="5d608-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="5d608-111">**Inflaterect**</span><span class="sxs-lookup"><span data-stu-id="5d608-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="5d608-112">Erhöht oder verringert die Breite und Höhe des angegebenen Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="5d608-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="5d608-113">**IntersectRect**</span><span class="sxs-lookup"><span data-stu-id="5d608-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="5d608-114">Berechnet die Schnittmenge zweier Quell Rechtecke und platziert die Koordinaten des Schnittstellen Rechtecks in das Ziel Rechteck.</span><span class="sxs-lookup"><span data-stu-id="5d608-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="5d608-115">**Isrectempty**</span><span class="sxs-lookup"><span data-stu-id="5d608-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="5d608-116">Bestimmt, ob das angegebene Rechteck leer ist.</span><span class="sxs-lookup"><span data-stu-id="5d608-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="5d608-117">**Offsetrect**</span><span class="sxs-lookup"><span data-stu-id="5d608-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="5d608-118">Verschiebt das angegebene Rechteck um die angegebenen Offsets.</span><span class="sxs-lookup"><span data-stu-id="5d608-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="5d608-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="5d608-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="5d608-120">Bestimmt, ob der angegebene Punkt innerhalb des angegebenen Rechtecks liegt.</span><span class="sxs-lookup"><span data-stu-id="5d608-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="5d608-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="5d608-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="5d608-122">Legt die Koordinaten des angegebenen Rechtecks fest.</span><span class="sxs-lookup"><span data-stu-id="5d608-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="5d608-123">**Setrectempty**</span><span class="sxs-lookup"><span data-stu-id="5d608-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="5d608-124">Erstellt ein leeres Rechteck, in dem alle Koordinaten auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="5d608-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="5d608-125">**Subtractrect**</span><span class="sxs-lookup"><span data-stu-id="5d608-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="5d608-126">Bestimmt die Koordinaten eines Rechtecks, das durch Subtraktion eines Rechtecks von einem anderen formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="5d608-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="5d608-127">**Unionrect**</span><span class="sxs-lookup"><span data-stu-id="5d608-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="5d608-128">Erstellt die Union von zwei Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="5d608-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



