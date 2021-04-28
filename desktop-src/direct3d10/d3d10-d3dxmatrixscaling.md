---
description: 'D3DXMatrixScaling-Funktion (D3DX10Math.h): Erstellt eine Matrix, die entlang der X-Achse, der Y-Achse und der Z-Achse skaliert wird.'
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: D3DXMatrixScaling-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108928"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="8f60f-103">D3DXMatrixScaling-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="8f60f-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="8f60f-104">Erstellt eine Matrix, die entlang der x-Achse, der y-Achse und der Z-Achse skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="8f60f-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f60f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f60f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="8f60f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f60f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f60f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8f60f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60f-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f60f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8f60f-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="8f60f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f60f-110">*sx* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8f60f-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60f-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f60f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f60f-112">Skalierungsfaktor, der entlang der X-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f60f-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8f60f-113">*sy* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8f60f-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60f-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f60f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f60f-115">Skalierungsfaktor, der entlang der y-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f60f-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8f60f-116">*sz* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8f60f-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f60f-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f60f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f60f-118">Skalierungsfaktor, der entlang der Z-Achse angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f60f-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f60f-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f60f-119">Return value</span></span>

<span data-ttu-id="8f60f-120">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f60f-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="8f60f-121">Zeiger auf die Skalierungstransformation D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="8f60f-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f60f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f60f-122">Remarks</span></span>

<span data-ttu-id="8f60f-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f60f-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="8f60f-124">Auf diese Weise kann die D3DXMatrixScaling-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f60f-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f60f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f60f-125">Requirements</span></span>



| <span data-ttu-id="8f60f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f60f-126">Requirement</span></span> | <span data-ttu-id="8f60f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="8f60f-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f60f-128">Header</span><span class="sxs-lookup"><span data-stu-id="8f60f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8f60f-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="8f60f-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="8f60f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f60f-130">Library</span></span><br/> | <dl> <span data-ttu-id="8f60f-131"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f60f-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f60f-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8f60f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f60f-133">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="8f60f-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
