---
description: 'D3DXColorAdjustContrast-Funktion (D3dx9math.h): Passt den Kontrastwert einer Farbe an.'
ms.assetid: be49c9c7-b625-4cbc-bd63-1d5766ae2dbb
title: D3DXColorAdjustContrast-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9dc9bb79d1ebbe536661347d76d13846dead6aa8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115878"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx9mathh"></a><span data-ttu-id="31ab6-103">D3DXColorAdjustContrast-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="31ab6-103">D3DXColorAdjustContrast function (D3dx9math.h)</span></span>

<span data-ttu-id="31ab6-104">Passt den Kontrastwert einer Farbe an.</span><span class="sxs-lookup"><span data-stu-id="31ab6-104">Adjusts the contrast value of a color.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ab6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31ab6-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     c
);
```



## <a name="parameters"></a><span data-ttu-id="31ab6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ab6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ab6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="31ab6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ab6-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="31ab6-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="31ab6-109">Zeiger auf eine [**D3DXCOLOR-Struktur,**](d3dxcolor.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="31ab6-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="31ab6-110">*pC* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="31ab6-110">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ab6-111">Typ: **const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="31ab6-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="31ab6-112">Zeiger auf eine [**D3DXCOLOR-Quellstruktur.**](d3dxcolor.md)</span><span class="sxs-lookup"><span data-stu-id="31ab6-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="31ab6-113">*c* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31ab6-113">*c* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31ab6-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31ab6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31ab6-115">Kontrastwert.</span><span class="sxs-lookup"><span data-stu-id="31ab6-115">Contrast value.</span></span> <span data-ttu-id="31ab6-116">Dieser Parameter interpoliert linear zwischen 15 Prozent Grau und der Farbe pC.</span><span class="sxs-lookup"><span data-stu-id="31ab6-116">This parameter linearly interpolates between fifty percent gray and the color, pC.</span></span> <span data-ttu-id="31ab6-117">Es gibt keine Grenzwerte für den Wert von c.</span><span class="sxs-lookup"><span data-stu-id="31ab6-117">There are not limits on the value of c.</span></span> <span data-ttu-id="31ab6-118">Wenn dieser Parameter 0 (null) ist, ist die zurückgegebene Farbe prozentgrau.</span><span class="sxs-lookup"><span data-stu-id="31ab6-118">If this parameter is zero, then the returned color is fifty percent gray.</span></span> <span data-ttu-id="31ab6-119">Wenn dieser Parameter 1 ist, ist die zurückgegebene Farbe die ursprüngliche Farbe.</span><span class="sxs-lookup"><span data-stu-id="31ab6-119">If this parameter is 1, then the returned color is the original color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ab6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31ab6-120">Return value</span></span>

<span data-ttu-id="31ab6-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="31ab6-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="31ab6-122">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR-Struktur**](d3dxcolor.md) zurück, die das Ergebnis der Kontrastanpassung ist.</span><span class="sxs-lookup"><span data-stu-id="31ab6-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the contrast adjustment.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ab6-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31ab6-123">Remarks</span></span>

<span data-ttu-id="31ab6-124">Der Eingabe-Alphakanal wird unverändert in den Alphakanal der Ausgabe kopiert.</span><span class="sxs-lookup"><span data-stu-id="31ab6-124">The input alpha channel is copied, unmodified, to the output alpha channel.</span></span>

<span data-ttu-id="31ab6-125">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="31ab6-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="31ab6-126">Auf diese Weise kann diese Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31ab6-126">In this way, this function can be used as a parameter for another function.</span></span>

<span data-ttu-id="31ab6-127">Diese Funktion interpoliert die Rot-, Grün- und Blaufarbkomponenten einer [**D3DXCOLOR-Struktur**](d3dxcolor.md) zwischen 10 Prozent Grau und einem angegebenen Kontrastwert, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="31ab6-127">This function interpolates the red, green, and blue color components of a [**D3DXCOLOR**](d3dxcolor.md) structure between fifty percent gray and a specified contrast value, as shown in the following example.</span></span>


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



<span data-ttu-id="31ab6-128">Wenn c größer als 0 und kleiner als 1 ist, wird der Kontrast verringert.</span><span class="sxs-lookup"><span data-stu-id="31ab6-128">If c is greater than 0 and less than 1, the contrast is decreased.</span></span> <span data-ttu-id="31ab6-129">Wenn c größer als 1 ist, wird der Kontrast erhöht.</span><span class="sxs-lookup"><span data-stu-id="31ab6-129">If c is greater than 1, the contrast is increased.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ab6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31ab6-130">Requirements</span></span>



| <span data-ttu-id="31ab6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31ab6-131">Requirement</span></span> | <span data-ttu-id="31ab6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="31ab6-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ab6-133">Header</span><span class="sxs-lookup"><span data-stu-id="31ab6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="31ab6-134"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="31ab6-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="31ab6-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31ab6-135">Library</span></span><br/> | <dl> <span data-ttu-id="31ab6-136"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="31ab6-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31ab6-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31ab6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ab6-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="31ab6-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="31ab6-139">**D3DXColorAdjustSaturation**</span><span class="sxs-lookup"><span data-stu-id="31ab6-139">**D3DXColorAdjustSaturation**</span></span>](d3dxcoloradjustsaturation.md)
</dt> </dl>

 

 
