---
title: Ret-PS
description: Nimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort. Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976345"
---
# <a name="ret---ps"></a><span data-ttu-id="f1079-104">Ret-PS</span><span class="sxs-lookup"><span data-stu-id="f1079-104">ret - ps</span></span>

<span data-ttu-id="f1079-105">Nimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="f1079-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="f1079-106">Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.</span><span class="sxs-lookup"><span data-stu-id="f1079-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1079-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1079-107">Syntax</span></span>



| <span data-ttu-id="f1079-108">TZI</span><span class="sxs-lookup"><span data-stu-id="f1079-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="f1079-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1079-109">Remarks</span></span>



| <span data-ttu-id="f1079-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f1079-110">Pixel shader versions</span></span> | <span data-ttu-id="f1079-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1079-111">1\_1</span></span> | <span data-ttu-id="f1079-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="f1079-112">1\_2</span></span> | <span data-ttu-id="f1079-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f1079-113">1\_3</span></span> | <span data-ttu-id="f1079-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="f1079-114">1\_4</span></span> | <span data-ttu-id="f1079-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1079-115">2\_0</span></span> | <span data-ttu-id="f1079-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1079-116">2\_x</span></span> | <span data-ttu-id="f1079-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1079-117">2\_sw</span></span> | <span data-ttu-id="f1079-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1079-118">3\_0</span></span> | <span data-ttu-id="f1079-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1079-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f1079-120">TZI</span><span class="sxs-lookup"><span data-stu-id="f1079-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="f1079-121">x</span><span class="sxs-lookup"><span data-stu-id="f1079-121">x</span></span>    | <span data-ttu-id="f1079-122">x</span><span class="sxs-lookup"><span data-stu-id="f1079-122">x</span></span>     | <span data-ttu-id="f1079-123">x</span><span class="sxs-lookup"><span data-stu-id="f1079-123">x</span></span>    | <span data-ttu-id="f1079-124">x</span><span class="sxs-lookup"><span data-stu-id="f1079-124">x</span></span>     |



 

<span data-ttu-id="f1079-125">Diese Anweisung übernimmt die Adresse einer Anweisung aus dem Rückgabe Adress Stapel und setzt deren Ausführung fort.</span><span class="sxs-lookup"><span data-stu-id="f1079-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="f1079-126">Bei der Main-Funktion beendet diese Anweisung die Ausführung von Shaders.</span><span class="sxs-lookup"><span data-stu-id="f1079-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="f1079-127">Die ret-Anweisung verwendet einen Vertex-Shader-Anweisungs Slot.</span><span class="sxs-lookup"><span data-stu-id="f1079-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="f1079-128">Wenn ein Shader keine Unterroutinen enthält, ist die Verwendung von Ret am Ende des Hauptprogramms optional.</span><span class="sxs-lookup"><span data-stu-id="f1079-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="f1079-129">Mehrere Return-Anweisungen sind im Hauptprogramm oder in einer Unterroutine nicht zulässig. die erste Return-Anweisung wird als Ende des Hauptprogramms oder der Unterroutine behandelt.</span><span class="sxs-lookup"><span data-stu-id="f1079-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1079-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1079-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1079-131">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="f1079-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




