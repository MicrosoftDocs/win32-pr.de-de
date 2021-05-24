---
description: Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Effektzustandsgruppen (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335569"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="306d3-103">Effektzustandsgruppen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="306d3-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="306d3-104">Effektzustände sind Name-Wert-Paare in Form eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="306d3-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="306d3-105">Überblenden des Zustands</span><span class="sxs-lookup"><span data-stu-id="306d3-105">Blend state</span></span>

| <span data-ttu-id="306d3-106">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="306d3-106">Effect state</span></span> | <span data-ttu-id="306d3-107">Group</span><span class="sxs-lookup"><span data-stu-id="306d3-107">Group</span></span> |
|-|-|
| <span data-ttu-id="306d3-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="306d3-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="306d3-109">Elemente von [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="306d3-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="306d3-110">Tiefen- und Schablonenzustand</span><span class="sxs-lookup"><span data-stu-id="306d3-110">Depth and stencil state</span></span>

| <span data-ttu-id="306d3-111">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="306d3-111">Effect state</span></span>| <span data-ttu-id="306d3-112">Group</span><span class="sxs-lookup"><span data-stu-id="306d3-112">Group</span></span> |
|-|-|
| <span data-ttu-id="306d3-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="306d3-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="306d3-114">Elemente der [ **D3D10 \_ \_ DEPTH-SCHABLONE \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="306d3-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="306d3-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="306d3-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="306d3-116">Member von [ **D3D10 \_ DEPTH \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="306d3-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="306d3-117">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="306d3-117">Rasterizer state</span></span>

| <span data-ttu-id="306d3-118">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="306d3-118">Effect state</span></span>| <span data-ttu-id="306d3-119">Group</span><span class="sxs-lookup"><span data-stu-id="306d3-119">Group</span></span> |
|-|-|
| <span data-ttu-id="306d3-120">Fillmode</span><span class="sxs-lookup"><span data-stu-id="306d3-120">FILLMODE</span></span> | [<span data-ttu-id="306d3-121">**FÜLLMODUS D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="306d3-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="306d3-122">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="306d3-122">CULLMODE</span></span> | [<span data-ttu-id="306d3-123">**D3D10 \_ \_ CULL-MODUS**</span><span class="sxs-lookup"><span data-stu-id="306d3-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="306d3-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **VERSKALIERTDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="306d3-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="306d3-125">Elemente von [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="306d3-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="306d3-126">Samplerzustand</span><span class="sxs-lookup"><span data-stu-id="306d3-126">Sampler state</span></span>

| <span data-ttu-id="306d3-127">Auswirkungszustand</span><span class="sxs-lookup"><span data-stu-id="306d3-127">Effect state</span></span> | <span data-ttu-id="306d3-128">Group</span><span class="sxs-lookup"><span data-stu-id="306d3-128">Group</span></span> |
|-|-|
| <span data-ttu-id="306d3-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="306d3-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="306d3-130">Member von [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="306d3-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="306d3-131">Beispiele finden Sie unter [Sampler type (DirectX HLSL) (Samplertyp (DirectX HLSL)).](../direct3dhlsl/dx-graphics-hlsl-sampler.md)</span><span class="sxs-lookup"><span data-stu-id="306d3-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="306d3-132">Effect-Objektzustand</span><span class="sxs-lookup"><span data-stu-id="306d3-132">Effect object state</span></span>

| <span data-ttu-id="306d3-133">Dieses Effektobjekt</span><span class="sxs-lookup"><span data-stu-id="306d3-133">This effect object</span></span> | <span data-ttu-id="306d3-134">Entsprechung</span><span class="sxs-lookup"><span data-stu-id="306d3-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="306d3-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="306d3-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="306d3-136">Ein [Zustandsobjekt des Rasterizerzustands.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="306d3-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="306d3-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="306d3-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="306d3-138">Ein [Tiefen- und Schablonenzustandsobjekt.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="306d3-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="306d3-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="306d3-139">BLENDSTATE</span></span> | <span data-ttu-id="306d3-140">Ein [Blend State State-Objekt.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="306d3-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="306d3-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="306d3-141">VERTEXSHADER</span></span> | <span data-ttu-id="306d3-142">Ein kompiliertes Vertex-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="306d3-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="306d3-143">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="306d3-143">PIXELSHADER</span></span> | <span data-ttu-id="306d3-144">Ein kompiliertes Pixelshaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="306d3-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="306d3-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="306d3-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="306d3-146">Ein kompiliertes geometry-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="306d3-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="306d3-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="306d3-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="306d3-148">Member von [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="306d3-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="306d3-149">Definieren und Verwenden von Zustandsobjekten</span><span class="sxs-lookup"><span data-stu-id="306d3-149">Defining and using state objects</span></span>

<span data-ttu-id="306d3-150">Zustandsobjekte werden in FX-Dateien im folgenden Format deklariert.</span><span class="sxs-lookup"><span data-stu-id="306d3-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="306d3-151">*StateObjectType* ist einer der oben aufgeführten Zustände, und *MemberName* ist der Name jedes Mitglieds, das einen nicht standardmäßigen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="306d3-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="306d3-152">Wenn Sie beispielsweise ein Blend-Zustandsobjekt einrichten möchten, bei dem AlphaToCoverageEnable und BlendEnable 0 auf FALSE festgelegt sind, wird der folgende \[ \] Code verwendet. </span><span class="sxs-lookup"><span data-stu-id="306d3-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="306d3-153">Das Zustandsobjekt wird mithilfe einer der SetStateGroup-Funktionen, die unter [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md)beschrieben sind, auf einen Technikpass angewendet.</span><span class="sxs-lookup"><span data-stu-id="306d3-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="306d3-154">Um beispielsweise das oben beschriebene BlendState-Objekt anzuwenden, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="306d3-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="306d3-155">Ein Tutorial, in dem die Verwendung von Status beschrieben wird, finden Sie [unter Zustandsverwaltung.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="306d3-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="306d3-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="306d3-156">Related topics</span></span>

* [<span data-ttu-id="306d3-157">Syntax der Effekttechnik</span><span class="sxs-lookup"><span data-stu-id="306d3-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="306d3-158">Effect-Format (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="306d3-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
