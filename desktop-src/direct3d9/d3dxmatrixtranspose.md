---
description: Gibt die Matrix zurück, die eine Matrix umgibt.
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: D3DXMatrixTranspose-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366435"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="d7da6-103">D3DXMatrixTranspose-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="d7da6-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="d7da6-104">Gibt die Matrix zurück, die eine Matrix umgibt.</span><span class="sxs-lookup"><span data-stu-id="d7da6-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7da6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7da6-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="d7da6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7da6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7da6-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d7da6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7da6-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7da6-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d7da6-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d7da6-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d7da6-110">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7da6-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7da6-111">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d7da6-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d7da6-112">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7da6-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7da6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7da6-113">Return value</span></span>

<span data-ttu-id="d7da6-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d7da6-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d7da6-115">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Matrix ist, die die Matrix umgibt.</span><span class="sxs-lookup"><span data-stu-id="d7da6-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7da6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7da6-116">Remarks</span></span>

<span data-ttu-id="d7da6-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7da6-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d7da6-118">Auf diese Weise kann die **D3DXMatrixTranspose** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7da6-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7da6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7da6-119">Requirements</span></span>



| <span data-ttu-id="d7da6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7da6-120">Requirement</span></span> | <span data-ttu-id="d7da6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d7da6-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7da6-122">Header</span><span class="sxs-lookup"><span data-stu-id="d7da6-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d7da6-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7da6-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d7da6-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7da6-124">Library</span></span><br/> | <dl> <span data-ttu-id="d7da6-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7da6-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7da6-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7da6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7da6-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d7da6-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




