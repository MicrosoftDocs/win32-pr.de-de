---
title: Texturkoordinaten Register (HLSL vs-Referenz)
description: Dieses Vertex-Shader-Ausgabe Register enthält pro-Scheitelpunkt-Texturkoordinaten.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102246"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a><span data-ttu-id="27876-103">Texturkoordinaten Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="27876-103">Texture Coordinate Register (HLSL VS reference)</span></span>

<span data-ttu-id="27876-104">Dieses Vertex-Shader-Ausgabe Register enthält pro-Scheitelpunkt-Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="27876-104">This vertex shader output register contains per-vertex texture coordinates.</span></span>

<span data-ttu-id="27876-105">Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.</span><span class="sxs-lookup"><span data-stu-id="27876-105">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="27876-106">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="27876-106">Property</span></span>        | <span data-ttu-id="27876-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27876-107">Description</span></span>   |
|-----------------|---------------|
| <span data-ttu-id="27876-108">Name</span><span class="sxs-lookup"><span data-stu-id="27876-108">Name</span></span>            | <span data-ttu-id="27876-109">oT0 - oT7</span><span class="sxs-lookup"><span data-stu-id="27876-109">oT0 - oT7</span></span>     |
| <span data-ttu-id="27876-110">Anzahl</span><span class="sxs-lookup"><span data-stu-id="27876-110">Count</span></span>           | <span data-ttu-id="27876-111">Acht Vektoren</span><span class="sxs-lookup"><span data-stu-id="27876-111">Eight vectors</span></span> |
| <span data-ttu-id="27876-112">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="27876-112">I/O permissions</span></span> | <span data-ttu-id="27876-113">Lesegeschützt</span><span class="sxs-lookup"><span data-stu-id="27876-113">Write-only</span></span>    |



 

<span data-ttu-id="27876-114">Bei den Ausgabe Texturkoordinaten Register handelt es sich um ein Array von Ausgabedaten Registern.</span><span class="sxs-lookup"><span data-stu-id="27876-114">The output texture coordinates registers are an array of output data registers.</span></span> <span data-ttu-id="27876-115">Die Register Daten werden durchlaufen und als Texturkoordinaten durch die Textur-samplingphasen verwendet, um Daten für den Pixelshader bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="27876-115">The register data is iterated and used as texture coordinates by the texture sampling stages to supply data to the pixel shader.</span></span>

<span data-ttu-id="27876-116">Wenn Sie in ein Texturkoordinaten Register schreiben, empfiehlt es sich, nur so viele Gleit Komma Werte wie die Dimension der entsprechenden Textur Zuordnung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="27876-116">When writing to a texture coordinate register, it is recommended that you pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="27876-117">Steuern Sie die Werte, die mit einem-Modifizierer übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="27876-117">Control the values that are passed with a modifier.</span></span> <span data-ttu-id="27876-118">Verwenden Sie beispielsweise. XY für eine 2D-Textur Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="27876-118">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="27876-119">Die [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF COUNT2, D3DTTFF COUNT3, D3DTTFF COUNT4) der Fixed-Funktion der Scheitelpunkt Pipeline \_ \_ \_ muss auf 0 (null) festgelegt werden, wenn Sie einen programmierbaren Scheitelpunkt-Shader verwenden.</span><span class="sxs-lookup"><span data-stu-id="27876-119">The fixed function vertex pipeline flags, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF\_COUNT1, D3DTTFF\_COUNT2, D3DTTFF\_COUNT3, D3DTTFF\_COUNT4), should be set to zero if you are using a programmable vertex shader.</span></span>

<span data-ttu-id="27876-120">Objekt-Vertex-Daten liefern Eingabe Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="27876-120">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="27876-121">Objekte, die keine Kacheln verwenden, weisen häufig Texturkoordinaten im Bereich von \[ 0 bis 1 auf \] .</span><span class="sxs-lookup"><span data-stu-id="27876-121">Objects that do not use tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="27876-122">Objekte, die gekachelte Texturen verwenden (z. b. das Gelände), verfügen in der Regel über Texturkoordinaten, die von \[ -n, + n reichen \]</span><span class="sxs-lookup"><span data-stu-id="27876-122">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-n,+n\] where n can be any floating point number.</span></span>

<span data-ttu-id="27876-123">Die Texturkoordinaten Interpolation wird für Scheitelpunkt Daten für die rasterisierung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27876-123">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="27876-124">Während der rasterisierung werden Texturkoordinaten zwischen Objekt Scheitel Punkten interpoliert, durch Textur Umbrüchen geändert und durch die Textur Größe skaliert (auch die Textur Adressierungs Modi werden berücksichtigt), um einen ganzzahligen Index zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="27876-124">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping, and scaled by the texture size (also taking into account texture addressing modes) to produce an integer index.</span></span> <span data-ttu-id="27876-125">Der Index wird dann verwendet, um eine Textur Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="27876-125">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="27876-126">Verwenden Sie den MaxTextureRepeat-Wert in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) , um zu bestimmen, wie oft eine Textur gekachelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="27876-126">Use the MaxTextureRepeat value in [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) to determine how many times a texture can be tiled.</span></span>

## <a name="example"></a><span data-ttu-id="27876-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="27876-127">Example</span></span>

<span data-ttu-id="27876-128">Deklarieren Sie das Texturkoordinaten Register.</span><span class="sxs-lookup"><span data-stu-id="27876-128">Declare the texture coordinate register.</span></span>


```
dcl_texcoord v7
```



<span data-ttu-id="27876-129">Kopieren Sie die Texturkoordinaten pro Scheitelpunkt in das Ausgabe Register.</span><span class="sxs-lookup"><span data-stu-id="27876-129">Copy the per-vertex texture coordinates to the output register.</span></span>


```
mov oT0, v7
```





| <span data-ttu-id="27876-130">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="27876-130">Vertex shader versions</span></span>      | <span data-ttu-id="27876-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="27876-131">1\_1</span></span> | <span data-ttu-id="27876-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27876-132">2\_0</span></span> | <span data-ttu-id="27876-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="27876-133">2\_sw</span></span> | <span data-ttu-id="27876-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="27876-134">2\_x</span></span> | <span data-ttu-id="27876-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="27876-135">3\_0</span></span> | <span data-ttu-id="27876-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="27876-136">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="27876-137">Texturkoordinaten Register</span><span class="sxs-lookup"><span data-stu-id="27876-137">Texture Coordinate Register</span></span> | <span data-ttu-id="27876-138">x</span><span class="sxs-lookup"><span data-stu-id="27876-138">x</span></span>    | <span data-ttu-id="27876-139">x</span><span class="sxs-lookup"><span data-stu-id="27876-139">x</span></span>    | <span data-ttu-id="27876-140">x</span><span class="sxs-lookup"><span data-stu-id="27876-140">x</span></span>     | <span data-ttu-id="27876-141">x</span><span class="sxs-lookup"><span data-stu-id="27876-141">x</span></span>    | <span data-ttu-id="27876-142">x</span><span class="sxs-lookup"><span data-stu-id="27876-142">x</span></span>    | <span data-ttu-id="27876-143">x</span><span class="sxs-lookup"><span data-stu-id="27876-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="27876-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27876-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27876-145">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="27876-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 