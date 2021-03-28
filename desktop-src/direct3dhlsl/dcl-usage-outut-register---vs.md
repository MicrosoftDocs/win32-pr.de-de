---
title: dcl_usage Ausgabe (SM1, SM2, SM3-vs ASM)
description: Die verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert (zwei für Farbe, acht für die Textur, eine für die Position und eine für den Nebel und die Punktgröße).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c653c5af43bd3392f97e30571ac56ded66cbfc04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993526"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="b2b2d-103">DCL- \_ Verwendungs Ausgabe (SM1, SM2, SM3-vs ASM)</span><span class="sxs-lookup"><span data-stu-id="b2b2d-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="b2b2d-104">Die verschiedenen Typen von Ausgabe Registern wurden in zwölf Ausgabe Register reduziert (zwei für Farbe, acht für die Textur, eine für die Position und eine für den Nebel und die Punktgröße).</span><span class="sxs-lookup"><span data-stu-id="b2b2d-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="b2b2d-105">Diese können für alle Elemente verwendet werden, die der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Nebel usw.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="b2b2d-106">Ausgabe Register erfordern Deklarationen, die Semantik einschließen.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="b2b2d-107">Beispielsweise werden die alten Positions-und Punktgrößen Register durch Deklarieren eines Ausgabe Registers mit einer Position oder einer Semantik für die Punktgröße ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="b2b2d-108">Von den zwölf Ausgabe Registern verfügen alle zehn (nicht notwendigerweise o0 bis O9) über vier Komponenten (xyzw), eine andere muss als Position deklariert werden (und müssen auch alle vier Komponenten enthalten), und optional kann auch eine skalare Punktgröße sein.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b2d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b2d-109">Syntax</span></span>

<span data-ttu-id="b2b2d-110">Die Syntax zum Deklarieren von Ausgabe Registern ähnelt den Deklarationen für das Eingabe Register:</span><span class="sxs-lookup"><span data-stu-id="b2b2d-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="b2b2d-111">DCL- \_ Semantik o \[ . Schreib \_ Maske\]</span><span class="sxs-lookup"><span data-stu-id="b2b2d-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="b2b2d-112">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="b2b2d-112">Where:</span></span>

-   <span data-ttu-id="b2b2d-113">die DCL- \_ Semantik kann denselben Satz von Semantik wie für die Eingabe Deklaration verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="b2b2d-114">Semantik Namen stammen aus [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (und sind mit einem Index gekoppelt, z. b. Position3).</span><span class="sxs-lookup"><span data-stu-id="b2b2d-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="b2b2d-115">Es muss immer ein Ausgabe Register mit der positiont0 Semantic vorhanden sein, wenn es nicht für die Verarbeitung von Scheitel Punkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="b2b2d-116">Die Semantik positiont0 Semantic und pointsize0 sind die einzigen, die die Bedeutung haben, die über die einfache Verknüpfung von Scheitel Punkten zu Pixel-Shadern hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="b2b2d-117">Für Shader mit Fluss Steuerung wird angenommen, dass die schlechteste Fall Ausgabe deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="b2b2d-118">Es gibt keine Standardwerte, wenn ein Shader nicht tatsächlich angibt, was er deklariert (aufgrund der Fluss Steuerung).</span><span class="sxs-lookup"><span data-stu-id="b2b2d-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="b2b2d-119">o ist ein Ausgabe Register.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-119">o is an output register.</span></span> <span data-ttu-id="b2b2d-120">Siehe [Ausgabe \_ Register](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="b2b2d-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="b2b2d-121">\_die Schreib Maske gibt das gleiche Ausgabe Register an, das mehrmals deklariert werden kann (damit unterschiedliche Semantik auf einzelne Komponenten angewendet werden kann), und zwar jedes Mal mit einer eindeutigen Schreib Maske.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="b2b2d-122">Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="b2b2d-123">Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über vier Komponenten Register Grenzen (einzelne Register) hinausgehen können.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="b2b2d-124">Wenn die Semantik für die Punktgröße verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da Sie als Skalar angesehen wird.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="b2b2d-125">Wenn die Positions Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da alle vier Komponenten geschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b2d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2b2d-126">Remarks</span></span>



| <span data-ttu-id="b2b2d-127">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b2b2d-127">Vertex shader versions</span></span> | <span data-ttu-id="b2b2d-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2b2d-128">3\_0</span></span> | <span data-ttu-id="b2b2d-129">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2b2d-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="b2b2d-130">DCL- \_ Verwendung</span><span class="sxs-lookup"><span data-stu-id="b2b2d-130">dcl\_usage</span></span>             | <span data-ttu-id="b2b2d-131">x</span><span class="sxs-lookup"><span data-stu-id="b2b2d-131">x</span></span>    | <span data-ttu-id="b2b2d-132">x</span><span class="sxs-lookup"><span data-stu-id="b2b2d-132">x</span></span>     |



 

<span data-ttu-id="b2b2d-133">Alle [DCL- \_ Verwendungs](dcl-usage-input-register---vs.md) Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b2b2d-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="b2b2d-134">Deklarations Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2b2d-134">Declaration Examples</span></span>


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a><span data-ttu-id="b2b2d-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b2b2d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2b2d-136">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b2b2d-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 