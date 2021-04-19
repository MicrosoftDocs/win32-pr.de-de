---
description: Berechnet den Bezeichner.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: D3DXQuaternionExp-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b9cb5765e01c4fbbc6ab3785363425262ee491ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355801"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="ccebb-103">D3DXQuaternionExp-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="ccebb-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="ccebb-104">Berechnet den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="ccebb-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccebb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccebb-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="ccebb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccebb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccebb-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ccebb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccebb-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccebb-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ccebb-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ccebb-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ccebb-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ccebb-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccebb-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccebb-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ccebb-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ccebb-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccebb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ccebb-113">Return value</span></span>

<span data-ttu-id="ccebb-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ccebb-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ccebb-115">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Exponentialwert ist.</span><span class="sxs-lookup"><span data-stu-id="ccebb-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccebb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ccebb-116">Remarks</span></span>

<span data-ttu-id="ccebb-117">Diese Methode konvertiert eine reine Quaternion in eine Einheits Quaternion.</span><span class="sxs-lookup"><span data-stu-id="ccebb-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="ccebb-118">**D3DXQuaternionExp** erwartet eine reine Quaternion, bei der w in der Berechnung ignoriert wird (w = = 0).</span><span class="sxs-lookup"><span data-stu-id="ccebb-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="ccebb-119">Dabei ist v der Vektor Teil einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="ccebb-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="ccebb-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ccebb-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ccebb-121">Auf diese Weise kann die **D3DXQuaternionExp** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccebb-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ccebb-122">Die [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) -Methode kann auch zum Einrichten der Steuerungs Punkte einer Quaternion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ccebb-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="ccebb-123">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="ccebb-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccebb-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ccebb-124">Requirements</span></span>



| <span data-ttu-id="ccebb-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ccebb-125">Requirement</span></span> | <span data-ttu-id="ccebb-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ccebb-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccebb-127">Header</span><span class="sxs-lookup"><span data-stu-id="ccebb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ccebb-128"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccebb-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ccebb-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ccebb-129">Library</span></span><br/> | <dl> <span data-ttu-id="ccebb-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccebb-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ccebb-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccebb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccebb-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ccebb-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ccebb-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="ccebb-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="ccebb-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="ccebb-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




