---
title: Quell Register Invert
description: Führt für jeden Kanal des angegebenen Register eine (1-Wert)-Berechnung aus.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976168"
---
# <a name="source-register-invert"></a><span data-ttu-id="05fec-103">Quell Register Invert</span><span class="sxs-lookup"><span data-stu-id="05fec-103">Source Register Invert</span></span>

<span data-ttu-id="05fec-104">Führt für jeden Kanal des angegebenen Register eine (1-Wert)-Berechnung aus.</span><span class="sxs-lookup"><span data-stu-id="05fec-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="05fec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05fec-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="05fec-106">Register</span><span class="sxs-lookup"><span data-stu-id="05fec-106">Registers</span></span>

<span data-ttu-id="05fec-107">Quell Register.</span><span class="sxs-lookup"><span data-stu-id="05fec-107">Source Register.</span></span> <span data-ttu-id="05fec-108">Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="05fec-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="05fec-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05fec-109">Remarks</span></span>

<span data-ttu-id="05fec-110">Der Inhalt des Registers wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="05fec-110">The contents of the register are not changed.</span></span> <span data-ttu-id="05fec-111">Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.</span><span class="sxs-lookup"><span data-stu-id="05fec-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="05fec-112">Der umkehren-Vorgang wird auf alle vier Farbkanäle (RGBA) angewendet.</span><span class="sxs-lookup"><span data-stu-id="05fec-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="05fec-113">Dieser Modifizierer kann nur mit arithmetischen Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05fec-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="05fec-114">Außerdem kann dieser Modifizierer nicht mit der anderen Ziel- [Schreib Maske](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)für das Schreiben kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="05fec-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="05fec-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="05fec-115">Example</span></span>

<span data-ttu-id="05fec-116">In diesem Beispiel wird Inversion verwendet, um das Komplement von Register R1 zu generieren.</span><span class="sxs-lookup"><span data-stu-id="05fec-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="05fec-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05fec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05fec-118">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="05fec-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




