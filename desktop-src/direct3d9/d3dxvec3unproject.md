---
description: 'D3DXVec3Unproject-Funktion (D3dx9math.h): Projiziert einen Vektor aus dem Bildschirmbereich in den Objektraum.'
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: D3DXVec3Unproject-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c3ea6ec1aa60f48589b10575e279bed81b2c94f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115558"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="83093-103">D3DXVec3Unproject-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="83093-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="83093-104">Projektiert einen Vektor aus dem Bildschirmbereich in den Objektraum.</span><span class="sxs-lookup"><span data-stu-id="83093-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="83093-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83093-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a><span data-ttu-id="83093-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83093-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83093-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="83093-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="83093-109">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="83093-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="83093-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83093-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="83093-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="83093-112">Zeiger auf die [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="83093-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="83093-113">*pViewport* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83093-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-114">Typ: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="83093-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="83093-115">Zeiger auf eine [**D3DVIEWPORT9-Struktur,**](d3dviewport9.md) die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="83093-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="83093-116">*pProjection* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83093-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-117">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="83093-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="83093-118">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Projektionsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="83093-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="83093-119">*pView* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83093-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-120">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="83093-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="83093-121">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Ansichtsmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="83093-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="83093-122">*pWorld* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="83093-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83093-123">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="83093-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="83093-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="83093-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83093-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83093-125">Return value</span></span>

<span data-ttu-id="83093-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="83093-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="83093-127">Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) bei der es sich um den Vektor handelt, der vom Bildschirmbereich in den Objektbereich projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="83093-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="83093-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83093-128">Remarks</span></span>

<span data-ttu-id="83093-129">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="83093-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="83093-130">Auf diese Weise kann die **D3DXVec3Unproject-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83093-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="83093-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83093-131">Requirements</span></span>



| <span data-ttu-id="83093-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83093-132">Requirement</span></span> | <span data-ttu-id="83093-133">Wert</span><span class="sxs-lookup"><span data-stu-id="83093-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83093-134">Header</span><span class="sxs-lookup"><span data-stu-id="83093-134">Header</span></span><br/>  | <dl> <span data-ttu-id="83093-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="83093-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="83093-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83093-136">Library</span></span><br/> | <dl> <span data-ttu-id="83093-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="83093-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83093-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83093-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83093-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="83093-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="83093-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="83093-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




