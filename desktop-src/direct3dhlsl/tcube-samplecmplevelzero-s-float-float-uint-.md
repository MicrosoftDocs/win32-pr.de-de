---
title: 'Samplecmplevelzero:: samplecmplevelzero (S, float, float, uint)-Funktion für texturecube'
description: Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert. Gibt den Status des Vorgangs zurück. Für texturecube.
ms.assetid: FE40307D-B9BE-434F-A6EF-7CA3C5BC7D70
keywords:
- Samplecmplevelzero-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleCmpLevelZero
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff58c51919e575260c71f7b58d8f3d0fda6c1dd1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982701"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="5d007-106">Samplecmplevelzero:: samplecmplevelzero (S, float, float, uint)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="5d007-106">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="5d007-107">Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="5d007-107">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="5d007-108">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="5d007-108">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d007-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d007-109">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="5d007-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d007-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d007-111">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d007-111">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d007-112">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="5d007-112">Type: **SamplerState**</span></span>

<span data-ttu-id="5d007-113">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="5d007-113">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="5d007-114">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="5d007-114">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="5d007-115">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d007-115">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d007-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5d007-116">Type: **float**</span></span>

<span data-ttu-id="5d007-117">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="5d007-117">The texture coordinates.</span></span> <span data-ttu-id="5d007-118">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="5d007-118">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="5d007-119">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="5d007-119">Texture-Object Type</span></span>                    | <span data-ttu-id="5d007-120">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="5d007-120">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="5d007-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="5d007-121">Texture1D</span></span>                              | <span data-ttu-id="5d007-122">float</span><span class="sxs-lookup"><span data-stu-id="5d007-122">float</span></span>          |
| <span data-ttu-id="5d007-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="5d007-123">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="5d007-124">float2</span><span class="sxs-lookup"><span data-stu-id="5d007-124">float2</span></span>         |
| <span data-ttu-id="5d007-125">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="5d007-125">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="5d007-126">float3</span><span class="sxs-lookup"><span data-stu-id="5d007-126">float3</span></span>         |
| <span data-ttu-id="5d007-127">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="5d007-127">TextureCubeArray</span></span>                       | <span data-ttu-id="5d007-128">float4</span><span class="sxs-lookup"><span data-stu-id="5d007-128">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="5d007-129">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5d007-129">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d007-130">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="5d007-130">Type: **float**</span></span>

<span data-ttu-id="5d007-131">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5d007-131">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="5d007-132">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5d007-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d007-133">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="5d007-133">Type: **uint**</span></span>

<span data-ttu-id="5d007-134">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="5d007-134">The status of the operation.</span></span> <span data-ttu-id="5d007-135">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5d007-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="5d007-136">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="5d007-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="5d007-137">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5d007-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d007-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d007-138">Return value</span></span>

<span data-ttu-id="5d007-139">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="5d007-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="5d007-140">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="5d007-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="5d007-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d007-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d007-142">Samplecmplevelzero-Methoden</span><span class="sxs-lookup"><span data-stu-id="5d007-142">SampleCmpLevelZero methods</span></span>](texturecube-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="5d007-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="5d007-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
