---
description: 'D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h): Berechnet das transponierte Produkt zweier Matrizen.'
ms.assetid: 3db4138c-407c-47b5-b8b9-04af8771e98e
title: D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiplyTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fcf3d5578aa6e2ad13bd3f91dfd2206d6eaf0b13
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103417"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx10mathh"></a><span data-ttu-id="8ca61-103">D3DXMatrixMultiplyTranspose-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8ca61-103">D3DXMatrixMultiplyTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="8ca61-104">Berechnet das transponierte Produkt zweier Matrizen.</span><span class="sxs-lookup"><span data-stu-id="8ca61-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ca61-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="8ca61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ca61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca61-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ca61-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca61-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca61-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ca61-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8ca61-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8ca61-110">*pM1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ca61-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca61-111">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ca61-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ca61-112">Zeiger auf eine D3DXMATRIX-Quellstruktur (linke Seite).</span><span class="sxs-lookup"><span data-stu-id="8ca61-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="8ca61-113">*pM2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8ca61-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca61-114">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8ca61-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ca61-115">Zeiger auf eine D3DXMATRIX-Quellstruktur (rechte Seite).</span><span class="sxs-lookup"><span data-stu-id="8ca61-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca61-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ca61-116">Return value</span></span>

<span data-ttu-id="8ca61-117">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ca61-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8ca61-118">Zeiger auf eine D3DXMATRIX-Struktur, die das Produkt zweier Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="8ca61-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca61-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ca61-119">Remarks</span></span>

<span data-ttu-id="8ca61-120">Das Ergebnis ist die transponierte des Produkts von zwei Transformationsmatrizen, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="8ca61-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="8ca61-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ca61-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8ca61-122">Auf diese Weise kann die D3DXMatrixMultiplyTranspose-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ca61-122">In this way, the D3DXMatrixMultiplyTranspose function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8ca61-123">Diese Funktion ist nützlich, um Matrizen als Konstanten für Vertex- und Pixel-Shader festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ca61-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca61-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ca61-124">Requirements</span></span>



| <span data-ttu-id="8ca61-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ca61-125">Requirement</span></span> | <span data-ttu-id="8ca61-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8ca61-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca61-127">Header</span><span class="sxs-lookup"><span data-stu-id="8ca61-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8ca61-128"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca61-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8ca61-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ca61-129">Library</span></span><br/> | <dl> <span data-ttu-id="8ca61-130"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ca61-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ca61-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8ca61-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca61-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8ca61-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
