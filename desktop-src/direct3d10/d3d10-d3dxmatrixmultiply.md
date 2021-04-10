---
description: Bestimmt das Produkt von zwei Matrizen.
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: D3DXMatrixMultiply-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 5f07130c25ce9ef1c588309460e4e12e67bb2485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961732"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="60198-103">D3DXMatrixMultiply-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="60198-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="60198-104">Bestimmt das Produkt von zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="60198-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="60198-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60198-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="60198-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60198-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60198-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60198-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60198-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="60198-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60198-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="60198-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="60198-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60198-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60198-111">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="60198-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60198-112">Zeiger auf eine Quell-D3DXMATRIX-Struktur (auf der linken Seite).</span><span class="sxs-lookup"><span data-stu-id="60198-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="60198-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60198-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60198-114">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="60198-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60198-115">Zeiger auf eine Quell-D3DXMATRIX-Struktur (auf der rechten Seite).</span><span class="sxs-lookup"><span data-stu-id="60198-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60198-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60198-116">Return value</span></span>

<span data-ttu-id="60198-117">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="60198-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="60198-118">Zeiger auf eine D3DXMATRIX-Struktur, die das Produkt von zwei Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="60198-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="60198-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60198-119">Remarks</span></span>

<span data-ttu-id="60198-120">Das Ergebnis stellt die Transformation M1 dar, gefolgt von der Transformation m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="60198-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="60198-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60198-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="60198-122">Auf diese Weise kann die D3DXMatrixMultiply-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60198-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="60198-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60198-123">Requirements</span></span>



| <span data-ttu-id="60198-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60198-124">Requirement</span></span> | <span data-ttu-id="60198-125">Wert</span><span class="sxs-lookup"><span data-stu-id="60198-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60198-126">Header</span><span class="sxs-lookup"><span data-stu-id="60198-126">Header</span></span><br/>  | <dl> <span data-ttu-id="60198-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="60198-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="60198-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60198-128">Library</span></span><br/> | <dl> <span data-ttu-id="60198-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60198-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60198-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60198-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60198-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="60198-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
