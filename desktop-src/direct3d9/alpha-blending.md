---
description: Alpha Blending wird zum Anzeigen eines Bilds mit transparenten oder semitransparenten Pixeln verwendet.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Alpha Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f4ae2883c7a9a92ba1b62306dc26bf09d0d9947
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127240"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="a1c1e-103">Alpha Mischung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-103">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="a1c1e-104">Alpha Blending wird zum Anzeigen eines Bilds mit transparenten oder semitransparenten Pixeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-104">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="a1c1e-105">Zusätzlich zu einem roten, grünen und blauen Farbkanal weist jedes Pixel in einer Alpha Bitmap eine Transparenz Komponente auf, die als Alphakanal bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="a1c1e-106">Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="a1c1e-107">Ein 8-Bit-Alphakanal kann z. b. 256 Ebenen der Transparenz darstellen, von 0 (das gesamte Pixel ist transparent) bis 255 (das gesamte Pixel ist nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="a1c1e-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="a1c1e-108">Die nachstehende Liste zeigt einige besondere Effekte, die Sie mithilfe von Alpha Blending erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-108">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="a1c1e-109">Die Farbe kann mit oder ohne Alpha Werte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-109">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="a1c1e-110">Farbe ohne Alpha ist RGB-Farbe, wobei Alpha als ARGB gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-110">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="a1c1e-111">Vertexdaten, Materialdaten und Textur Daten können verwendet werden, um die Transparenz von Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-111">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="a1c1e-112">Der Frame Puffer kann auch zum Generieren von Transparenz Effekten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1c1e-112">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="a1c1e-113">Vertex Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-113">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="a1c1e-114">Material Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-114">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="a1c1e-115">Textur Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-115">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="a1c1e-116">Frame-Puffer Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-116">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="a1c1e-117">Renderziel Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-117">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="a1c1e-118">Zu den Beispielen, die Alpha veranschaulichen, gehören:</span><span class="sxs-lookup"><span data-stu-id="a1c1e-118">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="a1c1e-119">Fakboardingvorgang (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-119">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="a1c1e-120">Clouds, Rauch und Dampfwege (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-120">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="a1c1e-121">Feuer, Flares und Explosionen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a1c1e-121">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="a1c1e-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a1c1e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1c1e-123">Direct3D-Rendering</span><span class="sxs-lookup"><span data-stu-id="a1c1e-123">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



