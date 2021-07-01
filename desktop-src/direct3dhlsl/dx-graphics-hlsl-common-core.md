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
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129717"
---
# <a name="common-shader-core"></a><span data-ttu-id="269b4-103">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="269b4-103">Common-Shader Core</span></span>

<span data-ttu-id="269b4-104">In Shader Model 4 implementieren alle Shaderstufen die gleiche Basisfunktionalität mit einem gemeinsamen Shaderkern.</span><span class="sxs-lookup"><span data-stu-id="269b4-104">In Shader Model 4, all shader stages implement the same base functionality using a common-shader core.</span></span> <span data-ttu-id="269b4-105">Darüber hinaus bietet jede der drei Shaderstufen (Scheitelpunkt, Geometrie und Pixel) funktionen, die für jede Stufe spezifisch sind, z. B. die Möglichkeit, neue Primitive aus der Geometrie-Shader-Stufe zu generieren oder ein bestimmtes Pixel in der Pixel-Shader-Stufe zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="269b4-105">In addition, each of the three shader stages (vertex, geometry, and pixel) offer functionality unique to each stage, such as the ability to generate new primitives from the geometry shader stage or to discard a specific pixel in the pixel shader stage.</span></span> <span data-ttu-id="269b4-106">Das folgende Diagramm zeigt, wie Daten durch eine Shaderphase fließen, und die Beziehung zwischen dem gemeinsamen Shaderkern und Shaderspeicherressourcen.</span><span class="sxs-lookup"><span data-stu-id="269b4-106">The following diagram shows how data flows through a shader stage, and the relationship of the common-shader core with shader memory resources.</span></span>

![Diagramm des Datenflusses in einer Shaderphase](images/d3d10-shader-unit.png)

-   <span data-ttu-id="269b4-108">**Eingabedaten:** Ein Vertex-Shader empfängt seine Eingaben aus der Eingabe-Assemblerphase. Geometry- und Pixel-Shader erhalten ihre Eingaben aus der vorherigen Shaderphase.</span><span class="sxs-lookup"><span data-stu-id="269b4-108">**Input Data**: A vertex shader receives its inputs from the input assembler stage; geometry and pixel shaders receive their inputs from the previous shader stage.</span></span> <span data-ttu-id="269b4-109">Weitere Eingaben umfassen [die Systemwertsemantik,](dx-graphics-hlsl-semantics.md)die von der ersten Einheit in der Pipeline verwendet werden kann, auf die sie anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="269b4-109">Additional inputs include [system-value semantics](dx-graphics-hlsl-semantics.md), which are consumable by the first unit in the pipeline to which they are applicable.</span></span>
-   <span data-ttu-id="269b4-110">**Ausgabedaten:** Shader generieren Ausgabeergebnisse, die an die nachfolgende Phase in der Pipeline übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-110">**Output Data**: Shaders generate output results to be passed onto the subsequent stage in the pipeline.</span></span> <span data-ttu-id="269b4-111">Bei einem Geometrie-Shader kann die Datenmenge, die von einem einzelnen Aufruf ausgegeben wird, variieren.</span><span class="sxs-lookup"><span data-stu-id="269b4-111">For a geometry shader, the amount of data output from a single invocation can vary.</span></span> <span data-ttu-id="269b4-112">Einige Ausgaben werden vom gemeinsamen Shaderkern interpretiert (z. B. Scheitelpunktposition und Renderzielarrayindex), andere sind so konzipiert, dass sie von einer Anwendung interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-112">Some outputs are interpreted by the common-shader core (such as vertex position and render-target-array index), others are designed to be interpreted by an application.</span></span>
-   <span data-ttu-id="269b4-113">**Shadercode:** Shader können aus dem Arbeitsspeicher lesen, Vektor-Gleitkomma- und ganzzahlige arithmetische Operationen oder Flusssteuerungsvorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="269b4-113">**Shader Code**: Shaders can read from memory, perform vector floating point and integer arithmetic operations, or flow control operations.</span></span> <span data-ttu-id="269b4-114">Es gibt keine Beschränkung für die Anzahl von Anweisungen, die in einem Shader implementiert werden können.</span><span class="sxs-lookup"><span data-stu-id="269b4-114">There is no limit to the number of statements that can be implemented in a shader.</span></span>
-   <span data-ttu-id="269b4-115">**Sampler:** Sampler definieren, wie Texturen entnommen und gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-115">**Samplers**: Samplers define how to sample and filter textures.</span></span> <span data-ttu-id="269b4-116">Bis zu 16 Sampler können gleichzeitig an einen Shader gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-116">As many as 16 samplers can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="269b4-117">**Texturen:** Texturen können mit Samplern gefiltert oder direkt mit der systeminternen Load-Funktion pro Texel [gelesen](dx-graphics-hlsl-to-load.md) werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-117">**Textures**: Textures can be filtered using samplers or read on a per-texel basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span>
-   <span data-ttu-id="269b4-118">**Puffer:** Puffer werden nie gefiltert, können jedoch direkt mit der systeminternen Load-Funktion pro Element aus dem [Arbeitsspeicher](dx-graphics-hlsl-to-load.md) gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-118">**Buffers**: Buffers are never filtered, but can be read from memory on a per-element basis directly with the [load](dx-graphics-hlsl-to-load.md) intrinsic function.</span></span> <span data-ttu-id="269b4-119">Bis zu 128 Textur- und Pufferressourcen (kombiniert) können gleichzeitig an einen Shader gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-119">As many as 128 texture and buffer resources (combined) can be bound to a shader simultaneously.</span></span>
-   <span data-ttu-id="269b4-120">**Konstantenpuffer:** Konstante Puffer sind für Shaderkonstuntervariablen optimiert.</span><span class="sxs-lookup"><span data-stu-id="269b4-120">**Constant Buffers**: Constant buffers are optimized for shader constant-variables.</span></span> <span data-ttu-id="269b4-121">Bis zu 16 konstante Puffer können gleichzeitig an eine Shaderphase gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-121">As many as 16 constant buffers can be bound to a shader stage simultaneously.</span></span> <span data-ttu-id="269b4-122">Sie sind für eine häufigere Aktualisierung der CPU konzipiert. daher gelten zusätzliche Größen-, Layout- und Zugriffseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="269b4-122">They are designed for more frequent update from the CPU; therefore, they have additional size, layout, and access restrictions.</span></span>


