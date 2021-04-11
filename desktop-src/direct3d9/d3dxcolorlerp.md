---
description: Verwendet die lineare interpolung, um einen Farbwert zu erstellen.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: D3DXColorLerp-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3521ee9e76aecd486093f903d336c08553e0e4ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870127"
---
# <a name="d3dxcolorlerp-function"></a><span data-ttu-id="29316-103">D3DXColorLerp-Funktion</span><span class="sxs-lookup"><span data-stu-id="29316-103">D3DXColorLerp function</span></span>

<span data-ttu-id="29316-104">Verwendet die lineare interpolung, um einen Farbwert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="29316-104">Uses linear interpolation to create a color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="29316-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="29316-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a><span data-ttu-id="29316-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="29316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29316-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="29316-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29316-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="29316-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="29316-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="29316-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="29316-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29316-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29316-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="29316-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="29316-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="29316-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29316-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29316-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29316-114">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="29316-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="29316-115">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="29316-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29316-116">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29316-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29316-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="29316-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="29316-118">-Parameter, der linear zwischen den Farben, pC1 und pC2, interpoliert und beide als 4D-Vektoren behandelt.</span><span class="sxs-lookup"><span data-stu-id="29316-118">Parameter that linearly interpolates between the colors, pC1 and pC2, treating them both as 4D vectors.</span></span> <span data-ttu-id="29316-119">Es gibt keine Einschränkungen für den Wert von s.</span><span class="sxs-lookup"><span data-stu-id="29316-119">There are no limits on the value of s.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29316-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29316-120">Return value</span></span>

<span data-ttu-id="29316-121">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="29316-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="29316-122">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die das Ergebnis der linearen interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="29316-122">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="29316-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29316-123">Remarks</span></span>

<span data-ttu-id="29316-124">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29316-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="29316-125">Auf diese Weise kann die **D3DXColorLerp** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29316-125">In this way, the **D3DXColorLerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="29316-126">Diese Funktion interpoliert die roten, grünen, blauen und Alpha Komponenten einer [**D3DXCOLOR**](d3dxcolor.md) -Struktur zwischen zwei Farben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="29316-126">This function interpolates the red, green, blue, and alpha components of a [**D3DXCOLOR**](d3dxcolor.md) structure between two colors, as shown in the following example.</span></span>


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



<span data-ttu-id="29316-127">Wenn Sie eine lineare Interpolation zwischen den Farben A und B durchführen und s 0 (null) ist, ist die resultierende Farbe ein. Wenn s den Wert 1 hat, ist die resultierende Farbe Color B.</span><span class="sxs-lookup"><span data-stu-id="29316-127">If you are linearly interpolating between the colors A and B, and s is 0, the resulting color is A. If s is 1, the resulting color is color B.</span></span>

## <a name="requirements"></a><span data-ttu-id="29316-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29316-128">Requirements</span></span>



| <span data-ttu-id="29316-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29316-129">Requirement</span></span> | <span data-ttu-id="29316-130">Wert</span><span class="sxs-lookup"><span data-stu-id="29316-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29316-131">Header</span><span class="sxs-lookup"><span data-stu-id="29316-131">Header</span></span><br/>  | <dl> <span data-ttu-id="29316-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="29316-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="29316-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="29316-133">Library</span></span><br/> | <dl> <span data-ttu-id="29316-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29316-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="29316-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29316-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29316-136">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="29316-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="29316-137">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="29316-137">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="29316-138">**D3DXColorNegative**</span><span class="sxs-lookup"><span data-stu-id="29316-138">**D3DXColorNegative**</span></span>](d3dxcolornegative.md)
</dt> <dt>

[<span data-ttu-id="29316-139">**D3DXColorScale**</span><span class="sxs-lookup"><span data-stu-id="29316-139">**D3DXColorScale**</span></span>](d3dxcolorscale.md)
</dt> </dl>

 

 
