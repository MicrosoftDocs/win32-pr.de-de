---
title: D2DSampleInputAtOffset-Funktion (D2d1effecthelpers. h)
description: Stichproben Eingabe N bei einem Offset des Offsets von der eingabekoordinate. Nur für komplexe Eingaben verfügbar.
ms.assetid: 4A01264E-04E3-49BD-9EF8-7834D9B8B0B8
keywords:
- D2DSampleInputAtOffset-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtOffset
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7718f8f48ddfd316d1312dbdff3a5da1f45dfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354795"
---
# <a name="d2dsampleinputatoffset-function"></a><span data-ttu-id="ae8a7-105">D2DSampleInputAtOffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae8a7-105">D2DSampleInputAtOffset function</span></span>

<span data-ttu-id="ae8a7-106">Stichproben Eingabe N bei einem Offset des Offsets von der eingabekoordinate.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-106">Samples input N at an offset of offset from the input coordinate.</span></span> <span data-ttu-id="ae8a7-107">Nur für komplexe Eingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae8a7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae8a7-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtOffset(
  in uint N,
  in float2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="ae8a7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae8a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae8a7-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae8a7-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae8a7-111">Die Eingabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="ae8a7-112">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae8a7-112">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae8a7-113">Der UV-Offset.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-113">The uv offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae8a7-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae8a7-114">Return value</span></span>

<span data-ttu-id="ae8a7-115">Die-Funktion gibt ein **float4** im Format texcoordn zurück.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae8a7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae8a7-116">Remarks</span></span>

<span data-ttu-id="ae8a7-117">Im folgenden Beispiel wird die Funktion gezeigt, die als Teil einer Hervorhebungs-und Schatten Farbverlaufs Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae8a7-117">The following example shows the function being used as part of a highlighting and shadows gradient mask.</span></span>

``` syntax
  
D2D_PS_ENTRY(HighlightsAndShadowsGradientMask)  
{  
    MIN_TYPE(float4) blurred = D2DGetInput(0);  
  
    // Compute X and Y gradients 
    MIN_TYPE(float) dX1 = D2DSampleInputAtOffset(0, float2(1, 0));
    MIN_TYPE(float) dX2 = D2DSampleInputAtOffset(0, float2(-1, 0));
    MIN_TYPE(float) dY1 = D2DSampleInputAtOffset(0, float2(0, 1));
    MIN_TYPE(float) dY2 = D2DSampleInputAtOffset(0, float2(0, -1));
    
    // TODO: math to calculate shadow gradients

    // Return the value in the alpha channel.  
    blurred.a = // TODO: math to calculate blurred value
  
    return blurred;  
}  
```

## <a name="requirements"></a><span data-ttu-id="ae8a7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae8a7-118">Requirements</span></span>



| <span data-ttu-id="ae8a7-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae8a7-119">Requirement</span></span> | <span data-ttu-id="ae8a7-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ae8a7-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae8a7-121">Header</span><span class="sxs-lookup"><span data-stu-id="ae8a7-121">Header</span></span><br/> | <dl> <span data-ttu-id="ae8a7-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="ae8a7-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="ae8a7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ae8a7-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="ae8a7-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae8a7-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="ae8a7-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae8a7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae8a7-126">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="ae8a7-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="ae8a7-127">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="ae8a7-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





