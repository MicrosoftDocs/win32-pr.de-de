---
description: 'D3DXQuaternionNormalize-Funktion (D3DX10Math.h): Berechnet eine Einheitslängen-Quaternion.'
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: D3DXQuaternionNormalize-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6d031dfc63cb92d43a9cca27813c9425e2ff1acb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103138"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="352fa-103">D3DXQuaternionNormalize-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="352fa-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="352fa-104">Berechnet eine Einheitslängen-Quaternion.</span><span class="sxs-lookup"><span data-stu-id="352fa-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="352fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="352fa-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="352fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="352fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352fa-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="352fa-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="352fa-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="352fa-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352fa-109">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="352fa-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="352fa-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="352fa-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352fa-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="352fa-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352fa-112">Zeiger auf die D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="352fa-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="352fa-113">Return value</span></span>

<span data-ttu-id="352fa-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="352fa-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="352fa-115">Zeiger auf eine D3DXQUATERNION-Struktur, die der Normalität der Quaternion entspricht.</span><span class="sxs-lookup"><span data-stu-id="352fa-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="352fa-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="352fa-116">Remarks</span></span>

<span data-ttu-id="352fa-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="352fa-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="352fa-118">Auf diese Weise kann die D3DXQuaternionNormalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="352fa-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="352fa-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="352fa-119">Requirements</span></span>



| <span data-ttu-id="352fa-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="352fa-120">Requirement</span></span> | <span data-ttu-id="352fa-121">Wert</span><span class="sxs-lookup"><span data-stu-id="352fa-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="352fa-122">Header</span><span class="sxs-lookup"><span data-stu-id="352fa-122">Header</span></span><br/>  | <dl> <span data-ttu-id="352fa-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="352fa-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="352fa-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="352fa-124">Library</span></span><br/> | <dl> <span data-ttu-id="352fa-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="352fa-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="352fa-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="352fa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352fa-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="352fa-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
