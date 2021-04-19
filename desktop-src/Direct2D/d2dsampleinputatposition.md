---
title: D2DSampleInputAtPosition-Funktion (D2d1effecthelpers. h)
description: Gibt eine Stichproben Eingabe N an der absoluten Szenen Position statt an eine Eingabe relative Position aus. Nur für komplexe Eingaben verfügbar.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- D2DSampleInputAtPosition-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354794"
---
# <a name="d2dsampleinputatposition-function"></a><span data-ttu-id="e6909-105">D2DSampleInputAtPosition-Funktion</span><span class="sxs-lookup"><span data-stu-id="e6909-105">D2DSampleInputAtPosition function</span></span>

<span data-ttu-id="e6909-106">Gibt eine Stichproben Eingabe N an der absoluten Szenen Position statt an eine Eingabe relative Position aus.</span><span class="sxs-lookup"><span data-stu-id="e6909-106">Samples input N at an absolute scene position, rather than an input-relative position.</span></span> <span data-ttu-id="e6909-107">Nur für komplexe Eingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6909-107">Only available for complex inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6909-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6909-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a><span data-ttu-id="e6909-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6909-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6909-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6909-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6909-111">Die Eingabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="e6909-111">The input number.</span></span>

</dd> <dt>

<span data-ttu-id="e6909-112">*UV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6909-112">*uv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6909-113">Die UV-Position.</span><span class="sxs-lookup"><span data-stu-id="e6909-113">The uv position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6909-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6909-114">Return value</span></span>

<span data-ttu-id="e6909-115">Die-Funktion gibt ein **float4** im Format texcoordn zurück.</span><span class="sxs-lookup"><span data-stu-id="e6909-115">The function returns a **float4**, in the format TEXCOORDN.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6909-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6909-116">Remarks</span></span>

<span data-ttu-id="e6909-117">Das folgende Beispiel zeigt die-Funktion, die in einem Zirkel Umbruch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e6909-117">The following example shows the function used in a circular wrap.</span></span>

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a><span data-ttu-id="e6909-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6909-118">Requirements</span></span>



| <span data-ttu-id="e6909-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6909-119">Requirement</span></span> | <span data-ttu-id="e6909-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e6909-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6909-121">Header</span><span class="sxs-lookup"><span data-stu-id="e6909-121">Header</span></span><br/> | <dl> <span data-ttu-id="e6909-122"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="e6909-122"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="e6909-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e6909-123">DLL</span></span><br/>    | <dl> <span data-ttu-id="e6909-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6909-124"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="e6909-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6909-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6909-126">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="e6909-126">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="e6909-127">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="e6909-127">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





