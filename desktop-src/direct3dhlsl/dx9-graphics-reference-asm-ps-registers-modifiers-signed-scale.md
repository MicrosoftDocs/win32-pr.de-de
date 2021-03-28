---
title: Quell Registrierung mit signierter Skalierung
description: Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0. Der Name bx2 stammt von "Bias" und "Scale-Time-Two", bei dem es sich um den ausgeführten Vorgang handelt.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207448"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="67c7c-104">Quell Registrierung mit signierter Skalierung</span><span class="sxs-lookup"><span data-stu-id="67c7c-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="67c7c-105">Subtrahiert 0,5 von jedem Kanal und skaliert das Ergebnis um 2,0.</span><span class="sxs-lookup"><span data-stu-id="67c7c-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="67c7c-106">Der Name bx2 stammt von "Bias" und "Scale-Time-Two", bei dem es sich um den ausgeführten Vorgang handelt.</span><span class="sxs-lookup"><span data-stu-id="67c7c-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c7c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67c7c-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="67c7c-108">Register</span><span class="sxs-lookup"><span data-stu-id="67c7c-108">Register</span></span>

<span data-ttu-id="67c7c-109">Quell Register.</span><span class="sxs-lookup"><span data-stu-id="67c7c-109">Source Register.</span></span> <span data-ttu-id="67c7c-110">Weitere Informationen zu Register Typen finden Sie unter [PS \_ 1 1 PS 1 \_ \_ \_ \_ \_ 2 \_ \_ PS \_ 1 \_ 3 \_ \_ PS \_ 1 \_ 4 Registern](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="67c7c-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="67c7c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67c7c-111">Remarks</span></span>

<span data-ttu-id="67c7c-112">Dieser Vorgang wird häufig zum Erweitern von Daten zwischen \[ 0,0 und 1,0 \] auf \[ -1,0 bis 1,0 verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="67c7c-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="67c7c-113">Dieser Modifizierer ist für die Verwendung mit arithmetischen Anweisungen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="67c7c-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="67c7c-114">Dieser Modifizierer wird häufig bei Eingaben für die dot-Produkt Anweisung ([DP3-PS](dp3---ps.md)) verwendet.</span><span class="sxs-lookup"><span data-stu-id="67c7c-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="67c7c-115">\_Die Verwendung von bx2 für Daten außerhalb des Bereichs 0 bis 1 kann zu undefinierten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="67c7c-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="67c7c-116">Der Vorgang für die signierte Skalierung wird auf die aus dem Register gelesenen Daten angewendet, bevor die nächste Anweisung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67c7c-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="67c7c-117">Der Vorgang wird wie folgt auf alle vier Farbkanäle (RGBA) angewendet:</span><span class="sxs-lookup"><span data-stu-id="67c7c-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="67c7c-118">Der Inhalt des Registers wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="67c7c-118">The contents of the register are not changed.</span></span> <span data-ttu-id="67c7c-119">Der-Modifizierer wird nur auf die aus dem Register gelesenen Daten angewendet.</span><span class="sxs-lookup"><span data-stu-id="67c7c-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="67c7c-120">Dieser Modifizierer schließt sich mit dem [Quell Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) gegenseitig aus, sodass er nicht auf dasselbe Register angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="67c7c-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="67c7c-121">Versionsinformationen:</span><span class="sxs-lookup"><span data-stu-id="67c7c-121">Version information:</span></span>

-   <span data-ttu-id="67c7c-122">Für PS \_ 1 \_ 0 und PS \_ 1 \_ 1 können Sie \_ bx2 für ein beliebiges Quell Register für Textur Anweisungen im Format texm3x2 \* und texm3x3 verwenden \* .</span><span class="sxs-lookup"><span data-stu-id="67c7c-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="67c7c-123">\_bx2 kann nicht für eine der anderen Textur Anweisungen wie [texreg2ar-PS](texreg2ar---ps.md) oder [texreg2gb-PS](texreg2gb---ps.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="67c7c-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="67c7c-124">Für PS \_ 1 \_ 2 und PS \_ 1 \_ 3 können Sie \_ bx2 für beliebige Quell Register für jede beliebige tex- \* Anweisung mit Ausnahme von: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) oder [texbeml-PS](texbeml---ps.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="67c7c-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="67c7c-125">Beispiel</span><span class="sxs-lookup"><span data-stu-id="67c7c-125">Example</span></span>

<span data-ttu-id="67c7c-126">Dieses Beispiel veranschaulicht eine Textur, konvertiert Daten in den Bereich von-1 bis + 1 und berechnet ein Punktprodukt.</span><span class="sxs-lookup"><span data-stu-id="67c7c-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="67c7c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67c7c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67c7c-128">Pixel-Shader-quellregistrierungs Modifizierern</span><span class="sxs-lookup"><span data-stu-id="67c7c-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




