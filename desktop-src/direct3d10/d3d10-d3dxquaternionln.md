---
description: Berechnet den natürlichen Logarithmus.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: D3DXQuaternionLn-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 07b081e0e2063d18ab8f2bb010e2b436c38df097
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365330"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a><span data-ttu-id="60cc2-103">D3DXQuaternionLn-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="60cc2-103">D3DXQuaternionLn function (D3DX10Math.h)</span></span>

<span data-ttu-id="60cc2-104">Berechnet den natürlichen Logarithmus.</span><span class="sxs-lookup"><span data-stu-id="60cc2-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="60cc2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60cc2-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="60cc2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60cc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60cc2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="60cc2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60cc2-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="60cc2-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60cc2-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="60cc2-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="60cc2-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60cc2-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60cc2-111">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="60cc2-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60cc2-112">Ein Zeiger auf die Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="60cc2-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60cc2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60cc2-113">Return value</span></span>

<span data-ttu-id="60cc2-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="60cc2-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60cc2-115">Zeiger auf eine D3DXQUATERNION-Struktur, die der natürliche Logarithmus ist.</span><span class="sxs-lookup"><span data-stu-id="60cc2-115">Pointer to a D3DXQUATERNION structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="60cc2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60cc2-116">Remarks</span></span>

<span data-ttu-id="60cc2-117">Die D3DXQuaternionLn-Funktion funktioniert nur bei Einheiten Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="60cc2-117">The D3DXQuaternionLn function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="60cc2-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60cc2-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="60cc2-119">Auf diese Weise kann die D3DXQuaternionLn-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60cc2-119">In this way, the D3DXQuaternionLn function can be used as a parameter for another function.</span></span>

<span data-ttu-id="60cc2-120">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="60cc2-120">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="60cc2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60cc2-121">Requirements</span></span>



| <span data-ttu-id="60cc2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60cc2-122">Requirement</span></span> | <span data-ttu-id="60cc2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="60cc2-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60cc2-124">Header</span><span class="sxs-lookup"><span data-stu-id="60cc2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="60cc2-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="60cc2-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="60cc2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60cc2-126">Library</span></span><br/> | <dl> <span data-ttu-id="60cc2-127"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60cc2-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60cc2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60cc2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60cc2-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="60cc2-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
