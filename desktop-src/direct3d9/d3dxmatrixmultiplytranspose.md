---
description: Berechnet das übersetzte Produkt von zwei Matrizen.
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: D3DXMatrixMultiplyTranspose-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b599453ae108a5a8bab8ee896858760c85799948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363119"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="a4cf8-103">D3DXMatrixMultiplyTranspose-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a4cf8-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="a4cf8-104">Berechnet das übersetzte Produkt von zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4cf8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4cf8-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="a4cf8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4cf8-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a4cf8-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4cf8-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4cf8-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4cf8-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4cf8-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4cf8-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4cf8-111">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4cf8-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4cf8-112">Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4cf8-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4cf8-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4cf8-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4cf8-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4cf8-115">Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4cf8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4cf8-116">Return value</span></span>

<span data-ttu-id="a4cf8-117">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4cf8-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a4cf8-118">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Produkt von zwei Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4cf8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4cf8-119">Remarks</span></span>

<span data-ttu-id="a4cf8-120">Das Ergebnis ist die Umsetzung des Produkts von zwei Transformations Matrizen: Out = T (M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="a4cf8-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="a4cf8-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a4cf8-122">Auf diese Weise kann die **D3DXMatrixMultiplyTranspose** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="a4cf8-123">Diese Funktion ist nützlich, um Matrizen als Konstanten für Scheitelpunkt-und Pixel-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a4cf8-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4cf8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4cf8-124">Requirements</span></span>



| <span data-ttu-id="a4cf8-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4cf8-125">Requirement</span></span> | <span data-ttu-id="a4cf8-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a4cf8-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4cf8-127">Header</span><span class="sxs-lookup"><span data-stu-id="a4cf8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a4cf8-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4cf8-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4cf8-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4cf8-129">Library</span></span><br/> | <dl> <span data-ttu-id="a4cf8-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4cf8-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4cf8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4cf8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cf8-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a4cf8-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a4cf8-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="a4cf8-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="a4cf8-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="a4cf8-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




