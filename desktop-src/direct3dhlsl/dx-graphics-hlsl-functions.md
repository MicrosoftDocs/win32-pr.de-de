---
title: Functions (HLSL-Referenz)
description: Funktionen Kapseln HLSL-Anweisungen.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313775"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="5517b-103">Functions (HLSL-Referenz)</span><span class="sxs-lookup"><span data-stu-id="5517b-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="5517b-104">Funktionen Kapseln HLSL-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="5517b-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="5517b-105">Auf diese Weise können Sie eine Reihe von Funktionen Debuggen und Sie dann über Shader oder Effekte hinweg wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="5517b-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="5517b-106">Möglicherweise möchten Sie eine Funktion erstellen, die die Funktionalität eines Vertex-Shaders, Pixel-Shader oder Textur-Shaders kapselt.</span><span class="sxs-lookup"><span data-stu-id="5517b-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="5517b-107">In anderen Fällen empfiehlt es sich, eine Hilfsfunktion zu schreiben, die eine häufig verwendete Aufgabe ausführt, und dann diese Hilfsfunktion von der shaderfunktion aus aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="5517b-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="5517b-108">Die Regeln zum Schreiben von Shaderfunktionen für HLSL ähneln dem Schreiben von C-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="5517b-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="5517b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5517b-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="5517b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5517b-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="5517b-111">Return-Anweisung</span><span class="sxs-lookup"><span data-stu-id="5517b-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="5517b-112">Signaturen</span><span class="sxs-lookup"><span data-stu-id="5517b-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="5517b-113">HLSL verfügt auch über eine Reihe integrierter System interner [**Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5517b-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="5517b-114">Da alle intrinsischen Funktionen getestet und optimiert wurden, empfiehlt es sich, möglichst eine intrinsische Funktion zu verwenden, anstatt eine eigene Funktion zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5517b-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5517b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5517b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5517b-116">Sprach Syntax (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5517b-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