<span data-ttu-id="269b4-123">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="269b4-123">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="269b4-124">In Direct3D 9 hatte jede Shadereinheit eine einzelne, kleine konstante Registerdatei zum Speichern aller konstanten Shadervariablen.</span><span class="sxs-lookup"><span data-stu-id="269b4-124">In Direct3D 9, each shader unit had a single, small constant register file to store all constant shader variables.</span></span> <span data-ttu-id="269b4-125">Die Aufnahme aller Shader mit diesem begrenzten konstanten Speicherplatz erforderte eine häufige Wiederverwendung von Konstanten durch die CPU.</span><span class="sxs-lookup"><span data-stu-id="269b4-125">Accommodating all shaders with this limited constant space required frequent recycling of constants by the CPU.</span></span>
- <span data-ttu-id="269b4-126">In Direct3D 10 werden Konstanten in unveränderlichen Puffern im Arbeitsspeicher gespeichert und wie jede andere Ressource verwaltet.</span><span class="sxs-lookup"><span data-stu-id="269b4-126">In Direct3D 10, constants are stored in immutable buffers in memory and are managed like any other resource.</span></span> <span data-ttu-id="269b4-127">Es gibt keine Beschränkung für die Anzahl konstanter Puffer, die eine Anwendung erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="269b4-127">There is no limit to the number of constant buffers an application can create.</span></span> <span data-ttu-id="269b4-128">Durch das Organisieren von Konstanten in Puffern nach Aktualisierungs- und Nutzungshäufigkeit kann die Bandbreite, die zum Aktualisieren von Konstanten erforderlich ist, um alle Shader zu berücksichtigen, erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-128">By organizing constants into buffers by frequency of update and usage, the amount of bandwidth required to update constants to accommodate all shaders can be significantly reduced.</span></span>



 

