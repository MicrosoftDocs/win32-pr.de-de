---
title: Farbräume
description: Das menschliche Auge ist häufig in der Lage, viel mehr Farben zu erkennen, als digitale Geräte reproduzieren können.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS), Farbbereiche
- WCS (Windows Color System), Farbbereiche
- Bild Farbverwaltung, Farbbereiche
- Farbverwaltung, Farbbereiche
- Farben, Farbbereiche
- Farbbereiche, Informationen
- Farbkanäle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ded035d773956f09949b51cafc6680f66725b82
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "106363867"
---
# <a name="color-spaces"></a><span data-ttu-id="4bfc9-110">Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-110">Color Spaces</span></span>

<span data-ttu-id="4bfc9-111">Das menschliche Auge ist häufig in der Lage, viel mehr Farben zu erkennen, als digitale Geräte reproduzieren können.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-111">The human eye is often able to detect many more colors than digital devices can reproduce.</span></span> <span data-ttu-id="4bfc9-112">Wenn Sie z. b. eine leere, weiße Seite des Papiers betrachten, werden Sie wahrscheinlich mindestens 100 verschiedene weiß-Schattierungen erkennen.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-112">For instance, if you look at a blank, white page of paper, your eye is probably detecting at least 100 distinct shades of white.</span></span> <span data-ttu-id="4bfc9-113">Eine weiße Wand kann problemlos 1500-Schattierungen weiß.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-113">A white wall can easily have 1500 shades of white.</span></span>

<span data-ttu-id="4bfc9-114">Qualitativ hochwertige digitale Kameras, Scanner und andere Abbild Erfassungsgeräte können auch Hunderttausende oder sogar Millionen von Farben erkennen.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-114">High-quality digital cameras, scanners, and other image acquisition devices can also detect hundreds of thousands or even millions of colors.</span></span> <span data-ttu-id="4bfc9-115">Da so viele erkennbare Farben vorhanden sind, haben Abbild Fachleute Modelle zum Angeben von Farben erfunden.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-115">Because of the presence of so many detectable colors, imaging professionals have invented models for specifying colors.</span></span> <span data-ttu-id="4bfc9-116">Diese Modelle werden als *Farbbereiche* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-116">These models are called *color spaces*.</span></span>

<span data-ttu-id="4bfc9-117">Der Grund dafür, dass diese Modelle als Farbbereiche bezeichnet werden, besteht darin, dass die meisten von Ihnen in einem 2D-, 3D-oder 4-d-Koordinatensystem ähnlich einem kartesischen Koordinatensystem zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-117">The reason these models are referred to as color spaces is that most of them can be mapped into a 2-D, 3-D, or 4-D coordinate system similar to a Cartesian coordinate system.</span></span> <span data-ttu-id="4bfc9-118">Daher können Farben als Zusammensetzung aus Koordinaten in einem 2D-, 3D-oder 4-d-Raum bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-118">Hence colors can be said to be composed of coordinates in a 2-D, 3-D, or 4-D space.</span></span> <span data-ttu-id="4bfc9-119">Die Farbkomponenten in einem Farbraum werden auch als *Farbkanäle* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-119">The color components in a color space are also referred to as *color channels*.</span></span>

<span data-ttu-id="4bfc9-120">Einige Farbbereiche sollen unabhängig von Geräten sein, die zum Entwickeln von Farbbildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-120">Some color spaces are intended to be independent of any device that is used to produce color images.</span></span> <span data-ttu-id="4bfc9-121">Einige sind sehr Geräte abhängig.</span><span class="sxs-lookup"><span data-stu-id="4bfc9-121">Some are very device dependent.</span></span> <span data-ttu-id="4bfc9-122">In den folgenden Abschnitten werden sowohl Geräte abhängige als auch geräteunabhängige Farbbereiche behandelt:</span><span class="sxs-lookup"><span data-stu-id="4bfc9-122">Both device-dependent and device-independent color spaces are discussed in the following sections:</span></span>

-   [<span data-ttu-id="4bfc9-123">RGB-Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-123">RGB Color Spaces</span></span>](rgb-color-spaces.md)
-   [<span data-ttu-id="4bfc9-124">HSV-Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-124">HSV Color Spaces</span></span>](hsv-color-spaces.md)
-   [<span data-ttu-id="4bfc9-125">HLS-Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-125">HLS Color Spaces</span></span>](hls-color-spaces.md)
-   [<span data-ttu-id="4bfc9-126">CMY- und CMYK-Farbraum</span><span class="sxs-lookup"><span data-stu-id="4bfc9-126">CMY and CMYK Color Spaces</span></span>](cmy-and-cmyk-color-spaces.md)
-   [<span data-ttu-id="4bfc9-127">Geräteabhängige Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-127">Device-Dependent Color Spaces</span></span>](device-dependent-color-spaces.md)
-   [<span data-ttu-id="4bfc9-128">Geräteunabhängige Farbräume</span><span class="sxs-lookup"><span data-stu-id="4bfc9-128">Device-Independent Color Spaces</span></span>](device-independent-color-spaces.md)

 

 




