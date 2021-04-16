---
description: Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Effektzustandsgruppen (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351739"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="16627-103">Effektzustandsgruppen (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="16627-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="16627-104">Effekt Zustände sind Name-Wert-Paare in Form eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="16627-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="16627-105">Blend-Status</span><span class="sxs-lookup"><span data-stu-id="16627-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="16627-106">**Alpha atocoverageenable**, **blendenable**, **srcblend**, **destblend**, **blendop**, **srcblendalpha**, **destblendalpha**, **blendopalpha**, **rendertargetschreitemask**</span><span class="sxs-lookup"><span data-stu-id="16627-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="16627-107">Mitglieder von [ **d3d10 \_ Blend- \_ ABSC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="16627-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="16627-108">Tiefen-und Schablonen Zustand</span><span class="sxs-lookup"><span data-stu-id="16627-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="16627-109">**depthenable**, **depthwrite temask**, **depthfunc**, **stencilenable**, **stencilread Mask**, **stencilwrite temask**</span><span class="sxs-lookup"><span data-stu-id="16627-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="16627-110">Mitglieder der [ **d3d10- \_ tiefen \_ Schablone \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="16627-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="16627-111">frontfakesttcilfail \* \*, **frontfakestin cilzfail**, **frontfakesteincilpass**, **frontfakesteincilfunc**, **backfakestdcilfail**, **backfakesteincilzfail**, **backfakesteincilpass**, **backfakesteincilfunc**</span><span class="sxs-lookup"><span data-stu-id="16627-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="16627-112">Mitglied von [ **d3d10 \_ tiefen \_ Schablone (encilop \_** )](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="16627-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="16627-113">Status des Rasterizers</span><span class="sxs-lookup"><span data-stu-id="16627-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="16627-114">FillMode</span><span class="sxs-lookup"><span data-stu-id="16627-114">FILLMODE</span></span> | [<span data-ttu-id="16627-115">**D3d10 \_ Füll \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="16627-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="16627-116">CullMode</span><span class="sxs-lookup"><span data-stu-id="16627-116">CULLMODE</span></span> | [<span data-ttu-id="16627-117">**D3d10- \_ cull- \_ Modus**</span><span class="sxs-lookup"><span data-stu-id="16627-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="16627-118">**frontcounter Uhrzeigersinn**, **depthbias**, **depthbiasclamp**, **slopescaleddepthbias**, **zclipenable**, **scissorenable**, **multisampleenable**, **antialiasedlineenable**</span><span class="sxs-lookup"><span data-stu-id="16627-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="16627-119">Mitglieder des [ **d3d10 \_ Rasterizer \_** -Moduls](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="16627-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="16627-120">Samplerstatus</span><span class="sxs-lookup"><span data-stu-id="16627-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="16627-121">**Filter**, **adressssu**, **adressssv**, **AddressW**, **miplodbias**, **MaxAnisotropy**, **comparisonfunc**, **BorderColor**, **minlod**, **maxlod**</span><span class="sxs-lookup"><span data-stu-id="16627-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="16627-122">Mitglieder des [ **d3d10 \_ - \_ samplerentsc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="16627-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="16627-123">Beispiele hierfür finden Sie unter [Sampler Type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="16627-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="16627-124">Effekt Objektstatus</span><span class="sxs-lookup"><span data-stu-id="16627-124">Effect object state</span></span>

| <span data-ttu-id="16627-125">This Effect-Objekt</span><span class="sxs-lookup"><span data-stu-id="16627-125">This effect object</span></span> | <span data-ttu-id="16627-126">Entsprechung</span><span class="sxs-lookup"><span data-stu-id="16627-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="16627-127">Rasterizerstate</span><span class="sxs-lookup"><span data-stu-id="16627-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="16627-128">Ein [Rasterizer State](#rasterizer-state) State-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="16627-129">Depthstencilstate</span><span class="sxs-lookup"><span data-stu-id="16627-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="16627-130">Ein [tiefen-und Schablonen Zustands](#depth-and-stencil-state) Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="16627-131">Blendstate</span><span class="sxs-lookup"><span data-stu-id="16627-131">BLENDSTATE</span></span> | <span data-ttu-id="16627-132">Ein [Blend](#blend-state) -Zustands Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="16627-133">Titellink</span><span class="sxs-lookup"><span data-stu-id="16627-133">VERTEXSHADER</span></span> | <span data-ttu-id="16627-134">Ein kompiliertes Vertex-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="16627-135">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="16627-135">PIXELSHADER</span></span> | <span data-ttu-id="16627-136">Ein kompiliertes Pixel-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="16627-137">Geometryshader</span><span class="sxs-lookup"><span data-stu-id="16627-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="16627-138">Ein kompiliertes Geometry-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="16627-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="16627-139">DS \_ stencilref ab \_ blendfactor ab \_ samplemask</span><span class="sxs-lookup"><span data-stu-id="16627-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="16627-140">Mitglieder von [**d3d10 \_ Pass \_**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc)(Debug).</span><span class="sxs-lookup"><span data-stu-id="16627-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="16627-141">Definieren und Verwenden von Zustands Objekten</span><span class="sxs-lookup"><span data-stu-id="16627-141">Defining and using state objects</span></span>

<span data-ttu-id="16627-142">Zustands Objekte werden in FX-Dateien im folgenden Format deklariert.</span><span class="sxs-lookup"><span data-stu-id="16627-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="16627-143">*Stateobjecttype* ist einer der oben aufgeführten Zustände, und der *Member Name* ist der Name eines beliebigen Members, der einen nicht standardmäßigen Wert hat.</span><span class="sxs-lookup"><span data-stu-id="16627-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="16627-144">Wenn Sie z. b. ein Blend-Zustands Objekt mit Alpha atocoverageenable und blendenable \[ 0 \] auf **false** festlegen möchten, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="16627-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="16627-145">Das State-Objekt wird auf eine Technik Übergabe mithilfe einer der setstategroup-Funktionen angewendet, die in der [Effekt Techniken-Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="16627-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="16627-146">Wenn Sie z. b. das oben beschriebene blendstate-Objekt anwenden möchten, wird der folgende Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="16627-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="16627-147">Ein Tutorial, in dem die Verwendung von Zuständen beschrieben wird, finden Sie unter [Zustands Verwaltung](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="16627-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="16627-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16627-148">Related topics</span></span>

* [<span data-ttu-id="16627-149">Syntax der Effekt Technik</span><span class="sxs-lookup"><span data-stu-id="16627-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="16627-150">Effekt Format (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="16627-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
