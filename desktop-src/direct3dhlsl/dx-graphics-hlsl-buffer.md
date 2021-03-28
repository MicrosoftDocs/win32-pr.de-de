---
title: Puffertyp
description: Verwenden Sie die folgende Syntax, um eine Puffer Variable zu deklarieren.
ms.assetid: f21f0de5-58e3-466b-97bb-e4e7efa9cc1c
keywords:
- Pusl-Puffertyp
topic_type:
- apiref
api_name:
- Buffer Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e36030f3dd31f1bdada238e89c1048e4971cd45c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039190"
---
# <a name="buffer-type"></a><span data-ttu-id="f8418-104">Puffertyp</span><span class="sxs-lookup"><span data-stu-id="f8418-104">Buffer Type</span></span>

<span data-ttu-id="f8418-105">Verwenden Sie die folgende Syntax, um eine Puffer Variable zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="f8418-105">Use the following syntax to declare a buffer variable.</span></span>



| <span data-ttu-id="f8418-106">Puffer< >  *Typname*;</span><span class="sxs-lookup"><span data-stu-id="f8418-106">Buffer<*Type*> *Name*;</span></span> |
|------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f8418-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8418-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8418-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Ert**</span><span class="sxs-lookup"><span data-stu-id="f8418-108"><span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="f8418-109">Erforderliches Schlüsselwort.</span><span class="sxs-lookup"><span data-stu-id="f8418-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="f8418-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="f8418-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="f8418-111">Einer der Typen [skalare](dx-graphics-hlsl-scalar.md), [Vector](dx-graphics-hlsl-vector.md)und some [Matrix](dx-graphics-hlsl-matrix.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="f8418-111">One of the [scalar](dx-graphics-hlsl-scalar.md), [vector](dx-graphics-hlsl-vector.md), and some [matrix](dx-graphics-hlsl-matrix.md) HLSL types.</span></span> <span data-ttu-id="f8418-112">Sie können eine Puffer Variable mit einer Matrix deklarieren, solange Sie in 4 32-Bit-Mengen passt.</span><span class="sxs-lookup"><span data-stu-id="f8418-112">You can declare a buffer variable with a matrix as long as it fits in 4 32-bit quantities.</span></span> <span data-ttu-id="f8418-113">Daher können Sie schreiben `Buffer<float2x2>` .</span><span class="sxs-lookup"><span data-stu-id="f8418-113">So, you can write `Buffer<float2x2>`.</span></span> <span data-ttu-id="f8418-114">Aber `Buffer<float4x4>` ist zu groß, und der Compiler generiert einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="f8418-114">But `Buffer<float4x4>` is too large, and the compiler will generate an error.</span></span>

</dd> <dt>

<span data-ttu-id="f8418-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="f8418-115"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="f8418-116">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f8418-116">An ASCII string that uniquely identifies the variable name.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="f8418-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f8418-117">Example</span></span>

<span data-ttu-id="f8418-118">Im folgenden finden Sie ein Beispiel für eine Puffer Deklaration aus der Datei "pipesgs. FX" in [pipesgs Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="f8418-118">Here is an example of a buffer declaration from the PipesGS.fx file in [PipesGS Sample](https://msdn.microsoft.com/library/Ee416423(v=VS.85).aspx).</span></span>


```
Buffer<float4> g_Buffer;
```



<span data-ttu-id="f8418-119">Daten werden aus einem Puffer mithilfe einer überladenen Version der systeminternen [**Load**](dx-graphics-hlsl-to-load.md) HLSL-Funktion gelesen, die einen Eingabeparameter (einen ganzzahligen Index) annimmt.</span><span class="sxs-lookup"><span data-stu-id="f8418-119">Data is read from a buffer using an overloaded version of the [**Load**](dx-graphics-hlsl-to-load.md) HLSL intrinsic function that takes one input parameter (an integer index).</span></span> <span data-ttu-id="f8418-120">Auf einen Puffer wird wie ein Array von Elementen zugegriffen. Daher wird in diesem Beispiel das zweite Element gelesen.</span><span class="sxs-lookup"><span data-stu-id="f8418-120">A buffer is accessed like an array of elements; therefore, this example reads the second element.</span></span>


```
float4 bufferData = g_Buffer.Load( 1 );
```



<span data-ttu-id="f8418-121">Verwenden Sie die [Stream-Output-Phase](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) , um Daten in einen Puffer auszugeben.</span><span class="sxs-lookup"><span data-stu-id="f8418-121">Use the [stream-output stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-stream-stage) to output data to a buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8418-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f8418-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8418-123">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8418-123">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 