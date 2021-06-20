---
description: Erfahren Sie mehr über die Texturunterstützung in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet. Es handelt sich um eine Ebene über der Direct3D-Komponente.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Texturunterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404603"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="f683e-105">Texturunterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f683e-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="f683e-106">D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bietet.</span><span class="sxs-lookup"><span data-stu-id="f683e-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="f683e-107">Es handelt sich um eine Ebene über der Direct3D-Komponente.</span><span class="sxs-lookup"><span data-stu-id="f683e-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="f683e-108">Texturen</span><span class="sxs-lookup"><span data-stu-id="f683e-108">Textures</span></span>

<span data-ttu-id="f683e-109">In den folgenden Themen werden viele verschiedene Texturen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f683e-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="f683e-110">Standardmäßige mipmapped-Texturunterstützung.</span><span class="sxs-lookup"><span data-stu-id="f683e-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="f683e-111">Weitere [Informationen finden Sie unter Automatische Generierung von Mipmaps (Direct3D 9).](automatic-generation-of-mipmaps.md)</span><span class="sxs-lookup"><span data-stu-id="f683e-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="f683e-112">Cubezuordnungsunterstützung.</span><span class="sxs-lookup"><span data-stu-id="f683e-112">Cube map support.</span></span> <span data-ttu-id="f683e-113">Weitere Informationen [finden Sie unter Kubische Umgebungszuordnung (Direct3D 9).](cubic-environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="f683e-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="f683e-114">Volumentexturunterstützung.</span><span class="sxs-lookup"><span data-stu-id="f683e-114">Volume texture support.</span></span> <span data-ttu-id="f683e-115">Siehe [Volumetexturressourcen (Direct3D 9).](volume-texture-resources.md)</span><span class="sxs-lookup"><span data-stu-id="f683e-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="f683e-116">Unterstützung der Umgebungszuordnung.</span><span class="sxs-lookup"><span data-stu-id="f683e-116">Environment mapping support.</span></span> <span data-ttu-id="f683e-117">Weitere Informationen [finden Sie unter Umgebungszuordnung (Direct3D 9).](environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="f683e-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="f683e-118">Unterstützung für die Bumpzuordnung.</span><span class="sxs-lookup"><span data-stu-id="f683e-118">Bump mapping support.</span></span> <span data-ttu-id="f683e-119">Weitere Informationen [finden Sie unter Bump Mapping (Direct3D 9) (Bumpzuordnung (Direct3D 9)).](bump-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="f683e-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="f683e-120">Texturfarbkonvertierung</span><span class="sxs-lookup"><span data-stu-id="f683e-120">Texture Color Conversion</span></span>

<span data-ttu-id="f683e-121">Wenn Sie eine der Funktionen D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx oder D3DXCreateVolumeTexturexxx verwenden, muss möglicherweise eine Farbkonvertierung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f683e-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="f683e-122">Beispielsweise kann eine Oberfläche den Typ RGBA und die andere UVWQ haben.</span><span class="sxs-lookup"><span data-stu-id="f683e-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="f683e-123">Bei unterschiedlichen Formaten lautet die Konvertierungssequenz wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f683e-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="f683e-124">Zuordnen von RGBA zu UVWQ</span><span class="sxs-lookup"><span data-stu-id="f683e-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="f683e-125">R <-> U, R-Kanal wird dem U-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-126">G <-> V, G-Kanal wird dem V-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-127">B <-> W, der B-Kanal wird dem W-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-128">Ein <-> Q/L, ein Kanal wird entweder dem Q- oder dem L-Kanal zugeordnet (je nachdem, welcher kanal im Zielformat verfügbar ist) oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="f683e-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="f683e-129">Zuordnen von UV zu RGBA</span><span class="sxs-lookup"><span data-stu-id="f683e-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="f683e-130">U <-> R, U-Kanal wird dem R-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-131">V <-> G, V-Kanal wird dem G-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-132">1 <-> B, 1 wird dem B-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="f683e-133">1 <-> A, 1 wird dem A-Kanal zugeordnet (oder umgekehrt).</span><span class="sxs-lookup"><span data-stu-id="f683e-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="f683e-134">Wenn ein Kanal in der Quelle nicht vorhanden ist, wird davon ausgegangen, dass er 1 ist (mit Ausnahme von A8, wobei R, G, B als 0 angenommen wird).</span><span class="sxs-lookup"><span data-stu-id="f683e-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="f683e-135">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f683e-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="f683e-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f683e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f683e-137">D3dx</span><span class="sxs-lookup"><span data-stu-id="f683e-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



