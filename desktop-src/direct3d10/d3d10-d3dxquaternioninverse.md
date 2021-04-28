---
description: 'D3DXQuaternionInverse-Funktion (D3DX10Math.h): Konjugiert und normalisiert eine Quaternion.'
ms.assetid: 8e1bba91-8895-43a2-805b-1368050f8e82
title: D3DXQuaternionInverse-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 84816ac72841dcda0aef726535b7f5219d5467e4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103198"
---
# <a name="d3dxquaternioninverse-function-d3dx10mathh"></a><span data-ttu-id="f33f3-103">D3DXQuaternionInverse-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f33f3-103">D3DXQuaternionInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="f33f3-104">Konjugiert und renormalisiert eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="f33f3-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f33f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f33f3-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="f33f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f33f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f33f3-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f33f3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f3-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f33f3-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f33f3-109">Zeiger auf das [**D3DXQUATERNION-Steuerelement,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f33f3-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f33f3-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f33f3-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f33f3-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f33f3-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f33f3-112">Zeiger auf die D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="f33f3-112">Pointer to the source D3DXQUATERNION structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f33f3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f33f3-113">Return value</span></span>

<span data-ttu-id="f33f3-114">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f33f3-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f33f3-115">Zeiger auf eine D3DXQUATERNION-Struktur, die die umgekehrte Quaternion der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="f33f3-115">Pointer to a D3DXQUATERNION structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="f33f3-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f33f3-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="f33f3-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f33f3-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f33f3-118">Auf diese Weise kann die D3DXQuaternionInverse-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f33f3-118">In this way, the D3DXQuaternionInverse function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f33f3-119">Verwenden [**Sie D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f33f3-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f33f3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f33f3-120">Requirements</span></span>



| <span data-ttu-id="f33f3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f33f3-121">Requirement</span></span> | <span data-ttu-id="f33f3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f33f3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f33f3-123">Header</span><span class="sxs-lookup"><span data-stu-id="f33f3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f33f3-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f33f3-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f33f3-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f33f3-125">Library</span></span><br/> | <dl> <span data-ttu-id="f33f3-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f33f3-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f33f3-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f33f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f33f3-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f33f3-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
