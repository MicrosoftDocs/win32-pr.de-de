---
description: Konjugiert eine Quaternion und benennt Sie um.
ms.assetid: 25407a60-f7c0-4063-8d1d-2d6d03bdb217
title: D3DXQuaternionInverse-Funktion (D3dx9math. h)
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
ms.openlocfilehash: b2f830b7f8f797e4ed94eb22b4c2a05c3bd3e4cd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394217"
---
# <a name="d3dxquaternioninverse-function-d3dx9mathh"></a><span data-ttu-id="451ee-103">D3DXQuaternionInverse-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="451ee-103">D3DXQuaternionInverse function (D3dx9math.h)</span></span>

<span data-ttu-id="451ee-104">Konjugiert eine Quaternion und benennt Sie um.</span><span class="sxs-lookup"><span data-stu-id="451ee-104">Conjugates and renormalizes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="451ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="451ee-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionInverse(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="451ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="451ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451ee-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="451ee-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="451ee-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="451ee-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="451ee-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="451ee-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="451ee-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="451ee-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451ee-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="451ee-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="451ee-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="451ee-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451ee-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="451ee-113">Return value</span></span>

<span data-ttu-id="451ee-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="451ee-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="451ee-115">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die umgekehrte Quaternion der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="451ee-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the inverse quaternion of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="451ee-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="451ee-116">Remarks</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="451ee-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="451ee-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="451ee-118">Auf diese Weise kann die **D3DXQuaternionInverse** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="451ee-118">In this way, the **D3DXQuaternionInverse** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="451ee-119">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="451ee-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="451ee-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="451ee-120">Requirements</span></span>



| <span data-ttu-id="451ee-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="451ee-121">Requirement</span></span> | <span data-ttu-id="451ee-122">Wert</span><span class="sxs-lookup"><span data-stu-id="451ee-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="451ee-123">Header</span><span class="sxs-lookup"><span data-stu-id="451ee-123">Header</span></span><br/>  | <dl> <span data-ttu-id="451ee-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="451ee-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="451ee-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="451ee-125">Library</span></span><br/> | <dl> <span data-ttu-id="451ee-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="451ee-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="451ee-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="451ee-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451ee-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="451ee-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="451ee-129">**D3DXQuaternionConjugate**</span><span class="sxs-lookup"><span data-stu-id="451ee-129">**D3DXQuaternionConjugate**</span></span>](d3dxquaternionconjugate.md)
</dt> <dt>

[<span data-ttu-id="451ee-130">**D3DXQuaternionNormalize**</span><span class="sxs-lookup"><span data-stu-id="451ee-130">**D3DXQuaternionNormalize**</span></span>](d3dxquaternionnormalize.md)
</dt> </dl>

 

 




