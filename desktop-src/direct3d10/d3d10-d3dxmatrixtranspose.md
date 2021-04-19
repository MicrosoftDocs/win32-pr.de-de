---
description: Gibt die Matrix zurück, die eine Matrix umgibt.
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: D3DXMatrixTranspose-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 0ecc93a560e15b8f0abe4337b866efc292c9355e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370462"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="9859a-103">D3DXMatrixTranspose-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="9859a-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="9859a-104">Gibt die Matrix zurück, die eine Matrix umgibt.</span><span class="sxs-lookup"><span data-stu-id="9859a-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9859a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9859a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="9859a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9859a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9859a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9859a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9859a-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9859a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9859a-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9859a-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9859a-110">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9859a-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9859a-111">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="9859a-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9859a-112">Ein Zeiger auf die Quell-D3DXMATRIX-Struktur.</span><span class="sxs-lookup"><span data-stu-id="9859a-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9859a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9859a-113">Return value</span></span>

<span data-ttu-id="9859a-114">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9859a-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9859a-115">Ein Zeiger auf die D3DXMATRIX-Struktur, die die Matrix ist, die die Matrix umgibt.</span><span class="sxs-lookup"><span data-stu-id="9859a-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="9859a-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9859a-116">Remarks</span></span>

<span data-ttu-id="9859a-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9859a-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="9859a-118">Auf diese Weise kann die D3DXMatrixTranspose-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9859a-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9859a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9859a-119">Requirements</span></span>



| <span data-ttu-id="9859a-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9859a-120">Requirement</span></span> | <span data-ttu-id="9859a-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9859a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9859a-122">Header</span><span class="sxs-lookup"><span data-stu-id="9859a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9859a-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9859a-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="9859a-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9859a-124">Library</span></span><br/> | <dl> <span data-ttu-id="9859a-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9859a-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9859a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9859a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9859a-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9859a-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
