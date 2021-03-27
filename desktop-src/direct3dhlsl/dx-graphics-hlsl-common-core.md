---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e27ebe7d908c473890ac5b851eac3e0bc840c859
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855723"
---
# <a name="common-shader-core"></a><span data-ttu-id="b036d-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="b036d-103">Common-Shader Core</span></span>

<span data-ttu-id="b036d-104">In Shader Model 4 implementieren alle Shader-Stufen die gleiche Basisfunktionalität mithilfe eines gemeinsamen shaderkerns.</span><span class="sxs-lookup"><span data-stu-id="b036d-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="b036d-105">Außerdem bieten jede der drei Shader-Stufen (Scheitelpunkt, Geometrie und Pixel) Funktionen, die für jede Phase eindeutig sind, z. b. die Möglichkeit, neue primitive aus der Geometrie-Shader-Phase zu generieren oder ein bestimmtes Pixel in der Pixel-Shader-Stufe zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="b036d-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="b036d-106">Das folgende Diagramm zeigt, wie Daten durch eine Shader-Stufe und die Beziehung des Common-Shader-Kerns mit Shader-Speicherressourcen fließen.</span><span class="sxs-lookup"><span data-stu-id="b036d-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![Diagramm des Datenflusses in einer Shader-Phase](images/d3d10-shader-unit.png)

-   <span data-ttu-id="b036d-108">**Eingabedaten**: ein Vertex-Shader empfängt seine Eingaben aus der Eingabe Assembler-Stufe. Geometry-und Pixel-Shader erhalten Ihre Eingaben aus der vorherigen Shader-Stufe.</span><span class="sxs-lookup"><span data-stu-id="b036d-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="b036d-109">Weitere Eingaben umfassen eine [System Wert Semantik](dx-graphics-hlsl-semantics.md), die von der ersten Einheit in der Pipeline, auf die Sie anwendbar sind, genutzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b036d-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="b036d-110">**Ausgabedaten**: Shaders generieren Ausgabe Ergebnisse, die an die nachfolgende Phase in der Pipeline übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="b036d-111">Bei einem Geometry-Shader kann die Menge an Daten, die von einem einzelnen Aufruf ausgegeben werden, variieren.</span><span class="sxs-lookup"><span data-stu-id="b036d-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="b036d-112">Einige Ausgaben werden vom Common-Shader-Kern (z. b. Scheitelpunkt Position und Renderziel-Array-Index) interpretiert, andere sind so konzipiert, dass Sie von einer Anwendung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="b036d-113">**Shadercode: Shader** können aus dem Arbeitsspeicher lesen, die arithmetischen Operationen für Vektor Gleit Komma-und ganzzahlige Operationen oder Fluss Steuerungs Vorgänge durchführen.</span><span class="sxs-lookup"><span data-stu-id="b036d-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="b036d-114">Es gibt keine Beschränkung für die Anzahl der Anweisungen, die in einem Shader implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="b036d-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="b036d-115">**Samplers**: Samplers definieren, wie Texturen von Beispielen und Filtern gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="b036d-116">Bis zu 16 samplz können gleichzeitig an einen Shader gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="b036d-117">**Texturen**: Texturen können mithilfe von Samplern gefiltert werden, oder Sie können direkt mit der systeminternen [Load](dx-graphics-hlsl-to-load.md) -Funktion gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="b036d-118">**Puffer**: Puffer werden nie gefiltert, können jedoch direkt mit der systeminternen [Load](dx-graphics-hlsl-to-load.md) -Funktion aus dem Arbeitsspeicher aus dem Arbeitsspeicher gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="b036d-119">So viele wie 128 Textur-und Puffer Ressourcen (kombiniert) können gleichzeitig an einen Shader gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="b036d-120">**Konstante Puffer**: Konstante Puffer werden für Shader-Konstantenvariablen optimiert.</span><span class="sxs-lookup"><span data-stu-id="b036d-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="b036d-121">Bis zu 16 Konstante Puffer können gleichzeitig an eine Shader-Phase gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="b036d-122">Sie sind für häufigere Updates von der CPU konzipiert. Daher haben Sie zusätzliche Größen-, Layout-und Zugriffsbeschränkungen.</span><span class="sxs-lookup"><span data-stu-id="b036d-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b036d-123">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b036d-123">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="b036d-124">In Direct3D 9 besaß jede Shader-Einheit eine einzelne, kleine Konstante Registrierungsdatei, um alle Konstanten shadervariablen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b036d-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="b036d-125">Wenn alle Shader mit diesem eingeschränkten Konstanten Raum untergebracht werden, ist eine häufige Wiederverwendung von Konstanten durch die CPU erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b036d-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span><br/> <span data-ttu-id="b036d-126">In Direct3D 10 werden Konstanten in unveränderlichen Puffer im Arbeitsspeicher gespeichert und wie jede andere Ressource verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b036d-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="b036d-127">Es gibt keine Beschränkung für die Anzahl der Konstanten Puffer, die eine Anwendung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="b036d-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="b036d-128">Durch die Organisation von Konstanten in Puffern nach Aktualisierungs-und Verwendungs Häufigkeit kann die Menge an Bandbreite, die zum Aktualisieren von Konstanten für alle Shader erforderlich ist, erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span><br/> |



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="b036d-129">Ganzzahlige und bitweise Unterstützung</span><span class="sxs-lookup"><span data-stu-id="b036d-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="b036d-130">Der gemeinsame Shader-Kern bietet einen vollständigen Satz von IEEE-kompatiblen, ganzzahligen 32-Bit-und bitweisen Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="b036d-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="b036d-131">Diese Vorgänge ermöglichen eine neue Klasse von Algorithmen in Grafikhardware Beispielen, einschließlich Komprimierungs-und Komprimierungs Techniken, FFTs und der programmflusssteuerung für das Bitfeld.</span><span class="sxs-lookup"><span data-stu-id="b036d-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="b036d-132">Die Datentypen " **int** " und " **uint** " in Direct3D 10 HLSL sind in der Hardware 32-Bit-Ganzzahlen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b036d-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b036d-133">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b036d-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="b036d-134">In Direct3D 9 werden Datenstrom Eingaben, die in HLSL als Integer gekennzeichnet sind, als Gleit Komma interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b036d-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="b036d-135">In Direct3D 10 werden als Integer markierte streameingaben als 32-Bit-Ganzzahl interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b036d-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="b036d-136">Außerdem sind boolesche Werte jetzt alle Bits festgelegt, oder alle Bits sind nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b036d-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="b036d-137">Daten, die in **bool** konvertiert werden, werden als true interpretiert, wenn der Wert nicht mit 0,0 f übereinstimmt (sowohl positive als auch negative Null sind zulässig), andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="b036d-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="b036d-138">Bitweise Operatoren</span><span class="sxs-lookup"><span data-stu-id="b036d-138">Bitwise operators</span></span>

