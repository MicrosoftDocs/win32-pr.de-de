---
description: Das Vertex Shader 3,0-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe der texldl-vs-Textur Lade Anweisung.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Scheitelpunkt Texturen in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e8e7bbf7e1ae9764fe5b30647f318dfaeb3ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747160"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a><span data-ttu-id="c5c05-103">Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c5c05-103">Vertex Textures in vs\_3\_0 (DirectX HLSL)</span></span>

<span data-ttu-id="c5c05-104">Das Vertex Shader 3,0-Modell unterstützt die Textur Suche im Vertex-Shader mithilfe der [texldl-vs-](../direct3dhlsl/texldl---vs.md) Textur Lade Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c5c05-104">The vertex shader 3.0 model supports texture lookup in the vertex shader using the [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load statement.</span></span> <span data-ttu-id="c5c05-105">Die Vertex-Engine enthält vier textursampler-Phasen mit den Namen [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 und D3DVERTEXTEXTURESAMPLER3.</span><span class="sxs-lookup"><span data-stu-id="c5c05-105">The vertex engine contains four texture sampler stages, named [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2, and D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="c5c05-106">Diese unterscheiden sich von der Verschiebung des Verschiebungs Karten Samplern und der Textur Samplern in der Pixel-Engine.</span><span class="sxs-lookup"><span data-stu-id="c5c05-106">These are distinct from the displacement map sampler and texture samplers in the pixel engine.</span></span>

<span data-ttu-id="c5c05-107">Zum Beispiel für Texturen, die in diesen vier Phasen festgelegt werden, können Sie die Vertex-Engine verwenden und die Phasen mit der [**CheckDeviceFormat**](/windows/desktop/api) -Methode programmieren.</span><span class="sxs-lookup"><span data-stu-id="c5c05-107">To sample textures set at those four stages, you can use the vertex engine and program the stages with the [**CheckDeviceFormat**](/windows/desktop/api) method.</span></span> <span data-ttu-id="c5c05-108">Legen Sie mithilfe von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)Texturen in diesen Phasen fest, wobei Sie den Phasen Index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) bis D3DVERTEXTEXTURESAMPLER3 verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-108">Set textures at those stages using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), with the stage index [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) through D3DVERTEXTEXTURESAMPLER3.</span></span> <span data-ttu-id="c5c05-109">Ein neues Register wurde im Vertex-Shader eingeführt, das Samplerregister (wie in PS \_ 2 \_ 0), das den Scheitelpunkt Textur Sampler darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5c05-109">A new register has been introduced in the vertex shader, the sampler register (like in ps\_2\_0), which represents the vertex texture sampler.</span></span> <span data-ttu-id="c5c05-110">Dieses Register muss im Shader definiert werden, bevor es verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5c05-110">This register needs to be defined in the shader before using it.</span></span>

