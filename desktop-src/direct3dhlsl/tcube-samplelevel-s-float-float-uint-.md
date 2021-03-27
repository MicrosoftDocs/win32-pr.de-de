---
title: 'Samplelevel:: samplelevel (S, float, float, uint)-Funktion für texturecube'
description: 'Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück. | Samplelevel:: samplelevel (S, float, float, uint)-Funktion'
ms.assetid: DB27D8B9-11AB-4F0C-947A-9469BA565F41
keywords:
- Samplelevel-Funktion HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a31eaa2351b4758c29327aaa08ccee5ed0c3056c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104394289"
---
# <a name="samplelevelsamplelevelsfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="401bf-105">Samplelevel:: samplelevel (S, float, float, uint)-Funktion für texturecube</span><span class="sxs-lookup"><span data-stu-id="401bf-105">SampleLevel::SampleLevel(S,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="401bf-106">Führt eine Stichprobe für eine Textur auf der angegebenen MipMap-Ebene aus und gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="401bf-106">Samples a texture on the specified mipmap level and returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="401bf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="401bf-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="401bf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="401bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401bf-109">*S* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="401bf-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401bf-110">Typ: **samplerstate**</span><span class="sxs-lookup"><span data-stu-id="401bf-110">Type: **SamplerState**</span></span>

<span data-ttu-id="401bf-111">Ein [samplerzustand](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="401bf-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="401bf-112">Dies ist ein Objekt, das in einer Effekt Datei deklariert wurde, die Zustands Zuweisungen enthält.</span><span class="sxs-lookup"><span data-stu-id="401bf-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="401bf-113">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="401bf-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401bf-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="401bf-114">Type: **float**</span></span>

<span data-ttu-id="401bf-115">Texturkoordinaten</span><span class="sxs-lookup"><span data-stu-id="401bf-115">The texture coordinates.</span></span> <span data-ttu-id="401bf-116">Der Argumenttyp ist vom Textur Objekttyp abhängig.</span><span class="sxs-lookup"><span data-stu-id="401bf-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="401bf-117">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="401bf-117">Texture-Object Type</span></span>                    | <span data-ttu-id="401bf-118">Parametertyp</span><span class="sxs-lookup"><span data-stu-id="401bf-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="401bf-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="401bf-119">Texture1D</span></span>                              | <span data-ttu-id="401bf-120">float</span><span class="sxs-lookup"><span data-stu-id="401bf-120">float</span></span>          |
| <span data-ttu-id="401bf-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="401bf-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="401bf-122">float2</span><span class="sxs-lookup"><span data-stu-id="401bf-122">float2</span></span>         |
| <span data-ttu-id="401bf-123">Texture2DArray, Texture3D, texturecube</span><span class="sxs-lookup"><span data-stu-id="401bf-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="401bf-124">float3</span><span class="sxs-lookup"><span data-stu-id="401bf-124">float3</span></span>         |
| <span data-ttu-id="401bf-125">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="401bf-125">TextureCubeArray</span></span>                       | <span data-ttu-id="401bf-126">float4</span><span class="sxs-lookup"><span data-stu-id="401bf-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="401bf-127">*Lod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="401bf-127">*LOD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="401bf-128">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="401bf-128">Type: **float**</span></span>

<span data-ttu-id="401bf-129">\[in \] einer Zahl, die die MipMap-Ebene angibt.</span><span class="sxs-lookup"><span data-stu-id="401bf-129">\[in\] A number that specifies the mipmap level.</span></span> <span data-ttu-id="401bf-130">Wenn der Wert 0 (null) ist, wird MipMap Level 0 (größte Zuordnung) verwendet.</span><span class="sxs-lookup"><span data-stu-id="401bf-130">If the value is ≤ 0, mipmap level 0 (biggest map) is used.</span></span> <span data-ttu-id="401bf-131">Der Bruch Wert (falls angegeben) wird verwendet, um zwischen zwei MipMap-Ebenen zu interpolieren.</span><span class="sxs-lookup"><span data-stu-id="401bf-131">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="401bf-132">*Status* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="401bf-132">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="401bf-133">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="401bf-133">Type: **uint**</span></span>

<span data-ttu-id="401bf-134">Der Status des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="401bf-134">The status of the operation.</span></span> <span data-ttu-id="401bf-135">Sie können nicht direkt auf den Status zugreifen. übergeben Sie stattdessen den Status an die systeminterne [**checkaccessfullymapping**](checkaccessfullymapped.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="401bf-135">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="401bf-136">**Checkaccessfullymapping** gibt **true** zurück, wenn alle Werte aus dem entsprechenden **Sample**-, **Gather**-oder **Load** -Vorgang auf zugeordnete Kacheln in einer [gekachelten Ressource](/windows/desktop/direct3d11/direct3d-11-2-features)zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="401bf-136">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="401bf-137">Wenn Werte von einer nicht zugeordneten Kachel entnommen wurden, gibt **checkaccessfullymapping** den Wert **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="401bf-137">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401bf-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="401bf-138">Return value</span></span>

<span data-ttu-id="401bf-139">Typ: **[ **DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="401bf-139">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="401bf-140">Das Textur Format, bei dem es sich um einen der im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)aufgelisteten typisierten Werte handelt.</span><span class="sxs-lookup"><span data-stu-id="401bf-140">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="401bf-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="401bf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401bf-142">Samplelevel-Methoden</span><span class="sxs-lookup"><span data-stu-id="401bf-142">SampleLevel methods</span></span>](texturecube-samplelevel.md)
</dt> <dt>

[<span data-ttu-id="401bf-143">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="401bf-143">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
