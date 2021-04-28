---
description: 'D3DXMatrixPerspectiveRH-Funktion (D3DX10Math.h): Erstellt eine rechtshändige Perspektivische Projektionsmatrix.'
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: D3DXMatrixPerspectiveRH-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03ffd99d016023612daa3de96ae29275d71074a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109008"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="1ac7c-103">D3DXMatrixPerspectiveRH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1ac7c-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="1ac7c-104">Erstellt eine rechtshändige perspektivische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac7c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="1ac7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ac7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac7c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ac7c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7c-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ac7c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ac7c-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ac7c-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac7c-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7c-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac7c-112">Breite des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ac7c-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ac7c-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7c-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac7c-115">Höhe des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ac7c-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1ac7c-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7c-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac7c-118">Z-Wert der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="1ac7c-119">*( )* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1ac7c-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac7c-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ac7c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ac7c-121">Z-Wert der fernen Ansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac7c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1ac7c-122">Return value</span></span>

<span data-ttu-id="1ac7c-123">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ac7c-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1ac7c-124">Zeiger auf eine D3DXMATRIX-Struktur, bei der es sich um eine rechtshändige Perspektivprojektionsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac7c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ac7c-125">Remarks</span></span>

<span data-ttu-id="1ac7c-126">Alle Parameter der D3DXMatrixPerspectiveRH-Funktion sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="1ac7c-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="1ac7c-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="1ac7c-129">Auf diese Weise kann die D3DXMatrixPerspectiveRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1ac7c-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1ac7c-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="1ac7c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac7c-131">Requirements</span></span>



| <span data-ttu-id="1ac7c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac7c-132">Requirement</span></span> | <span data-ttu-id="1ac7c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="1ac7c-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac7c-134">Header</span><span class="sxs-lookup"><span data-stu-id="1ac7c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1ac7c-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7c-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1ac7c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1ac7c-136">Library</span></span><br/> | <dl> <span data-ttu-id="1ac7c-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ac7c-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ac7c-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ac7c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac7c-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1ac7c-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
