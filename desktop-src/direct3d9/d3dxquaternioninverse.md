---
description: 'D3DXQuaternionInverse-Funktion (D3dx9math.h): Konjugiert und normalisiert eine Quaternion.'
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: D3DXQuaternionInverse-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ebb2520efa3c7c78d98fd8b90ec1ba9615e9927
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094068"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="f546e-103">D3DXQuaternionInverse-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f546e-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="f546e-104">Konjugiert und renormalisiert eine Quaternion.</span><span class="sxs-lookup"><span data-stu-id="f546e-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="f546e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f546e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="f546e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f546e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f546e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f546e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f546e-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f546e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f546e-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f546e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f546e-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f546e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f546e-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f546e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f546e-112">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="f546e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f546e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f546e-113">Return value</span></span>

<span data-ttu-id="f546e-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f546e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f546e-115">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die die umgekehrte Quaternion der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="f546e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="f546e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f546e-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="f546e-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f546e-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f546e-118">Auf diese Weise kann die **D3DXQuaternionInverse-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f546e-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f546e-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f546e-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f546e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f546e-120">Requirements</span></span>



| <span data-ttu-id="f546e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f546e-121">Requirement</span></span> | <span data-ttu-id="f546e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f546e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f546e-123">Header</span><span class="sxs-lookup"><span data-stu-id="f546e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f546e-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f546e-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f546e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f546e-125">Library</span></span><br/> | <dl> <span data-ttu-id="f546e-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f546e-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f546e-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f546e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f546e-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f546e-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f546e-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="f546e-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="f546e-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="f546e-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




