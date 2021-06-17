---
description: Erfahren Sie mehr über Alphablending. Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen.
ms.assetid: 553b0bc8-1bd8-4282-9260-cdc5f2b8788d
title: Alphablending (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd79c622778e17c5acb9b17d52b6d5db278b1508
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262002"
---
# <a name="alpha-blending-direct3d-9"></a><span data-ttu-id="25c85-104">Alphablending (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-104">Alpha Blending (Direct3D 9)</span></span>

<span data-ttu-id="25c85-105">Alphablending wird verwendet, um ein Bild mit transparenten oder halbtransparenten Pixeln anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="25c85-105">Alpha blending is used to display an image that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="25c85-106">Zusätzlich zu einem roten, grünen und blauen Farbkanal verfügt jedes Pixel in einer Alphabitmap über eine Transparenzkomponente, die als Alphakanal bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="25c85-106">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its alpha channel.</span></span> <span data-ttu-id="25c85-107">Der Alphakanal enthält in der Regel so viele Bits wie ein Farbkanal.</span><span class="sxs-lookup"><span data-stu-id="25c85-107">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="25c85-108">Beispielsweise kann ein 8-Bit-Alphakanal 256 Transparenzebenen darstellen, von 0 (das gesamte Pixel ist transparent) bis 255 (das gesamte Pixel ist nicht transparent).</span><span class="sxs-lookup"><span data-stu-id="25c85-108">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire pixel is transparent) to 255 (the entire pixel is opaque).</span></span> <span data-ttu-id="25c85-109">Die folgende Liste zeigt einige Sondereffekte, die Sie mithilfe von Alphablending erstellen können.</span><span class="sxs-lookup"><span data-stu-id="25c85-109">The list below shows some special effects you can create using alpha blending.</span></span>

<span data-ttu-id="25c85-110">Farbe kann mit oder ohne Alphawerte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="25c85-110">Color can be defined with or without alpha values.</span></span> <span data-ttu-id="25c85-111">Farbe ohne Alpha ist RGB-Farbe, wobei Alpha als ARGB gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="25c85-111">Color without alpha is RGB color with alpha is stored as ARGB.</span></span> <span data-ttu-id="25c85-112">Scheitelpunktdaten, Materialdaten und Texturdaten können verwendet werden, um die Transparenz des Objekts zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="25c85-112">Vertex data, material data and texture data can be used to give object's transparency.</span></span> <span data-ttu-id="25c85-113">Der Framepuffer kann auch verwendet werden, um Transparenzeffekte zu generieren.</span><span class="sxs-lookup"><span data-stu-id="25c85-113">The frame buffer can also be used to generate transparency effects.</span></span>

-   [<span data-ttu-id="25c85-114">Vertex Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-114">Vertex Alpha (Direct3D 9)</span></span>](vertex-alpha.md)
-   [<span data-ttu-id="25c85-115">Material Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-115">Material Alpha (Direct3D 9)</span></span>](material-alpha.md)
-   [<span data-ttu-id="25c85-116">Textur alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-116">Texture Alpha (Direct3D 9)</span></span>](texture-alpha.md)
-   [<span data-ttu-id="25c85-117">Framepuffer alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-117">Frame Buffer Alpha (Direct3D 9)</span></span>](frame-buffer-alpha.md)
-   [<span data-ttu-id="25c85-118">Renderziel Alpha (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-118">Render Target Alpha (Direct3D 9)</span></span>](render-target-alpha.md)

<span data-ttu-id="25c85-119">Beispiele, die Alpha veranschaulichen, sind:</span><span class="sxs-lookup"><span data-stu-id="25c85-119">Samples that demonstrate alpha include:</span></span>

-   [<span data-ttu-id="25c85-120">Aussteigend (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-120">Billboarding (Direct3D 9)</span></span>](billboarding.md)
-   [<span data-ttu-id="25c85-121">Clouds, Smoke und Trails (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-121">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>](clouds--smoke--and-vapor-trails.md)
-   [<span data-ttu-id="25c85-122">Fire, Flares und Explosionen (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25c85-122">Fire, Flares, and Explosions (Direct3D 9)</span></span>](fire--flares--and-explosions.md)

## <a name="related-topics"></a><span data-ttu-id="25c85-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="25c85-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25c85-124">Direct3D-Rendering</span><span class="sxs-lookup"><span data-stu-id="25c85-124">Direct3D Rendering</span></span>](direct3d-rendering.md)
</dt> </dl>

 

 



