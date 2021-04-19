---
description: Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.
ms.assetid: 35ee12d6-0a58-4b00-ac8f-82f82215f02e
title: D3DXMatrixPerspectiveFovLH-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 141c0a1468b2e073881976738cbd2a10b6108edc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357259"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx10mathh"></a><span data-ttu-id="2162d-103">D3DXMatrixPerspectiveFovLH-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2162d-103">D3DXMatrixPerspectiveFovLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="2162d-104">Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.</span><span class="sxs-lookup"><span data-stu-id="2162d-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="2162d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2162d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="2162d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2162d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2162d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2162d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2162d-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2162d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2162d-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2162d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2162d-110">*fovy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2162d-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2162d-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2162d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2162d-112">Feld der Ansicht in y-Richtung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="2162d-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2162d-113">*Aspekt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2162d-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2162d-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2162d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2162d-115">Seitenverhältnis, definiert als Breite des Ansichts Raums dividiert durch Höhe.</span><span class="sxs-lookup"><span data-stu-id="2162d-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="2162d-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2162d-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2162d-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2162d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2162d-118">Z-Wert der nahen Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="2162d-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2162d-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2162d-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2162d-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2162d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2162d-121">Z-Wert der weit entfernten Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="2162d-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2162d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2162d-122">Return value</span></span>

<span data-ttu-id="2162d-123">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2162d-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2162d-124">Zeiger auf eine D3DXMATRIX-Struktur, bei der es sich um eine Perspektiven Projektions Matrix mit linker Übergabe handelt.</span><span class="sxs-lookup"><span data-stu-id="2162d-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2162d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2162d-125">Remarks</span></span>

<span data-ttu-id="2162d-126">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2162d-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2162d-127">Auf diese Weise kann die D3DXMatrixPerspectiveFovLH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2162d-127">In this way, the D3DXMatrixPerspectiveFovLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2162d-128">Diese Funktion berechnet die zurückgegebene Matrix wie gezeigt:</span><span class="sxs-lookup"><span data-stu-id="2162d-128">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="2162d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2162d-129">Requirements</span></span>



| <span data-ttu-id="2162d-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2162d-130">Requirement</span></span> | <span data-ttu-id="2162d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2162d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2162d-132">Header</span><span class="sxs-lookup"><span data-stu-id="2162d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2162d-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2162d-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2162d-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2162d-134">Library</span></span><br/> | <dl> <span data-ttu-id="2162d-135"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2162d-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2162d-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2162d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2162d-137">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2162d-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
