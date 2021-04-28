---
description: 'D3DXVec4Normalize-Funktion (D3DX10Math.h): Gibt die normalisierte Version eines 4D-Vektors zurück.'
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: D3DXVec4Normalize-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102908"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="58a6b-103">D3DXVec4Normalize-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="58a6b-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="58a6b-104">Gibt die normalisierte Version eines 4D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="58a6b-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="58a6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58a6b-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="58a6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58a6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58a6b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="58a6b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="58a6b-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="58a6b-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="58a6b-109">Zeiger auf [**D3DXVECTOR4,**](d3d10-d3dxvector4.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="58a6b-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="58a6b-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="58a6b-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58a6b-111">Typ: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="58a6b-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="58a6b-112">Zeiger auf die D3DXVECTOR4-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="58a6b-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58a6b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58a6b-113">Return value</span></span>

<span data-ttu-id="58a6b-114">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="58a6b-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="58a6b-115">Zeiger auf eine D3DXVECTOR4-Struktur, die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="58a6b-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="58a6b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58a6b-116">Remarks</span></span>

<span data-ttu-id="58a6b-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="58a6b-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="58a6b-118">Auf diese Weise kann die D3DXVec4Normalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58a6b-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="58a6b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58a6b-119">Requirements</span></span>



| <span data-ttu-id="58a6b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58a6b-120">Requirement</span></span> | <span data-ttu-id="58a6b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="58a6b-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58a6b-122">Header</span><span class="sxs-lookup"><span data-stu-id="58a6b-122">Header</span></span><br/> | <dl> <span data-ttu-id="58a6b-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="58a6b-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58a6b-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58a6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58a6b-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="58a6b-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
