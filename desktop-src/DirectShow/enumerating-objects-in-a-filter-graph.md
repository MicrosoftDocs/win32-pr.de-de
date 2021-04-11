---
description: Auflisten von Objekten in einem Filter Diagramm
ms.assetid: 04a3dbc8-33c4-4b70-930e-686be2f8301f
title: Auflisten von Objekten in einem Filter Diagramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369cd3400d3b7fc9944662ed6d32fd67234af90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124406"
---
# <a name="enumerating-objects-in-a-filter-graph"></a><span data-ttu-id="b8e1b-103">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="b8e1b-103">Enumerating Objects in a Filter Graph</span></span>

<span data-ttu-id="b8e1b-104">Möglicherweise muss eine Anwendung einen bestimmten Filter im Filter Diagramm oder sogar eine bestimmte PIN für einen Filter finden.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-104">An application might need to locate a particular filter in the filter graph, or even a particular pin on a filter.</span></span> <span data-ttu-id="b8e1b-105">Beispielsweise kann eine Schnittstelle verwendet werden, die von einem bestimmten Filter verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-105">For example, it might use an interface that a particular filter exposes.</span></span> <span data-ttu-id="b8e1b-106">Oder es kann ein spezielles Filter Diagramm erstellt werden, und es müssen Methoden auf einzelnen Pins aufgerufen werden, um die Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-106">Or, it might construct a specialized filter graph and need to call methods on individual pins to connect the filters.</span></span> <span data-ttu-id="b8e1b-107">Zu diesem Zweck stellt DirectShow mehrere Methoden zum Aufzählen von Objekten in einem Filter Diagramm bereit.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-107">For this purpose, DirectShow provides several methods for enumerating objects in a filter graph.</span></span>

<span data-ttu-id="b8e1b-108">Die in diesem Abschnitt erläuterten Enumeratoren befolgen das Standardformular, das von com-enumerationsschnittstellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-108">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="b8e1b-109">Weitere Informationen finden Sie im Thema "IEnumXXXX" im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="b8e1b-109">For more information, see the "IEnumXXXX" topic in the Platform SDK.</span></span> <span data-ttu-id="b8e1b-110">Informationen zum Auflisten von Filtern, die auf dem Computer des Benutzers registriert sind, jedoch noch nicht im Filter Diagramm aufgeführt sind, finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b8e1b-110">For information on enumerating filters that are registered on the user's computer, but aren't yet in the filter graph, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="b8e1b-111">Dieser Artikel enthält folgende Themen:</span><span class="sxs-lookup"><span data-stu-id="b8e1b-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="b8e1b-112">Auflisten von Filtern</span><span class="sxs-lookup"><span data-stu-id="b8e1b-112">Enumerating Filters</span></span>](enumerating-filters.md)
-   [<span data-ttu-id="b8e1b-113">Auflisten von Pins</span><span class="sxs-lookup"><span data-stu-id="b8e1b-113">Enumerating Pins</span></span>](enumerating-pins.md)
-   [<span data-ttu-id="b8e1b-114">Auflisten von Medientypen</span><span class="sxs-lookup"><span data-stu-id="b8e1b-114">Enumerating Media Types</span></span>](enumerating-media-types.md)

## <a name="related-topics"></a><span data-ttu-id="b8e1b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8e1b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e1b-116">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="b8e1b-116">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



