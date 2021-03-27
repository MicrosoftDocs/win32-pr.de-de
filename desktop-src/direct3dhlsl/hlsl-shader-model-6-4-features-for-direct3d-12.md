---
title: HLSL-Shader-Modell 6,4
description: Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869644"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="c52d6-103">HLSL-Shader-Modell 6,4</span><span class="sxs-lookup"><span data-stu-id="c52d6-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="c52d6-104">Beschreibt die Machine Learning-systeminternen Funktionen, die dem HLSL-Shadermodell 6,4 hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c52d6-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="c52d6-105">Shadermodell 6,4</span><span class="sxs-lookup"><span data-stu-id="c52d6-105">Shader Model 6.4</span></span>
<span data-ttu-id="c52d6-106">Diese systeminternen Funktionen sind ein erforderliches/unterstütztes Feature von Shader-Modell 6,4.</span><span class="sxs-lookup"><span data-stu-id="c52d6-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="c52d6-107">Folglich ist keine separate Funktionalitäts bitüberprüfung erforderlich, außer die Sicherstellung der Verwendung von Shader-Modell 6,4.</span><span class="sxs-lookup"><span data-stu-id="c52d6-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="c52d6-108">Der unterstützte mindestclient für diese Routinen ist Windows 10, Version 1903.</span><span class="sxs-lookup"><span data-stu-id="c52d6-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="c52d6-109">Intrinsische Funktionen für Schattierungs Sprache</span><span class="sxs-lookup"><span data-stu-id="c52d6-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c52d6-110">Ganzzahlige Dot-Product ohne Vorzeichen von vier Elementen und Kumulierung</span><span class="sxs-lookup"><span data-stu-id="c52d6-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="c52d6-111">Eine 4-dimensionale Ganzzahl ohne Vorzeichen mit dem Wert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c52d6-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="c52d6-112">Multipliziert jedes entsprechende Paar von 8-Bit-int-Bytes ohne Vorzeichen in den beiden Eingabe-DWords und fasst die Ergebnisse in den 32-Bit-Integer-Akkumulator (ohne Vorzeichen) zusammen.</span><span class="sxs-lookup"><span data-stu-id="c52d6-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="c52d6-113">Diese Anweisung funktioniert innerhalb einer einzelnen 32-Bit-weiten SIMD-Strecke.</span><span class="sxs-lookup"><span data-stu-id="c52d6-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c52d6-114">Die Eingaben werden auch als 32-Bit-Mengen angenommen.</span><span class="sxs-lookup"><span data-stu-id="c52d6-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="c52d6-115">Ganzzahlige Dot-Product mit Vorzeichen von vier Elementen und Kumulierung</span><span class="sxs-lookup"><span data-stu-id="c52d6-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="c52d6-116">Eine 4-dimensionale Ganzzahl mit Vorzeichen und einem Wert von "Add".</span><span class="sxs-lookup"><span data-stu-id="c52d6-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="c52d6-117">Multipliziert jedes entsprechende Paar von 8-Bit-int-Bytes mit Vorzeichen in den beiden Eingabe-DWords und fasst die Ergebnisse in den 32-Bit-integerakkumulator mit Vorzeichen um.</span><span class="sxs-lookup"><span data-stu-id="c52d6-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="c52d6-118">Diese Anweisung funktioniert innerhalb einer einzelnen 32-Bit-weiten SIMD-Strecke.</span><span class="sxs-lookup"><span data-stu-id="c52d6-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c52d6-119">Die Eingaben werden auch als 32-Bit-Mengen angenommen.</span><span class="sxs-lookup"><span data-stu-id="c52d6-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="c52d6-120">Gleit Komma Wert mit einfacher Genauigkeit 2-Element Dot-Product und ansammeln</span><span class="sxs-lookup"><span data-stu-id="c52d6-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="c52d6-121">Ein zweidimensionales Gleit Komma-Punkt-Product von half2 Vektoren mit Add.</span><span class="sxs-lookup"><span data-stu-id="c52d6-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="c52d6-122">Multipliziert die Elemente der zwei Gleit Komma Eingabe-Vektoren mit halber Genauigkeit und fasst die Ergebnisse in den 32-Bit-Float-Akkumulator um.</span><span class="sxs-lookup"><span data-stu-id="c52d6-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="c52d6-123">Diese Anweisungen werden innerhalb einer einzelnen 32-Bit-weiten SIMD-Spur betrieben.</span><span class="sxs-lookup"><span data-stu-id="c52d6-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="c52d6-124">Die Eingaben sind 16-Bit-Mengen, die in denselben Bereich verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="c52d6-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="c52d6-125">Dies wird im featurebit mit niedriger Genauigkeit behandelt (gibt an, dass die systemeigene Hälfte und die kurze Unterstützung vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="c52d6-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="c52d6-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="c52d6-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="c52d6-127">Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Ziel Pixel darstellt, die bei jedem Aufruf des Pixel-Shaders geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c52d6-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="c52d6-128">Gültige Werte gehören zum Satz von Enumerationswerten [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="c52d6-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="c52d6-129">Dieser System Wert ist auf Plattformen verfügbar, die [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) oder höher sind.</span><span class="sxs-lookup"><span data-stu-id="c52d6-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="c52d6-130">Sie kann von höchstens einer der Scheitelpunkt-oder Geometrie-shaderphasen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c52d6-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="c52d6-131">Sie kann aus der Pixel-Shader-Stufe gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="c52d6-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="c52d6-132">Weitere Informationen finden Sie unter [Variable-Rate-Schattierung](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="c52d6-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>