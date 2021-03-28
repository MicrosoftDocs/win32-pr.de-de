---
title: Quellen Register-Bias
description: Subtrahieren Sie 0,5 von allen Komponenten.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948087"
---
# <a name="source-register-bias"></a><span data-ttu-id="c8d42-103">Quellen Register-Bias</span><span class="sxs-lookup"><span data-stu-id="c8d42-103">Source Register Bias</span></span>

<span data-ttu-id="c8d42-104">Subtrahieren Sie 0,5 von allen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c8d42-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="c8d42-105">Register</span><span class="sxs-lookup"><span data-stu-id="c8d42-105">Registers</span></span>

<span data-ttu-id="c8d42-106">Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c8d42-106">Source register.</span></span> <span data-ttu-id="c8d42-107">Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="c8d42-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d42-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8d42-108">Remarks</span></span>

<span data-ttu-id="c8d42-109">Der Inhalt des Registers wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c8d42-109">The contents of the register are not changed.</span></span> <span data-ttu-id="c8d42-110">Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8d42-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="c8d42-111">Der Bias wird wie folgt auf alle vier Farbkanäle (RGBA) angewendet:</span><span class="sxs-lookup"><span data-stu-id="c8d42-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="c8d42-112">Der Effekt besteht darin, die Daten im Bereich von 0 bis 1 im Bereich von-0,5 bis 0,5 zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c8d42-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="c8d42-113">Das Anwenden von Bias auf Daten außerhalb dieses Bereichs kann zu undefinierten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="c8d42-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="c8d42-114">Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)gegenseitig aus und kann daher nicht auf dasselbe Register angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8d42-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="c8d42-115">Dieser Modifizierer ist für die Verwendung mit arithmetischen Anweisungen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="c8d42-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="c8d42-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c8d42-116">Example</span></span>

<span data-ttu-id="c8d42-117">In diesem Beispiel wird der gleiche Vorgang wie D3DTOP \_ AddSigned in DirectX 6,0 und 7,0 multiple texture-Syntax durchführt.</span><span class="sxs-lookup"><span data-stu-id="c8d42-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="c8d42-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8d42-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8d42-119">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="c8d42-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




