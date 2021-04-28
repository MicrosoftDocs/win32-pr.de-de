---
description: 'D3DXMatrixPerspectiveLH-Funktion (D3dx9math.h): Erstellt eine linkshändige Perspektivische Projektionsmatrix'
ms.assetid: 07bbbca8-ad1e-4177-97d4-601b33179b47
title: D3DXMatrixPerspectiveLH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d898a7d40cd1c9f7b46100c19d86573806ccb1b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118308"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx9mathh"></a><span data-ttu-id="ab9f5-103">D3DXMatrixPerspectiveLH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="ab9f5-103">D3DXMatrixPerspectiveLH function (D3dx9math.h)</span></span>

<span data-ttu-id="ab9f5-104">Erstellt eine linkshändige Perspektivprojektionsmatrix</span><span class="sxs-lookup"><span data-stu-id="ab9f5-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9f5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab9f5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="ab9f5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab9f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9f5-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab9f5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9f5-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab9f5-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab9f5-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab9f5-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9f5-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9f5-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab9f5-112">Breite des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="ab9f5-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab9f5-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9f5-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab9f5-115">Höhe des Ansichtsvolumens auf der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="ab9f5-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab9f5-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9f5-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab9f5-118">Z-Wert der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="ab9f5-119">*( )* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab9f5-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9f5-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab9f5-121">Z-Wert der fernen Ansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9f5-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab9f5-122">Return value</span></span>

<span data-ttu-id="ab9f5-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab9f5-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab9f5-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) bei der es sich um eine linkshändige Perspektivprojektionsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9f5-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab9f5-125">Remarks</span></span>

<span data-ttu-id="ab9f5-126">Alle Parameter der **D3DXMatrixPerspectiveLH-Funktion** sind Abstände im Kameraraum.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-126">All the parameters of the **D3DXMatrixPerspectiveLH** function are distances in camera space.</span></span> <span data-ttu-id="ab9f5-127">Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="ab9f5-128">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ab9f5-129">Auf diese Weise kann die **D3DXMatrixPerspectiveLH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-129">In this way, the **D3DXMatrixPerspectiveLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ab9f5-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ab9f5-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="ab9f5-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab9f5-131">Requirements</span></span>



| <span data-ttu-id="ab9f5-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab9f5-132">Requirement</span></span> | <span data-ttu-id="ab9f5-133">Wert</span><span class="sxs-lookup"><span data-stu-id="ab9f5-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9f5-134">Header</span><span class="sxs-lookup"><span data-stu-id="ab9f5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="ab9f5-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9f5-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab9f5-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab9f5-136">Library</span></span><br/> | <dl> <span data-ttu-id="ab9f5-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab9f5-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab9f5-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab9f5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9f5-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ab9f5-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ab9f5-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="ab9f5-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="ab9f5-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="ab9f5-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="ab9f5-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="ab9f5-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
