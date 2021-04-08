---
description: Berechnet den Bezeichner.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: D3DXQuaternionExp-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d00292cc073679e3e90c2470630ba1851d0d3cd8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762174"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a><span data-ttu-id="bb575-103">D3DXQuaternionExp-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bb575-103">D3DXQuaternionExp function (D3DX10Math.h)</span></span>

<span data-ttu-id="bb575-104">Berechnet den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="bb575-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb575-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb575-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="bb575-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb575-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bb575-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb575-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb575-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bb575-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bb575-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb575-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb575-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb575-111">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb575-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bb575-112">Ein Zeiger auf die Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb575-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb575-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb575-113">Return value</span></span>

<span data-ttu-id="bb575-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb575-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bb575-115">Zeiger auf eine D3DXQUATERNION-Struktur, die das Exponentialwert ist.</span><span class="sxs-lookup"><span data-stu-id="bb575-115">Pointer to a D3DXQUATERNION structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb575-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb575-116">Remarks</span></span>

<span data-ttu-id="bb575-117">Diese Methode konvertiert eine reine Quaternion in eine Einheits Quaternion.</span><span class="sxs-lookup"><span data-stu-id="bb575-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="bb575-118">D3DXQuaternionExp erwartet eine reine Quaternion, bei der w in der Berechnung ignoriert wird (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="bb575-118">D3DXQuaternionExp expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="bb575-119">Dabei ist v der Vektor Teil einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="bb575-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="bb575-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bb575-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bb575-121">Auf diese Weise kann die D3DXQuaternionExp-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb575-121">In this way, the D3DXQuaternionExp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bb575-122">Die [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) -Methode kann auch zum Einrichten der Steuerungs Punkte einer Quaternion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb575-122">The [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="bb575-123">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="bb575-123">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb575-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb575-124">Requirements</span></span>



| <span data-ttu-id="bb575-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb575-125">Requirement</span></span> | <span data-ttu-id="bb575-126">Wert</span><span class="sxs-lookup"><span data-stu-id="bb575-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb575-127">Header</span><span class="sxs-lookup"><span data-stu-id="bb575-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bb575-128"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb575-128"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb575-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb575-129">Library</span></span><br/> | <dl> <span data-ttu-id="bb575-130"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb575-130"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb575-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb575-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb575-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bb575-132">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
