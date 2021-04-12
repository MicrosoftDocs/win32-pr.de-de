---
description: Erstellt eine rechtshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: D3DXMatrixPerspectiveFovRH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da478a027db8c366a2cfec827075d3d4b73ae014
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355416"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="aa48d-103">D3DXMatrixPerspectiveFovRH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="aa48d-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="aa48d-104">Erstellt eine rechtshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.</span><span class="sxs-lookup"><span data-stu-id="aa48d-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa48d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa48d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="aa48d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa48d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa48d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="aa48d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa48d-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa48d-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aa48d-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="aa48d-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="aa48d-110">*fovy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa48d-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa48d-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa48d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa48d-112">Feld der Ansicht in y-Richtung im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="aa48d-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="aa48d-113">*Aspekt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa48d-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa48d-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa48d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa48d-115">Seitenverhältnis, definiert als Breite des Ansichts Raums dividiert durch Höhe.</span><span class="sxs-lookup"><span data-stu-id="aa48d-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="aa48d-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa48d-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa48d-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa48d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa48d-118">Z-Wert der nahen Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="aa48d-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="aa48d-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa48d-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa48d-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aa48d-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aa48d-121">Z-Wert der weit entfernten Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="aa48d-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa48d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa48d-122">Return value</span></span>

<span data-ttu-id="aa48d-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="aa48d-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="aa48d-124">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine rechts übergebene Perspektiven Projektions Matrix handelt.</span><span class="sxs-lookup"><span data-stu-id="aa48d-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa48d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa48d-125">Remarks</span></span>

<span data-ttu-id="aa48d-126">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa48d-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="aa48d-127">Auf diese Weise kann die **D3DXMatrixPerspectiveFovRH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aa48d-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="aa48d-128">Verwenden Sie zum Ändern der Seitenverhältnis Achse die Berechnungsformel: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/Aspekt).</span><span class="sxs-lookup"><span data-stu-id="aa48d-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="aa48d-129">Fügen Sie alternativ die Variablen X und Y-Seitenverhältnis in der Struktur hinzu, um den vertikalen Ansichts Bereich zu skalieren: fovy = 2 \* Math. Atan (Math. Tan (fovy \* 0,5)/aspecty), Aspekt = aspectx \* Aspekt Y.</span><span class="sxs-lookup"><span data-stu-id="aa48d-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="aa48d-130">Diese Funktion berechnet die zurückgegebene Matrix wie gezeigt.</span><span class="sxs-lookup"><span data-stu-id="aa48d-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="aa48d-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa48d-131">Requirements</span></span>



| <span data-ttu-id="aa48d-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa48d-132">Requirement</span></span> | <span data-ttu-id="aa48d-133">Wert</span><span class="sxs-lookup"><span data-stu-id="aa48d-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa48d-134">Header</span><span class="sxs-lookup"><span data-stu-id="aa48d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="aa48d-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa48d-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="aa48d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa48d-136">Library</span></span><br/> | <dl> <span data-ttu-id="aa48d-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa48d-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa48d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa48d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa48d-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="aa48d-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="aa48d-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="aa48d-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="aa48d-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="aa48d-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="aa48d-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="aa48d-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="aa48d-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="aa48d-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="aa48d-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="aa48d-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
