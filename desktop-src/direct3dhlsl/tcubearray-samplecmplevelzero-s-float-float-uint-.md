---
title: 'Samplecmplevelzero:: samplecmplevelzero (S, float, float, uint)-Funktion für texturecubearray'
description: Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert und gibt dann den Status des Vorgangs zurück. Für texturecubearray.
ms.assetid: D73447C6-E77C-4027-B265-24F96C679357
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
ms.openlocfilehash: ac042bd2856aa69bbba1293fb91ff74d95c0de53
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762399"
---
# <a name="samplecmplevelzerosamplecmplevelzerosfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="7abaf-105">Samplecmplevelzero:: samplecmplevelzero (S, float, float, uint)-Funktion für texturecubearray</span><span class="sxs-lookup"><span data-stu-id="7abaf-105">SampleCmpLevelZero::SampleCmpLevelZero(S,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="7abaf-106">Vergleicht nur eine Textur auf MipMap-Ebene 0 und vergleicht das Ergebnis mit einem Vergleichswert.</span><span class="sxs-lookup"><span data-stu-id="7abaf-106">Samples a texture on mipmap level 0 only and compares the result to a comparison value.</span></span> <span data-ttu-id="7abaf-107">Gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="7abaf-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abaf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7abaf-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmpLevelZero(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="7abaf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7abaf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abaf-110">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7abaf-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abaf-111">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="7abaf-111">Type: **SamplerState**</span></span>

<span data-ttu-id="7abaf-112">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="7abaf-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="7abaf-113">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="7abaf-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="7abaf-114">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7abaf-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abaf-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="7abaf-115">Type: **float**</span></span>

<span data-ttu-id="7abaf-116">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="7abaf-116">The texture coordinates.</span></span> <span data-ttu-id="7abaf-117">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="7abaf-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="7abaf-118">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="7abaf-118">Texture-Object Type</span></span>                    | <span data-ttu-id="7abaf-119">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="7abaf-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="7abaf-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="7abaf-120">Texture1D</span></span>                              | <span data-ttu-id="7abaf-121">float</span><span class="sxs-lookup"><span data-stu-id="7abaf-121">float</span></span>          |
| <span data-ttu-id="7abaf-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="7abaf-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="7abaf-123">float2</span><span class="sxs-lookup"><span data-stu-id="7abaf-123">float2</span></span>         |
| <span data-ttu-id="7abaf-124">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="7abaf-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="7abaf-125">float3</span><span class="sxs-lookup"><span data-stu-id="7abaf-125">float3</span></span>         |
| <span data-ttu-id="7abaf-126">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="7abaf-126">TextureCubeArray</span></span>                       | <span data-ttu-id="7abaf-127">float4</span><span class="sxs-lookup"><span data-stu-id="7abaf-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="7abaf-128">*CompareValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7abaf-128">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abaf-129">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="7abaf-129">Type: **float**</span></span>

<span data-ttu-id="7abaf-130">Ein Gleit Komma Wert, der als Vergleichswert verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7abaf-130">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="7abaf-131">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7abaf-131">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7abaf-132">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="7abaf-132">Type: **uint**</span></span>

<span data-ttu-id="7abaf-133">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="7abaf-133">The status of the operation.</span></span> <span data-ttu-id="7abaf-134">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7abaf-134">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="7abaf-135">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="7abaf-135">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="7abaf-136">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="7abaf-136">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abaf-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7abaf-137">Return value</span></span>

<span data-ttu-id="7abaf-138">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="7abaf-138">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="7abaf-139">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="7abaf-139">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="7abaf-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7abaf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abaf-141">Samplecmplevelzero-Methoden</span><span class="sxs-lookup"><span data-stu-id="7abaf-141">SampleCmpLevelZero methods</span></span>](texturecubearray-samplecmplevelzero.md)
</dt> <dt>

[<span data-ttu-id="7abaf-142">**Texturecubearray**</span><span class="sxs-lookup"><span data-stu-id="7abaf-142">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
