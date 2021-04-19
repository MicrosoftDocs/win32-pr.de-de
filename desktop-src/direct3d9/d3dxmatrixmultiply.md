---
description: Bestimmt das Produkt von zwei Matrizen.
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: D3DXMatrixMultiply-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea578f54d3f690f01d9280e840cb9ee039d0cdf0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350659"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="7a698-103">D3DXMatrixMultiply-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7a698-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="7a698-104">Bestimmt das Produkt von zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="7a698-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a698-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a698-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="7a698-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a698-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a698-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7a698-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a698-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a698-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a698-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7a698-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7a698-110">*pM1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a698-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a698-111">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a698-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a698-112">Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7a698-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7a698-113">*pM2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a698-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a698-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a698-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a698-115">Zeiger auf eine Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7a698-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a698-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a698-116">Return value</span></span>

<span data-ttu-id="7a698-117">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a698-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7a698-118">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Produkt von zwei Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="7a698-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a698-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a698-119">Remarks</span></span>

<span data-ttu-id="7a698-120">Das Ergebnis stellt die Transformation M1 dar, gefolgt von der Transformation m2 (out = M1 \* m2).</span><span class="sxs-lookup"><span data-stu-id="7a698-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="7a698-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a698-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7a698-122">Auf diese Weise kann die **D3DXMatrixMultiply** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a698-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a698-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a698-123">Requirements</span></span>



| <span data-ttu-id="7a698-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a698-124">Requirement</span></span> | <span data-ttu-id="7a698-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7a698-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a698-126">Header</span><span class="sxs-lookup"><span data-stu-id="7a698-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7a698-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a698-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7a698-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a698-128">Library</span></span><br/> | <dl> <span data-ttu-id="7a698-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a698-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7a698-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a698-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a698-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a698-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7a698-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="7a698-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




