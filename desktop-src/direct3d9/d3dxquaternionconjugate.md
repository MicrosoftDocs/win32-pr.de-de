---
description: Gibt die konjugierte einer Quaternion zurück.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: D3DXQuaternionConjugate-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219600"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="7d5a1-103">D3DXQuaternionConjugate-Funktion</span><span class="sxs-lookup"><span data-stu-id="7d5a1-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="7d5a1-104">Gibt die konjugierte einer Quaternion zurück.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d5a1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="7d5a1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d5a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d5a1-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7d5a1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d5a1-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d5a1-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7d5a1-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7d5a1-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d5a1-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d5a1-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="7d5a1-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7d5a1-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d5a1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d5a1-113">Return value</span></span>

<span data-ttu-id="7d5a1-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d5a1-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="7d5a1-115">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die konjugierte der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5a1-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d5a1-116">Remarks</span></span>

<span data-ttu-id="7d5a1-117">Wenn eine Quaternion (x, y, z, w) angegeben wird, gibt die **D3DXQuaternionConjugate** -Funktion die Quaternion (-x,-y,-z, w) zurück.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="7d5a1-118">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7d5a1-119">Auf diese Weise kann die **D3DXQuaternionConjugate** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7d5a1-120">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="7d5a1-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d5a1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d5a1-121">Requirements</span></span>



| <span data-ttu-id="7d5a1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d5a1-122">Requirement</span></span> | <span data-ttu-id="7d5a1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7d5a1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5a1-124">Header</span><span class="sxs-lookup"><span data-stu-id="7d5a1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7d5a1-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d5a1-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7d5a1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d5a1-126">Library</span></span><br/> | <dl> <span data-ttu-id="7d5a1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d5a1-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7d5a1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d5a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5a1-129">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7d5a1-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7d5a1-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="7d5a1-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




