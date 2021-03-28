---
title: Ret-vs
description: Rückgabe aus einer Unterroutine oder einer Main-Funktion.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313650"
---
# <a name="ret---vs"></a><span data-ttu-id="9483c-103">Ret-vs</span><span class="sxs-lookup"><span data-stu-id="9483c-103">ret - vs</span></span>

<span data-ttu-id="9483c-104">Rückgabe aus einer Unterroutine oder einer Main-Funktion.</span><span class="sxs-lookup"><span data-stu-id="9483c-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9483c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9483c-105">Syntax</span></span>



| <span data-ttu-id="9483c-106">TZI</span><span class="sxs-lookup"><span data-stu-id="9483c-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="9483c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9483c-107">Remarks</span></span>



| <span data-ttu-id="9483c-108">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="9483c-108">Vertex shader versions</span></span> | <span data-ttu-id="9483c-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="9483c-109">1\_1</span></span> | <span data-ttu-id="9483c-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9483c-110">2\_0</span></span> | <span data-ttu-id="9483c-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9483c-111">2\_x</span></span> | <span data-ttu-id="9483c-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9483c-112">2\_sw</span></span> | <span data-ttu-id="9483c-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9483c-113">3\_0</span></span> | <span data-ttu-id="9483c-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9483c-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9483c-115">TZI</span><span class="sxs-lookup"><span data-stu-id="9483c-115">ret</span></span>                    |      | <span data-ttu-id="9483c-116">x</span><span class="sxs-lookup"><span data-stu-id="9483c-116">x</span></span>    | <span data-ttu-id="9483c-117">x</span><span class="sxs-lookup"><span data-stu-id="9483c-117">x</span></span>    | <span data-ttu-id="9483c-118">x</span><span class="sxs-lookup"><span data-stu-id="9483c-118">x</span></span>     | <span data-ttu-id="9483c-119">x</span><span class="sxs-lookup"><span data-stu-id="9483c-119">x</span></span>    | <span data-ttu-id="9483c-120">x</span><span class="sxs-lookup"><span data-stu-id="9483c-120">x</span></span>     |



 

<span data-ttu-id="9483c-121">Diese Anweisung übernimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="9483c-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="9483c-122">Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.</span><span class="sxs-lookup"><span data-stu-id="9483c-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="9483c-123">Die ret-Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="9483c-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="9483c-124">Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von Ret am Ende des Hauptprogramms optional.</span><span class="sxs-lookup"><span data-stu-id="9483c-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="9483c-125">Mehrere Return-Anweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. die erste Return-Anweisung wird als Ende des Hauptprogramms oder der Unterroutine behandelt.</span><span class="sxs-lookup"><span data-stu-id="9483c-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9483c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9483c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9483c-127">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="9483c-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




