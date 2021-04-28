---
description: 'D3DXQuaternionExp-Funktion (D3dx9math.h): Berechnet das Exponentielle.'
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: D3DXQuaternionExp-Funktion (D3dx9math.h)
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
ms.openlocfilehash: 30e48e21e2dc6af487f1fb076af3b3f2df57f9f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094098"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a><span data-ttu-id="e6783-103">D3DXQuaternionExp-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e6783-103">D3DXQuaternionExp function (D3dx9math.h)</span></span>

<span data-ttu-id="e6783-104">Berechnet den Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e6783-104">Calculates the exponential.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6783-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6783-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="e6783-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6783-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e6783-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6783-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6783-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e6783-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="e6783-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e6783-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e6783-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6783-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6783-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e6783-112">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="e6783-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6783-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6783-113">Return value</span></span>

<span data-ttu-id="e6783-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6783-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="e6783-115">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die exponentiell ist.</span><span class="sxs-lookup"><span data-stu-id="e6783-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the exponential.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6783-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6783-116">Remarks</span></span>

<span data-ttu-id="e6783-117">Diese Methode konvertiert eine reine Quaternion in eine Einheiten quaternion.</span><span class="sxs-lookup"><span data-stu-id="e6783-117">This method converts a pure quaternion to a unit quaternion.</span></span> <span data-ttu-id="e6783-118">**D3DXQuaternionExp** erwartet eine reine Quaternion, bei der w in der Berechnung ignoriert wird (w == 0).</span><span class="sxs-lookup"><span data-stu-id="e6783-118">**D3DXQuaternionExp** expects a pure quaternion, where w is ignored in the calculation (w == 0).</span></span>


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



<span data-ttu-id="e6783-119">Wobei v der Vektorteil einer Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="e6783-119">where v is the vector portion of a quaternion.</span></span>

<span data-ttu-id="e6783-120">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="e6783-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e6783-121">Auf diese Weise kann die **D3DXQuaternionExp-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6783-121">In this way, the **D3DXQuaternionExp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="e6783-122">Die [**D3DXQuaternionSquadSetup-Methode**](d3dxquaternionsquadsetup.md) kann auch zum Einrichten der Kontrollpunkte einer Quaternion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6783-122">The [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) method can also be used to set up the control points of a quaternion.</span></span>

<span data-ttu-id="e6783-123">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="e6783-123">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6783-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6783-124">Requirements</span></span>



| <span data-ttu-id="e6783-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6783-125">Requirement</span></span> | <span data-ttu-id="e6783-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e6783-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6783-127">Header</span><span class="sxs-lookup"><span data-stu-id="e6783-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e6783-128"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e6783-128"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e6783-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e6783-129">Library</span></span><br/> | <dl> <span data-ttu-id="e6783-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6783-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6783-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e6783-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6783-132">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="e6783-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e6783-133">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="e6783-133">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="e6783-134">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="e6783-134">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




