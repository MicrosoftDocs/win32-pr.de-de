---
title: D2DSampleInput-Funktion (D2d1effecthelpers. h)
description: Stichproben Eingabe N an der Position-UV. Nur für komplexe Eingaben verfügbar.
ms.assetid: 8C1E3B23-D05B-4FCC-B32F-A5870A7C3FEF
keywords:
- D2DSampleInput-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5929e9c113e5fa9a7c8a72003357b280a810e49e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370820"
---
# <a name="d2dsampleinput-function"></a><span data-ttu-id="84c24-105">D2DSampleInput-Funktion</span><span class="sxs-lookup"><span data-stu-id="84c24-105">D2DSampleInput function</span></span>

<span data-ttu-id="84c24-106">Stichproben Eingabe N an der Position-UV.</span><span class="sxs-lookup"><span data-stu-id="84c24-106">Samples input N at position uv.</span></span> <span data-ttu-id="84c24-107">Nur für komplexe Eingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="84c24-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="84c24-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInput(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="84c24-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="84c24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c24-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84c24-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c24-111">Die Eingabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="84c24-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="84c24-112">*UV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84c24-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c24-113">Die UV-Position.</span><span class="sxs-lookup"><span data-stu-id="84c24-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c24-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84c24-114">Return value</span></span>

<span data-ttu-id="84c24-115">Die-Funktion gibt ein **float4** im Format texcoordn zurück.</span><span class="sxs-lookup"><span data-stu-id="84c24-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c24-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84c24-116">Remarks</span></span>

<span data-ttu-id="84c24-117">Das folgende Beispiel zeigt die-Funktion, die zum Berechnen von Oberflächen normalen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="84c24-117">The following example shows the function being used to calculate surface normals.</span></span>

``` syntax
   
float3 CalculateSurfaceNormal(TAPARGS)  
{  
    float3 normal = float3(0, 0, 1.0);  
  
    // unrolled loop  
    normal.xy += tap1.zw * D2DSampleInput(0, tap1.xy).a;  
    normal.xy += tap2.zw * D2DSampleInput(0, tap2.xy).a;  
    normal.xy += tap3.zw * D2DSampleInput(0, tap3.xy).a;  
    normal.xy += tap4.zw * D2DSampleInput(0, tap4.xy).a;  
    normal.xy += tap5.zw * D2DSampleInput(0, tap5.xy).a;  
    normal.xy += tap6.zw * D2DSampleInput(0, tap6.xy).a;  
  
    normal = normalize(normal);  
      
    return normal;  
}  
```

## <a name="requirements"></a><span data-ttu-id="84c24-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84c24-118">Requirements</span></span>



| <span data-ttu-id="84c24-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84c24-119">Requirement</span></span> | <span data-ttu-id="84c24-120">Wert</span><span class="sxs-lookup"><span data-stu-id="84c24-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c24-121">Header</span><span class="sxs-lookup"><span data-stu-id="84c24-121">Header</span></span><br/> | <dl> <span data-ttu-id="84c24-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="84c24-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="84c24-123">DLL</span><span class="sxs-lookup"><span data-stu-id="84c24-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="84c24-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84c24-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="84c24-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84c24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c24-126">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="84c24-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="84c24-127">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="84c24-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





