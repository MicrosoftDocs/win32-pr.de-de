---
title: dcl_interface_dynamicindexed (SM5-ASM)
description: Deklarieren Sie Funktionstabellen Zeiger (Schnittstellen). | dcl_interface_dynamicindexed (SM5-ASM)
ms.assetid: 5C77EBB6-7AEC-4471-AA6E-0F6D3E215156
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78bb0152b44f7e29b9e76221db13da0c465a434
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995694"
---
# <a name="dcl_interface_dynamicindexed-sm5---asm"></a><span data-ttu-id="00940-104">DCL \_ -Schnittstelle \_ dynamicindiziert (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="00940-104">dcl\_interface\_dynamicindexed (sm5 - asm)</span></span>

<span data-ttu-id="00940-105">Deklarieren Sie Funktionstabellen Zeiger (Schnittstellen).</span><span class="sxs-lookup"><span data-stu-id="00940-105">Declare function table pointers (interfaces).</span></span>



| <span data-ttu-id="00940-106">DCL- \_ Schnittstelle \_ dynamicindiziert FP \# \[ arraySize \] \[ numcallsites \] = {ft \# , ft \# ,...}</span><span class="sxs-lookup"><span data-stu-id="00940-106">dcl\_interface\_dynamicindexed fp\#\[arraySize\]\[numCallSites\] = {ft\#, ft\#, ...}</span></span> |
|--------------------------------------------------------------------------------------|



 



| <span data-ttu-id="00940-107">Element</span><span class="sxs-lookup"><span data-stu-id="00940-107">Item</span></span>                                                          | <span data-ttu-id="00940-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="00940-108">Description</span></span>                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="00940-109"><span id="fp_"></span><span id="FP_"></span>*FP\#*</span><span class="sxs-lookup"><span data-stu-id="00940-109"><span id="fp_"></span><span id="FP_"></span>*fp\#*</span></span><br/> | <span data-ttu-id="00940-110">\[in \] den Funktionstabellen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="00940-110">\[in\] The function table pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00940-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00940-111">Remarks</span></span>

<span data-ttu-id="00940-112">Jede Schnittstelle muss von der API gebunden werden, bevor der Shader verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="00940-112">Each interface needs to be bound from the API before the shader is usable.</span></span> <span data-ttu-id="00940-113">Die Bindung gibt einen Verweis auf eine der Funktionstabellen aus, sodass die Methoden Slots ausgefüllt werden können.</span><span class="sxs-lookup"><span data-stu-id="00940-113">Binding gives a reference to one of the function tables so that the method slots can be filled in.</span></span> <span data-ttu-id="00940-114">Der Compiler generiert keine Zeiger für Objekte, auf die nicht verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="00940-114">The compiler will not generate pointers for unreferenced objects.</span></span>

<span data-ttu-id="00940-115">Ein Funktionstabellen Zeiger verfügt über einen vollständigen Satz von Methoden Slots, um die zusätzliche Dereferenzierungsebene zu vermeiden, die eine C++-Darstellung von Zeiger auf Vtable erfordern würde.</span><span class="sxs-lookup"><span data-stu-id="00940-115">A function table pointer has a full set of method slots to avoid the extra level of indirection that a C++ pointer-to- pointer-to-vtable representation would require.</span></span> <span data-ttu-id="00940-116">Dies erfordert auch, dass es sich bei diesen Zeigern um 5 Tupel handelt.</span><span class="sxs-lookup"><span data-stu-id="00940-116">That would also require that this pointers be 5-tuples.</span></span> <span data-ttu-id="00940-117">Im virtuellen HLSL-Inlining-Modell ist immer bekannt, welche globale Variable/Eingabe für einen-Rückruf verwendet wird, sodass wir Tabellen pro Stamm Objekt einrichten können.</span><span class="sxs-lookup"><span data-stu-id="00940-117">In the HLSL virtual inlining model it's always known what global variable/input is used for a call so we can set up tables per root object.</span></span>

<span data-ttu-id="00940-118">Funktionszeiger Deklarationen geben an, welche Funktionstabellen für Sie zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="00940-118">Function pointer declarations indicate which function tables are legal to use with them.</span></span> <span data-ttu-id="00940-119">Dadurch wird auch die Ableitung von Methoden Korrelations Informationen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="00940-119">This also allows derivation of method correlation information.</span></span>

