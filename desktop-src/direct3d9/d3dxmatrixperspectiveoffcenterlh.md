---
description: Erstellt eine angepasste, Links übergebene perspektivische Projektions Matrix.
ms.assetid: de2732dd-a4f2-47bc-9509-de16f1ca85c2
title: D3DXMatrixPerspectiveOffCenterLH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 15743af16be84587fd8dc03e845ffcd8bd8dbc2b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373480"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx9mathh"></a><span data-ttu-id="f3212-103">D3DXMatrixPerspectiveOffCenterLH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f3212-103">D3DXMatrixPerspectiveOffCenterLH function (D3dx9math.h)</span></span>

<span data-ttu-id="f3212-104">Erstellt eine angepasste, Links übergebene perspektivische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="f3212-104">Builds a customized, left-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3212-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3212-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f3212-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3212-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3212-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f3212-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3212-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3212-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f3212-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-112">Minimaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-115">Maximaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-118">Minimaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-121">Maximaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="f3212-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3212-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3212-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3212-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3212-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3212-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f3212-128">Return value</span></span>

<span data-ttu-id="f3212-129">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3212-129">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3212-130">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die eine angepasste, Links übergebene perspektivische Projektions Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="f3212-130">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a customized, left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3212-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3212-131">Remarks</span></span>

<span data-ttu-id="f3212-132">Alle Parameter der **D3DXMatrixPerspectiveOffCenterLH** -Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="f3212-132">All the parameters of the **D3DXMatrixPerspectiveOffCenterLH** function are distances in camera space.</span></span> <span data-ttu-id="f3212-133">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="f3212-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="f3212-134">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3212-134">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f3212-135">Auf diese Weise kann die **D3DXMatrixPerspectiveOffCenterLH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3212-135">In this way, the **D3DXMatrixPerspectiveOffCenterLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f3212-136">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f3212-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="f3212-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3212-137">Requirements</span></span>



| <span data-ttu-id="f3212-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3212-138">Requirement</span></span> | <span data-ttu-id="f3212-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f3212-139">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3212-140">Header</span><span class="sxs-lookup"><span data-stu-id="f3212-140">Header</span></span><br/>  | <dl> <span data-ttu-id="f3212-141"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3212-141"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f3212-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f3212-142">Library</span></span><br/> | <dl> <span data-ttu-id="f3212-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3212-143"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3212-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3212-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3212-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f3212-145">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f3212-146">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="f3212-146">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="f3212-147">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="f3212-147">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="f3212-148">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="f3212-148">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="f3212-149">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="f3212-149">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="f3212-150">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="f3212-150">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> </dl>

 

 
