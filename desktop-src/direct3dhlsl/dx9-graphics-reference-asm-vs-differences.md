---
title: Vertexshader-Unterschiede
description: Vertexshader-Unterschiede
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039121"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="f8c4e-103">Vertexshader-Unterschiede</span><span class="sxs-lookup"><span data-stu-id="f8c4e-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="f8c4e-104">Anweisungs Slots</span><span class="sxs-lookup"><span data-stu-id="f8c4e-104">Instruction Slots</span></span>

<span data-ttu-id="f8c4e-105">Jede Version unterstützt eine abweichende Anzahl an maximalen Anweisungs Slots.</span><span class="sxs-lookup"><span data-stu-id="f8c4e-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="f8c4e-106">Version</span><span class="sxs-lookup"><span data-stu-id="f8c4e-106">Version</span></span>  | <span data-ttu-id="f8c4e-107">Maximale Anzahl von Anweisungs Slots</span><span class="sxs-lookup"><span data-stu-id="f8c4e-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8c4e-108">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f8c4e-108">vs\_1\_1</span></span> | <span data-ttu-id="f8c4e-109">128</span><span class="sxs-lookup"><span data-stu-id="f8c4e-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="f8c4e-110">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8c4e-110">vs\_2\_0</span></span> | <span data-ttu-id="f8c4e-111">256</span><span class="sxs-lookup"><span data-stu-id="f8c4e-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="f8c4e-112">vs \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f8c4e-112">vs\_2\_x</span></span> | <span data-ttu-id="f8c4e-113">256</span><span class="sxs-lookup"><span data-stu-id="f8c4e-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="f8c4e-114">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f8c4e-114">vs\_3\_0</span></span> | <span data-ttu-id="f8c4e-115">512 (minimal) und bis zur Anzahl der Slots in D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="f8c4e-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="f8c4e-116">Siehe [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f8c4e-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="f8c4e-117">Informationen zu den Einschränkungen von Software-Shadern finden Sie unter [Software-Shader](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="f8c4e-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="f8c4e-118">Schachtelungs Limits der Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="f8c4e-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="f8c4e-119">Siehe Schachtelungs [Limits der Fluss Steuerung](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="f8c4e-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="f8c4e-120">vs \_ 1 \_ 1-Features</span><span class="sxs-lookup"><span data-stu-id="f8c4e-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="f8c4e-121">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-121">New instructions:</span></span>

<span data-ttu-id="f8c4e-122">Weitere Informationen finden Sie unter [Anweisungen-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="f8c4e-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="f8c4e-123">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-123">New registers:</span></span>

<span data-ttu-id="f8c4e-124">Weitere Informationen finden Sie unter [Registern-vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="f8c4e-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="f8c4e-125">vs \_ 2 \_ 0-Features</span><span class="sxs-lookup"><span data-stu-id="f8c4e-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="f8c4e-126">Neue Funktionen:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-126">New features:</span></span>

-   <span data-ttu-id="f8c4e-127">Statische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="f8c4e-127">Static flow control</span></span>
-   <span data-ttu-id="f8c4e-128">Alle vier Komponenten des [Adress Registers](dx9-graphics-reference-asm-vs-registers-address.md) (a0) sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8c4e-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="f8c4e-129">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-129">New instructions:</span></span>

-   <span data-ttu-id="f8c4e-130">Setup Anweisungen- [DEFB-vs](defb---vs.md), [defi-vs](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="f8c4e-131">Arithmetische Anweisungen: [ABS-vs](abs---vs.md), [CRS-vs](crs---vs.md), [LRP-vs](lrp---vs.md), [MUVA-vs](mova---vs.md), [NRM-vs](nrm---vs.md), [Pow-vs](pow---vs.md), [SGN-vs](sgn---vs.md), [SinCos-vs](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="f8c4e-132">Anweisungen zur statischen Fluss Steuerung: [aufrufen-vs](call---vs.md), [callnz bool-vs](callnz-bool---vs.md), [else-vs](else---vs.md), [EndIf-vs](endif---vs.md), [ENDLOOP-vs](endloop---vs.md), [ENDREP-vs](endrep---vs.md), [if bool-vs](if-bool---vs.md), [Label-vs](label---vs.md), [Loop-vs](loop---vs.md), [Rep-vs](rep---vs.md), [ret-vs](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="f8c4e-133">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-133">New registers:</span></span>

-   <span data-ttu-id="f8c4e-134">[Konstantes boolesches Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="f8c4e-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="f8c4e-135">[Konstantes ganzzahliges Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="f8c4e-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="f8c4e-136">[Schleifen-Counter-Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="f8c4e-137">vs \_ 2 \_ x-Features</span><span class="sxs-lookup"><span data-stu-id="f8c4e-137">vs\_2\_x Features</span></span>

<span data-ttu-id="f8c4e-138">Neue Features (D3DCAPS9). VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="f8c4e-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="f8c4e-139">Dynamische Fluss Steuerung</span><span class="sxs-lookup"><span data-stu-id="f8c4e-139">Dynamic flow control</span></span>
-   <span data-ttu-id="f8c4e-140">Schachtelung für dynamische und statische Fluss Steuerungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="f8c4e-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="f8c4e-141">Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-vs-registers-temporary.md)-e (r \# )</span><span class="sxs-lookup"><span data-stu-id="f8c4e-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="f8c4e-142">Prädikation</span><span class="sxs-lookup"><span data-stu-id="f8c4e-142">Predication</span></span>

<span data-ttu-id="f8c4e-143">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-143">New Instructions:</span></span>

-   <span data-ttu-id="f8c4e-144">Dynamische Fluss Steuerungs Anweisungen: unter [brechen](break---vs.md)von [Comp- \_ vs](break-comp---vs.md), Break [p-vs](breakp---vs.md), [callnz pred-vs](callnz-pred---vs.md), [if \_ Comp-vs](if-comp---vs.md), [if pred-vs](if-pred---vs.md), [SETP \_ Comp-vs](setp-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="f8c4e-145">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-145">New registers:</span></span>

-   <span data-ttu-id="f8c4e-146">[Prädikat Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="f8c4e-147">vs \_ 3 \_ 0-Features</span><span class="sxs-lookup"><span data-stu-id="f8c4e-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="f8c4e-148">Neue Features:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-148">New features :</span></span>

-   <span data-ttu-id="f8c4e-149">Textur Suche</span><span class="sxs-lookup"><span data-stu-id="f8c4e-149">Texture lookup</span></span>
-   <span data-ttu-id="f8c4e-150">Indizierbare [Ausgabe Register](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )</span><span class="sxs-lookup"><span data-stu-id="f8c4e-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="f8c4e-151">Anzahl der [temporären Registrierungs](dx9-graphics-reference-asm-vs-registers-temporary.md)-e (r \# ) wurde auf 32 erweitert.</span><span class="sxs-lookup"><span data-stu-id="f8c4e-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="f8c4e-152">Neue Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-152">New instructions:</span></span>

-   <span data-ttu-id="f8c4e-153">Setup Anweisung- [DCL \_ samplertype (SM3-vs ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="f8c4e-154">Textur Anweisung- [texldl-vs](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="f8c4e-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="f8c4e-155">Neue Register:</span><span class="sxs-lookup"><span data-stu-id="f8c4e-155">New registers:</span></span>

-   <span data-ttu-id="f8c4e-156">[Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s \# )</span><span class="sxs-lookup"><span data-stu-id="f8c4e-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8c4e-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8c4e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8c4e-158">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="f8c4e-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 