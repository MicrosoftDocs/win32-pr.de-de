---
description: Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.
ms.assetid: 9fd69cae-1d9c-4fae-9e15-8eb9950b4850
title: D3DXVec3Unproject-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 2bab9af4a2c88a3e3b3b7f342b6c7c9cc89ceb66
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355626"
---
# <a name="d3dxvec3unproject-function-d3dx9mathh"></a><span data-ttu-id="429e6-103">D3DXVec3Unproject-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="429e6-103">D3DXVec3Unproject function (D3dx9math.h)</span></span>

<span data-ttu-id="429e6-104">Projiziert einen Vektor aus dem Bildschirmbereich in den Objektbereich.</span><span class="sxs-lookup"><span data-stu-id="429e6-104">Projects a vector from screen space into object space.</span></span>

## <a name="syntax"></a><span data-ttu-id="429e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="429e6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="429e6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="429e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429e6-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="429e6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="429e6-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="429e6-109">Ein Zeiger auf die [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="429e6-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="429e6-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429e6-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-111">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="429e6-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="429e6-112">Ein Zeiger auf die Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="429e6-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="429e6-113">*pviewport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429e6-113">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-114">Typ: **Konstanten [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="429e6-114">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="429e6-115">Zeiger auf eine [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur, die den Viewport darstellt.</span><span class="sxs-lookup"><span data-stu-id="429e6-115">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, representing the viewport.</span></span>

</dd> <dt>

<span data-ttu-id="429e6-116">*pprojection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429e6-116">*pProjection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-117">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="429e6-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="429e6-118">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Projektions Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="429e6-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the projection matrix.</span></span>

</dd> <dt>

<span data-ttu-id="429e6-119">*PView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429e6-119">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="429e6-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="429e6-121">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Ansichts Matrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="429e6-121">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the view matrix.</span></span>

</dd> <dt>

<span data-ttu-id="429e6-122">*pworld* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="429e6-122">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429e6-123">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="429e6-123">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="429e6-124">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die die Weltmatrix darstellt.</span><span class="sxs-lookup"><span data-stu-id="429e6-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure, representing the world matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="429e6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="429e6-125">Return value</span></span>

<span data-ttu-id="429e6-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="429e6-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="429e6-127">Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, bei der es sich um den Vektor handelt, der vom Bildschirmbereich zum Objekt Raum projiziert</span><span class="sxs-lookup"><span data-stu-id="429e6-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the vector projected from screen space to object space.</span></span>

## <a name="remarks"></a><span data-ttu-id="429e6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="429e6-128">Remarks</span></span>

<span data-ttu-id="429e6-129">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="429e6-129">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="429e6-130">Auf diese Weise kann die **D3DXVec3Unproject** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="429e6-130">In this way, the **D3DXVec3Unproject** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="429e6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="429e6-131">Requirements</span></span>



| <span data-ttu-id="429e6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="429e6-132">Requirement</span></span> | <span data-ttu-id="429e6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="429e6-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="429e6-134">Header</span><span class="sxs-lookup"><span data-stu-id="429e6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="429e6-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="429e6-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="429e6-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="429e6-136">Library</span></span><br/> | <dl> <span data-ttu-id="429e6-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="429e6-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="429e6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="429e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429e6-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="429e6-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="429e6-140">**D3DXVec3Project**</span><span class="sxs-lookup"><span data-stu-id="429e6-140">**D3DXVec3Project**</span></span>](d3dxvec3project.md)
</dt> </dl>

 

 




