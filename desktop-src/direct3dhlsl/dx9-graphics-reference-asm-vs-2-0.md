---
title: vs_2_0
description: Erfahren Sie vs_2_0, einem programmierbaren Vertex-Shader, der aus einer Reihe von Anweisungen besteht, die mit Scheitelpunktdaten arbeiten.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010853"
---
# <a name="vs_2_0"></a><span data-ttu-id="31506-103">vs \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31506-103">vs\_2\_0</span></span>

<span data-ttu-id="31506-104">Ein programmierbarer Vertex-Shader besteht aus einer Reihe von Anweisungen, die mit Scheitelpunktdaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="31506-104">A programmable vertex shader is made up of a set of instructions that operate on vertex data.</span></span> <span data-ttu-id="31506-105">Registriert Übertragungsdaten in und aus der ALU.</span><span class="sxs-lookup"><span data-stu-id="31506-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="31506-106">Zusätzliche Steuerung kann angewendet werden, um die Anweisung, die Ergebnisse oder die ausgeschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="31506-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="31506-107">[Anweisungen im Vergleich \_ zu \_ 2 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="31506-107">[Instructions - vs\_2\_0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="31506-108">[Register : Im Vergleich \_ zu 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) werden die verschiedenen Typen von Registern aufgeführt, die vom Vertex-Shader ALU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31506-108">[Registers - vs\_2\_0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="31506-109">[Vertex-Shader-Registermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers.md) werden verwendet, um die Art und Weise zu ändern, wie eine Anweisung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="31506-109">[Vertex Shader Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers.md) are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="31506-110">[Vertex-Shader-Quellregistermodifizierer](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31506-110">[Vertex Shader Source Register Modifiers](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="31506-111">[Source Register Swizzling bietet](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="31506-111">[Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>
-   <span data-ttu-id="31506-112">[Zielregistermaskierung](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="31506-112">[Destination Register Masking](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) determines what components of the destination register get written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="31506-113">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="31506-113">Instruction Count</span></span>

<span data-ttu-id="31506-114">Für jeden Vertex-Shader können bis zu 256 Anweisungen gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="31506-114">Each vertex shader can have up to 256 instructions stored.</span></span> <span data-ttu-id="31506-115">Die Anzahl der ausgeführten Anweisungen kann viel höher sein (aufgrund der Unterstützung von Schleifen/Wiederholungen) und ist durch D3DCAPS9 begrenzt. MaxVShaderInstructionsExecuted, die mindestens 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="31506-115">The number of instructions run can be much higher (because of the loop/rep support), and is capped by D3DCAPS9.MaxVShaderInstructionsExecuted, which should be at least 0xFFFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31506-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="31506-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31506-117">Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="31506-117">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




