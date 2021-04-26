---
title: dcl_usage Ausgabe (sm1, sm2, sm3 – vs asm)
description: Die verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert (zwei für Farbe, acht für Textur, eins für die Position und eins für Dies und Punktgröße).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 314c9c9a9a9e62915e9224b3cf165bc54d09a516
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999167"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="796bf-103">dcl \_ usage output (sm1, sm2, sm3 - vs asm)</span><span class="sxs-lookup"><span data-stu-id="796bf-103">dcl\_usage output (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="796bf-104">Die verschiedenen Arten von Ausgaberegistern wurden in zwölf Ausgaberegister reduziert (zwei für Farbe, acht für Textur, eins für die Position und eins für Dies und Punktgröße).</span><span class="sxs-lookup"><span data-stu-id="796bf-104">The various types of output registers have been collapsed into twelve output registers (two for color, eight for texture, one for position, and one for fog and point size).</span></span> <span data-ttu-id="796bf-105">Diese können für alles verwendet werden, was der Benutzer für den Pixelshader interpolieren möchte: Texturkoordinaten, Farben, Oberflächen usw.</span><span class="sxs-lookup"><span data-stu-id="796bf-105">These can be used for anything the user wants to interpolate for the pixel shader: texture coordinates, colors, fog, and so on.</span></span>

<span data-ttu-id="796bf-106">Ausgaberegister erfordern Deklarationen, die Semantik enthalten.</span><span class="sxs-lookup"><span data-stu-id="796bf-106">Output registers require declarations that include semantics.</span></span> <span data-ttu-id="796bf-107">Beispielsweise werden die alten Register für Position und Punktgröße ersetzt, indem ein Ausgaberegister mit einer Position oder einer Punktgrößensemantik deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="796bf-107">For instance, the old position and point size registers are replaced by declaring an output register with a position or point-size semantic.</span></span>

<span data-ttu-id="796bf-108">Von den zwölf Ausgaberegistern verfügen alle zehn (nicht unbedingt o0 bis o9) über vier Komponenten (xyzw), eine andere muss als Position deklariert werden (und muss auch alle vier Komponenten enthalten), und optional kann eine weitere Skalarpunktgröße sein.</span><span class="sxs-lookup"><span data-stu-id="796bf-108">Of the twelve output registers, any ten (not necessarily o0 to o9) have four components (xyzw), another one must be declared as position (and must also include all four components), and optionally one more can be a scalar point size.</span></span>

## <a name="syntax"></a><span data-ttu-id="796bf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="796bf-109">Syntax</span></span>

<span data-ttu-id="796bf-110">Die Syntax zum Deklarieren von Ausgaberegistern ähnelt den Deklarationen für das Eingaberegister:</span><span class="sxs-lookup"><span data-stu-id="796bf-110">The syntax for declaring output registers is similar to the declarations for the input register:</span></span>



|                                  |
|----------------------------------|
| <span data-ttu-id="796bf-111">dcl \_ semantics o \[ .write \_ mask\]</span><span class="sxs-lookup"><span data-stu-id="796bf-111">dcl\_semantics o\[.write\_mask\]</span></span> |



 

<span data-ttu-id="796bf-112">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="796bf-112">Where:</span></span>

