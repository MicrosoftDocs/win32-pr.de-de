---
title: texcoord-PS
description: Interpretiert Texturkoordinaten Daten (UVW1) als Farbdaten (RGBA).
ms.assetid: 0f79a62c-1142-4dcd-aa2f-a5bd1c369ffc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e871d1f91d89d0eb0ddadee34b5ac215916d0af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728057"
---
# <a name="texcoord---ps"></a><span data-ttu-id="04ee9-103">texcoord-PS</span><span class="sxs-lookup"><span data-stu-id="04ee9-103">texcoord - ps</span></span>

<span data-ttu-id="04ee9-104">Interpretiert Texturkoordinaten Daten (UVW1) als Farbdaten (RGBA).</span><span class="sxs-lookup"><span data-stu-id="04ee9-104">Interprets texture coordinate data (UVW1) as color data (RGBA).</span></span>

## <a name="syntax"></a><span data-ttu-id="04ee9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04ee9-105">Syntax</span></span>



| <span data-ttu-id="04ee9-106">texcoord-DST</span><span class="sxs-lookup"><span data-stu-id="04ee9-106">texcoord dst</span></span> |
|--------------|



 

<span data-ttu-id="04ee9-107">where</span><span class="sxs-lookup"><span data-stu-id="04ee9-107">where</span></span>

-   <span data-ttu-id="04ee9-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="04ee9-108">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="04ee9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04ee9-109">Remarks</span></span>



| <span data-ttu-id="04ee9-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="04ee9-110">Pixel shader versions</span></span> | <span data-ttu-id="04ee9-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="04ee9-111">1\_1</span></span> | <span data-ttu-id="04ee9-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="04ee9-112">1\_2</span></span> | <span data-ttu-id="04ee9-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="04ee9-113">1\_3</span></span> | <span data-ttu-id="04ee9-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="04ee9-114">1\_4</span></span> | <span data-ttu-id="04ee9-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04ee9-115">2\_0</span></span> | <span data-ttu-id="04ee9-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="04ee9-116">2\_x</span></span> | <span data-ttu-id="04ee9-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="04ee9-117">2\_sw</span></span> | <span data-ttu-id="04ee9-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04ee9-118">3\_0</span></span> | <span data-ttu-id="04ee9-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="04ee9-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="04ee9-120">texcoord</span><span class="sxs-lookup"><span data-stu-id="04ee9-120">texcoord</span></span>              | <span data-ttu-id="04ee9-121">x</span><span class="sxs-lookup"><span data-stu-id="04ee9-121">x</span></span>    | <span data-ttu-id="04ee9-122">x</span><span class="sxs-lookup"><span data-stu-id="04ee9-122">x</span></span>    | <span data-ttu-id="04ee9-123">x</span><span class="sxs-lookup"><span data-stu-id="04ee9-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="04ee9-124">Diese Anweisung interpretiert den Texturkoordinaten Satz (UVW1), der der Ziel Registernummer als Farbdaten (RGBA) entspricht.</span><span class="sxs-lookup"><span data-stu-id="04ee9-124">This instruction interprets the texture coordinate set (UVW1) corresponding to the destination register number as color data (RGBA).</span></span> <span data-ttu-id="04ee9-125">Wenn der Texturkoordinaten Satz weniger als drei Komponenten enthält, werden die fehlenden Komponenten auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-125">If the texture coordinate set contains fewer than three components, the missing components are set to 0.</span></span> <span data-ttu-id="04ee9-126">Die vierte Komponente ist immer auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-126">The fourth component is always set to 1.</span></span> <span data-ttu-id="04ee9-127">Alle Werte werden zwischen 0 und 1 geklammert.</span><span class="sxs-lookup"><span data-stu-id="04ee9-127">All values are clamped between 0 and 1.</span></span>

<span data-ttu-id="04ee9-128">Der Vorteil von texcoord besteht darin, dass es eine Möglichkeit bietet, Scheitelpunkt Daten mit hoher Genauigkeit direkt in den Pixelshader zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="04ee9-128">The advantage of texcoord is that it provides a way to pass vertex data interpolated at high precision directly into the pixel shader.</span></span> <span data-ttu-id="04ee9-129">Wenn die Daten jedoch in das Ziel Register geschrieben werden, gehen einige Genauigkeit verloren, abhängig von der Anzahl der Bits, die von der Hardware für Register verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04ee9-129">However, when the data is written into the destination register, some precision will be lost, depending on the number of bits used by the hardware for registers.</span></span>

<span data-ttu-id="04ee9-130">Von dieser Anweisung wird keine Textur entnommen.</span><span class="sxs-lookup"><span data-stu-id="04ee9-130">No texture is sampled by this instruction.</span></span> <span data-ttu-id="04ee9-131">Nur für diese Textur Stufe festgelegte Texturkoordinaten sind relevant.</span><span class="sxs-lookup"><span data-stu-id="04ee9-131">Only texture coordinates set on this texture stage are relevant.</span></span>

