---
title: texkill-PS
description: Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313614"
---
# <a name="texkill---ps"></a><span data-ttu-id="92cda-103">texkill-PS</span><span class="sxs-lookup"><span data-stu-id="92cda-103">texkill - ps</span></span>

<span data-ttu-id="92cda-104">Bricht das Rendering des aktuellen Pixels ab, wenn eine der ersten drei Komponenten (UVW) der Texturkoordinaten kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="92cda-104">Cancels rendering of the current pixel if any of the first three components (UVW) of the texture coordinates is less than zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="92cda-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="92cda-105">Syntax</span></span>



| <span data-ttu-id="92cda-106">texkill DST</span><span class="sxs-lookup"><span data-stu-id="92cda-106">texkill dst</span></span> |
|-------------|



 

<span data-ttu-id="92cda-107">where</span><span class="sxs-lookup"><span data-stu-id="92cda-107">where</span></span>

-   <span data-ttu-id="92cda-108">DST ist ein Ziel Register</span><span class="sxs-lookup"><span data-stu-id="92cda-108">dst is a destination register</span></span>

## <a name="remarks"></a><span data-ttu-id="92cda-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92cda-109">Remarks</span></span>



| <span data-ttu-id="92cda-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="92cda-110">Pixel shader versions</span></span> | <span data-ttu-id="92cda-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="92cda-111">1\_1</span></span> | <span data-ttu-id="92cda-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="92cda-112">1\_2</span></span> | <span data-ttu-id="92cda-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="92cda-113">1\_3</span></span> | <span data-ttu-id="92cda-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="92cda-114">1\_4</span></span> | <span data-ttu-id="92cda-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92cda-115">2\_0</span></span> | <span data-ttu-id="92cda-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="92cda-116">2\_x</span></span> | <span data-ttu-id="92cda-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="92cda-117">2\_sw</span></span> | <span data-ttu-id="92cda-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="92cda-118">3\_0</span></span> | <span data-ttu-id="92cda-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="92cda-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="92cda-120">texkill</span><span class="sxs-lookup"><span data-stu-id="92cda-120">texkill</span></span>               | <span data-ttu-id="92cda-121">x</span><span class="sxs-lookup"><span data-stu-id="92cda-121">x</span></span>    | <span data-ttu-id="92cda-122">x</span><span class="sxs-lookup"><span data-stu-id="92cda-122">x</span></span>    | <span data-ttu-id="92cda-123">x</span><span class="sxs-lookup"><span data-stu-id="92cda-123">x</span></span>    | <span data-ttu-id="92cda-124">x</span><span class="sxs-lookup"><span data-stu-id="92cda-124">x</span></span>    | <span data-ttu-id="92cda-125">x</span><span class="sxs-lookup"><span data-stu-id="92cda-125">x</span></span>    | <span data-ttu-id="92cda-126">x</span><span class="sxs-lookup"><span data-stu-id="92cda-126">x</span></span>    | <span data-ttu-id="92cda-127">x</span><span class="sxs-lookup"><span data-stu-id="92cda-127">x</span></span>     | <span data-ttu-id="92cda-128">x</span><span class="sxs-lookup"><span data-stu-id="92cda-128">x</span></span>    | <span data-ttu-id="92cda-129">x</span><span class="sxs-lookup"><span data-stu-id="92cda-129">x</span></span>     |



 

<span data-ttu-id="92cda-130">Diese Anweisung entspricht der " [**Clip**](dx-graphics-hlsl-clip.md) "-Funktion von HLSL.</span><span class="sxs-lookup"><span data-stu-id="92cda-130">This instruction corresponds to the HLSL's [**clip**](dx-graphics-hlsl-clip.md) function.</span></span>

<span data-ttu-id="92cda-131">texkill führt keine Stichprobe für eine Textur aus.</span><span class="sxs-lookup"><span data-stu-id="92cda-131">texkill does not sample any texture.</span></span> <span data-ttu-id="92cda-132">Er arbeitet auf den ersten drei Komponenten der Texturkoordinaten, die von der Ziel Registernummer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="92cda-132">It operates on the first three components of the texture coordinates given by the destination register number.</span></span> <span data-ttu-id="92cda-133">Für PS \_ 1 \_ 4 arbeitet texkill mit den Daten in den ersten drei Komponenten des Ziel Registers.</span><span class="sxs-lookup"><span data-stu-id="92cda-133">For ps\_1\_4, texkill operates on the data in the first three components of the destination register.</span></span>

<span data-ttu-id="92cda-134">Sie können diese Anweisung verwenden, um beliebige Clip-Ebenen im Rasterizer zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="92cda-134">You can use this instruction to implement arbitrary clip planes in the rasterizer.</span></span>

<span data-ttu-id="92cda-135">Bei der Verwendung von Vertex-Shadern ist die Anwendung für das Anwenden der Perspektiven Transformation verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="92cda-135">When using vertex shaders, the application is responsible for applying the perspective transform.</span></span> <span data-ttu-id="92cda-136">Dies kann Probleme für die willkürlichen clippingflächen verursachen, denn wenn Sie anfügende Skalierungsfaktoren enthält, müssen auch die Clip-Ebenen transformiert werden.</span><span class="sxs-lookup"><span data-stu-id="92cda-136">This can cause problems for the arbitrary clipping planes because if it contains anisomorphic scale factors, the clip planes need to be transformed as well.</span></span> <span data-ttu-id="92cda-137">Daher ist es am besten, eine nicht projizierte Scheitelpunkt Position für die Verwendung im beliebigen clipperdienst bereitzustellen. dabei handelt es sich um den durch den texkill-Operator identifizierten Texturkoordinaten Satz.</span><span class="sxs-lookup"><span data-stu-id="92cda-137">Therefore, it is best to provide an unprojected vertex position to use in the arbitrary clipper, which is the texture coordinate set identified by the texkill operator.</span></span>

