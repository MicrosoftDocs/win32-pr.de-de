---
title: dcl_semantics (SM3-PS ASM)
description: Deklarieren Sie die Zuordnung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101958"
---
# <a name="dcl_semantics-sm3---ps-asm"></a><span data-ttu-id="7cee9-103">DCL \_ -Semantik (SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="7cee9-103">dcl\_semantics (sm3 - ps asm)</span></span>

<span data-ttu-id="7cee9-104">Deklarieren Sie die Zuordnung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe.</span><span class="sxs-lookup"><span data-stu-id="7cee9-104">Declare the association between vertex shader output and pixel shader input.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cee9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cee9-105">Syntax</span></span>



|                                                   |
|---------------------------------------------------|
| <span data-ttu-id="7cee9-106">DCL- \_ Semantik \[ \_ Schwerpunkt \] DST \[ . Write \_ Mask\]</span><span class="sxs-lookup"><span data-stu-id="7cee9-106">dcl\_semantics \[\_centroid\] dst\[.write\_mask\]</span></span> |



 

<span data-ttu-id="7cee9-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="7cee9-107">Where:</span></span>

-   <span data-ttu-id="7cee9-108">\_Semantik: identifiziert die beabsichtigte Datenverwendung und kann beliebige Werte in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (ohne das \_ Präfix D3DDECLUSAGE) sein.</span><span class="sxs-lookup"><span data-stu-id="7cee9-108">\_semantics: Identifies the intended data usage, and may be any of the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (without the D3DDECLUSAGE\_ prefix).</span></span> <span data-ttu-id="7cee9-109">Außerdem kann ein ganzzahliger Index an die Semantik angehängt werden, um Parameter zu unterscheiden, die eine ähnliche Semantik verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cee9-109">Additionally, an integer index can be appended to the semantic to distinguish parameters that use similar semantics.</span></span>
-   <span data-ttu-id="7cee9-110">\[\_Schwerpunkt [](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] ist ein optionaler Anweisungs Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="7cee9-110">\[\_[Centroid](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)\] is an optional instruction modifier.</span></span> <span data-ttu-id="7cee9-111">Sie wird in DCL \_ -Verwendungs Anweisungen unterstützt, die die Eingabe Register deklarieren, und in den Anweisungen für die Textur Suche.</span><span class="sxs-lookup"><span data-stu-id="7cee9-111">It is is supported on dcl\_usage instructions that declare the input registers and on texture lookup instructions.</span></span> <span data-ttu-id="7cee9-112">Dem Schwerpunkt wird kein Leerzeichen angefügt.</span><span class="sxs-lookup"><span data-stu-id="7cee9-112">The centroid is appended with no space.</span></span>
-   <span data-ttu-id="7cee9-113">DST: Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="7cee9-113">dst: destination register.</span></span> <span data-ttu-id="7cee9-114">Siehe [PS \_ 3 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="7cee9-114">See [ps\_3\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).</span></span>
-   <span data-ttu-id="7cee9-115">Schreib \_ Maske: dasselbe Ausgabe Register kann mehrmals deklariert werden, jedes Mal mit einer eindeutigen Schreib Maske (damit eine andere Semantik auf einzelne Komponenten angewendet werden kann).</span><span class="sxs-lookup"><span data-stu-id="7cee9-115">write\_mask: The same output register may be declared multiple times, each time with a unique write mask (so different semantics can be applied to individual components).</span></span> <span data-ttu-id="7cee9-116">Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7cee9-116">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="7cee9-117">Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über vier Komponenten Register Grenzen (einzelne Ausgabe Register) hinausgehen können.</span><span class="sxs-lookup"><span data-stu-id="7cee9-117">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual output registers).</span></span> <span data-ttu-id="7cee9-118">Wenn die \_ Psize-Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da Sie als Skalar angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="7cee9-118">When the \_psize semantic is used, it should have a full write mask because it is considered a scalar.</span></span> <span data-ttu-id="7cee9-119">Wenn die \_ Positions Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da alle vier Komponenten geschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7cee9-119">When the \_position semantic is used, it should have full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cee9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7cee9-120">Remarks</span></span>



| <span data-ttu-id="7cee9-121">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="7cee9-121">Pixel shader versions</span></span> | <span data-ttu-id="7cee9-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="7cee9-122">1\_1</span></span> | <span data-ttu-id="7cee9-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="7cee9-123">1\_2</span></span> | <span data-ttu-id="7cee9-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7cee9-124">1\_3</span></span> | <span data-ttu-id="7cee9-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="7cee9-125">1\_4</span></span> | <span data-ttu-id="7cee9-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cee9-126">2\_0</span></span> | <span data-ttu-id="7cee9-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7cee9-127">2\_x</span></span> | <span data-ttu-id="7cee9-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cee9-128">2\_sw</span></span> | <span data-ttu-id="7cee9-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7cee9-129">3\_0</span></span> | <span data-ttu-id="7cee9-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7cee9-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7cee9-131">DCL- \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="7cee9-131">dcl\_usage</span></span>            |      |      |      |      |      |      |       | <span data-ttu-id="7cee9-132">x</span><span class="sxs-lookup"><span data-stu-id="7cee9-132">x</span></span>    | <span data-ttu-id="7cee9-133">x</span><span class="sxs-lookup"><span data-stu-id="7cee9-133">x</span></span>     |



 

<span data-ttu-id="7cee9-134">Alle DCL- \_ Verwendungs Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7cee9-134">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="7cee9-135">Deklarations Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cee9-135">Declaration Examples</span></span>


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a><span data-ttu-id="7cee9-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7cee9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cee9-137">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="7cee9-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

<span data-ttu-id="7cee9-138">[Beispiel für AntiAlias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="7cee9-138">[Antialias Sample](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 