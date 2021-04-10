---
description: Gibt die normalisierte Version eines 3D-Vektors zurück.
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: D3DXVec3Normalize-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870164"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="ad0b9-103">D3DXVec3Normalize-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="ad0b9-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="ad0b9-104">Gibt die normalisierte Version eines 3D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad0b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad0b9-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="ad0b9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad0b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad0b9-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad0b9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad0b9-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad0b9-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad0b9-109">Zeiger auf das [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad0b9-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad0b9-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad0b9-111">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ad0b9-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad0b9-112">Ein Zeiger auf die Quell-D3DXVECTOR3-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad0b9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad0b9-113">Return value</span></span>

<span data-ttu-id="ad0b9-114">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad0b9-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ad0b9-115">Zeiger auf eine D3DXVECTOR3-Struktur, die die normalisierte Version des angegebenen Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad0b9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad0b9-116">Remarks</span></span>

<span data-ttu-id="ad0b9-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ad0b9-118">Auf diese Weise kann die D3DXVec3Normalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ad0b9-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad0b9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad0b9-119">Requirements</span></span>



| <span data-ttu-id="ad0b9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad0b9-120">Requirement</span></span> | <span data-ttu-id="ad0b9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ad0b9-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0b9-122">Header</span><span class="sxs-lookup"><span data-stu-id="ad0b9-122">Header</span></span><br/> | <dl> <span data-ttu-id="ad0b9-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad0b9-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad0b9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad0b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0b9-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad0b9-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
