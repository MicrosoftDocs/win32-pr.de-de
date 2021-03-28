---
title: vs_2_0
description: Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce4e986e610ff95716cd6899d6167e4f69efe042
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976145"
---
# <a name="vs_2_0"></a><span data-ttu-id="e783d-105">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e783d-105">vs\_2\_0</span></span>

<span data-ttu-id="e783d-106">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die für Scheitelpunkt Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e783d-106">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="e783d-107">Registriert Übertragungsdaten in und aus dem Alu.</span><span class="sxs-lookup"><span data-stu-id="e783d-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="e783d-108">Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e783d-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="e783d-109">[Anweisungen: vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="e783d-109">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="e783d-110">[Register-vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader-Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e783d-110">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="e783d-111">[Vertex-Shader-registermodifiziererer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e783d-111">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="e783d-112">[Vertex-Shader-Quell Registrierungs Modifizierers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e783d-112">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="e783d-113">Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e783d-113">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="e783d-114">Die [Ziel Register Maskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e783d-114">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="e783d-115">Anweisungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="e783d-115">Instruction Count</span></span>

<span data-ttu-id="e783d-116">Jeder Vertex-Shader kann bis zu 256 Anweisungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e783d-116">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="e783d-117">Die Anzahl der auszuwerenden Anweisungen kann aufgrund der Unterstützung für Schleifen/Rep erheblich höher sein und wird von D3DCAPS9 begrenzt. Maxvshaderinstructionsexecuted, mindestens 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e783d-117">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e783d-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e783d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e783d-119">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="e783d-119">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




