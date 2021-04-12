---
description: Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: D3DXVec3Project-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c8198987b970fd6d79db3c73f715df4f0ac6981
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354697"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="838cb-103">D3DXVec3Project-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="838cb-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="838cb-104">Projiziert einen 3D-Vektor aus dem Objekt Raum in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="838cb-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="838cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="838cb-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="838cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="838cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="838cb-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="838cb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="838cb-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="838cb-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="838cb-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="838cb-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838cb-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="838cb-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="838cb-112">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="838cb-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="838cb-113">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838cb-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-114">Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="838cb-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="838cb-115">Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="838cb-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="838cb-116">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838cb-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-117">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="838cb-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="838cb-118">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="838cb-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="838cb-119">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838cb-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="838cb-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="838cb-121">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="838cb-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="838cb-122">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="838cb-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="838cb-123">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="838cb-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="838cb-124">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="838cb-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="838cb-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="838cb-125">Return value</span></span>

<span data-ttu-id="838cb-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="838cb-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="838cb-127">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, bei der es sich um den Vektor handelt, der vom Objekt Raum zum Bildschirmbereich projiziert</span><span class="sxs-lookup"><span data-stu-id="838cb-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="838cb-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="838cb-128">Remarks</span></span>

<span data-ttu-id="838cb-129">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="838cb-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="838cb-130">Auf diese Weise kann die **D3DXVec3Project** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="838cb-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="838cb-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="838cb-131">Requirements</span></span>



| <span data-ttu-id="838cb-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="838cb-132">Requirement</span></span> | <span data-ttu-id="838cb-133">Wert</span><span class="sxs-lookup"><span data-stu-id="838cb-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="838cb-134">Header</span><span class="sxs-lookup"><span data-stu-id="838cb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="838cb-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="838cb-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="838cb-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="838cb-136">Library</span></span><br/> | <dl> <span data-ttu-id="838cb-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="838cb-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="838cb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="838cb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="838cb-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="838cb-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="838cb-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="838cb-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




