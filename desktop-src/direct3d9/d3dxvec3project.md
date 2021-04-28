---
description: 'D3DXVec3Project-Funktion (D3dx9math.h): Projiziert einen 3D-Vektor aus dem Objektraum in den Bildschirmraum.'
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: D3DXVec3Project-Funktion (D3dx9math.h)
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
ms.openlocfilehash: a5a9abcb54c883d74bde831570b9df0b40fedfae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115648"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a><span data-ttu-id="3d3f7-103">D3DXVec3Project-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3d3f7-103">D3DXVec3Project function (D3dx9math.h)</span></span>

<span data-ttu-id="3d3f7-104">Projektet einen 3D-Vektor aus dem Objektbereich in den Bildschirmbereich.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-104">Projects a 3D vector from object space into screen space.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d3f7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d3f7-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3d3f7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d3f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d3f7-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3d3f7-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f7-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3d3f7-112">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="3d3f7-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f7-113">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-114">Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="3d3f7-115">Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f7-116">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-117">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3d3f7-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f7-119">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3d3f7-121">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="3d3f7-122">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3d3f7-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d3f7-123">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3d3f7-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d3f7-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d3f7-125">Return value</span></span>

<span data-ttu-id="3d3f7-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d3f7-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3d3f7-127">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um den Vektor handelt, der vom Objektbereich in den Bildschirmbereich projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from object space to screen space.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d3f7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d3f7-128">Remarks</span></span>

<span data-ttu-id="3d3f7-129">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3d3f7-130">Auf diese Weise kann die **D3DXVec3Project-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d3f7-130">In this way, the **D3DXVec3Project** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d3f7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d3f7-131">Requirements</span></span>



| <span data-ttu-id="3d3f7-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d3f7-132">Requirement</span></span> | <span data-ttu-id="3d3f7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="3d3f7-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d3f7-134">Header</span><span class="sxs-lookup"><span data-stu-id="3d3f7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="3d3f7-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3d3f7-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3d3f7-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d3f7-136">Library</span></span><br/> | <dl> <span data-ttu-id="3d3f7-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d3f7-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d3f7-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d3f7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d3f7-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d3f7-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3d3f7-140">**D3DXVec3Unproject**</span><span class="sxs-lookup"><span data-stu-id="3d3f7-140">**D3DXVec3Unproject**</span></span>](d3dxvec3unproject.md)
</dt> </dl>

 

 




