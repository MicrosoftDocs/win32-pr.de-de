---
description: Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2ffff3d1dcc1f68912847b9ce1677c2031189c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393206"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="a5820-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="a5820-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="a5820-104">Eine Kombination aus einem oder mehreren Flags, die das Erstellungs Verhalten des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="a5820-104">A combination of one or more flags that control the device create behavior.</span></span>



|                                         |                                                                                                                                                                                                    |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5820-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="a5820-105">\#define</span></span>                                | <span data-ttu-id="a5820-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5820-106">Description</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="a5820-107">D3DVTXPCAPS \_ DirectionalLights</span><span class="sxs-lookup"><span data-stu-id="a5820-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="a5820-108">Das Gerät kann direktionale Lichter ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5820-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a5820-109">D3DVTXPCAPS \_ localviewer</span><span class="sxs-lookup"><span data-stu-id="a5820-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="a5820-110">Das Gerät kann den lokalen Viewer ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5820-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a5820-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="a5820-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="a5820-112">Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farb Materialzustände: D3DRS \_ AmbientMaterialSource, D3DRS \_ DiffuseMaterialSource, D3DRS \_ emissivematerialsource und D3DRS \_ SpecularMaterialSource.</span><span class="sxs-lookup"><span data-stu-id="a5820-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="a5820-113">D3DVTXPCAPS \_ keine \_ TEXGEN- \_ nonlocalviewer</span><span class="sxs-lookup"><span data-stu-id="a5820-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="a5820-114">Das Gerät unterstützt keine Textur Generierung im nicht lokalen Viewer-Modus.</span><span class="sxs-lookup"><span data-stu-id="a5820-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="a5820-115">D3DVTXPCAPS \_ positionallights</span><span class="sxs-lookup"><span data-stu-id="a5820-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="a5820-116">Das Gerät kann Positionsleuchten (einschließlich Punkt und Punkt) verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5820-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="a5820-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="a5820-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="a5820-118">Das Gerät kann TEXGEN ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5820-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="a5820-119">D3DVTXPCAPS \_ TEXGEN- \_ spheremap</span><span class="sxs-lookup"><span data-stu-id="a5820-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="a5820-120">Das Gerät unterstützt D3DTSS \_ TCI \_ sphiermap.</span><span class="sxs-lookup"><span data-stu-id="a5820-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="a5820-121">D3DVTXPCAPS- \_ twiening</span><span class="sxs-lookup"><span data-stu-id="a5820-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="a5820-122">Das Gerät kann Vertex-twiening durchführen.</span><span class="sxs-lookup"><span data-stu-id="a5820-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="a5820-123">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="a5820-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="a5820-124">Header</span><span class="sxs-lookup"><span data-stu-id="a5820-124">Header</span></span>                   | <span data-ttu-id="a5820-125">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="a5820-125">d3d9caps.h</span></span> |
| <span data-ttu-id="a5820-126">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="a5820-126">Minimum operating system</span></span> | <span data-ttu-id="a5820-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a5820-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a5820-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5820-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5820-129">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a5820-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



