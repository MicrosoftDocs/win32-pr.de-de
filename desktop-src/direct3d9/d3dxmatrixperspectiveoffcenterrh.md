---
description: Erstellt eine angepasste, rechts übergebene perspektivische Projektions Matrix.
ms.assetid: e6826e46-fc80-41fa-b0d8-45b6797df76f
title: D3DXMatrixPerspectiveOffCenterRH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c4f211c6f57f60f8399fb5639edd07c3fc02377
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219634"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx9mathh"></a><span data-ttu-id="c626b-103">D3DXMatrixPerspectiveOffCenterRH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c626b-103">D3DXMatrixPerspectiveOffCenterRH function (D3dx9math.h)</span></span>

<span data-ttu-id="c626b-104">Erstellt eine angepasste, rechts übergebene perspektivische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="c626b-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c626b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c626b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="c626b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c626b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c626b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c626b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c626b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c626b-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c626b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-112">Minimaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-115">Maximaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-118">Minimaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-121">Maximaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c626b-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c626b-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c626b-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c626b-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c626b-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c626b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c626b-128">Return value</span></span>

<span data-ttu-id="c626b-129">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c626b-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c626b-130">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die eine angepasste, rechts übergebene perspektivische Projektions Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="c626b-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c626b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c626b-131">Remarks</span></span>

<span data-ttu-id="c626b-132">Alle Parameter der **D3DXMatrixPerspectiveOffCenterRH** -Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="c626b-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterRH** function are distances in camera space.</span></span> <span data-ttu-id="c626b-133">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c626b-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c626b-134">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c626b-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c626b-135">Auf diese Weise kann die **D3DXMatrixPerspectiveOffCenterRH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c626b-135">In this way, the **D3DXMatrixPerspectiveOffCenterRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c626b-136">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c626b-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="c626b-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c626b-137">Requirements</span></span>



| <span data-ttu-id="c626b-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c626b-138">Requirement</span></span> | <span data-ttu-id="c626b-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c626b-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c626b-140">Header</span><span class="sxs-lookup"><span data-stu-id="c626b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c626b-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c626b-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c626b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c626b-142">Library</span></span><br/> | <dl> <span data-ttu-id="c626b-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c626b-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c626b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c626b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c626b-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c626b-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c626b-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="c626b-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="c626b-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="c626b-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="c626b-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="c626b-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="c626b-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="c626b-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="c626b-150">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="c626b-150">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
