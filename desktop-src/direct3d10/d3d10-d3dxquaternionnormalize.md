---
description: Berechnet eine Einheits Längen-Quaternion.
ms.assetid: 6735a632-64d7-4bc1-b63e-d0cd27f5a29b
title: D3DXQuaternionNormalize-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: e121ef4892c65a0f04acaa89d44d4a5a9090740e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219624"
---
# <a name="d3dxquaternionnormalize-function-d3dx10mathh"></a><span data-ttu-id="af350-103">D3DXQuaternionNormalize-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="af350-103">D3DXQuaternionNormalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="af350-104">Berechnet eine Einheits Längen-Quaternion.</span><span class="sxs-lookup"><span data-stu-id="af350-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="af350-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af350-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="af350-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="af350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af350-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="af350-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af350-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="af350-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="af350-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="af350-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="af350-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af350-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af350-111">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="af350-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="af350-112">Ein Zeiger auf die Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="af350-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af350-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af350-113">Return value</span></span>

<span data-ttu-id="af350-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="af350-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="af350-115">Zeiger auf eine D3DXQUATERNION-Struktur, die die normale der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="af350-115">Pointer to a D3DXQUATERNION structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="af350-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af350-116">Remarks</span></span>

<span data-ttu-id="af350-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="af350-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="af350-118">Auf diese Weise kann die D3DXQuaternionNormalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af350-118">In this way, the D3DXQuaternionNormalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="af350-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af350-119">Requirements</span></span>



| <span data-ttu-id="af350-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af350-120">Requirement</span></span> | <span data-ttu-id="af350-121">Wert</span><span class="sxs-lookup"><span data-stu-id="af350-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af350-122">Header</span><span class="sxs-lookup"><span data-stu-id="af350-122">Header</span></span><br/>  | <dl> <span data-ttu-id="af350-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="af350-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="af350-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af350-124">Library</span></span><br/> | <dl> <span data-ttu-id="af350-125"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af350-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af350-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af350-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af350-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="af350-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
