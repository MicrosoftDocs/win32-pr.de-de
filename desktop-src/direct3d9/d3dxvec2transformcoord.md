---
description: Transformiert einen 2D-Vektor durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.
ms.assetid: 0c0efdf8-77df-4f4a-86ce-89e11555f4dc
title: D3DXVec2TransformCoord-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc047075cd2f9f6aba6903f85ea6960e78e0ba1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357241"
---
# <a name="d3dxvec2transformcoord-function-d3dx9mathh"></a><span data-ttu-id="f5077-103">D3DXVec2TransformCoord-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f5077-103">D3DXVec2TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="f5077-104">Transformiert einen 2D-Vektor durch eine angegebene Matrix und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="f5077-104">Transforms a 2D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5077-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5077-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2TransformCoord(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="f5077-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5077-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5077-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f5077-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5077-108">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5077-108">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5077-109">Ein Zeiger auf die [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f5077-109">Pointer to the [**D3DXVECTOR2**](d3dxvector2.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f5077-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5077-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5077-111">Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5077-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5077-112">Ein Zeiger auf die Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f5077-112">Pointer to the source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f5077-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5077-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5077-114">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5077-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f5077-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f5077-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5077-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5077-116">Return value</span></span>

<span data-ttu-id="f5077-117">Typ: **[ **D3DXVECTOR2**](d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5077-117">Type: **[**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="f5077-118">Zeiger auf eine [**D3DXVECTOR2**](d3dxvector2.md) -Struktur, die der transformierte Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="f5077-118">Pointer to a [**D3DXVECTOR2**](d3dxvector2.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5077-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5077-119">Remarks</span></span>

<span data-ttu-id="f5077-120">Diese Funktion transformiert den Vektor, *PV* (x, y, 0, 1), durch die Matrix, *pm* und projiziert das Ergebnis zurück in w = 1.</span><span class="sxs-lookup"><span data-stu-id="f5077-120">This function transforms the vector, *pV* (x, y, 0, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="f5077-121">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f5077-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f5077-122">Auf diese Weise kann die **D3DXVec2TransformCoord** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5077-122">In this way, the **D3DXVec2TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5077-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5077-123">Requirements</span></span>



| <span data-ttu-id="f5077-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5077-124">Requirement</span></span> | <span data-ttu-id="f5077-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f5077-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5077-126">Header</span><span class="sxs-lookup"><span data-stu-id="f5077-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f5077-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5077-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f5077-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f5077-128">Library</span></span><br/> | <dl> <span data-ttu-id="f5077-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5077-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5077-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5077-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5077-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f5077-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f5077-132">**D3DXVec2Transform**</span><span class="sxs-lookup"><span data-stu-id="f5077-132">**D3DXVec2Transform**</span></span>](d3dxvec2transform.md)
</dt> <dt>

[<span data-ttu-id="f5077-133">**D3DXVec2TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="f5077-133">**D3DXVec2TransformNormal**</span></span>](d3dxvec2transformnormal.md)
</dt> </dl>

 

 




