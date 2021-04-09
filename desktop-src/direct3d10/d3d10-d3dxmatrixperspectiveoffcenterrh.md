---
description: Erstellt eine angepasste, rechts übergebene perspektivische Projektions Matrix.
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: D3DXMatrixPerspectiveOffCenterRH-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54fc98658d5466acd69d3245af7488c40cd352c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050917"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="c8bf6-103">D3DXMatrixPerspectiveOffCenterRH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c8bf6-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="c8bf6-104">Erstellt eine angepasste, rechts übergebene perspektivische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bf6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8bf6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c8bf6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8bf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bf6-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8bf6-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8bf6-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-112">Minimaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-115">Maximaler x-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-118">Minimaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-121">Maximaler y-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-122">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-124">Der minimale z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="c8bf6-125">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8bf6-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8bf6-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8bf6-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8bf6-127">Maximaler z-Wert des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bf6-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8bf6-128">Return value</span></span>

<span data-ttu-id="c8bf6-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8bf6-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8bf6-130">Zeiger auf eine D3DXMATRIX-Struktur, die eine angepasste, rechts übergebene perspektivische Projektions Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8bf6-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8bf6-131">Remarks</span></span>

<span data-ttu-id="c8bf6-132">Alle Parameter der D3DXMatrixPerspectiveOffCenterRH-Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="c8bf6-133">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="c8bf6-134">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="c8bf6-135">Auf diese Weise kann die D3DXMatrixPerspectiveOffCenterRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c8bf6-136">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c8bf6-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="c8bf6-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8bf6-137">Requirements</span></span>



| <span data-ttu-id="c8bf6-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8bf6-138">Requirement</span></span> | <span data-ttu-id="c8bf6-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c8bf6-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bf6-140">Header</span><span class="sxs-lookup"><span data-stu-id="c8bf6-140">Header</span></span><br/>  | <dl> <span data-ttu-id="c8bf6-141"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bf6-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8bf6-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8bf6-142">Library</span></span><br/> | <dl> <span data-ttu-id="c8bf6-143"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8bf6-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8bf6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8bf6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bf6-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c8bf6-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
