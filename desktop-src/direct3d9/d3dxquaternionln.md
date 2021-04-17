---
description: Berechnet den natürlichen Logarithmus.
ms.assetid: 73ca7d13-1e20-48fc-b0ed-0d3127d094a7
title: D3DXQuaternionLn-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b51fcc77da29216acd2bfc1c011a063014da5d69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531016"
---
# <a name="d3dxquaternionln-function-d3dx9mathh"></a><span data-ttu-id="bd0c2-103">D3DXQuaternionLn-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="bd0c2-103">D3DXQuaternionLn function (D3dx9math.h)</span></span>

<span data-ttu-id="bd0c2-104">Berechnet den natürlichen Logarithmus.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-104">Calculates the natural logarithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd0c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd0c2-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="bd0c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd0c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd0c2-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd0c2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd0c2-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd0c2-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bd0c2-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bd0c2-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bd0c2-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd0c2-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd0c2-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bd0c2-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd0c2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd0c2-113">Return value</span></span>

<span data-ttu-id="bd0c2-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd0c2-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="bd0c2-115">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die der natürliche Logarithmus ist.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the natural logarithm.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0c2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd0c2-116">Remarks</span></span>

<span data-ttu-id="bd0c2-117">Die **D3DXQuaternionLn** -Funktion funktioniert nur bei Einheiten Quaternionen.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-117">The **D3DXQuaternionLn** function works only for unit quaternions.</span></span>


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



<span data-ttu-id="bd0c2-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="bd0c2-119">Auf diese Weise kann die **D3DXQuaternionLn** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-119">In this way, the **D3DXQuaternionLn** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="bd0c2-120">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="bd0c2-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0c2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd0c2-121">Requirements</span></span>



| <span data-ttu-id="bd0c2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd0c2-122">Requirement</span></span> | <span data-ttu-id="bd0c2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bd0c2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0c2-124">Header</span><span class="sxs-lookup"><span data-stu-id="bd0c2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="bd0c2-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd0c2-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bd0c2-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd0c2-126">Library</span></span><br/> | <dl> <span data-ttu-id="bd0c2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd0c2-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd0c2-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd0c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0c2-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bd0c2-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bd0c2-130">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="bd0c2-130">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="bd0c2-131">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="bd0c2-131">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




