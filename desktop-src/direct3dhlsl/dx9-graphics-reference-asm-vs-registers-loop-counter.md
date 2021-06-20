---
title: Schleifenzählerregister (HLSL VS-Referenz)
description: Informieren Sie sich über das Schleifenzählerregister für Vertex-Shader. Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fb728420dc48c6cb67d5973085845b0eab742a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405773"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a><span data-ttu-id="94fee-104">Schleifenzählerregister (HLSL VS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="94fee-104">Loop Counter Register (HLSL VS reference)</span></span>

<span data-ttu-id="94fee-105">Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).</span><span class="sxs-lookup"><span data-stu-id="94fee-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="94fee-106">Sie wird bei jeder Ausführung der [Schleife](loop---vs.md)automatisch erhöht – im Vergleich zu ... [endloop – vs](endloop---vs.md) block.</span><span class="sxs-lookup"><span data-stu-id="94fee-106">It automatically gets incremented in each execution of the [loop - vs](loop---vs.md)...[endloop - vs](endloop---vs.md) block.</span></span> <span data-ttu-id="94fee-107">Daher kann sie im -Block bei Bedarf für die relative Adressierung verwendet werden und ist ungültig, um sie außerhalb der Schleife zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="94fee-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94fee-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94fee-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fee-109">Vertex-Shaderregister</span><span class="sxs-lookup"><span data-stu-id="94fee-109">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




