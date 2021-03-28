---
title: Quellen Register Negate
description: Führt für alle Register Komponenten eine Negation (y-x) aus.
ms.assetid: fe11f7a7-81be-4237-8194-15704f6fe43c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6082523926d70e670e0b792c6e7e8f41c7c1a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036852"
---
# <a name="source-register-negate"></a><span data-ttu-id="d4cb6-103">Quellen Register Negate</span><span class="sxs-lookup"><span data-stu-id="d4cb6-103">Source Register Negate</span></span>

<span data-ttu-id="d4cb6-104">Führt für alle Register Komponenten eine Negation (y =-x) aus.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-104">Performs a negate (y = -x), on all register components.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4cb6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4cb6-105">Syntax</span></span>


```
- register
```



## <a name="registers"></a><span data-ttu-id="d4cb6-106">Register</span><span class="sxs-lookup"><span data-stu-id="d4cb6-106">Registers</span></span>

<span data-ttu-id="d4cb6-107">Quell Register.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-107">Source Register.</span></span> <span data-ttu-id="d4cb6-108">Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="d4cb6-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4cb6-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4cb6-109">Remarks</span></span>

<span data-ttu-id="d4cb6-110">Der Inhalt des Registers wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-110">The contents of the register are not changed.</span></span> <span data-ttu-id="d4cb6-111">Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="d4cb6-112">Der Negation-Vorgang wird auf alle vier Farbkanäle (RGBA) angewendet.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-112">The negate operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="d4cb6-113">Dieser Vorgang wird ausgeführt, nachdem alle anderen Modifizierer für dasselbe Argument vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-113">This operation is performed after any other modifiers present on the same argument.</span></span>

<span data-ttu-id="d4cb6-114">Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig aus, sodass er nicht auf dasselbe Register angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="d4cb6-115">Dieser Modifizierer kann nur mit arithmetischen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-115">This modifier is for use only with arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="d4cb6-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4cb6-116">Example</span></span>

<span data-ttu-id="d4cb6-117">Im folgenden Beispiel wird gezeigt, wie dieser Modifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4cb6-117">The following example shows how to use this modifier.</span></span>


```
mul r0, r0, -v1;
```



## <a name="related-topics"></a><span data-ttu-id="d4cb6-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4cb6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4cb6-119">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="d4cb6-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




