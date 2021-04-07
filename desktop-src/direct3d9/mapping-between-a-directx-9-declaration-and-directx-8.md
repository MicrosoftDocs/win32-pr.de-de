---
title: Zuordnung zwischen d3d9-und D3D8-Deklarationen
description: In dieser Tabelle werden Member einer D3DVERTEXELEMENT9-Deklaration einer Direct3D 8-Deklaration zugeordnet.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745552"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="72df2-103">Zuordnung zwischen d3d9-und D3D8-Deklarationen</span><span class="sxs-lookup"><span data-stu-id="72df2-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="72df2-104">In dieser Tabelle werden Member einer [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Deklaration einer Direct3D 8-Deklaration zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="72df2-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="72df2-105">Direct3D 9-Nutzung</span><span class="sxs-lookup"><span data-stu-id="72df2-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="72df2-106">Direct3D 9-Verwendungs Index</span><span class="sxs-lookup"><span data-stu-id="72df2-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="72df2-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="72df2-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="72df2-108">D3DDECLUSAGE- \_ Position</span><span class="sxs-lookup"><span data-stu-id="72df2-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="72df2-109">0</span><span class="sxs-lookup"><span data-stu-id="72df2-109">0</span></span>                      | <span data-ttu-id="72df2-110">D3DVSDE- \_ Position</span><span class="sxs-lookup"><span data-stu-id="72df2-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="72df2-111">D3DDECLUSAGE- \_ Position</span><span class="sxs-lookup"><span data-stu-id="72df2-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="72df2-112">1</span><span class="sxs-lookup"><span data-stu-id="72df2-112">1</span></span>                      | <span data-ttu-id="72df2-113">D3DVSDE \_ POSITION2</span><span class="sxs-lookup"><span data-stu-id="72df2-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="72df2-114">D3DDECLUSAGE \_ Normal</span><span class="sxs-lookup"><span data-stu-id="72df2-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="72df2-115">0</span><span class="sxs-lookup"><span data-stu-id="72df2-115">0</span></span>                      | <span data-ttu-id="72df2-116">D3DVSDE \_ Normal</span><span class="sxs-lookup"><span data-stu-id="72df2-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="72df2-117">D3DDECLUSAGE \_ Normal</span><span class="sxs-lookup"><span data-stu-id="72df2-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="72df2-118">1</span><span class="sxs-lookup"><span data-stu-id="72df2-118">1</span></span>                      | <span data-ttu-id="72df2-119">D3DVSDE \_ NORMAL2</span><span class="sxs-lookup"><span data-stu-id="72df2-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="72df2-120">D3DDECLUSAGE \_ blendweight</span><span class="sxs-lookup"><span data-stu-id="72df2-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="72df2-121">0</span><span class="sxs-lookup"><span data-stu-id="72df2-121">0</span></span>                      | <span data-ttu-id="72df2-122">D3DVSDE \_ blendweight</span><span class="sxs-lookup"><span data-stu-id="72df2-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="72df2-123">D3DDECLUSAGE \_ blendindices</span><span class="sxs-lookup"><span data-stu-id="72df2-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="72df2-124">0</span><span class="sxs-lookup"><span data-stu-id="72df2-124">0</span></span>                      | <span data-ttu-id="72df2-125">D3DVSDE \_ blendindices</span><span class="sxs-lookup"><span data-stu-id="72df2-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="72df2-126">D3DDECLUSAGE \_ Psize</span><span class="sxs-lookup"><span data-stu-id="72df2-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="72df2-127">0</span><span class="sxs-lookup"><span data-stu-id="72df2-127">0</span></span>                      | <span data-ttu-id="72df2-128">D3DVSDE \_ Psize</span><span class="sxs-lookup"><span data-stu-id="72df2-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="72df2-129">D3DDECLUSAGE- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="72df2-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="72df2-130">0</span><span class="sxs-lookup"><span data-stu-id="72df2-130">0</span></span>                      | <span data-ttu-id="72df2-131">D3DVSDE \_ diffuses</span><span class="sxs-lookup"><span data-stu-id="72df2-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="72df2-132">D3DDECLUSAGE- \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="72df2-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="72df2-133">1</span><span class="sxs-lookup"><span data-stu-id="72df2-133">1</span></span>                      | <span data-ttu-id="72df2-134">D3DVSDE \_ Glanz</span><span class="sxs-lookup"><span data-stu-id="72df2-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="72df2-135">D3DDECLUSAGE \_ texcoord</span><span class="sxs-lookup"><span data-stu-id="72df2-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="72df2-136">n</span><span class="sxs-lookup"><span data-stu-id="72df2-136">n</span></span>                      | <span data-ttu-id="72df2-137">D3DVSDE \_ texcoordn</span><span class="sxs-lookup"><span data-stu-id="72df2-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="72df2-138">Wenn eine Deklaration für die Verarbeitung von Hardware Scheitel Punkten auf einem Direct3D 7-Treiber verwendet wird, wird Sie von der Direct3D-Laufzeit mit den folgenden Regeln in eine FVF-Datei konvertiert:</span><span class="sxs-lookup"><span data-stu-id="72df2-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="72df2-139">Es sollte nur Stream 0 verwendet werden (ersichtlich aus der maxstreams-Obergrenze).</span><span class="sxs-lookup"><span data-stu-id="72df2-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="72df2-140">Die Reihenfolge der Scheitelpunkt Elemente sollte mit der Reihenfolge der "f"-Bits identisch sein.</span><span class="sxs-lookup"><span data-stu-id="72df2-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="72df2-141">Lücken in Texturkoordinaten sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="72df2-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="72df2-142">Alle Vertex-Elemente, die nicht in der Tabelle beschrieben werden, können nicht für alle Pre-DirectX 8-Treiber in eine gültige FVF konvertiert werden und können daher nicht für diese Treiber verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="72df2-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="72df2-143">Nur D3DDECLTYPE \_ FLOAT2 ist für Scheitelpunkt Elemente mit D3DDECLUSAGE \_ texcoord zulässig, wenn das Gerät keines der D3DPTEXTURECAPS \_ projizierten oder D3DPTEXTURECAPS \_ cubemap-Caps festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="72df2-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72df2-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="72df2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72df2-145">Vertex-Deklaration</span><span class="sxs-lookup"><span data-stu-id="72df2-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



