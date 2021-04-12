---
description: 'Die Position, die Geschwindigkeit und die Ausrichtung von Soundquellen und Listenern im 3D-Raum werden durch kartesische Koordinaten dargestellt, bei denen es sich um Werte auf drei Achsen handelt: die x-Achse, die y-Achse und die z-Achse.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Koordinaten von 3D-Raum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216793"
---
# <a name="coordinates-of-3d-space"></a><span data-ttu-id="3c19d-103">Koordinaten von 3D-Raum</span><span class="sxs-lookup"><span data-stu-id="3c19d-103">Coordinates of 3D Space</span></span>

<span data-ttu-id="3c19d-104">Die Position, die Geschwindigkeit und die Ausrichtung von Soundquellen und Listenern im 3D-Raum werden durch kartesische Koordinaten dargestellt, bei denen es sich um Werte auf drei Achsen handelt: die x-Achse, die y-Achse und die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="3c19d-104">The position, velocity, and orientation of sound sources and listeners in 3D space are represented by Cartesian coordinates, which are values on three axes: the x-axis, the y-axis, and the z-axis.</span></span>

<span data-ttu-id="3c19d-105">Die Achsen sind relativ zu einem von der Anwendung festgelegten Standpunkt.</span><span class="sxs-lookup"><span data-stu-id="3c19d-105">The axes are relative to a viewpoint established by the application.</span></span> <span data-ttu-id="3c19d-106">Werte auf der x-Achse steigen von links nach rechts, auf der y-Achse von unten nach oben und auf der z-Achse von fast zu weit.</span><span class="sxs-lookup"><span data-stu-id="3c19d-106">Values on the x-axis increase from left to right, on the y-axis from down to up, and on the z-axis from near to far.</span></span>

<span data-ttu-id="3c19d-107">Die **X3DAUDIO- \_ Vektor** Struktur enthält Werte, die die Position, die Geschwindigkeit oder die Ausrichtung auf den drei Achsen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3c19d-107">The **X3DAUDIO\_VECTOR** structure contains values describing position, velocity, or orientation on the three axes.</span></span>

<span data-ttu-id="3c19d-108">Die Vektoren werden in der Reihenfolge (x, y, z) als drei Werte in Klammern eingeschlossen und durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="3c19d-108">Conventionally, vectors are expressed as three values enclosed in parentheses and separated by commas, in the order (x, y, z).</span></span>

<span data-ttu-id="3c19d-109">Für die Position befinden sich die Werte in benutzerdefinierten Welteinheiten.</span><span class="sxs-lookup"><span data-stu-id="3c19d-109">For position, the values are in user-defined world units.</span></span>

<span data-ttu-id="3c19d-110">Der Vektor beschreibt die Geschwindigkeit der Bewegung entlang jeder Achse in Welteinheiten pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3c19d-110">For velocity, the vector describes the rate of movement along each axis in world units per second.</span></span>

<span data-ttu-id="3c19d-111">Aus Gründen der Ausrichtung befinden sich die Werte in beliebigen Einheiten und sind relativ zueinander.</span><span class="sxs-lookup"><span data-stu-id="3c19d-111">For orientation, the values are in arbitrary units, and they are relative to one another.</span></span> <span data-ttu-id="3c19d-112">Wenn z. b. die Basis Ansicht der 3D-Welt dem Horizont Nordweg zusteht und die Ausrichtung des Listener (-1, 0, 1) ist, wird der Listener mit Nordwest angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3c19d-112">For example, if the base view of the 3D world is facing north toward the horizon, and the orientation of the listener is (-1, 0, 1), then the listener is facing northwest.</span></span> <span data-ttu-id="3c19d-113">Da sich die Werte in einem Vektor nicht in absoluten Einheiten befinden, könnte der Vektor gleichermaßen als (-5, 0, 5) oder (-0,25, 0, 0,25) ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="3c19d-113">Because the values within a vector are not in absolute units, the vector equally could be expressed as (-5, 0, 5) or (-0.25, 0, 0.25).</span></span>

<span data-ttu-id="3c19d-114">3D-Vektoren arbeiten ähnlich wie 2D-Vektoren, aber mit einer zusätzlichen Achse in der nach-unten-Richtung.</span><span class="sxs-lookup"><span data-stu-id="3c19d-114">3D vectors work much like 2D vectors, but with an additional axis in the up-down direction.</span></span> <span data-ttu-id="3c19d-115">Sie können sehen, wie Vektoren im 2D-Raum funktionieren, indem Sie Sie auf einem Blatt mit Diagramm Papier zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3c19d-115">You can see how vectors work in 2D space by drawing them on a sheet of graph paper.</span></span> <span data-ttu-id="3c19d-116">Lassen Sie die Werte von unten nach oben im Papier und von links nach rechts vergrößern.</span><span class="sxs-lookup"><span data-stu-id="3c19d-116">Let the values increase from the bottom to the top of the paper, and from left to right.</span></span> <span data-ttu-id="3c19d-117">Eine Linie, die von (0,0) bis (1, 1) gezeichnet wird, hat dieselbe Ausrichtung bzw. Richtung wie eine, die von (0,0) bis (5, 5) gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3c19d-117">A line drawn from (0, 0) to (1, 1) has the same orientation, or direction, as one drawn from (0, 0) to (5, 5).</span></span> <span data-ttu-id="3c19d-118">Die zweite Zeile weist jedoch auf eine größere Entfernung oder Geschwindigkeit hin.</span><span class="sxs-lookup"><span data-stu-id="3c19d-118">However, the second line indicates a greater distance, or velocity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c19d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c19d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c19d-120">Allgemeine audiokonzepte</span><span class="sxs-lookup"><span data-stu-id="3c19d-120">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="3c19d-121">X3DAudio Übersicht</span><span class="sxs-lookup"><span data-stu-id="3c19d-121">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> </dl>

 

 



