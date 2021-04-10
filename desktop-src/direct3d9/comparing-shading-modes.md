---
description: Im Flatshading-Modus wird die folgende Pyramide mit einem Spitzen Rand zwischen angrenzenden Gesichtern angezeigt. Im Modus "Gouraud-Schattierung" werden Schattierungs Werte jedoch über den gesamten Rand hinweg interpoliert, und die endgültige Darstellung ist eine gekrümmte Oberfläche.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Vergleichen von Schattierungs Modi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127777"
---
# <a name="comparing-shading-modes-direct3d-9"></a><span data-ttu-id="e24d5-104">Vergleichen von Schattierungs Modi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e24d5-104">Comparing Shading Modes (Direct3D 9)</span></span>

<span data-ttu-id="e24d5-105">Im Flatshading-Modus wird die folgende Pyramide mit einem Spitzen Rand zwischen angrenzenden Gesichtern angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e24d5-105">In flat shading mode, the following pyramid is displayed with a sharp edge between adjoining faces.</span></span> <span data-ttu-id="e24d5-106">Im Modus "Gouraud-Schattierung" werden Schattierungs Werte jedoch über den gesamten Rand hinweg interpoliert, und die endgültige Darstellung ist eine gekrümmte Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e24d5-106">In Gouraud shading mode, however, shading values are interpolated across the edge, and the final appearance is of a curved surface.</span></span>

![Abbildung einer Pyramide mit Spitzen Kanten und Pfeilen, die auf das Gesicht "normale" zeigen](images/shade2.png)

<span data-ttu-id="e24d5-108">Die Schattierung von Gouraud-Schattierungen ist eine realistischere Oberfläche als flache Schattierung.</span><span class="sxs-lookup"><span data-stu-id="e24d5-108">Gouraud shading lights flat surfaces more realistically than flat shading.</span></span> <span data-ttu-id="e24d5-109">Ein Gesicht im Flatshading-Modus ist eine einheitliche Farbe, aber die Schattierung von Gouraud ermöglicht, dass das Licht besser auf ein Gesicht fällt.</span><span class="sxs-lookup"><span data-stu-id="e24d5-109">A face in the flat shading mode is a uniform color, but Gouraud shading enables light to fall across a face more correctly.</span></span> <span data-ttu-id="e24d5-110">Dieser Effekt ist besonders offensichtlich, wenn eine Punktquelle in der Nähe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e24d5-110">This effect is particularly obvious if there is a nearby point source.</span></span>

<span data-ttu-id="e24d5-111">Durch die Schattierung von Gouraud werden die Spitzen Ränder zwischen Polygonen, die mit flacher Schattierung sichtbar sind, glätten.</span><span class="sxs-lookup"><span data-stu-id="e24d5-111">Gouraud shading smoothes the sharp edges between polygons that are visible with flat shading.</span></span> <span data-ttu-id="e24d5-112">Allerdings kann dies zu Mach-Bändern führen, bei denen es sich um Farb-oder Lichtbänder handelt, die nicht nahtlos über angrenzende Polygone gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="e24d5-112">However, it can result in mach bands, which are bands of color or light that are not smoothly blended across adjacent polygons.</span></span> <span data-ttu-id="e24d5-113">Die Anwendung kann die Darstellung von Mach-Bändern verringern, indem die Anzahl der Polygone in einem Objekt erhöht wird, die Bildschirmauflösung erhöht oder die Farbtiefe der Anwendung erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="e24d5-113">Your application can reduce the appearance of Mach bands by increasing the number of polygons in an object, increasing screen resolution, or increasing the color depth of the application.</span></span>

<span data-ttu-id="e24d5-114">Bei der Schattierung von Gouraud können einige Details übersehen werden.</span><span class="sxs-lookup"><span data-stu-id="e24d5-114">Gouraud shading can miss some details.</span></span> <span data-ttu-id="e24d5-115">Beispielsweise ist in der folgenden Abbildung ein Spotlight vollständig in einem Polygon Gesicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="e24d5-115">For example, in the following illustration, a spotlight is completely contained within a polygon face.</span></span>

![Abbildung eines Spotlight in einem Polygon Gesicht](images/gouraud.png)

<span data-ttu-id="e24d5-117">In diesem Fall würde die Schattierung von Gouraud, die zwischen Scheitel Punkten interpoliert, das Spotlight vollständig übersehen. das Gesicht würde so gerendert werden, als wäre der Spotlight nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e24d5-117">In this case, Gouraud shading, which interpolates between vertices, would miss the spotlight altogether; the face would be rendered as though the spotlight did not exist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e24d5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e24d5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e24d5-119">Schattierung</span><span class="sxs-lookup"><span data-stu-id="e24d5-119">Shading</span></span>](shading.md)
</dt> </dl>

 

 



