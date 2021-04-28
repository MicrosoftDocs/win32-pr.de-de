---
description: 'D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h): Erstellt eine linkshändige Projektionsmatrix basierend auf einem Sichtfeld.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118348"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="f38f4-103">D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="f38f4-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="f38f4-104">Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.</span><span class="sxs-lookup"><span data-stu-id="f38f4-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f38f4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f38f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f38f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f38f4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f38f4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f38f4-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f38f4-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f38f4-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f38f4-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f38f4-110">*fovy* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f38f4-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38f4-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f38f4-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f38f4-112">Sichtfeld in y-Richtung, im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="f38f4-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f38f4-113">*Aspekt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f38f4-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38f4-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f38f4-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f38f4-115">Seitenverhältnis, definiert als Ansichtsraumbreite dividiert durch Höhe.</span><span class="sxs-lookup"><span data-stu-id="f38f4-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="f38f4-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f38f4-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38f4-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f38f4-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f38f4-118">Z-Wert der ansichtsnahen Ebene.</span><span class="sxs-lookup"><span data-stu-id="f38f4-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="f38f4-119">*NSD* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f38f4-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f38f4-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f38f4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f38f4-121">Z-Wert der fernen Ansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="f38f4-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f38f4-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f38f4-122">Return value</span></span>

<span data-ttu-id="f38f4-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f38f4-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f38f4-124">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) bei der es sich um eine linkshändige Projektionsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="f38f4-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38f4-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f38f4-125">Remarks</span></span>

<span data-ttu-id="f38f4-126">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f38f4-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f38f4-127">Auf diese Weise kann die **D3DXMatrixPerspectiveFovLH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f38f4-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f38f4-128">Um die Seitenverhältnisachse zu ändern, verwenden Sie die Berechnungsformel: fovy = 2 \* math.atan(math.tan(fovy \* 0,5) / aspect).</span><span class="sxs-lookup"><span data-stu-id="f38f4-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="f38f4-129">Fügen Sie alternativ X- und Y-Seitenverhältnisvariablen in der Struktur hinzu, um den vertikalen Ansichtsbereich zu skalieren: fovy = 2 \* math.atan(math.tan(fovy \* 0,5) / aspectY), aspect = aspectX \* aspect Y.</span><span class="sxs-lookup"><span data-stu-id="f38f4-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="f38f4-130">Diese Funktion berechnet die zurückgegebene Matrix wie gezeigt:</span><span class="sxs-lookup"><span data-stu-id="f38f4-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="f38f4-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f38f4-131">Requirements</span></span>



| <span data-ttu-id="f38f4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f38f4-132">Requirement</span></span> | <span data-ttu-id="f38f4-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f38f4-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38f4-134">Header</span><span class="sxs-lookup"><span data-stu-id="f38f4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f38f4-135"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f38f4-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f38f4-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f38f4-136">Library</span></span><br/> | <dl> <span data-ttu-id="f38f4-137"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f38f4-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f38f4-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f38f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38f4-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f38f4-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f38f4-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="f38f4-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="f38f4-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="f38f4-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="f38f4-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="f38f4-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="f38f4-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="f38f4-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="f38f4-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="f38f4-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
