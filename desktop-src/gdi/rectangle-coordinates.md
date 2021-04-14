---
description: Eine Anwendung muss eine Rect-Struktur verwenden, um ein Rechteck zu definieren.
ms.assetid: 93c63dcb-6c8e-4c8b-aa19-6f8952d75e2e
title: Rechteck Koordinaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8a3fbc3f42c6d69a3d0eac6555b85fbfc1eecb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993902"
---
# <a name="rectangle-coordinates"></a><span data-ttu-id="8c15c-103">Rechteck Koordinaten</span><span class="sxs-lookup"><span data-stu-id="8c15c-103">Rectangle Coordinates</span></span>

<span data-ttu-id="8c15c-104">Eine Anwendung muss eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur verwenden, um ein Rechteck zu definieren.</span><span class="sxs-lookup"><span data-stu-id="8c15c-104">An application must use a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to define a rectangle.</span></span> <span data-ttu-id="8c15c-105">Die-Struktur gibt die Koordinaten zweier Punkte an: die linke obere und untere rechte Ecke des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="8c15c-105">The structure specifies the coordinates of two points: the upper left and lower right corners of the rectangle.</span></span> <span data-ttu-id="8c15c-106">Die Seiten des Rechtecks werden von diesen beiden Punkten erweitert und sind parallel zur x-und y-Achse.</span><span class="sxs-lookup"><span data-stu-id="8c15c-106">The sides of the rectangle extend from these two points and are parallel to the x-axis and y-axis.</span></span>

<span data-ttu-id="8c15c-107">Die Koordinaten Werte für ein Rechteck werden als ganze Zahlen mit Vorzeichen ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="8c15c-107">The coordinate values for a rectangle are expressed as signed integers.</span></span> <span data-ttu-id="8c15c-108">Der Koordinaten Wert der rechten Seite eines Rechtecks muss größer sein als der Wert der linken Seite.</span><span class="sxs-lookup"><span data-stu-id="8c15c-108">The coordinate value of a rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="8c15c-109">Ebenso muss der Koordinaten Wert des unteren Werts größer als der obere Wert sein.</span><span class="sxs-lookup"><span data-stu-id="8c15c-109">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

<span data-ttu-id="8c15c-110">Da Anwendungen Rechtecke für viele verschiedene Zwecke verwenden können, verwenden die Rechteck Funktionen keine explizite Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="8c15c-110">Because applications can use rectangles for many different purposes, the rectangle functions do not use an explicit unit of measure.</span></span> <span data-ttu-id="8c15c-111">Stattdessen werden alle Rechteck Koordinaten und-Dimensionen in signierten, logischen Werten angegeben.</span><span class="sxs-lookup"><span data-stu-id="8c15c-111">Instead, all rectangle coordinates and dimensions are given in signed, logical values.</span></span> <span data-ttu-id="8c15c-112">Der Mapping-Modus und die Funktion, in der das Rechteck verwendet wird, bestimmen die Maßeinheiten.</span><span class="sxs-lookup"><span data-stu-id="8c15c-112">The mapping mode and the function in which the rectangle is used determine the units of measure.</span></span> <span data-ttu-id="8c15c-113">Weitere Informationen zu Koordinaten und Karten Modi finden Sie unter [Koordinaten Bereiche und Transformationen](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="8c15c-113">For more information about coordinates and mapping modes, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

 
