---
title: Texturkoordinaten Register (HLSL PS-Referenz)
description: Ein Pixel-Shader-Eingabe Register, das Texturkoordinaten enthält.
ms.assetid: 423f249d-fa9f-41f2-adbf-d97ceace06f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 456ea0da6c1c23f51dbdba357f18de747b318e6a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104976512"
---
# <a name="texture-coordinate-register-hlsl-ps-reference"></a><span data-ttu-id="37e57-103">Texturkoordinaten Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="37e57-103">Texture coordinate register (HLSL PS reference)</span></span>

<span data-ttu-id="37e57-104">Ein Pixel-Shader-Eingabe Register, das Texturkoordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="37e57-104">Pixel shader input register containing texture coordinates.</span></span>



| <span data-ttu-id="37e57-105">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="37e57-105">Pixel shader versions</span></span>       | <span data-ttu-id="37e57-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="37e57-106">1\_1</span></span> | <span data-ttu-id="37e57-107">1\_2</span><span class="sxs-lookup"><span data-stu-id="37e57-107">1\_2</span></span> | <span data-ttu-id="37e57-108">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="37e57-108">1\_3</span></span> | <span data-ttu-id="37e57-109">1\_4</span><span class="sxs-lookup"><span data-stu-id="37e57-109">1\_4</span></span> | <span data-ttu-id="37e57-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e57-110">2\_0</span></span> | <span data-ttu-id="37e57-111">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37e57-111">2\_sw</span></span> | <span data-ttu-id="37e57-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="37e57-112">2\_x</span></span> | <span data-ttu-id="37e57-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="37e57-113">3\_0</span></span> | <span data-ttu-id="37e57-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="37e57-114">3\_sw</span></span> |
|-----------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="37e57-115">Texturkoordinaten Register</span><span class="sxs-lookup"><span data-stu-id="37e57-115">Texture Coordinate Register</span></span> |      |      |      |      | <span data-ttu-id="37e57-116">x</span><span class="sxs-lookup"><span data-stu-id="37e57-116">x</span></span>    | <span data-ttu-id="37e57-117">x</span><span class="sxs-lookup"><span data-stu-id="37e57-117">x</span></span>     | <span data-ttu-id="37e57-118">x</span><span class="sxs-lookup"><span data-stu-id="37e57-118">x</span></span>    | <span data-ttu-id="37e57-119">x</span><span class="sxs-lookup"><span data-stu-id="37e57-119">x</span></span>    | <span data-ttu-id="37e57-120">x</span><span class="sxs-lookup"><span data-stu-id="37e57-120">x</span></span>     |



 

<span data-ttu-id="37e57-121">Ein Texturkoordinaten Register enthält Texturkoordinaten Daten.</span><span class="sxs-lookup"><span data-stu-id="37e57-121">A texture coordinate register contains texture coordinate data.</span></span> <span data-ttu-id="37e57-122">Bevor ein Texturkoordinaten Register verwendet wird, muss es durch eine Pixel-Shader-Deklaration deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="37e57-122">Before a texture coordinate register is used, it must be declared by a pixel shader declaration.</span></span> <span data-ttu-id="37e57-123">Ausführliche Informationen zum Deklarieren eines Textur Registers finden Sie unter [DCL-(SM2, SM3-PS ASM)](dcl---ps.md).</span><span class="sxs-lookup"><span data-stu-id="37e57-123">For details about how to declare a texture register, see [dcl - (sm2, sm3 - ps asm)](dcl---ps.md).</span></span>

<span data-ttu-id="37e57-124">Außerdem sind hier einige weitere Eigenschaften von Texturkoordinaten Registern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="37e57-124">In addition, here are some other properties of texture coordinate registers.</span></span>

-   <span data-ttu-id="37e57-125">Es gibt acht Pixel-Shader-Texturkoordinaten Register, t0 bis T7.</span><span class="sxs-lookup"><span data-stu-id="37e57-125">There are eight pixel-shader texture coordinate registers, t0 to t7.</span></span>
-   <span data-ttu-id="37e57-126">Hierbei handelt es sich um schreibgeschützte Register.</span><span class="sxs-lookup"><span data-stu-id="37e57-126">These are read-only registers.</span></span>
-   <span data-ttu-id="37e57-127">Sie enthalten vier Komponenten-RGBA-Werte, die aus Eingabe Scheitel Punkten durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="37e57-127">They contain four-component RGBA values iterated from input vertices.</span></span>
-   <span data-ttu-id="37e57-128">Sie enthalten hohe Genauigkeit, hohe dynamische Bereichs Datenwerte, die von den Scheitelpunkt Daten interpoliert werden.</span><span class="sxs-lookup"><span data-stu-id="37e57-128">They contain high precision, high dynamic range data values interpolated from the vertex data.</span></span> <span data-ttu-id="37e57-129">Werte werden mit Perspective-korrekter interpolung generiert.</span><span class="sxs-lookup"><span data-stu-id="37e57-129">Values are generated with perspective-correct interpolation.</span></span> <span data-ttu-id="37e57-130">Bei den Daten handelt es sich um Gleit Komma Genauigkeit und wird signiert.</span><span class="sxs-lookup"><span data-stu-id="37e57-130">Data is floating-point precision, and is signed.</span></span>
-   <span data-ttu-id="37e57-131">Es gibt maximal einen in einer einzigen Anweisung.</span><span class="sxs-lookup"><span data-stu-id="37e57-131">There is a maximum of one in a single instruction.</span></span>
-   <span data-ttu-id="37e57-132">Mehrere Lesevorgänge eines Texturkoordinaten Registers innerhalb eines Shaders müssen die identische [Schreib Maske für das Ziel Register](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="37e57-132">Multiple reads of a texture coordinate register within a shader must use identical [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>
-   <span data-ttu-id="37e57-133">Die optionale PP für partielle Genauigkeits Modifizierer \[ \_ \] gilt für abhängige Lesevorgänge.</span><span class="sxs-lookup"><span data-stu-id="37e57-133">The optional partial precision modifier \[\_pp\] applies to dependent reads.</span></span> <span data-ttu-id="37e57-134">Dies liegt daran, dass die Teil Genauigkeit die arithmetischen Operationen mit dem Texturkoordinaten Register beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="37e57-134">This is because partial precision affects arithmetic operations involving the texture coordinate register.</span></span> <span data-ttu-id="37e57-135">Sie wirkt sich nicht auf die Genauigkeit von Textur Adress Anweisungen aus, da Sie sich nicht auf die Iteratoren der Textur Koordinate auswirkt.</span><span class="sxs-lookup"><span data-stu-id="37e57-135">It will not affect the precision of texture address instructions because it does not affect the texture coordinate iterators.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37e57-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37e57-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37e57-137">Register</span><span class="sxs-lookup"><span data-stu-id="37e57-137">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




