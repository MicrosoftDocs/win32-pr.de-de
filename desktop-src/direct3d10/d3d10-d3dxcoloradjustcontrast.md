---
description: Passt den Kontrastwert einer Farbe an.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: D3DXColorAdjustContrast-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364378"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a><span data-ttu-id="8f9ae-103">D3DXColorAdjustContrast-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="8f9ae-103">D3DXColorAdjustContrast function (D3DX10Math.h)</span></span>

<span data-ttu-id="8f9ae-104">Passt den Kontrastwert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f9ae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f9ae-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="8f9ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f9ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f9ae-107">*Pout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f9ae-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9ae-108">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f9ae-108">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8f9ae-109">\[in, out- \] Zeiger auf ein [**D3DXCOLOR**](d3d10-d3dxcolor.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-109">\[in, out\] Pointer to a [**D3DXCOLOR**](d3d10-d3dxcolor.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f9ae-110">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f9ae-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9ae-111">Typ: **Konstanten [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="8f9ae-111">Type: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8f9ae-112">Zeiger auf eine Quell-D3DXCOLOR-Struktur.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-112">Pointer to a source D3DXCOLOR structure.</span></span>

</dd> <dt>

<span data-ttu-id="8f9ae-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f9ae-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f9ae-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f9ae-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f9ae-115">Kontrastwert.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-115">Contrast value.</span></span> <span data-ttu-id="8f9ae-116">Dieser Parameter interpoliert eine lineare Interpolation zwischen 50 Prozent grau und der Farbe "PC".</span><span class="sxs-lookup"><span data-stu-id="8f9ae-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="8f9ae-117">Es gibt keine Einschränkungen für den Wert von c.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-117">There are no limits on the value of c.</span></span> <span data-ttu-id="8f9ae-118">Wenn dieser Parameter 0 (null) ist, ist die zurückgegebene Farbe 50 Prozent grau.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="8f9ae-119">Wenn dieser Parameter 1 ist, entspricht die zurückgegebene Farbe der ursprünglichen Farbe.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f9ae-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f9ae-120">Return value</span></span>

<span data-ttu-id="8f9ae-121">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f9ae-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***</span></span>

<span data-ttu-id="8f9ae-122">Diese Funktion gibt einen Zeiger auf eine D3DXCOLOR-Struktur zurück, die das Ergebnis der Kontrast Anpassung ist.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-122">This function returns a pointer to a D3DXCOLOR structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f9ae-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f9ae-123">Remarks</span></span>

<span data-ttu-id="8f9ae-124">Der Alphakanal für die Eingabe wird unverändert in den Alpha-Ausgabekanal kopiert.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="8f9ae-125">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8f9ae-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8f9ae-127">Diese Funktion interpoliert die roten, grünen und blauen Farbkomponenten einer D3DXCOLOR-Struktur zwischen 50 Prozent grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-127">This function interpolates the red, green, and blue color components of a D3DXCOLOR structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="8f9ae-128">Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="8f9ae-129">Wenn c größer als 1 ist, wird der Kontrast erweitert.</span><span class="sxs-lookup"><span data-stu-id="8f9ae-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f9ae-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f9ae-130">Requirements</span></span>



| <span data-ttu-id="8f9ae-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f9ae-131">Requirement</span></span> | <span data-ttu-id="8f9ae-132">Wert</span><span class="sxs-lookup"><span data-stu-id="8f9ae-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9ae-133">Header</span><span class="sxs-lookup"><span data-stu-id="8f9ae-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8f9ae-134"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9ae-134"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8f9ae-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f9ae-135">Library</span></span><br/> | <dl> <span data-ttu-id="8f9ae-136"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f9ae-136"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f9ae-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f9ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9ae-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8f9ae-138">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
