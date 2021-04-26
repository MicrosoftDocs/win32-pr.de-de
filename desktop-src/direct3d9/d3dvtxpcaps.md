---
description: Eine Kombination aus einem oder mehreren Flags, die das Erstellungsverhalten des Geräts steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7e5d423169e561df28b5d69017c77a71e183
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998657"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="15dd3-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="15dd3-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="15dd3-104">Eine Kombination aus einem oder mehreren Flags, die das Erstellungsverhalten des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="15dd3-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="15dd3-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="15dd3-105">\#define</span></span>                                | <span data-ttu-id="15dd3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15dd3-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dd3-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="15dd3-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="15dd3-108">Das Gerät kann gerichtete Beleuchtungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="15dd3-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="15dd3-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="15dd3-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="15dd3-110">Das Gerät kann den lokalen Viewer verwenden.</span><span class="sxs-lookup"><span data-stu-id="15dd3-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="15dd3-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="15dd3-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="15dd3-112">Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farbmaterialzustände D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE und D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="15dd3-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="15dd3-113">D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="15dd3-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="15dd3-114">Das Gerät unterstützt keine Texturgenerierung im nicht lokalen Viewermodus.</span><span class="sxs-lookup"><span data-stu-id="15dd3-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="15dd3-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="15dd3-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="15dd3-116">Das Gerät kann Positionslichter (einschließlich Punkt und Punkt) durchführen.</span><span class="sxs-lookup"><span data-stu-id="15dd3-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="15dd3-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="15dd3-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="15dd3-118">Das Gerät kann texgen.</span><span class="sxs-lookup"><span data-stu-id="15dd3-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="15dd3-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="15dd3-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="15dd3-120">Das Gerät unterstützt D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="15dd3-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="15dd3-121">D3DVTXPCAPS-TWEENING \_</span><span class="sxs-lookup"><span data-stu-id="15dd3-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="15dd3-122">Das Gerät kann Scheitelpunkt-Tweening verwenden.</span><span class="sxs-lookup"><span data-stu-id="15dd3-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="15dd3-123">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="15dd3-123">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="15dd3-124">Header</span><span class="sxs-lookup"><span data-stu-id="15dd3-124">Header</span></span>                   | <span data-ttu-id="15dd3-125">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="15dd3-125">d3d9caps.h</span></span> |
| <span data-ttu-id="15dd3-126">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="15dd3-126">Minimum operating system</span></span> | <span data-ttu-id="15dd3-127">Windows 98</span><span class="sxs-lookup"><span data-stu-id="15dd3-127">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="15dd3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15dd3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15dd3-129">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="15dd3-129">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