<span data-ttu-id="00940-120">Der erste \[ \] einer Schnittstellen Deklaration ist die Array Größe.</span><span class="sxs-lookup"><span data-stu-id="00940-120">The first \[\] of an interface declaration is the array size.</span></span> <span data-ttu-id="00940-121">Wenn die dynamische Indizierung verwendet wird, gibt die Deklaration dies wie gezeigt an.</span><span class="sxs-lookup"><span data-stu-id="00940-121">If dynamic indexing is used the declaration will indicate that as shown.</span></span> <span data-ttu-id="00940-122">Ein Array von Schnittstellen Zeigern kann auch statisch indiziert werden. es ist nicht erforderlich, dass Arrays von Schnittstellen Zeigern eine dynamische Indizierung bedeuten.</span><span class="sxs-lookup"><span data-stu-id="00940-122">An array of interface pointers can be indexed statically also, it is not required that arrays of interface pointers mean dynamic indexing.</span></span>

<span data-ttu-id="00940-123">Die Nummerierung von Schnittstellen Zeigern beginnt bei 0 für die erste Deklaration und nimmt anschließend die Array Größe in Betracht, sodass der erste Zeiger nach einem vier-Eintrag-Array FP0 \[ 4 \] \[ 1 \] FP4 ist \[ \] \[ \] .</span><span class="sxs-lookup"><span data-stu-id="00940-123">Numbering of interface pointers starts at 0 for the first declaration and subsequently takes array size into account, so the first pointer after a four entry array fp0\[4\]\[1\] would be fp4\[\]\[\].</span></span>

<span data-ttu-id="00940-124">Der zweite Wert \[ \] einer Schnittstellen Deklaration ist die Anzahl von CallSites, die der Anzahl von Text in jeder Tabelle entsprechen muss, auf die in der Deklaration verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="00940-124">The second \[\] of an interface declaration is the number of call sites, which must match the number of bodies in each table referenced in the declaration.</span></span>

