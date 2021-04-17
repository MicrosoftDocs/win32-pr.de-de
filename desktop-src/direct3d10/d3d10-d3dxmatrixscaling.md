---
description: Erstellt eine Matrix, die auf der x-Achse, der y-Achse und der z-Achse skaliert.
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: D3DXMatrixScaling-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: adb1becb67a561778b31c90ea3d6c96e776c9a67
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355597"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="bf63a-103">D3DXMatrixScaling-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="bf63a-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="bf63a-104">Erstellt eine Matrix, die auf der x-Achse, der y-Achse und der z-Achse skaliert.</span><span class="sxs-lookup"><span data-stu-id="bf63a-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf63a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf63a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="bf63a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf63a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf63a-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bf63a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf63a-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf63a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bf63a-109">Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bf63a-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bf63a-110">*SX* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf63a-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf63a-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf63a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf63a-112">Skalierungsfaktor, der auf der x-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf63a-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="bf63a-113">*Sy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf63a-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf63a-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf63a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf63a-115">Skalierungsfaktor, der auf der y-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf63a-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="bf63a-116">*SZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf63a-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf63a-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf63a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf63a-118">Skalierungsfaktor, der auf der z-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bf63a-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf63a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf63a-119">Return value</span></span>

<span data-ttu-id="bf63a-120">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf63a-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="bf63a-121">Zeiger auf die Skalierungs Transformation D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="bf63a-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf63a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf63a-122">Remarks</span></span>

<span data-ttu-id="bf63a-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf63a-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bf63a-124">Auf diese Weise kann die D3DXMatrixScaling-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf63a-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf63a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bf63a-125">Requirements</span></span>



| <span data-ttu-id="bf63a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf63a-126">Requirement</span></span> | <span data-ttu-id="bf63a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bf63a-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf63a-128">Header</span><span class="sxs-lookup"><span data-stu-id="bf63a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bf63a-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf63a-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bf63a-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bf63a-130">Library</span></span><br/> | <dl> <span data-ttu-id="bf63a-131"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf63a-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf63a-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf63a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf63a-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bf63a-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