<span data-ttu-id="04ee9-132">Alle Textur Daten (z. b. Position, normal und Lichtquellen Richtung) können von einem Vertexshader in eine Textur Koordinate zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="04ee9-132">Any texture data (such as position, normal, and light source direction) can be mapped by a vertex shader into a texture coordinate.</span></span> <span data-ttu-id="04ee9-133">Dies erfolgt durch Zuordnen einer Textur zu einem Textur Register mithilfe von [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) und durch Angeben der Art und Weise, wie die Textur Stichprobe mithilfe von [**settexturestagestate**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04ee9-133">This is done by associating a texture with a texture register using [**SetTexture**](/windows/desktop/direct3d9/id3dxbaseeffect--settexture) and by specifying how the texture sampling is done using [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span> <span data-ttu-id="04ee9-134">Wenn die Pipeline für eine fixierte Funktion verwendet wird, stellen Sie sicher, dass Sie das TSS \_ texcoordindex-Flag angeben.</span><span class="sxs-lookup"><span data-stu-id="04ee9-134">If the fixed function pipeline is used, be sure to supply the TSS\_TEXCOORDINDEX flag.</span></span>

<span data-ttu-id="04ee9-135">Diese Anweisung wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="04ee9-135">This instruction is used as follows:</span></span>


```
texcoord tn
```



<span data-ttu-id="04ee9-136">Ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) enthält vier Farbwerte (RGBA).</span><span class="sxs-lookup"><span data-stu-id="04ee9-136">An [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) contains four color values (RGBA).</span></span> <span data-ttu-id="04ee9-137">Die Daten können auch als Vektordaten (xyzw) betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="04ee9-137">The data can also be thought of as vector data (xyzw).</span></span> <span data-ttu-id="04ee9-138">texcoord ruft drei dieser Werte (XYZ) aus dem Texturkoordinaten Satz x ab, und die vierte Komponente (w) wird auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-138">texcoord will retrieve three of these values (xyz) from texture coordinate set x, and the fourth component (w) is set to 1.</span></span> <span data-ttu-id="04ee9-139">Die Textur Adresse wird aus dem Texturkoordinaten Satz n kopiert.</span><span class="sxs-lookup"><span data-stu-id="04ee9-139">The texture address is copied from the texture coordinate set n.</span></span> <span data-ttu-id="04ee9-140">Das Ergebnis wird zwischen 0 und 1 geklammert.</span><span class="sxs-lookup"><span data-stu-id="04ee9-140">The result is clamped between 0 and 1.</span></span>

<span data-ttu-id="04ee9-141">Dieses Beispiel dient nur zur Veranschaulichung.</span><span class="sxs-lookup"><span data-stu-id="04ee9-141">This example is for illustration only.</span></span> <span data-ttu-id="04ee9-142">Der C-Code, der den Shader begleitet, wurde nicht für die Leistung optimiert.</span><span class="sxs-lookup"><span data-stu-id="04ee9-142">The C code accompanying the shader has not been optimized for performance.</span></span>

<span data-ttu-id="04ee9-143">Hier ist ein Beispiel-Shader, der texcoord verwendet.</span><span class="sxs-lookup"><span data-stu-id="04ee9-143">Here is an example shader using texcoord.</span></span>


```
ps_1_1        ; version instruction
texcoord t0   ; declare t0 hold texture coordinates, 
              ; which represent rgba values in this example
mov r0, t0    ; move the color in t0 to output register r0
```



<span data-ttu-id="04ee9-144">Die gerenderte Ausgabe des Pixelshaders wird in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-144">The rendered output from the pixel shader is shown in the following illustration.</span></span> <span data-ttu-id="04ee9-145">Die Koordinaten Werte (u, v, w, 1) werden den Kanälen (RGB) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="04ee9-145">The (u,v,w,1) coordinate values map to the (rgb) channels.</span></span> <span data-ttu-id="04ee9-146">Der Alphakanal ist auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-146">The alpha channel is set to 1.</span></span> <span data-ttu-id="04ee9-147">In den Ecken der Abbildung wird Koordinate (0, 0, 0, 1) als schwarz interpretiert. (1, 0, 0, 1) ist rot. (0, 1, 0, 1) ist grün. und (1, 1, 0, 1) enthält grün und rot, wodurch gelb erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="04ee9-147">At the corners of the illustration, coordinate (0,0,0,1) is interpreted as black; (1,0,0,1) is red; (0,1,0,1) is green; and (1,1,0,1) contains green and red, producing yellow.</span></span>

![Abbildung der gerenderten Ausgabe des Pixelshaders example](images/pstexcoord.jpg)

<span data-ttu-id="04ee9-149">Zusätzlicher Code ist erforderlich, um diesen Shader zu verwenden, und ein Beispielszenario ist unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="04ee9-149">Additional code is required to use this shader and an example scenario is shown below.</span></span>


```
// This code creates the shader from a file. The contents of  
// the shader file can also be supplied as a text string.
LPD3DXBUFFER        pCode;

// Assemble the vertex shader from the file
D3DXAssembleShaderFromFile(strPShaderPath, 0, NULL, &pCode, NULL);
m_pd3dDevice->CreatePixelShader((DWORD*)pCode->GetBufferPointer(),
                   &m_hPixelShader);
pCode->Release();

// This code defines the object vertex data
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_TEX1|TEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z     u1    v1   
    { -1.0f, -1.0f, 0.0f, 0.0f, 0.0f, },
    { +1.0f, -1.0f, 0.0f, 1.0f, 0.0f, },
    { +1.0f, +1.0f, 0.0f, 1.0f, 1.0f, },
    { -1.0f, +1.0f, 0.0f, 0.0f, 1.0f, },
};
```



## <a name="related-topics"></a><span data-ttu-id="04ee9-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04ee9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04ee9-151">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="04ee9-151">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 