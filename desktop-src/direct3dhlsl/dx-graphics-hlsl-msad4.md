---
title: msad4
description: Vergleicht einen 4-Byte-Verweiswert und einen 8-Byte-Quellwert und sammelt einen Vektor von 4 Summen. Jede Summe entspricht der maskierten Summe absoluter Unterschiede einer anderen Byte Ausrichtung zwischen dem Verweis Wert und dem Quellwert.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104976968"
---
# <a name="msad4"></a><span data-ttu-id="cae58-105">msad4</span><span class="sxs-lookup"><span data-stu-id="cae58-105">msad4</span></span>

<span data-ttu-id="cae58-106">Vergleicht einen 4-Byte-Verweiswert und einen 8-Byte-Quellwert und sammelt einen Vektor von 4 Summen.</span><span class="sxs-lookup"><span data-stu-id="cae58-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="cae58-107">Jede Summe entspricht der maskierten Summe absoluter Unterschiede einer anderen Byte Ausrichtung zwischen dem Verweis Wert und dem Quellwert.</span><span class="sxs-lookup"><span data-stu-id="cae58-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="cae58-108">uint4 result = msad4 (uint-Referenz, uint2 Source, uint4 Accum);</span><span class="sxs-lookup"><span data-stu-id="cae58-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="cae58-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae58-110"><span id="reference"></span><span id="REFERENCE"></span>*Angabe*</span><span class="sxs-lookup"><span data-stu-id="cae58-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="cae58-111">\[im \] Verweis Array von 4 Bytes in einem **uint** -Wert.</span><span class="sxs-lookup"><span data-stu-id="cae58-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="cae58-112"><span id="source"></span><span id="SOURCE"></span>*Ausgangs*</span><span class="sxs-lookup"><span data-stu-id="cae58-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="cae58-113">\[im \] Quell Array von 8 Bytes in zwei **uint2** -Werten.</span><span class="sxs-lookup"><span data-stu-id="cae58-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="cae58-114"><span id="accum"></span><span id="ACCUM"></span>*Accum*</span><span class="sxs-lookup"><span data-stu-id="cae58-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="cae58-115">\[in \] einem Vektor von 4 Werten.</span><span class="sxs-lookup"><span data-stu-id="cae58-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="cae58-116">**msad4** fügt diesen Vektor der maskierten Summe absoluter Unterschiede der verschiedenen Byte Ausrichtungen zwischen dem Verweis Wert und dem Quellwert hinzu.</span><span class="sxs-lookup"><span data-stu-id="cae58-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae58-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cae58-117">Return Value</span></span>

<span data-ttu-id="cae58-118">Ein Vektor von 4 Summen.</span><span class="sxs-lookup"><span data-stu-id="cae58-118">A vector of 4 sums.</span></span> <span data-ttu-id="cae58-119">Jede Summe entspricht der maskierten Summe von absoluten Differenzen von verschiedenen Byteausrichtungen zwischen Verweiswert und Quellwert.</span><span class="sxs-lookup"><span data-stu-id="cae58-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="cae58-120">**msad4** enthält keinen Unterschied in der Summe, wenn dieser Unterschied maskiert ist (d. h., das Verweis Byte ist 0).</span><span class="sxs-lookup"><span data-stu-id="cae58-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="cae58-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae58-121">Remarks</span></span>

<span data-ttu-id="cae58-122">Um die intrinsische **msad4** -Funktion im Shader-Code zu verwenden, müssen Sie die [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) -Methode mit [**D3D11 \_ Feature \_ D3D11- \_ Optionen**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) aufrufen, um zu überprüfen, ob das Direct3D-Gerät die Funktion [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae58-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="cae58-123">Die systeminterne **msad4** -Funktion erfordert einen WDDM 1,2-Anzeigetreiber, und alle WDDM 1,2-Anzeigetreiber müssen **msad4** unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cae58-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="cae58-124">Wenn Ihre APP ein renderinggerät mit [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 oder 11,1 erstellt und das Kompilierungs Ziel Shader-Modell 5 oder höher ist, kann der HLSL-Quellcode die systeminterne Funktion **msad4** verwenden.</span><span class="sxs-lookup"><span data-stu-id="cae58-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="cae58-125">Rückgabewerte sind nur bis zu 65535-Werte genau.</span><span class="sxs-lookup"><span data-stu-id="cae58-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="cae58-126">Wenn Sie die systeminterne Funktion **msad4** mit Eingaben aufzurufen, die zu Rückgabe Werten größer als 65535 führen können, erzeugt **msad4** nicht definierte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="cae58-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="cae58-127">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="cae58-127">Minimum Shader Model</span></span>

<span data-ttu-id="cae58-128">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cae58-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cae58-129">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="cae58-129">Shader Model</span></span>                                                | <span data-ttu-id="cae58-130">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="cae58-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="cae58-131">Shadermodell 5 oder höher</span><span class="sxs-lookup"><span data-stu-id="cae58-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="cae58-132">ja</span><span class="sxs-lookup"><span data-stu-id="cae58-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="cae58-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cae58-133">Examples</span></span>

<span data-ttu-id="cae58-134">Im folgenden finden Sie eine Beispiel Ergebnisberechnung für **msad4**:</span><span class="sxs-lookup"><span data-stu-id="cae58-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="cae58-135">Im folgenden finden Sie ein Beispiel dafür, wie Sie **msad4** verwenden können, um in einem Puffer nach einem Verweis Muster zu suchen:</span><span class="sxs-lookup"><span data-stu-id="cae58-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="cae58-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cae58-136">Requirements</span></span>



| <span data-ttu-id="cae58-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae58-137">Requirement</span></span> | <span data-ttu-id="cae58-138">Wert</span><span class="sxs-lookup"><span data-stu-id="cae58-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="cae58-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae58-139">Minimum supported client</span></span><br/> | <span data-ttu-id="cae58-140">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cae58-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="cae58-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae58-141">Minimum supported server</span></span><br/> | <span data-ttu-id="cae58-142">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="cae58-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cae58-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cae58-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae58-144">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cae58-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