<span data-ttu-id="b036d-139">Der Common Shader Core unterstützt die folgenden bitweisen Operatoren:</span><span class="sxs-lookup"><span data-stu-id="b036d-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="b036d-140">Operator</span><span class="sxs-lookup"><span data-stu-id="b036d-140">Operator</span></span>  | <span data-ttu-id="b036d-141">Funktion</span><span class="sxs-lookup"><span data-stu-id="b036d-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="b036d-142">Logisches NOT</span><span class="sxs-lookup"><span data-stu-id="b036d-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="b036d-143">Nach links verschieben</span><span class="sxs-lookup"><span data-stu-id="b036d-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="b036d-144">Rechte Verschiebung</span><span class="sxs-lookup"><span data-stu-id="b036d-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="b036d-145">Logisches UND</span><span class="sxs-lookup"><span data-stu-id="b036d-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="b036d-146">Logisches ODER.</span><span class="sxs-lookup"><span data-stu-id="b036d-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="b036d-147">Logisches XOR</span><span class="sxs-lookup"><span data-stu-id="b036d-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="b036d-148">Left Shift gleich</span><span class="sxs-lookup"><span data-stu-id="b036d-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="b036d-149">Rechtsverschiebung gleich</span><span class="sxs-lookup"><span data-stu-id="b036d-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="b036d-150">Und gleich</span><span class="sxs-lookup"><span data-stu-id="b036d-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="b036d-151">Oder gleich</span><span class="sxs-lookup"><span data-stu-id="b036d-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="b036d-152">XOR-gleich</span><span class="sxs-lookup"><span data-stu-id="b036d-152">Xor Equal</span></span>         |



 

<span data-ttu-id="b036d-153">Bitweise Operatoren sind so definiert, dass Sie nur für die Datentypen **int** und **uint** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="b036d-154">Der Versuch, bitweise Operatoren für die Datentypen **float** oder **struct** zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="b036d-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="b036d-155">Bitweise Operatoren folgen in Bezug auf andere Operatoren der gleichen Rangfolge wie C.</span><span class="sxs-lookup"><span data-stu-id="b036d-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="b036d-156">Binäre Umwandlungen</span><span class="sxs-lookup"><span data-stu-id="b036d-156">Binary Casts</span></span>

<span data-ttu-id="b036d-157">Durch Umwandeln zwischen einer Ganzzahl und einem Gleit kommatyp wird der numerische Wert nach C-abkürzen konvertiert.</span><span class="sxs-lookup"><span data-stu-id="b036d-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="b036d-158">Das Umwandeln eines Werts aus **einer Gleit** Komma Zahl **in einen** ganzzahligen Wert in einen **float** -Wert ist eine verlustfreie Konvertierung, die von der Genauigkeit des Ziel Datentyps abhängt.</span><span class="sxs-lookup"><span data-stu-id="b036d-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="b036d-159">Im folgenden finden Sie einige der Konvertierungs Funktionen: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="b036d-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="b036d-160">Binäre Umwandlungen können auch mit systeminternen HLSL-Funktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b036d-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="b036d-161">Diese bewirken, dass der Compiler die Bit-Darstellung einer Zahl in den Ziel Datentyp uminterpretiert.</span><span class="sxs-lookup"><span data-stu-id="b036d-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b036d-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b036d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b036d-163">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b036d-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





