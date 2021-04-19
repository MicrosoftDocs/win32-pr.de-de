---
description: Erstellt eine Ebene von einem Punkt und einem normalen.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: D3DXPlaneFromPointNormal-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8eeb8ea3a1725e0bf615be888d8e862c97730a2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364343"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a><span data-ttu-id="add72-103">D3DXPlaneFromPointNormal-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="add72-103">D3DXPlaneFromPointNormal function (D3dx9math.h)</span></span>

<span data-ttu-id="add72-104">Erstellt eine Ebene von einem Punkt und einem normalen.</span><span class="sxs-lookup"><span data-stu-id="add72-104">Constructs a plane from a point and a normal.</span></span>

## <a name="syntax"></a><span data-ttu-id="add72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="add72-105">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a><span data-ttu-id="add72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="add72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add72-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="add72-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="add72-108">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="add72-108">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="add72-109">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="add72-109">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="add72-110">*PPoint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add72-110">*pPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add72-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="add72-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="add72-112">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die den zum Erstellen der Ebene verwendeten Punkt definiert.</span><span class="sxs-lookup"><span data-stu-id="add72-112">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the point used to construct the plane.</span></span>

</dd> <dt>

<span data-ttu-id="add72-113">*pnormal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add72-113">*pNormal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add72-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="add72-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="add72-115">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das normale definiert, das zum Erstellen der Ebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="add72-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, defining the normal used to construct the plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add72-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="add72-116">Return value</span></span>

<span data-ttu-id="add72-117">Typ: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="add72-117">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="add72-118">Ein Zeiger auf die [**D3DXPLANE**](d3dxplane.md) -Struktur, die aus dem Punkt und der normalen erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="add72-118">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure constructed from the point and the normal.</span></span>

## <a name="remarks"></a><span data-ttu-id="add72-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="add72-119">Remarks</span></span>

<span data-ttu-id="add72-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="add72-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="add72-121">Auf diese Weise kann die **D3DXPlaneFromPointNormal** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="add72-121">In this way, the **D3DXPlaneFromPointNormal** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="add72-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="add72-122">Requirements</span></span>



| <span data-ttu-id="add72-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="add72-123">Requirement</span></span> | <span data-ttu-id="add72-124">Wert</span><span class="sxs-lookup"><span data-stu-id="add72-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="add72-125">Header</span><span class="sxs-lookup"><span data-stu-id="add72-125">Header</span></span><br/>  | <dl> <span data-ttu-id="add72-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="add72-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="add72-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="add72-127">Library</span></span><br/> | <dl> <span data-ttu-id="add72-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="add72-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="add72-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="add72-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add72-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="add72-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="add72-131">**D3DXPlaneFromPoints**</span><span class="sxs-lookup"><span data-stu-id="add72-131">**D3DXPlaneFromPoints**</span></span>](d3dxplanefrompoints.md)
</dt> </dl>

 

 




