---
description: 'D3DXMatrixPerspectiveOffCenterRH-Funktion (D3DX10Math.h): Erstellt eine angepasste, rechtshändige Projektionsmatrix für die Perspektive.'
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: D3DXMatrixPerspectiveOffCenterRH-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: 3f80c32953dbc591d5d8bc7a95fc707e93fe384c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109038"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="b1e03-103">D3DXMatrixPerspectiveOffCenterRH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b1e03-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b1e03-104">Erstellt eine angepasste, rechtshändige Projektionsmatrix für die Perspektive.</span><span class="sxs-lookup"><span data-stu-id="b1e03-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1e03-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b1e03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1e03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e03-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1e03-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b1e03-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="b1e03-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-112">Minimaler x-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-115">Maximaler x-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-118">Minimaler y-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-119">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-121">Maximaler y-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-122">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-124">Minimaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="b1e03-125">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b1e03-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1e03-126">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1e03-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1e03-127">Maximaler Z-Wert des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e03-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1e03-128">Return value</span></span>

<span data-ttu-id="b1e03-129">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1e03-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b1e03-130">Zeiger auf eine D3DXMATRIX-Struktur, die eine angepasste, rechtshändige perspektivische Projektionsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="b1e03-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e03-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1e03-131">Remarks</span></span>

<span data-ttu-id="b1e03-132">Alle Parameter der D3DXMatrixPerspectiveOffCenterRH-Funktion sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="b1e03-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="b1e03-133">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="b1e03-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b1e03-134">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1e03-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b1e03-135">Auf diese Weise kann die D3DXMatrixPerspectiveOffCenterRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b1e03-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b1e03-136">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="b1e03-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="b1e03-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1e03-137">Requirements</span></span>



| <span data-ttu-id="b1e03-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1e03-138">Requirement</span></span> | <span data-ttu-id="b1e03-139">Wert</span><span class="sxs-lookup"><span data-stu-id="b1e03-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e03-140">Header</span><span class="sxs-lookup"><span data-stu-id="b1e03-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b1e03-141"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b1e03-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b1e03-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1e03-142">Library</span></span><br/> | <dl> <span data-ttu-id="b1e03-143"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1e03-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b1e03-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b1e03-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e03-145">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="b1e03-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
