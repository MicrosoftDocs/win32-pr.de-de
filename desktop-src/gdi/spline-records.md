---
description: Spline-Datensätze stellen die quadratischen Kurven (d. h. Quadratische b-Splines) dar, die von TrueType verwendet werden.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Spline-Datensätze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755840"
---
# <a name="spline-records"></a><span data-ttu-id="2c076-103">Spline-Datensätze</span><span class="sxs-lookup"><span data-stu-id="2c076-103">Spline Records</span></span>

<span data-ttu-id="2c076-104">Spline-Datensätze stellen die quadratischen Kurven (d. h. Quadratische b-Splines) dar, die von TrueType verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c076-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="2c076-105">Ein Spline-Datensatz beginnt mit dem letzten Punkt im vorherigen Datensatz (oder für den ersten Datensatz in der Kontur mit dem Ausgangspunkt).</span><span class="sxs-lookup"><span data-stu-id="2c076-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="2c076-106">Für den ersten Spline-Datensatz befinden sich der Anfangspunkt und der letzte Punkt im Datensatz in der Symbol Gliederung.</span><span class="sxs-lookup"><span data-stu-id="2c076-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="2c076-107">Für alle anderen Spline-Datensätze befindet sich nur der letzte Punkt in der Symbol Gliederung.</span><span class="sxs-lookup"><span data-stu-id="2c076-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="2c076-108">Alle anderen Punkte in den Spline-Datensätzen befinden sich außerhalb der Symbol Gliederung und müssen als Steuerpunkte der b-Splines gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="2c076-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="2c076-109">Der letzte Spline-oder polyliniendatensatz in einer Kontur endet immer mit dem Anfangspunkt der Kontur.</span><span class="sxs-lookup"><span data-stu-id="2c076-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="2c076-110">Durch diese Anordnung wird sichergestellt, dass jede Kontur geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="2c076-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="2c076-111">Da b-Splines drei Punkte benötigen (ein Punkt von der Symbol Gliederung zwischen zwei Punkten, die sich auf dem Umriss befinden), müssen Sie einige Berechnungen durchführen, wenn ein Spline-Datensatz mehr als einen Off-Kurven Punkt enthält.</span><span class="sxs-lookup"><span data-stu-id="2c076-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="2c076-112">Wenn ein Spline-Datensatz z. b. drei Punkte (a, B und C) enthält und es sich nicht um den ersten Datensatz handelt, werden die Punkte a und B außerhalb der Symbol Gliederung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c076-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="2c076-113">Um Punkt A zu interpretieren, verwenden Sie die aktuelle Position (die sich immer auf der Symbol Gliederung befindet) und den Punkt auf der Symbol Gliederung zwischen den Punkten A und B. Um den Mittelpunkt (M) zwischen A und B zu ermitteln, können Sie die folgende Berechnung ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c076-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="2c076-114">M = A + (B A)/2</span><span class="sxs-lookup"><span data-stu-id="2c076-114">M = A + (B A)/2</span></span>

<span data-ttu-id="2c076-115">Der Mittelpunkt zwischen aufeinanderfolgenden offumriss-Punkten in einem Spline-Datensatz ist ein Punkt auf der Symbol Gliederung, gemäß der Definition des in TrueType-Schriftarten verwendeten Spline-Formats.</span><span class="sxs-lookup"><span data-stu-id="2c076-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="2c076-116">Wenn die aktuelle Position durch P festgelegt wird, sind die beiden quadratischen Splines, die von diesem Spline-Datensatz definiert werden, (P, A, M) und (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="2c076-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



