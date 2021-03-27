---
title: ps_2_0
description: Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden. Registriert Übertragungsdaten in und aus dem Alu. Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104975905"
---
# <a name="ps_2_0"></a><span data-ttu-id="1e4f7-105">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1e4f7-105">ps\_2\_0</span></span>

<span data-ttu-id="1e4f7-106">Ein programmierbarer Pixelshader besteht aus einer Reihe von Anweisungen, die auf Pixeldaten angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-106">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="1e4f7-107">Registriert Übertragungsdaten in und aus dem Alu.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-107">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="1e4f7-108">Zusätzliche Steuerelemente können angewendet werden, um die Anweisung, die Ergebnisse oder die abgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-108">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="1e4f7-109">[die \_ Anweisungen für PS 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) enthalten eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-109">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="1e4f7-110">[PS \_ 2 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) listet die verschiedenen Register Typen auf, die von Vertex-Shader Alu verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-110">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="1e4f7-111">[Modifiziererer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Wird verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-111">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="1e4f7-112">Die [Ziel Register-Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Ziel Registers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-112">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="1e4f7-113">[Pixel-Shader-Quell Registrierungs Modifizierern](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quell Registrierungsdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-113">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="1e4f7-114">Das [Quellen Register "Schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) " bietet zusätzliche Kontrolle darüber, welche Register Komponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-114">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="1e4f7-115">Anweisungs Anzahl</span><span class="sxs-lookup"><span data-stu-id="1e4f7-115">Instruction Count</span></span>

<span data-ttu-id="1e4f7-116">Shader haben Beschränkungen für die maximale Anweisungs Anzahl.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-116">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="1e4f7-117">Anweisungs Slots gesamt: 96 (64 Arithmetik und 32 Textur).</span><span class="sxs-lookup"><span data-stu-id="1e4f7-117">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="1e4f7-118">Sampleranzahl</span><span class="sxs-lookup"><span data-stu-id="1e4f7-118">Sampler Count</span></span>

<span data-ttu-id="1e4f7-119">Die Anzahl der verfügbaren Textur-Samplern ist 16.</span><span class="sxs-lookup"><span data-stu-id="1e4f7-119">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e4f7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e4f7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e4f7-121">Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="1e4f7-121">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




