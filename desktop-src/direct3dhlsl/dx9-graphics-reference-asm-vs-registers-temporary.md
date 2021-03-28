---
title: Temporäres Register (HLSL vs-Referenz)
description: Ein temporäres Vertex-Shader-Register wird verwendet, um Zwischenergebnisse zu speichern.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313799"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="a4a50-103">Temporäres Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="a4a50-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="a4a50-104">Ein temporäres Vertex-Shader-Register wird verwendet, um Zwischenergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a4a50-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="a4a50-105">Ein temporäres Register muss initialisiert werden, bevor es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a4a50-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="a4a50-106">Jedes temporäre Register verfügt über einen einzelschreibzugriff und einen dreifach Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="a4a50-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="a4a50-107">Dies bedeutet, dass eine einzelne Shader-Anweisung bis zu drei temporäre Register als Eingaben verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a4a50-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="a4a50-108">Werte in einem temporären Register, die aus vorangehenden Aufrufen des Vertex-Shaders verbleiben, können nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4a50-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="a4a50-109">Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.</span><span class="sxs-lookup"><span data-stu-id="a4a50-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="a4a50-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4a50-110">Property</span></span>        | <span data-ttu-id="a4a50-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4a50-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a50-112">Name</span><span class="sxs-lookup"><span data-stu-id="a4a50-112">Name</span></span>            | <span data-ttu-id="a4a50-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="a4a50-113">r\[n\].</span></span> <span data-ttu-id="a4a50-114">n ist eine optionale Registernummer.</span><span class="sxs-lookup"><span data-stu-id="a4a50-114">n is an optional register number.</span></span> <span data-ttu-id="a4a50-115">Der Standardwert ist 0, und ist der Wert, der verwendet wird, wenn kein Wert angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4a50-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="a4a50-116">Anzahl</span><span class="sxs-lookup"><span data-stu-id="a4a50-116">Count</span></span>           | <span data-ttu-id="a4a50-117">Maximal 12 Register.</span><span class="sxs-lookup"><span data-stu-id="a4a50-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a4a50-118">E/a-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a4a50-118">I/O permissions</span></span> | <span data-ttu-id="a4a50-119">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a4a50-119">Read/write.</span></span> <span data-ttu-id="a4a50-120">Dieses Register kann von der API oder vom Shader gelesen oder geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a4a50-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="a4a50-121">Leseports</span><span class="sxs-lookup"><span data-stu-id="a4a50-121">Read ports</span></span>      | <span data-ttu-id="a4a50-122">Die Häufigkeit, mit der ein Register innerhalb einer einzigen Anweisung gelesen werden kann, ist 3.</span><span class="sxs-lookup"><span data-stu-id="a4a50-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="a4a50-123">Ein temporäres Register ist das einzige Register, das mehr als einmal in einer einzigen Anweisung gelesen und geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a4a50-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="a4a50-124">Jedes temporäre Register verfügt über einen einzelschreibzugriff und einen dreifach Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="a4a50-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="a4a50-125">Aus diesem Grund kann eine Anweisung in der Gruppe der Eingabe Quell Operanden bis zu drei temporäre Register aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a4a50-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="a4a50-126">Es können keine Werte in einem temporären Register verwendet werden, die aus vorangehenden Aufrufen des Vertex-Shaders verbleiben.</span><span class="sxs-lookup"><span data-stu-id="a4a50-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="a4a50-127">Vertex-Shader, die vor dem Schreiben einen Wert aus einem temporären Register lesen, führen zum Erstellen des Vertexshaders nicht zum Direct3D-API-aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a4a50-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="a4a50-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a4a50-128">Example</span></span>

<span data-ttu-id="a4a50-129">Im folgenden finden Sie ein Beispiel für die Verwendung eines temporären Registers:</span><span class="sxs-lookup"><span data-stu-id="a4a50-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="a4a50-130">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="a4a50-130">Vertex shader versions</span></span> | <span data-ttu-id="a4a50-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="a4a50-131">1\_1</span></span> | <span data-ttu-id="a4a50-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4a50-132">2\_0</span></span> | <span data-ttu-id="a4a50-133">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a4a50-133">2\_sw</span></span> | <span data-ttu-id="a4a50-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a4a50-134">2\_x</span></span> | <span data-ttu-id="a4a50-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a4a50-135">3\_0</span></span> | <span data-ttu-id="a4a50-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a4a50-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="a4a50-137">Temporäres Register</span><span class="sxs-lookup"><span data-stu-id="a4a50-137">Temporary Register</span></span>     | <span data-ttu-id="a4a50-138">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-138">x</span></span>    | <span data-ttu-id="a4a50-139">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-139">x</span></span>    | <span data-ttu-id="a4a50-140">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-140">x</span></span>     | <span data-ttu-id="a4a50-141">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-141">x</span></span>    | <span data-ttu-id="a4a50-142">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-142">x</span></span>    | <span data-ttu-id="a4a50-143">x</span><span class="sxs-lookup"><span data-stu-id="a4a50-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="a4a50-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4a50-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a50-145">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="a4a50-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




