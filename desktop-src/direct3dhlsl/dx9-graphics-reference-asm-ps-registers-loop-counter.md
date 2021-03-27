---
title: Schleifen Zählers-Register (HLSL PS-Referenz)
description: Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719541"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="4edba-103">Schleifen Zählers-Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="4edba-103">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="4edba-104">Das einzige Register in dieser Bank ist das aktuelle Loop Counter-Register (Al).</span><span class="sxs-lookup"><span data-stu-id="4edba-104">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="4edba-105">Sie wird bei jeder Ausführung des [Loop-PS](loop---ps.md)- / [ENDLOOP-PS-](endloop---ps.md) Blocks automatisch inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="4edba-105">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="4edba-106">Daher kann Sie bei Bedarf im-Block für die relative Adressierung verwendet werden und ist nicht für die Verwendung außerhalb der-Schleife ungültig.</span><span class="sxs-lookup"><span data-stu-id="4edba-106">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="4edba-107">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="4edba-107">Pixel shader versions</span></span> | <span data-ttu-id="4edba-108">1\_1</span><span class="sxs-lookup"><span data-stu-id="4edba-108">1\_1</span></span> | <span data-ttu-id="4edba-109">1\_2</span><span class="sxs-lookup"><span data-stu-id="4edba-109">1\_2</span></span> | <span data-ttu-id="4edba-110">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4edba-110">1\_3</span></span> | <span data-ttu-id="4edba-111">1\_4</span><span class="sxs-lookup"><span data-stu-id="4edba-111">1\_4</span></span> | <span data-ttu-id="4edba-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4edba-112">2\_0</span></span> | <span data-ttu-id="4edba-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4edba-113">2\_sw</span></span> | <span data-ttu-id="4edba-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4edba-114">2\_x</span></span> | <span data-ttu-id="4edba-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4edba-115">3\_0</span></span> | <span data-ttu-id="4edba-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4edba-116">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="4edba-117">Schleifen-Counter-Register</span><span class="sxs-lookup"><span data-stu-id="4edba-117">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="4edba-118">x</span><span class="sxs-lookup"><span data-stu-id="4edba-118">x</span></span>    | <span data-ttu-id="4edba-119">x</span><span class="sxs-lookup"><span data-stu-id="4edba-119">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4edba-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4edba-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4edba-121">Register</span><span class="sxs-lookup"><span data-stu-id="4edba-121">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




