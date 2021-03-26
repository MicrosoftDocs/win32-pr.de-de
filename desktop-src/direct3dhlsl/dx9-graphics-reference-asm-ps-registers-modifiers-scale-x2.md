---
title: Quell Register Skala x 2
description: Multiplizieren Sie den Wert mit zwei, bevor Sie ihn in der-Anweisung verwenden.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976161"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="c4b74-103">Quell Register Skala x 2</span><span class="sxs-lookup"><span data-stu-id="c4b74-103">Source Register Scale x 2</span></span>

<span data-ttu-id="c4b74-104">Multiplizieren Sie den Wert mit zwei, bevor Sie ihn in der-Anweisung verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4b74-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4b74-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="c4b74-106">Register</span><span class="sxs-lookup"><span data-stu-id="c4b74-106">Register</span></span>

<span data-ttu-id="c4b74-107">Quell Register.</span><span class="sxs-lookup"><span data-stu-id="c4b74-107">Source register.</span></span> <span data-ttu-id="c4b74-108">Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="c4b74-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4b74-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4b74-109">Remarks</span></span>

<span data-ttu-id="c4b74-110">Der Inhalt des Registers wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="c4b74-110">The contents of the register are not changed.</span></span> <span data-ttu-id="c4b74-111">Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.</span><span class="sxs-lookup"><span data-stu-id="c4b74-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="c4b74-112">Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)gegenseitig aus und kann daher nicht auf dasselbe Register angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4b74-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="c4b74-113">Dieser Modifizierer ist nur für arithmetische Anweisungen in Version 1 \_ 4 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4b74-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="c4b74-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c4b74-114">Example</span></span>

<span data-ttu-id="c4b74-115">Dieses Beispiel veranschaulicht eine Textur, konvertiert Daten in den Bereich von-1 bis + 1 und berechnet ein Punktprodukt.</span><span class="sxs-lookup"><span data-stu-id="c4b74-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="c4b74-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4b74-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b74-117">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="c4b74-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