## <a name="integer-and-bitwise-support"></a><span data-ttu-id="269b4-129">Ganzzahlige und bitweise Unterstützung</span><span class="sxs-lookup"><span data-stu-id="269b4-129">Integer and Bitwise Support</span></span>

<span data-ttu-id="269b4-130">Der allgemeine Shaderkern bietet einen vollständigen Satz von IEEE-konformen 32-Bit-Ganzzahlen und bitweise Operationen.</span><span class="sxs-lookup"><span data-stu-id="269b4-130">The common shader core provides a full set of IEEE-compliant 32-bit integer and bitwise operations.</span></span> <span data-ttu-id="269b4-131">Diese Vorgänge ermöglichen eine neue Klasse von Algorithmen in Grafikhardwarebeispielen, z. B. Komprimierungs- und Packtechniken, FFTs und bitfield-Programmflusssteuerung.</span><span class="sxs-lookup"><span data-stu-id="269b4-131">These operations enable a new class of algorithms in graphics hardware examples include compression and packing techniques, FFTs, and bitfield program-flow control.</span></span>

<span data-ttu-id="269b4-132">Die **Datentypen int** und **uint** in Direct3D 10 HLSL sind 32-Bit-Ganzzahlen in der Hardware zuordnen.</span><span class="sxs-lookup"><span data-stu-id="269b4-132">The **int** and **uint** data types in Direct3D 10 HLSL map to 32-bit integers in hardware.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="269b4-133">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="269b4-133">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="269b4-134">In Direct3D 9 wurden Streameingaben, die in HLSL als ganze Zahl gekennzeichnet sind, als Gleitkomma interpretiert.</span><span class="sxs-lookup"><span data-stu-id="269b4-134">In Direct3D 9 stream inputs marked as integer in HLSL were interpreted as floating-point.</span></span> <span data-ttu-id="269b4-135">In Direct3D 10 werden als ganze Zahl markierte Streameingaben als 32-Bit-Ganzzahl interpretiert.</span><span class="sxs-lookup"><span data-stu-id="269b4-135">In Direct3D 10, stream inputs marked as integer are interpreted as a 32- bit integer.</span></span><br/> <span data-ttu-id="269b4-136">Darüber hinaus sind boolesche Werte jetzt alle Bits festgelegt oder alle Bits nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="269b4-136">In addition, boolean values are now all bits set or all bits unset.</span></span> <span data-ttu-id="269b4-137">Daten, die in **bool** konvertiert werden, werden als TRUE interpretiert, wenn der Wert nicht gleich 0,0f ist (positive und negative Nullen dürfen false sein) und andernfalls FALSE.</span><span class="sxs-lookup"><span data-stu-id="269b4-137">Data converted to **bool** will be interpreted as true if the value is not equal to 0.0f (both positive and negative zero are allowed to be false) and false otherwise.</span></span><br/> |



 

## <a name="bitwise-operators"></a><span data-ttu-id="269b4-138">Bitweise Operatoren</span><span class="sxs-lookup"><span data-stu-id="269b4-138">Bitwise operators</span></span>

<span data-ttu-id="269b4-139">Der allgemeine Shaderkern unterstützt die folgenden bitweise Operatoren:</span><span class="sxs-lookup"><span data-stu-id="269b4-139">The common shader core supports the following bitwise operators:</span></span>



