---
title: ps_2_0
description: Erfahren Sie mehr über ps_2_0, einen programmierbaren Pixelshader, der aus einer Reihe von Anweisungen besteht, die mit Pixeldaten arbeiten.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a2433c8490af06d23d8dccef676ec206fdbb88c0
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010983"
---
# <a name="ps_2_0"></a><span data-ttu-id="88911-103">ps \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="88911-103">ps\_2\_0</span></span>

<span data-ttu-id="88911-104">Ein programmierbarer Pixel-Shader besteht aus einer Reihe von Anweisungen, die mit Pixeldaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="88911-104">A programmable pixel shader is made up of a set of instructions that operate on pixel data.</span></span> <span data-ttu-id="88911-105">Registriert Datenübertragungen in und aus der ALU.</span><span class="sxs-lookup"><span data-stu-id="88911-105">Registers transfer data in and out of the ALU.</span></span> <span data-ttu-id="88911-106">Es kann ein zusätzliches Steuerelement angewendet werden, um die Anweisung, die Ergebnisse oder die geschriebenen Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="88911-106">Additional control can be applied to modify the instruction, the results, or what data gets written out.</span></span>

-   <span data-ttu-id="88911-107">[ps \_ 2 \_ 0 Anweisungen](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) enthält eine Liste der verfügbaren Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="88911-107">[ps\_2\_0 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) contains a list of the available instructions.</span></span>
-   <span data-ttu-id="88911-108">[ps \_ 2 \_ 0 Register listet](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) die verschiedenen Registertypen auf, die vom Vertex-Shader ALU verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88911-108">[ps\_2\_0 Registers](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) lists the different types of registers used by the vertex shader ALU.</span></span>
-   <span data-ttu-id="88911-109">[Modifizierer](dx9-graphics-reference-asm-ps-registers-modifiers.md) Werden verwendet, um die Funktionsweise einer Anweisung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="88911-109">[Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers.md) Are used to modify the way an instruction works.</span></span>
-   <span data-ttu-id="88911-110">[Zielregister-Schreibmaske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) bestimmt, welche Komponenten des Zielregisters geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="88911-110">[Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) determines what components of the destination register get written.</span></span>
-   <span data-ttu-id="88911-111">[Die Quellregistermodifizierer des Pixelshader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) ändern die Quellregisterdaten, bevor die Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88911-111">[Pixel Shader Source Register Modifiers](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) alter the source register data before the instruction runs.</span></span>
-   <span data-ttu-id="88911-112">[Das Quellenregister swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) bietet zusätzliche Kontrolle darüber, welche Registerkomponenten gelesen, kopiert oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="88911-112">[Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) gives additional control over which register components are read, copied, or written.</span></span>

## <a name="instruction-count"></a><span data-ttu-id="88911-113">Anweisungsanzahl</span><span class="sxs-lookup"><span data-stu-id="88911-113">Instruction Count</span></span>

<span data-ttu-id="88911-114">Shader weisen Einschränkungen für die maximale Anzahl von Anweisungen auf.</span><span class="sxs-lookup"><span data-stu-id="88911-114">Shaders have restrictions for maximum instruction counts.</span></span> <span data-ttu-id="88911-115">Anweisungsslots gesamt: 96 (64 arithmetische und 32 Textur).</span><span class="sxs-lookup"><span data-stu-id="88911-115">Total Instruction slots: 96 (64 arithmetic and 32 texture).</span></span>

## <a name="sampler-count"></a><span data-ttu-id="88911-116">Sampleranzahl</span><span class="sxs-lookup"><span data-stu-id="88911-116">Sampler Count</span></span>

<span data-ttu-id="88911-117">Die Anzahl der verfügbaren Textur-Sampler beträgt 16.</span><span class="sxs-lookup"><span data-stu-id="88911-117">The number of texture samplers available is 16.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88911-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88911-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88911-119">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="88911-119">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




