---
title: Schleifen Zählers-Register (HLSL vs-Referenz)
description: Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104389621"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="6201e-103">Schleifen Zählers-Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="6201e-103">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="6201e-104">Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al).</span><span class="sxs-lookup"><span data-stu-id="6201e-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="6201e-105">Sie wird bei jeder Ausführung des [Schleifen-vs](loop---vs.md)... [ENDLOOP-vs-](endloop---vs.md) Block.</span><span class="sxs-lookup"><span data-stu-id="6201e-105">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="6201e-106">Daher kann Sie bei Bedarf im-Block für die relative Adressierung verwendet werden und ist nicht für die Verwendung außerhalb der-Schleife ungültig.</span><span class="sxs-lookup"><span data-stu-id="6201e-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6201e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6201e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6201e-108">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="6201e-108">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