| <span data-ttu-id="269b4-140">Operator</span><span class="sxs-lookup"><span data-stu-id="269b4-140">Operator</span></span>  | <span data-ttu-id="269b4-141">Funktion</span><span class="sxs-lookup"><span data-stu-id="269b4-141">Function</span></span>          |
|-----------|-------------------|
| ~         | <span data-ttu-id="269b4-142">Logical Not</span><span class="sxs-lookup"><span data-stu-id="269b4-142">Logical Not</span></span>       |
| <<  | <span data-ttu-id="269b4-143">Linksverschiebung</span><span class="sxs-lookup"><span data-stu-id="269b4-143">Left Shift</span></span>        |
| >>  | <span data-ttu-id="269b4-144">Rechtsverschiebung</span><span class="sxs-lookup"><span data-stu-id="269b4-144">Right Shift</span></span>       |
| &         | <span data-ttu-id="269b4-145">Logisches UND</span><span class="sxs-lookup"><span data-stu-id="269b4-145">Logical And</span></span>       |
| \|        | <span data-ttu-id="269b4-146">Logisches ODER.</span><span class="sxs-lookup"><span data-stu-id="269b4-146">Logical Or</span></span>        |
| ^         | <span data-ttu-id="269b4-147">Logischer Xor</span><span class="sxs-lookup"><span data-stu-id="269b4-147">Logical Xor</span></span>       |
| <<= | <span data-ttu-id="269b4-148">Left shift Equal</span><span class="sxs-lookup"><span data-stu-id="269b4-148">Left shift Equal</span></span>  |
| >>= | <span data-ttu-id="269b4-149">Rechtsverschiebung gleich</span><span class="sxs-lookup"><span data-stu-id="269b4-149">Right Shift Equal</span></span> |
| &=        | <span data-ttu-id="269b4-150">Und gleich</span><span class="sxs-lookup"><span data-stu-id="269b4-150">And Equal</span></span>         |
| \|=       | <span data-ttu-id="269b4-151">Oder gleich</span><span class="sxs-lookup"><span data-stu-id="269b4-151">Or Equal</span></span>          |
| ^=        | <span data-ttu-id="269b4-152">Xor Equal</span><span class="sxs-lookup"><span data-stu-id="269b4-152">Xor Equal</span></span>         |



 

<span data-ttu-id="269b4-153">Bitweise Operatoren werden so definiert, dass sie nur für **int-** und **uint-Datentypen** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-153">Bitwise operators are defined to operate only on **int** and **uint** data types.</span></span> <span data-ttu-id="269b4-154">Der Versuch, bitweise Operatoren für **float-** oder **struct-Datentypen** zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="269b4-154">Attempting to use bitwise operators on **float** or **struct** data types will result in an error.</span></span> <span data-ttu-id="269b4-155">Bitweise Operatoren haben im Hinblick auf andere Operatoren die gleiche Rangfolge wie C.</span><span class="sxs-lookup"><span data-stu-id="269b4-155">Bitwise operators follow the same precedence as C with regard to other operators.</span></span>

## <a name="binary-casts"></a><span data-ttu-id="269b4-156">Binäre Casts</span><span class="sxs-lookup"><span data-stu-id="269b4-156">Binary Casts</span></span>

<span data-ttu-id="269b4-157">Die Umwandlung zwischen einer ganzen Zahl und einem Gleitkommatyp konvertiert den numerischen Wert nach C-Abschneideregeln.</span><span class="sxs-lookup"><span data-stu-id="269b4-157">Casting between an integer and a floating-point type will convert the numeric value following C truncation rules.</span></span> <span data-ttu-id="269b4-158">Die Umwandlung eines Werts aus einem **float-Wert** in einen **int-Wert** und zurück in einen **float-Wert** ist eine verlustbewegte Konvertierung, die von der Genauigkeit des Zieldatentyps abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="269b4-158">Casting a value from a **float**, to an **int**, and back to a **float** is a lossy conversion dependent on the precision of the target data type.</span></span> <span data-ttu-id="269b4-159">Hier sind einige der Konvertierungsfunktionen: [**asfloat (DirectX HLSL),**](dx-graphics-hlsl-asfloat.md) [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span><span class="sxs-lookup"><span data-stu-id="269b4-159">Here are some of the conversion functions: [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**asint (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).</span></span>

<span data-ttu-id="269b4-160">Binäre Casts können auch mit systeminternen HLSL-Funktionen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="269b4-160">Binary casts can also be performed using HLSL intrinsic functions.</span></span> <span data-ttu-id="269b4-161">Diese bewirken, dass der Compiler die Bitdarstellung einer Zahl im Zieldatentyp neu interpretiert.</span><span class="sxs-lookup"><span data-stu-id="269b4-161">These cause the compiler to reinterpret the bit representation of a number into the target data type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="269b4-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="269b4-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269b4-163">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="269b4-163">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





