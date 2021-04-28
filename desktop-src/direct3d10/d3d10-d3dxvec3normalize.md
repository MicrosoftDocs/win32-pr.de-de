---
description: 'D3DXVec3Normalize-Funktion (D3DX10Math.h): Gibt die normalisierte Version eines 3D-Vektors zurück.'
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: D3DXVec3Normalize-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108178"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="7e976-103">D3DXVec3Normalize-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="7e976-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="7e976-104">Gibt die normalisierte Version eines 3D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="7e976-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e976-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e976-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="7e976-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e976-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7e976-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e976-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e976-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7e976-109">Zeiger auf [**D3DXVECTOR3,**](d3d10-d3dxvector3.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7e976-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7e976-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7e976-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e976-111">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e976-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7e976-112">Zeiger auf die D3DXVECTOR3-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="7e976-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e976-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e976-113">Return value</span></span>

<span data-ttu-id="7e976-114">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="7e976-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="7e976-115">Zeiger auf eine D3DXVECTOR3-Struktur, die die normalisierte Version des angegebenen Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="7e976-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e976-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e976-116">Remarks</span></span>

<span data-ttu-id="7e976-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7e976-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="7e976-118">Auf diese Weise kann die D3DXVec3Normalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e976-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e976-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e976-119">Requirements</span></span>



| <span data-ttu-id="7e976-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e976-120">Requirement</span></span> | <span data-ttu-id="7e976-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7e976-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e976-122">Header</span><span class="sxs-lookup"><span data-stu-id="7e976-122">Header</span></span><br/> | <dl> <span data-ttu-id="7e976-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7e976-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e976-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7e976-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e976-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7e976-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
