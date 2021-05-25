---
description: Erfahren Sie mehr über eine Kombination aus einem oder mehreren Flags, die das Geräteerstellungsverhalten steuern.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad3b5eca7a264e489382d80b336f5b2c660e1a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342915"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="a4707-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="a4707-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="a4707-104">Eine Kombination aus einem oder mehreren Flags, die das Erstellungsverhalten des Geräts steuern.</span><span class="sxs-lookup"><span data-stu-id="a4707-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="a4707-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="a4707-105">\#define</span></span>                                | <span data-ttu-id="a4707-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4707-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4707-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="a4707-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="a4707-108">Das Gerät kann gerichtete Beleuchtungen durchführen.</span><span class="sxs-lookup"><span data-stu-id="a4707-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a4707-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="a4707-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="a4707-110">Das Gerät kann den lokalen Viewer verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4707-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a4707-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="a4707-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="a4707-112">Wenn diese Obergrenze festgelegt ist, unterstützt das Gerät die Farbmaterialzustände D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE und D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="a4707-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="a4707-113">D3DVTXPCAPS \_ NO \_ TEXGEN \_ NONLOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="a4707-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="a4707-114">Das Gerät unterstützt keine Texturgenerierung im nicht lokalen Viewermodus.</span><span class="sxs-lookup"><span data-stu-id="a4707-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="a4707-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="a4707-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="a4707-116">Das Gerät kann Positionslichter (einschließlich Punkt und Punkt) durchführen.</span><span class="sxs-lookup"><span data-stu-id="a4707-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="a4707-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="a4707-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="a4707-118">Das Gerät kann texgen.</span><span class="sxs-lookup"><span data-stu-id="a4707-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="a4707-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="a4707-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="a4707-120">Das Gerät unterstützt D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="a4707-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="a4707-121">D3DVTXPCAPS-TWEENING \_</span><span class="sxs-lookup"><span data-stu-id="a4707-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="a4707-122">Das Gerät kann Scheitelpunkt-Tweening verwenden.</span><span class="sxs-lookup"><span data-stu-id="a4707-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="a4707-123">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="a4707-123">Constant Information</span></span>



| <span data-ttu-id="a4707-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4707-124">Requirement</span></span>                         | <span data-ttu-id="a4707-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a4707-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="a4707-126">Header</span><span class="sxs-lookup"><span data-stu-id="a4707-126">Header</span></span>                   | <span data-ttu-id="a4707-127">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="a4707-127">d3d9caps.h</span></span> |
| <span data-ttu-id="a4707-128">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="a4707-128">Minimum operating system</span></span> | <span data-ttu-id="a4707-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a4707-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a4707-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4707-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4707-131">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a4707-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



