---
title: D2DGetInputCoordinate-Funktion (D2d1effecthelpers. h)
description: Gibt den Wert des eingegebenen texcoordn zurück. Nur für komplexe Eingaben verfügbar.
ms.assetid: 60125E23-53B3-45ED-89FE-684E79004F6B
keywords:
- D2DGetInputCoordinate-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetInputCoordinate
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5d9ee759de12bb8b017d582026dd5b5ca8c3fb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361465"
---
# <a name="d2dgetinputcoordinate-function"></a><span data-ttu-id="a5b03-105">D2DGetInputCoordinate-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5b03-105">D2DGetInputCoordinate function</span></span>

<span data-ttu-id="a5b03-106">Gibt den Wert des eingegebenen texcoordn zurück.</span><span class="sxs-lookup"><span data-stu-id="a5b03-106">Returns the value of the input TEXCOORDN.</span></span> <span data-ttu-id="a5b03-107">Nur für komplexe Eingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a5b03-107">Available only for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b03-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5b03-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInputCoordinate(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="a5b03-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b03-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5b03-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b03-111">Die Eingabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="a5b03-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b03-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5b03-112">Return value</span></span>

<span data-ttu-id="a5b03-113">Die-Funktion gibt ein **float4** im Format texcoordn zurück.</span><span class="sxs-lookup"><span data-stu-id="a5b03-113">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b03-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5b03-114">Remarks</span></span>

<span data-ttu-id="a5b03-115">Die von dieser Funktion zurückgegebene Koordinate ist in textraum.</span><span class="sxs-lookup"><span data-stu-id="a5b03-115">The coordinate returned by this function is in texel space.</span></span> <span data-ttu-id="a5b03-116">Ein Shader sollte keinerlei Abhängigkeiten davon annehmen, wie dieser Wert berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="a5b03-116">A shader shouldn't take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="a5b03-117">Es sollte nur verwendet werden, um eine Stichprobe der Ausgabe des Pixelshaders zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a5b03-117">It should use it only to sample the pixel shader's input.</span></span> <span data-ttu-id="a5b03-118">Weitere Informationen finden Sie unter [Hinzufügen eines Pixelshaders zu einer benutzerdefinierten Transformation](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span><span class="sxs-lookup"><span data-stu-id="a5b03-118">For more info, see [Adding a pixel shader to a custom transform](./custom-effects.md#adding-a-pixel-shader-to-a-custom-transform).</span></span>

<span data-ttu-id="a5b03-119">Das folgende Beispiel zeigt die-Funktion, die für einen Verschiebungs Zuordnungs Effekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a5b03-119">The following example shows the function used for a displacement map effect.</span></span>

``` syntax
float2 GetDisplacementOffset(float4 uv0, float4 uv1)  
{  
    // TODO: return the displacement offset 
}  
  
D2D_PS_ENTRY(DisplacementMapBilinear)  
{  
    const float4 coord0 = D2DGetInputCoordinate(0);  
    const float4 coord1 = D2DGetInputCoordinate(1);  
    return D2DSampleInput(0, GetDisplacementOffset(coord0, coord1) * coord0.zw + coord0.xy);  
}  
```

## <a name="requirements"></a><span data-ttu-id="a5b03-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5b03-120">Requirements</span></span>



| <span data-ttu-id="a5b03-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5b03-121">Requirement</span></span> | <span data-ttu-id="a5b03-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a5b03-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b03-123">Header</span><span class="sxs-lookup"><span data-stu-id="a5b03-123">Header</span></span><br/> | <dl> <span data-ttu-id="a5b03-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="a5b03-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="a5b03-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b03-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="a5b03-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b03-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="a5b03-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5b03-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b03-128">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="a5b03-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="a5b03-129">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="a5b03-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

