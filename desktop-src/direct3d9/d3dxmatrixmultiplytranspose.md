---
description: 'D3DXMatrixMultiplyTranspose-Funktion (D3dx9math.h): Berechnet das transponierte Produkt aus zwei Matrizen.'
ms.assetid: 43927500-9413-41a4-a6ee-974d85dd1054
title: D3DXMatrixMultiplyTranspose-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 87aaa45e7a7a16884d17ab340f0bf1efeccd93bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107538"
---
# <a name="d3dxmatrixmultiplytranspose-function-d3dx9mathh"></a><span data-ttu-id="8bc7a-103">D3DXMatrixMultiplyTranspose-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-103">D3DXMatrixMultiplyTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="8bc7a-104">Berechnet das transponierte Produkt aus zwei Matrizen.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-104">Calculates the transposed product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bc7a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiplyTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="8bc7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bc7a-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8bc7a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc7a-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8bc7a-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8bc7a-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8bc7a-110">*pM1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8bc7a-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc7a-111">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8bc7a-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8bc7a-112">Zeiger auf eine [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8bc7a-113">*pM2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8bc7a-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bc7a-114">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="8bc7a-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8bc7a-115">Zeiger auf eine [**D3DXMATRIX-Quellstruktur.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="8bc7a-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bc7a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8bc7a-116">Return value</span></span>

<span data-ttu-id="8bc7a-117">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8bc7a-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8bc7a-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Produkt zweier Matrizen ist.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc7a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8bc7a-119">Remarks</span></span>

<span data-ttu-id="8bc7a-120">Das Ergebnis ist die transponierte des Produkts von zwei Transformationsmatrizen, Out = T(M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="8bc7a-120">The result is the transposed of the product of two transformation matrices, Out = T(M1\*M2).</span></span>

<span data-ttu-id="8bc7a-121">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8bc7a-122">Auf diese Weise kann die **D3DXMatrixMultiplyTranspose-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-122">In this way, the **D3DXMatrixMultiplyTranspose** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8bc7a-123">Diese Funktion ist nützlich, um Matrizen als Konstanten für Vertex- und Pixel-Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8bc7a-123">This function is useful to set matrices as constants for vertex and pixel shaders.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bc7a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bc7a-124">Requirements</span></span>



| <span data-ttu-id="8bc7a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8bc7a-125">Requirement</span></span> | <span data-ttu-id="8bc7a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8bc7a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bc7a-127">Header</span><span class="sxs-lookup"><span data-stu-id="8bc7a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="8bc7a-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8bc7a-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8bc7a-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8bc7a-129">Library</span></span><br/> | <dl> <span data-ttu-id="8bc7a-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bc7a-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8bc7a-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8bc7a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bc7a-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8bc7a-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8bc7a-133">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="8bc7a-133">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> <dt>

[<span data-ttu-id="8bc7a-134">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="8bc7a-134">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




