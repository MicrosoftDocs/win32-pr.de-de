---
description: 'D3DXMatrixPerspectiveRH-Funktion (D3dx9math.h): Erstellt eine rechtshändige Perspektivische Projektionsmatrix.'
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: D3DXMatrixPerspectiveRH-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3c583b74366a0a00054bbeced1ece2bd3d1c1cd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118238"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="2df53-103">D3DXMatrixPerspectiveRH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="2df53-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="2df53-104">Erstellt eine rechtshändige perspektivische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="2df53-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df53-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="2df53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2df53-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2df53-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2df53-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2df53-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2df53-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2df53-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2df53-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2df53-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df53-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2df53-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2df53-112">Breite des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="2df53-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2df53-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2df53-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df53-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2df53-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2df53-115">Höhe des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="2df53-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2df53-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2df53-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df53-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2df53-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2df53-118">Z-Wert der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="2df53-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="2df53-119">*( )* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2df53-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2df53-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2df53-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2df53-121">Z-Wert der fernen Ansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="2df53-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2df53-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2df53-122">Return value</span></span>

<span data-ttu-id="2df53-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2df53-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2df53-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) bei der es sich um eine rechtshändige Perspektivprojektionsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="2df53-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2df53-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2df53-125">Remarks</span></span>

<span data-ttu-id="2df53-126">Alle Parameter der **D3DXMatrixPerspectiveRH-Funktion** sind Entfernungen im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="2df53-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="2df53-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.</span><span class="sxs-lookup"><span data-stu-id="2df53-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="2df53-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2df53-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2df53-129">Auf diese Weise kann die **D3DXMatrixPerspectiveRH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2df53-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2df53-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="2df53-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="2df53-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df53-131">Requirements</span></span>



| <span data-ttu-id="2df53-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2df53-132">Requirement</span></span> | <span data-ttu-id="2df53-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2df53-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2df53-134">Header</span><span class="sxs-lookup"><span data-stu-id="2df53-134">Header</span></span><br/>  | <dl> <span data-ttu-id="2df53-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="2df53-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2df53-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2df53-136">Library</span></span><br/> | <dl> <span data-ttu-id="2df53-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2df53-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2df53-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2df53-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df53-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2df53-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2df53-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="2df53-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="2df53-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="2df53-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="2df53-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="2df53-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="2df53-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="2df53-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="2df53-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="2df53-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
