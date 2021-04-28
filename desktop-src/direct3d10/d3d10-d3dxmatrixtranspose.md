---
description: 'D3DXMatrixTranspose-Funktion (D3DX10Math.h): Gibt die Matrixübersetzung einer Matrix zurück.'
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: D3DXMatrixTranspose-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108858"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="2fc27-103">D3DXMatrixTranspose-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="2fc27-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="2fc27-104">Gibt die Matrix transponieren einer Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="2fc27-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fc27-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2fc27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc27-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2fc27-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc27-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fc27-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2fc27-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2fc27-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2fc27-110">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2fc27-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc27-111">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2fc27-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2fc27-112">Zeiger auf die D3DXMATRIX-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="2fc27-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc27-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2fc27-113">Return value</span></span>

<span data-ttu-id="2fc27-114">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fc27-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2fc27-115">Zeiger auf die D3DXMATRIX-Struktur, die die Matrix-Transponierung der Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="2fc27-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fc27-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fc27-116">Remarks</span></span>

<span data-ttu-id="2fc27-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2fc27-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2fc27-118">Auf diese Weise kann die D3DXMatrixTranspose-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc27-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc27-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fc27-119">Requirements</span></span>



| <span data-ttu-id="2fc27-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2fc27-120">Requirement</span></span> | <span data-ttu-id="2fc27-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2fc27-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc27-122">Header</span><span class="sxs-lookup"><span data-stu-id="2fc27-122">Header</span></span><br/>  | <dl> <span data-ttu-id="2fc27-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2fc27-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2fc27-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2fc27-124">Library</span></span><br/> | <dl> <span data-ttu-id="2fc27-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fc27-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2fc27-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fc27-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc27-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2fc27-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
