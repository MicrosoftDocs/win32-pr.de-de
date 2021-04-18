---
title: D2DGetInput-Funktion (D2d1effecthelpers. h)
description: Gibt die Farbe der Eingabe N an der eingabekoordinate zurück. Nur für einfache Eingaben verfügbar.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- D2DGetInput-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365600"
---
# <a name="d2dgetinput-function"></a><span data-ttu-id="3f68a-105">D2DGetInput-Funktion</span><span class="sxs-lookup"><span data-stu-id="3f68a-105">D2DGetInput function</span></span>

<span data-ttu-id="3f68a-106">Gibt die Farbe der Eingabe N an der eingabekoordinate zurück.</span><span class="sxs-lookup"><span data-stu-id="3f68a-106">Returns the color of input N at the input coordinate.</span></span> <span data-ttu-id="3f68a-107">Nur für einfache Eingaben verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f68a-107">Only available for simple inputs.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f68a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f68a-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a><span data-ttu-id="3f68a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f68a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f68a-110">*N* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f68a-110">*N* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f68a-111">Die Eingabe Nummer.</span><span class="sxs-lookup"><span data-stu-id="3f68a-111">The input number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f68a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f68a-112">Return value</span></span>

<span data-ttu-id="3f68a-113">Die-Funktion gibt ein **float4**-Wert zurück, der die RGBA-Farbe im Format inputn enthält.</span><span class="sxs-lookup"><span data-stu-id="3f68a-113">The function returns a **float4**, containing the RGBA color in the format INPUTN.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f68a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f68a-114">Remarks</span></span>

<span data-ttu-id="3f68a-115">Im folgenden Beispiel wird die Funktion gezeigt, die als Teil eines arithmetischen zusammengesetzten Effekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f68a-115">The following example shows the function being used as part of an arithmetic composite effect.</span></span>

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

<span data-ttu-id="3f68a-116">Ein weiteres Beispiel für die Verwendung dieser Funktion finden Sie auch in der Anmerkung zum [ \_ \_ Eintrag D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="3f68a-116">Also, refer to the remarks for [D2D\_PS\_ENTRY](d2d-ps-entry.md) for another example of the use of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f68a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f68a-117">Requirements</span></span>



| <span data-ttu-id="3f68a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f68a-118">Requirement</span></span> | <span data-ttu-id="3f68a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3f68a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f68a-120">Header</span><span class="sxs-lookup"><span data-stu-id="3f68a-120">Header</span></span><br/> | <dl> <span data-ttu-id="3f68a-121"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="3f68a-121"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="3f68a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3f68a-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="3f68a-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f68a-123"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="3f68a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f68a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f68a-125">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="3f68a-125">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="3f68a-126">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="3f68a-126">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





