---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Textur Unterstützung in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339643"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="165bd-104">Textur Unterstützung in D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="165bd-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="165bd-105">D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="165bd-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="165bd-106">Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.</span><span class="sxs-lookup"><span data-stu-id="165bd-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="165bd-107">Texturen</span><span class="sxs-lookup"><span data-stu-id="165bd-107">Textures</span></span>

<span data-ttu-id="165bd-108">In den folgenden Themen werden viele verschiedene Texturen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="165bd-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="165bd-109">Standard mäßige Mipmapping-Textur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="165bd-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="165bd-110">Weitere Informationen finden Sie [unter Automatische Generierung von Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="165bd-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="165bd-111">Cubezuordnungs Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="165bd-111">Cube map support.</span></span> <span data-ttu-id="165bd-112">Siehe [kubische Umgebungs Zuordnung (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="165bd-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="165bd-113">Volumetextur-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="165bd-113">Volume texture support.</span></span> <span data-ttu-id="165bd-114">Weitere Informationen finden Sie unter [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="165bd-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="165bd-115">Unterstützung der Umgebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="165bd-115">Environment mapping support.</span></span> <span data-ttu-id="165bd-116">Weitere Informationen finden Sie unter [Umgebungs Zuordnung (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="165bd-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="165bd-117">Unterstützung der Bump-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="165bd-117">Bump mapping support.</span></span> <span data-ttu-id="165bd-118">Weitere Informationen finden Sie unter [Bump Mapping (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="165bd-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="165bd-119">Textur Farbkonvertierung</span><span class="sxs-lookup"><span data-stu-id="165bd-119">Texture Color Conversion</span></span>

<span data-ttu-id="165bd-120">Bei Verwendung einer der Funktionen D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx oder D3DXCreateVolumeTexturexxx muss ggf. eine Farbkonvertierung durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="165bd-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="165bd-121">Eine Oberfläche könnte z. b. den Typ RGBA aufweisen, die andere z. b. uvwq.</span><span class="sxs-lookup"><span data-stu-id="165bd-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="165bd-122">In Fällen mit unterschiedlichen Formaten lautet die Konvertierungs Sequenz wie folgt:</span><span class="sxs-lookup"><span data-stu-id="165bd-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="165bd-123">Zuordnung von RGBA zu uvwq</span><span class="sxs-lookup"><span data-stu-id="165bd-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="165bd-124">R <-> u, der r-Kanal wird dem U-Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-125">G <-> v, der g-Kanal dem v-Kanal zugeordnet ist, oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-126">B <-> w, b-Kanal wird dem W-Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-127">Ein < > q/L, ein Kanal ist entweder dem q-oder dem L-Kanal (abhängig davon, welcher im Zielformat verfügbar ist) oder umgekehrt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="165bd-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="165bd-128">Zuordnung von UV zu RGBA</span><span class="sxs-lookup"><span data-stu-id="165bd-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="165bd-129">U <-> r, u-Kanal wird dem R-Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-130">V <-> g, der v-Kanal wird dem G-Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-131">1 <-> b, 1 wird dem b-Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="165bd-132">1 <-> a, 1 wird dem Kanal zugeordnet oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="165bd-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="165bd-133">Wenn ein Kanal nicht in der Quelle vorhanden ist, wird davon ausgegangen, dass er 1 ist (mit Ausnahme von A8, wobei R, G, B als 0 angenommen wird).</span><span class="sxs-lookup"><span data-stu-id="165bd-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="165bd-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="165bd-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="165bd-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="165bd-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="165bd-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="165bd-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