<span data-ttu-id="92cda-138">Diese Anweisung wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="92cda-138">This instruction is used as follows:</span></span>

<dl> <span data-ttu-id="92cda-139">texkill TN</span><span class="sxs-lookup"><span data-stu-id="92cda-139">texkill tn</span></span>  
<span data-ttu-id="92cda-140">Die Pixel Maskierung wird wie folgt durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="92cda-140">// The pixel masking is accomplished as follows:</span></span>  
<span data-ttu-id="92cda-141">if (x, y, z Komponenten von TextureCoordinates (Stufe n)<sub>uvwq</sub>< 0)</span><span class="sxs-lookup"><span data-stu-id="92cda-141">if ( the x,y,z components of TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )</span></span>  
<span data-ttu-id="92cda-142">Pixel Rendering Abbrechen</span><span class="sxs-lookup"><span data-stu-id="92cda-142">cancel pixel render</span></span>
</dl>

<span data-ttu-id="92cda-143">Für den Pixelshader 1 \_ 1, 1 \_ 2 und 1 \_ 3 arbeitet texkill mit dem Texturkoordinaten Satz, der von der Ziel Registernummer angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92cda-143">For pixel shader 1\_1, 1\_2, and 1\_3, texkill operates on the texture coordinate set given by the destination register number.</span></span> <span data-ttu-id="92cda-144">In Version 1 \_ 4 arbeitet texkill jedoch mit den Daten, die im [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) oder in dem temporären Register (RN) enthalten sind, das als Ziel angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="92cda-144">In version 1\_4, however, texkill operates on the data contained in the [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) or in the temporary register (rn) that has been specified as the destination.</span></span>

<span data-ttu-id="92cda-145">Wenn die multisamplinggrad-Funktion aktiviert ist, werden alle Antialiasing-Effekte, die aufgrund von multisamplinggrad auf Polygon Kanten erzielt wurden, nicht an einem von texkill generierten Edge erreicht.</span><span class="sxs-lookup"><span data-stu-id="92cda-145">When multisampling is enabled, any antialiasing effect achieved on polygon edges due to multisampling will not be achieved along any edge that has been generated by texkill.</span></span> <span data-ttu-id="92cda-146">Der Pixelshader wird einmal pro Pixel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92cda-146">The pixel shader runs once per pixel.</span></span>

<span data-ttu-id="92cda-147">Dieses Beispiel dient nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="92cda-147">This example is for illustration only.</span></span>

<span data-ttu-id="92cda-148">In diesem Beispiel werden Pixel mit negativen Texturkoordinaten maskiert.</span><span class="sxs-lookup"><span data-stu-id="92cda-148">This example masks out pixels that have negative texture coordinates.</span></span> <span data-ttu-id="92cda-149">Die Pixel Farben werden aus Scheitelpunkt Farben interpoliert, die in den Scheitelpunkt Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="92cda-149">The pixel colors are interpolated from vertex colors provided in the vertex data.</span></span>


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



<span data-ttu-id="92cda-150">Die Texturkoordinaten reichen von-0,5 bis 0,5 in u und 0,0 bis 1,0 in v.</span><span class="sxs-lookup"><span data-stu-id="92cda-150">The texture coordinates range from -0.5 to 0.5 in u, and 0.0 to 1.0 in v.</span></span> <span data-ttu-id="92cda-151">Diese Anweisung bewirkt, dass die negativen u-Werte maskiert werden. Die erste Abbildung unten zeigt die Vertexfarbe, die auf das Vierfache angewendet wird, ohne dass die texkill-Anweisung angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92cda-151">This instruction causes the negative u values to get masked out. The first illustration below shows the vertex color applied to the quad without the texkill instruction applied.</span></span> <span data-ttu-id="92cda-152">Die zweite Abbildung unten zeigt das Ergebnis der texkill-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="92cda-152">The second illustration below shows the result of the texkill instruction.</span></span> <span data-ttu-id="92cda-153">Die Pixel Farben aus den Texturkoordinaten unterhalb von 0 (wobei x von-0,5 bis 0,0 reicht) werden maskiert. Die Hintergrundfarbe (weiß) wird verwendet, wenn die Pixelfarbe maskiert ist.</span><span class="sxs-lookup"><span data-stu-id="92cda-153">The pixel colors from the texture coordinates below 0 (where x goes from -0.5 to 0.0) are masked out. The background color (white) is used where the pixel color is masked.</span></span>

![Abbildung der Ausgabe mit der auf das Vierfache angewendeten Vertexfarbe ohne die texkill-Anweisung](images/pstexkill-in.jpg)![Darstellung der Ausgabe mit angewendeter texkill-Anweisung](images/pstexkill-out.jpg)

<span data-ttu-id="92cda-156">Die Texturkoordinaten Daten werden in diesem Beispiel in der Vertex-Daten Deklaration deklariert.</span><span class="sxs-lookup"><span data-stu-id="92cda-156">The texture coordinate data is declared in the vertex data declaration in this example.</span></span>


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a><span data-ttu-id="92cda-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92cda-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92cda-158">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="92cda-158">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




