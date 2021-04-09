---
description: Nebel Parameter werden über den Geräte Rendering gesteuert.
ms.assetid: a3c5f439-6937-4ba9-991f-5a4154447cf9
title: Nebel Parameter (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03104df36aba0868c15ccc0b8ddc78d1352bef7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860194"
---
# <a name="fog-parameters-direct3d-9"></a><span data-ttu-id="57a74-103">Nebel Parameter (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="57a74-103">Fog Parameters (Direct3D 9)</span></span>

<span data-ttu-id="57a74-104">Nebel Parameter werden über den Geräte Rendering gesteuert.</span><span class="sxs-lookup"><span data-stu-id="57a74-104">Fog parameters are controlled through device render states.</span></span> <span data-ttu-id="57a74-105">Sowohl Pixel-als auch Scheitelpunkt Typen unterstützen alle in [Nebel Formeln (Direct3D 9)](fog-formulas.md)eingeführten Nebel Formeln.</span><span class="sxs-lookup"><span data-stu-id="57a74-105">Both pixel and vertex fog types support all the fog formulas introduced in [Fog Formulas (Direct3D 9)](fog-formulas.md).</span></span> <span data-ttu-id="57a74-106">Der [**D3DFOGMODE**](./d3dfogmode.md) -enumerierte Typ definiert Konstanten, die Sie verwenden können, um die von Microsoft Direct3D zu verwendende Nebel Formel zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="57a74-106">The [**D3DFOGMODE**](./d3dfogmode.md) enumerated type defines constants that you can use to identify the fog formula you want Microsoft Direct3D to use.</span></span> <span data-ttu-id="57a74-107">Der D3DRS \_ fogtablemode-renderzustand steuert den Nebelmodus, den Direct3D für den Pixel Nebel verwendet, und der D3DRS \_ fogvertexmode-renderzustand steuert den Modus für Scheitelpunkt Nebel.</span><span class="sxs-lookup"><span data-stu-id="57a74-107">The D3DRS\_FOGTABLEMODE render state controls the fog mode that Direct3D uses for pixel fog, and the D3DRS\_FOGVERTEXMODE render state controls the mode for vertex fog.</span></span>

<span data-ttu-id="57a74-108">Wenn Sie die lineare Nebel Formel verwenden, legen Sie die Start-und die endabstände über die \_ renderzustände D3DRS fogstart und D3DRS \_ fogend fest.</span><span class="sxs-lookup"><span data-stu-id="57a74-108">When using the linear fog formula, you set the starting and ending distances through the D3DRS\_FOGSTART and D3DRS\_FOGEND render states.</span></span> <span data-ttu-id="57a74-109">Wie das System diese Werte interpretiert, hängt vom Typ des schachtels, den Ihre Anwendung verwendet (Pixel oder Scheitelpunkt), und bei Verwendung von Pixel Nebel, wenn die z-oder w-basierte Tiefe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="57a74-109">How the system interprets these values depends on the type of fog your application uses - pixel or vertex fog - and, when using pixel fog, if z-based or w-based depth is being used.</span></span> <span data-ttu-id="57a74-110">In der folgenden Tabelle werden die Typen und deren Start-und Endeinheiten zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="57a74-110">The following table summarizes fog types and their start and end units.</span></span>



| <span data-ttu-id="57a74-111">Nebeltyp</span><span class="sxs-lookup"><span data-stu-id="57a74-111">Fog type</span></span>  | <span data-ttu-id="57a74-112">Start-/Endeinheiten für Nebel</span><span class="sxs-lookup"><span data-stu-id="57a74-112">Fog start/end units</span></span>      |
|-----------|--------------------------|
| <span data-ttu-id="57a74-113">Pixel (Z)</span><span class="sxs-lookup"><span data-stu-id="57a74-113">Pixel (Z)</span></span> | <span data-ttu-id="57a74-114">Geräteraum \[ 0,0, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="57a74-114">Device space \[0.0,1.0\]</span></span> |
| <span data-ttu-id="57a74-115">Pixel (W)</span><span class="sxs-lookup"><span data-stu-id="57a74-115">Pixel (W)</span></span> | <span data-ttu-id="57a74-116">Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="57a74-116">Camera space</span></span>             |
| <span data-ttu-id="57a74-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="57a74-117">Vertex</span></span>    | <span data-ttu-id="57a74-118">Kamerabereich</span><span class="sxs-lookup"><span data-stu-id="57a74-118">Camera space</span></span>             |



 

<span data-ttu-id="57a74-119">Der D3DRS \_ fogdensity-Rendering-Zustand steuert die beim Aktivieren einer exponentialnebelformel angewendete Nebeldichte.</span><span class="sxs-lookup"><span data-stu-id="57a74-119">The D3DRS\_FOGDENSITY render state controls the fog density applied when an exponential fog formula is enabled.</span></span> <span data-ttu-id="57a74-120">Die Nebeldichte ist im Wesentlichen ein Gewichtungsfaktor, der zwischen 0,0 und 1,0 (einschließlich) liegt, der den Entfernungs Wert im Exponent skaliert.</span><span class="sxs-lookup"><span data-stu-id="57a74-120">Fog density is essentially a weighting factor, ranging from 0.0 to 1.0 (inclusive), that scales the distance value in the exponent.</span></span>

<span data-ttu-id="57a74-121">Die Farbe, die das System für die Schnebel Mischung verwendet, wird über den D3DRS \_ fogcolor Device-Rendering-Zustand gesteuert.</span><span class="sxs-lookup"><span data-stu-id="57a74-121">The color that the system uses for fog blending is controlled through the D3DRS\_FOGCOLOR device render state.</span></span> <span data-ttu-id="57a74-122">Weitere Informationen finden Sie unter [Nebelfarbe (Direct3D 9)](fog-color.md) und [Nebel Mischung (Direct3D 9)](fog-blending.md).</span><span class="sxs-lookup"><span data-stu-id="57a74-122">For more information, see [Fog Color (Direct3D 9)](fog-color.md) and [Fog Blending (Direct3D 9)](fog-blending.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="57a74-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="57a74-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a74-124">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="57a74-124">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 
