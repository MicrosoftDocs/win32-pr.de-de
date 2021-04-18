---
title: D2DGetScenePosition-Funktion (D2d1effecthelpers. h)
description: Gibt den Wert der Eingabe Szenen \_ Position zurück. Nur verfügbar, wenn \_ \_ für D2D \_ die Szenen Position in der Quelldatei deklariert ist.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- D2DGetScenePosition-Funktion Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365642"
---
# <a name="d2dgetsceneposition-function"></a><span data-ttu-id="281e4-105">D2DGetScenePosition-Funktion</span><span class="sxs-lookup"><span data-stu-id="281e4-105">D2DGetScenePosition function</span></span>

<span data-ttu-id="281e4-106">Gibt den Wert der Eingabe Szenen \_ Position zurück.</span><span class="sxs-lookup"><span data-stu-id="281e4-106">Returns the value of the input SCENE\_POSITION.</span></span> <span data-ttu-id="281e4-107">Nur verfügbar, wenn \_ \_ für D2D \_ die Szenen Position in der Quelldatei deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="281e4-107">Only available when D2D\_REQUIRES\_SCENE\_POSITION is declared in the source file.</span></span>

## <a name="syntax"></a><span data-ttu-id="281e4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="281e4-108">Syntax</span></span>

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a><span data-ttu-id="281e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="281e4-109">Parameters</span></span>

<span data-ttu-id="281e4-110">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="281e4-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="281e4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="281e4-111">Return value</span></span>

<span data-ttu-id="281e4-112">Die-Funktion gibt ein **float4** -Wert in der Format Szenen \_ Position zurück.</span><span class="sxs-lookup"><span data-stu-id="281e4-112">The function returns a **float4** in the format SCENE\_POSITION.</span></span>

## <a name="remarks"></a><span data-ttu-id="281e4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="281e4-113">Remarks</span></span>

<span data-ttu-id="281e4-114">Im folgenden Beispiel wird die Verwendung der-Funktion zum Erstellen eines Auflösungs Musters veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="281e4-114">The following example shows the use of the function in generating a dissolve pattern.</span></span>

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
}  
```

## <a name="requirements"></a><span data-ttu-id="281e4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="281e4-115">Requirements</span></span>



| <span data-ttu-id="281e4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="281e4-116">Requirement</span></span> | <span data-ttu-id="281e4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="281e4-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="281e4-118">Header</span><span class="sxs-lookup"><span data-stu-id="281e4-118">Header</span></span><br/> | <dl> <span data-ttu-id="281e4-119"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="281e4-119"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="281e4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="281e4-120">DLL</span></span><br/>    | <dl> <span data-ttu-id="281e4-121"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="281e4-121"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="281e4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="281e4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281e4-123">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="281e4-123">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="281e4-124">HLSL-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="281e4-124">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