-   <span data-ttu-id="796bf-113">Die \_ dcl-Semantik kann den gleichen Semantiksatz wie für die Eingabedeklaration verwenden.</span><span class="sxs-lookup"><span data-stu-id="796bf-113">dcl\_semantics can use the same set of semantics as for the input declaration.</span></span> <span data-ttu-id="796bf-114">Semantische Namen stammen aus [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (und werden mit einem Index gekoppelt, z.B. position3).</span><span class="sxs-lookup"><span data-stu-id="796bf-114">Semantic names come from [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (and are paired with an index, such as position3).</span></span> <span data-ttu-id="796bf-115">Es muss immer ein Ausgaberegister mit der Semantik positiont0 vorhanden sein, wenn es nicht für die Verarbeitung von Scheitelpunkten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="796bf-115">There always has to be one output register with the positiont0 semantic when not used for processing vertices.</span></span> <span data-ttu-id="796bf-116">Die Positiont0-Semantik und die Pointsize0-Semantik sind die einzigen, die eine Bedeutung haben, die über die einfache Verknüpfung von Scheitelpunkt- zu Pixel-Shadern hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="796bf-116">The positiont0 semantic and the pointsize0 semantic are the only ones that have meaning beyond simply allowing linkage from vertex to pixel shaders.</span></span> <span data-ttu-id="796bf-117">Bei Shadern mit Flusssteuerung wird davon ausgegangen, dass die Ausgabe im schlechtesten Fall deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="796bf-117">For shaders with flow control, it is assumed that the worst case output is declared.</span></span> <span data-ttu-id="796bf-118">Es gibt keine Standardwerte, wenn ein Shader nicht tatsächlich ausgibt, was er deklariert (aufgrund der Flusssteuerung).</span><span class="sxs-lookup"><span data-stu-id="796bf-118">There are no defaults if a shader does not actually output what it declares it should (due to flow control).</span></span>
-   <span data-ttu-id="796bf-119">o ist ein Ausgaberegister.</span><span class="sxs-lookup"><span data-stu-id="796bf-119">o is an output register.</span></span> <span data-ttu-id="796bf-120">Weitere Informationen finden Sie [ \_ unter Ausgaberegister.](dx9-graphics-reference-asm-vs-registers-vs-3-0.md)</span><span class="sxs-lookup"><span data-stu-id="796bf-120">See [Output\_Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).</span></span>
-   <span data-ttu-id="796bf-121">Die Schreibmaske gibt dasselbe Ausgaberegister an, das mehrmals deklariert werden kann (sodass unterschiedliche Semantik auf einzelne Komponenten angewendet werden kann), jedes Mal mit einer eindeutigen \_ Schreibmaske.</span><span class="sxs-lookup"><span data-stu-id="796bf-121">write\_mask indicates the same output register that can be declared multiple times (so different semantics can be applied to individual components), each time with a unique write mask.</span></span> <span data-ttu-id="796bf-122">Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="796bf-122">However, the same semantic cannot be used multiple times in a declaration.</span></span> <span data-ttu-id="796bf-123">Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über Vier-Komponenten-Registergrenzen (einzelne Register) hinweg gehen können.</span><span class="sxs-lookup"><span data-stu-id="796bf-123">This means that vectors must be four components or less, and cannot go across four-component register boundaries (individual registers).</span></span> <span data-ttu-id="796bf-124">Wenn die Semantik der Punktgröße verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da sie als Skalar betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="796bf-124">When the point-size semantic is used, it should have full write mask because it is considered a scalar.</span></span> <span data-ttu-id="796bf-125">Wenn die Positionssemantik verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da alle vier Komponenten geschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="796bf-125">When the position semantic is used, it should have a full write mask because all four components have to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="796bf-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="796bf-126">Remarks</span></span>



| <span data-ttu-id="796bf-127">Vertex-Shaderversionen</span><span class="sxs-lookup"><span data-stu-id="796bf-127">Vertex shader versions</span></span> | <span data-ttu-id="796bf-128">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="796bf-128">3\_0</span></span> | <span data-ttu-id="796bf-129">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="796bf-129">3\_sw</span></span> |
|------------------------|------|-------|
| <span data-ttu-id="796bf-130">dcl \_ usage</span><span class="sxs-lookup"><span data-stu-id="796bf-130">dcl\_usage</span></span>             | <span data-ttu-id="796bf-131">x</span><span class="sxs-lookup"><span data-stu-id="796bf-131">x</span></span>    | <span data-ttu-id="796bf-132">x</span><span class="sxs-lookup"><span data-stu-id="796bf-132">x</span></span>     |



 

<span data-ttu-id="796bf-133">Alle [ \_ dcl-Verwendungsanweisungen](dcl-usage-input-register---vs.md) müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="796bf-133">All [dcl\_usage](dcl-usage-input-register---vs.md) instructions must appear before the first executable instruction.</span></span>

## <a name="declaration-examples"></a><span data-ttu-id="796bf-134">Deklarationsbeispiele</span><span class="sxs-lookup"><span data-stu-id="796bf-134">Declaration Examples</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="796bf-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="796bf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="796bf-136">Vertex-Shader-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="796bf-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
