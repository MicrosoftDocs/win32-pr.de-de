---
description: 'D3DXMatrixMultiply-Funktion (D3DX10Math.h): Bestimmt das Produkt zweier Matrizen.'
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: D3DXMatrixMultiply-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 89e103d441648643be0176ca34f72f6175c11213
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113128"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="9efc9-103">D3DXMatrixMultiply-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="9efc9-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="9efc9-104">Bestimmt das Produkt zweier Matrizen.</span><span class="sxs-lookup"><span data-stu-id="9efc9-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="9efc9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9efc9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="9efc9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9efc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9efc9-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9efc9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9efc9-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9efc9-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9efc9-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9efc9-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9efc9-110">*pM1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9efc9-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9efc9-111">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9efc9-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9efc9-112">Zeiger auf eine D3DXMATRIX-Quellstruktur (linke Seite).</span><span class="sxs-lookup"><span data-stu-id="9efc9-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="9efc9-113">*pM2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="9efc9-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9efc9-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9efc9-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9efc9-115">Zeiger auf eine D3DXMATRIX-Quellstruktur (rechte Seite).</span><span class="sxs-lookup"><span data-stu-id="9efc9-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9efc9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9efc9-116">Return value</span></span>

<span data-ttu-id="9efc9-117">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9efc9-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9efc9-118">Zeiger auf eine D3DXMATRIX-Struktur, die das Produkt zweier Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="9efc9-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="9efc9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9efc9-119">Remarks</span></span>

<span data-ttu-id="9efc9-120">Das Ergebnis stellt die Transformation M1 gefolgt von der Transformation M2 (Out = M1 \* M2) dar.</span><span class="sxs-lookup"><span data-stu-id="9efc9-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="9efc9-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9efc9-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9efc9-122">Auf diese Weise kann die D3DXMatrixMultiply-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9efc9-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9efc9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9efc9-123">Requirements</span></span>



| <span data-ttu-id="9efc9-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9efc9-124">Requirement</span></span> | <span data-ttu-id="9efc9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9efc9-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9efc9-126">Header</span><span class="sxs-lookup"><span data-stu-id="9efc9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9efc9-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9efc9-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9efc9-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9efc9-128">Library</span></span><br/> | <dl> <span data-ttu-id="9efc9-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9efc9-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9efc9-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9efc9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9efc9-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9efc9-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