<span data-ttu-id="c5c05-111">Eine Anwendung kann Abfragen, wenn ein Format als vertextextur unterstützt wird, indem [**CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ Query \_ vertextexture](d3dusage-query.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c5c05-111">An application can query if a format is supported as a vertex texture by calling [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE](d3dusage-query.md).</span></span>

> [!Note]  
> <span data-ttu-id="c5c05-112">Dabei handelt es sich um ein abfrageflag, sodass es in keiner der Funktionen von "-Funktion" akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5c05-112">This is a query flag so it is not accepted in any Createxxx function.</span></span> <span data-ttu-id="c5c05-113">Eine im Standard Pool erstellte Scheitelpunkt Textur kann als Pixel Textur festgelegt werden und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="c5c05-113">A vertex texture created in the default pool can be set as a pixel texture and vice versa.</span></span> <span data-ttu-id="c5c05-114">Um jedoch die Verarbeitung der Software Scheitel Punkte zu verwenden, muss die Vertex-Textur im Scratch-Pool erstellt werden (unabhängig davon, ob es sich um ein Gerät mit gemischtem Modus oder ein Software-Vertex-Verarbeitungs Gerät handelt).</span><span class="sxs-lookup"><span data-stu-id="c5c05-114">However, to use the software vertex processing, the vertex texture must be created in the scratch pool (no matter if it is a mixed-mode device or a software vertex processing device).</span></span>

 

<span data-ttu-id="c5c05-115">Die Funktionalität ist mit den Pixel Texturen identisch, mit Ausnahme der folgenden:</span><span class="sxs-lookup"><span data-stu-id="c5c05-115">The functionality is identical to the pixel textures, except for the following:</span></span>

-   <span data-ttu-id="c5c05-116">Die anisotrope Textur Filterung wird nicht unterstützt. daher \_ wird D3DSAMP MaxAnisotropy ignoriert, und D3DTEXF \_ anisotrope kann nicht für die Vergrößerung festgelegt werden, oder es kann für diese Phasen nicht minimal festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-116">Anisotropic texture filtering is not supported, hence D3DSAMP\_MAXANISOTROPY is ignored and D3DTEXF\_ANISOTROPIC cannot be set for magnify, or minify for these stages.</span></span>
-   <span data-ttu-id="c5c05-117">Die Rate der Änderungs Informationen ist nicht verfügbar. Daher muss die Anwendung die Detailebene berechnen und diese Informationen als Parameter für [texldl-vs](../direct3dhlsl/texldl---vs.md)bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c5c05-117">Rate of change information is not available, hence the application has to compute the level of detail and provide that information as a parameter to [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="c5c05-118">Es gelten folgende Beschränkungen:</span><span class="sxs-lookup"><span data-stu-id="c5c05-118">Restrictions include:</span></span>

-   <span data-ttu-id="c5c05-119">Wie bei Pixel-Shadern \_ wird D3DSAMP Elementindex verwendet, um herauszufinden, aus welchem Element ein Beispiel entnommen werden soll, wenn multielementtexturen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-119">As in pixel shaders, if multielement textures are supported, D3DSAMP\_ELEMENTINDEX is used to figure out which element to sample from.</span></span>
-   <span data-ttu-id="c5c05-120">Der Status "D3DSAMP \_ dmapoffset" wird für diese Phasen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c5c05-120">The state D3DSAMP\_DMAPOFFSET is ignored for these stages.</span></span>
-   <span data-ttu-id="c5c05-121">Verwenden Sie [**CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ Query \_ vertextexture "](d3dusage-query.md) , um eine Textur abzufragen, um festzustellen, ob Sie als vertextextur verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5c05-121">Use [**CheckDeviceFormat**](/windows/desktop/api) with [D3DUSAGE\_QUERY\_VERTEXTEXTURE"](d3dusage-query.md) to query a texture to see if it can be used as a vertex texture.</span></span>
-   <span data-ttu-id="c5c05-122">Vertextexturefiltercaps gibt an, welche Art von Filtern bei den Scheitelpunkt Textur-Samplern zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="c5c05-122">VertexTextureFilterCaps indicates what kind of filters are allowed at the vertex texture samplers.</span></span> <span data-ttu-id="c5c05-123">[D3DPTFILTERCAPS \_ Minsanisotropic](d3dptfiltercaps.md) und D3DPTFILTERCAPS \_ magsanisotrope sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c5c05-123">[D3DPTFILTERCAPS\_MINFANISOTROPIC](d3dptfiltercaps.md) and D3DPTFILTERCAPS\_MAGFANISOTROPIC are disallowed.</span></span>

## <a name="sampling-stage-registers"></a><span data-ttu-id="c5c05-124">Abtast Phasen Register</span><span class="sxs-lookup"><span data-stu-id="c5c05-124">Sampling Stage Registers</span></span>

<span data-ttu-id="c5c05-125">Ein Sampling-Phasen Register identifiziert eine samplingeinheit, die in Textur Ladeanweisungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5c05-125">A sampling stage register identifies a sampling unit that can be used in texture load statements.</span></span> <span data-ttu-id="c5c05-126">Eine samplingeinheit entspricht der Phase Textur Sampling und kapselt den in [**setsamplerstate angegebenen samplingspezifischen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)Zustand.</span><span class="sxs-lookup"><span data-stu-id="c5c05-126">A sampling unit corresponds to the texture sampling stage, encapsulating the sampling-specific state provided in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span>

<span data-ttu-id="c5c05-127">Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c5c05-127">Each sampler uniquely identifies a single texture surface that is set to the corresponding sampler using [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="c5c05-128">Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-128">However, the same texture surface can be set at multiple samplers.</span></span>

<span data-ttu-id="c5c05-129">Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-129">At draw time, a texture cannot be simultaneously set as a render target and a texture at a stage.</span></span>

<span data-ttu-id="c5c05-130">Da vs \_ 3 \_ 0 vier Samplers unterstützt, können bis zu vier Textur Oberflächen in einem einzelnen shaderdurchlauf aus gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c5c05-130">Because vs\_3\_0 supports four samplers, up to four texture surfaces can be read from in a single shader pass.</span></span> <span data-ttu-id="c5c05-131">Ein Samplerregister kann nur als Argument in der Textur Lade Anweisung angezeigt werden: [texldl-vs](../direct3dhlsl/texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="c5c05-131">A sampler register might appear only as an argument in the texture load statement: [texldl - vs](../direct3dhlsl/texldl---vs.md).</span></span>

<span data-ttu-id="c5c05-132">\_Wenn Sie in vs 3 \_ 0 einen Sampler verwenden, muss er am Anfang des Shader-Programms mit dem [DCL- \_ samplertype (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) deklariert werden (wie in PS \_ 2 \_ 0).</span><span class="sxs-lookup"><span data-stu-id="c5c05-132">In vs\_3\_0, if you use a sampler, it must be declared at the beginning of the shader program, using the [dcl\_samplerType (sm3 - vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (as in ps\_2\_0).</span></span>

## <a name="software-processing"></a><span data-ttu-id="c5c05-133">Software Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="c5c05-133">Software Processing</span></span>

<span data-ttu-id="c5c05-134">Diese Funktion wird bei der Verarbeitung von Software Scheitel Punkten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5c05-134">This feature will be supported in software vertex processing.</span></span> <span data-ttu-id="c5c05-135">Die unterstützten Filtertypen können überprüft werden, indem [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) aufgerufen und vertextexturefiltercaps überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="c5c05-135">The specific filter types supported can be checked by calling [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) and checking VertexTextureFilterCaps.</span></span> <span data-ttu-id="c5c05-136">Alle veröffentlichten Textur Formate werden als Scheitelpunkt Texturen bei der Verarbeitung von Software Scheitel Punkten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5c05-136">All published texture formats will be supported as vertex textures in software vertex processing.</span></span>

<span data-ttu-id="c5c05-137">Mithilfe von [**CheckDeviceFormat**](/windows/desktop/api) und Bereitstellen von (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ softwareprocessing**](d3dusage.md)) als Verwendung können Anwendungen überprüfen, ob ein bestimmtes Textur Format im Software Scheitelpunkt Verarbeitungsmodus unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c5c05-137">Applications can check if a particular texture format is supported in the software vertex processing mode by calling [**CheckDeviceFormat**](/windows/desktop/api) and providing (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md)) as usage.</span></span> <span data-ttu-id="c5c05-138">Alle Formate werden für die Verarbeitung von Software Scheitel Punkten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5c05-138">All formats are supported for software vertex processing.</span></span> <span data-ttu-id="c5c05-139">Der Scratch-Pool ist für die Verarbeitung von Software Scheitel Punkten erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5c05-139">The scratch pool is required for software vertex processing.</span></span>

## <a name="api-changes"></a><span data-ttu-id="c5c05-140">API-Änderungen</span><span class="sxs-lookup"><span data-stu-id="c5c05-140">API Changes</span></span>


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a><span data-ttu-id="c5c05-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5c05-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c05-142">Scheitelpunkt Pipeline</span><span class="sxs-lookup"><span data-stu-id="c5c05-142">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