<span data-ttu-id="00940-125">Es gibt keine Grenzen, wie viele Optionen für Funktionstabellen (ft \# ) in einer Schnittstellen Deklaration aufgelistet werden können.</span><span class="sxs-lookup"><span data-stu-id="00940-125">There are no bounds to how many function table (ft\#) choices can be listed in an interface declaration.</span></span>

<span data-ttu-id="00940-126">Eine bestimmte Funktions Tabelle (ft \# ) kann in einer oder mehreren Schnittstellen Deklarationen mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="00940-126">A given function table (ft\#) can appear more than once in one or more interface declarations.</span></span>

### <a name="restrictions"></a><span data-ttu-id="00940-127">Beschränkungen</span><span class="sxs-lookup"><span data-stu-id="00940-127">Restrictions</span></span>

-   <span data-ttu-id="00940-128">Die Anzahl der Objekt Standorte in einem Shader, die die Summe über alle *\# FP* -Deklarationen Ihrer \[ arraySize- \] Deklarationen hinweg ist, darf nicht größer als 253 sein.</span><span class="sxs-lookup"><span data-stu-id="00940-128">The number of object sites in a shader, which is the sum across all *fp\#* declarations of their \[arraySize\] declarations, must be no more than 253.</span></span> <span data-ttu-id="00940-129">Diese Zahl gibt an, wie viele **dieser** Zeiger vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="00940-129">This number corresponds to how many **this** pointers can be present.</span></span> <span data-ttu-id="00940-130">Die Runtime erzwingt dieses 253-Limit, um die Größe des DDI für die Kommunikation mit diesen Zeiger Daten zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="00940-130">The runtime enforces this 253 limit to keep a bound on the size of the DDI for communicating this pointer data.</span></span>
-   <span data-ttu-id="00940-131">Die Anzahl der Aufrufen von Websites in einem Shader, die die Summe aller fcallsanweisungen der Anzahl potenzieller Verzweigungs Ziele ist, darf nicht größer als 4096 sein.</span><span class="sxs-lookup"><span data-stu-id="00940-131">The number of call sites in a shader, which is the sum across all fcall statements of the number of potential branch targets, must be no more than 4096.</span></span>

    <span data-ttu-id="00940-132">Ein [fcalltyp](fcall--sm5---asm-.md) , der einen statischen Index für die erste *\[ \] \[ \] FP* -Dimension verwendet, zählt z. b. wie folgt:</span><span class="sxs-lookup"><span data-stu-id="00940-132">For example, an [fcall](fcall--sm5---asm-.md) that uses a static index for the first *fp\[\]\[\]* dimension counts as one:</span></span>

    `                       fcall fp0[0][0]         // +1`

    <span data-ttu-id="00940-133">Ein **fcalltyp** , der einen dynamischen Index verwendet, zählt als Anzahl von Elementen im Array (erste \[ \] der **DCL- \_ Schnittstelle**):</span><span class="sxs-lookup"><span data-stu-id="00940-133">An **fcall** that uses a dynamic index counts as the number of elements in the array (first \[\] of **dcl\_interface**):</span></span>

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    <span data-ttu-id="00940-134">Mit dieser Beschränkung können einige Implementierungen problemlos Tabellen der Funktions Textauswahl im Konstanten Puffer ähnlichen Speicher anpassen.</span><span class="sxs-lookup"><span data-stu-id="00940-134">This limit helps some implementations easily fit tables of function body selections in constant buffer-like storage.</span></span>

<span data-ttu-id="00940-135">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="00940-135">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="00940-136">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="00940-136">Vertex</span></span> | <span data-ttu-id="00940-137">Hülle</span><span class="sxs-lookup"><span data-stu-id="00940-137">Hull</span></span> | <span data-ttu-id="00940-138">Domain</span><span class="sxs-lookup"><span data-stu-id="00940-138">Domain</span></span> | <span data-ttu-id="00940-139">Geometrie</span><span class="sxs-lookup"><span data-stu-id="00940-139">Geometry</span></span> | <span data-ttu-id="00940-140">Pixel</span><span class="sxs-lookup"><span data-stu-id="00940-140">Pixel</span></span> | <span data-ttu-id="00940-141">Compute</span><span class="sxs-lookup"><span data-stu-id="00940-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="00940-142">X</span><span class="sxs-lookup"><span data-stu-id="00940-142">X</span></span>      | <span data-ttu-id="00940-143">X</span><span class="sxs-lookup"><span data-stu-id="00940-143">X</span></span>    | <span data-ttu-id="00940-144">X</span><span class="sxs-lookup"><span data-stu-id="00940-144">X</span></span>      | <span data-ttu-id="00940-145">X</span><span class="sxs-lookup"><span data-stu-id="00940-145">X</span></span>        | <span data-ttu-id="00940-146">X</span><span class="sxs-lookup"><span data-stu-id="00940-146">X</span></span>     | <span data-ttu-id="00940-147">X</span><span class="sxs-lookup"><span data-stu-id="00940-147">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="00940-148">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="00940-148">Minimum Shader Model</span></span>

<span data-ttu-id="00940-149">Diese Anweisung wird in den folgenden shadermodellen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="00940-149">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="00940-150">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="00940-150">Shader Model</span></span>                                              | <span data-ttu-id="00940-151">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="00940-151">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="00940-152">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="00940-152">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="00940-153">ja</span><span class="sxs-lookup"><span data-stu-id="00940-153">yes</span></span>       |
| [<span data-ttu-id="00940-154">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="00940-154">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="00940-155">nein</span><span class="sxs-lookup"><span data-stu-id="00940-155">no</span></span>        |
| [<span data-ttu-id="00940-156">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="00940-156">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="00940-157">nein</span><span class="sxs-lookup"><span data-stu-id="00940-157">no</span></span>        |
| [<span data-ttu-id="00940-158">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00940-158">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="00940-159">nein</span><span class="sxs-lookup"><span data-stu-id="00940-159">no</span></span>        |
| [<span data-ttu-id="00940-160">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00940-160">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="00940-161">nein</span><span class="sxs-lookup"><span data-stu-id="00940-161">no</span></span>        |
| [<span data-ttu-id="00940-162">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00940-162">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="00940-163">nein</span><span class="sxs-lookup"><span data-stu-id="00940-163">no</span></span>        |



 

<span data-ttu-id="00940-164">CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.</span><span class="sxs-lookup"><span data-stu-id="00940-164">cs\_4\_0 and cs\_4\_1 support this instruction for UAV and SRV.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00940-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00940-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00940-166">Shader Model 5-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="00940-166">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





