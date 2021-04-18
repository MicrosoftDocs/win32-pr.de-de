---
description: Erstellt eine Ebene aus drei Punkten.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: D3DXPlaneFromPoints-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c537915c56cdbbfb33228b0c5a5ea3f2acc2baff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354347"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a><span data-ttu-id="5f140-103">D3DXPlaneFromPoints-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="5f140-103">D3DXPlaneFromPoints function (D3dx9math.h)</span></span>

<span data-ttu-id="5f140-104">Erstellt eine Ebene aus drei Punkten.</span><span class="sxs-lookup"><span data-stu-id="5f140-104">Constructs a plane from three points.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f140-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f140-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a><span data-ttu-id="5f140-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f140-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f140-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5f140-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f140-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f140-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="5f140-109">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="5f140-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f140-110">*pV1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f140-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f140-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f140-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f140-112">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f140-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="5f140-113">*pV2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f140-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f140-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f140-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f140-115">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f140-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="5f140-116">*pV3* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f140-116">*pV3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f140-117">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5f140-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5f140-118">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die einen der Punkte definiert, die zum Erstellen der Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f140-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining one of the points used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f140-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f140-119">Return value</span></span>

<span data-ttu-id="5f140-120">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="5f140-120">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="5f140-121">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die aus den angegebenen Punkten erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f140-121">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the given points.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f140-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f140-122">Remarks</span></span>

<span data-ttu-id="5f140-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5f140-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="5f140-124">Auf diese Weise kann die **D3DXPlaneFromPoints** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f140-124">In this way, the **D3DXPlaneFromPoints** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f140-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f140-125">Requirements</span></span>



| <span data-ttu-id="5f140-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f140-126">Requirement</span></span> | <span data-ttu-id="5f140-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5f140-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f140-128">Header</span><span class="sxs-lookup"><span data-stu-id="5f140-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5f140-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f140-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5f140-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5f140-130">Library</span></span><br/> | <dl> <span data-ttu-id="5f140-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f140-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f140-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f140-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f140-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="5f140-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5f140-134">**D3DXPlaneFromPointNormal**</span><span class="sxs-lookup"><span data-stu-id="5f140-134">**D3DXPlaneFromPointNormal**</span></span>](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




