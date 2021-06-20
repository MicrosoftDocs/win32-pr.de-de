---
title: Schleifenzählerregister (HLSL-PS-Referenz)
description: Informieren Sie sich über das Schleifenzählerregister für Pixel-Shader. Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405513"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a><span data-ttu-id="863a0-104">Schleifenzählerregister (HLSL-PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="863a0-104">Loop counter register (HLSL PS reference)</span></span>

<span data-ttu-id="863a0-105">Das einzige Register in dieser Bank ist das aktuelle aL-Register (Loop Counter).</span><span class="sxs-lookup"><span data-stu-id="863a0-105">The only register in this bank is the current loop counter (aL) register.</span></span> <span data-ttu-id="863a0-106">Bei jeder Ausführung der [Schleife](loop---ps.md)– ps / [endloop](endloop---ps.md) – ps block – wird sie automatisch erhöht.</span><span class="sxs-lookup"><span data-stu-id="863a0-106">It automatically gets incremented in each execution of the [loop - ps](loop---ps.md)/[endloop - ps](endloop---ps.md) block.</span></span> <span data-ttu-id="863a0-107">Daher kann sie im -Block bei Bedarf für die relative Adressierung verwendet werden und ist ungültig, um sie außerhalb der Schleife zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="863a0-107">So it can be used in the block for relative addressing if needed and is invalid to use it outside the loop.</span></span>



| <span data-ttu-id="863a0-108">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="863a0-108">Pixel shader versions</span></span> | <span data-ttu-id="863a0-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="863a0-109">1\_1</span></span> | <span data-ttu-id="863a0-110">1\_2</span><span class="sxs-lookup"><span data-stu-id="863a0-110">1\_2</span></span> | <span data-ttu-id="863a0-111">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="863a0-111">1\_3</span></span> | <span data-ttu-id="863a0-112">1\_4</span><span class="sxs-lookup"><span data-stu-id="863a0-112">1\_4</span></span> | <span data-ttu-id="863a0-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="863a0-113">2\_0</span></span> | <span data-ttu-id="863a0-114">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="863a0-114">2\_sw</span></span> | <span data-ttu-id="863a0-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="863a0-115">2\_x</span></span> | <span data-ttu-id="863a0-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="863a0-116">3\_0</span></span> | <span data-ttu-id="863a0-117">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="863a0-117">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="863a0-118">Schleifenzählerregister</span><span class="sxs-lookup"><span data-stu-id="863a0-118">Loop Counter Register</span></span> |      |      |      |      |      |       |      | <span data-ttu-id="863a0-119">x</span><span class="sxs-lookup"><span data-stu-id="863a0-119">x</span></span>    | <span data-ttu-id="863a0-120">x</span><span class="sxs-lookup"><span data-stu-id="863a0-120">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="863a0-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="863a0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="863a0-122">Register</span><span class="sxs-lookup"><span data-stu-id="863a0-122">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




