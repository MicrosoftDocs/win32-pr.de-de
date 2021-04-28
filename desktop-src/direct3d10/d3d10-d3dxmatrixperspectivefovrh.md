---
description: 'D3DXMatrixPerspectiveFovRH-Funktion (D3DX10Math.h): Erstellt eine rechtshändige Perspektivprojektionsmatrix basierend auf einem Sichtfeld.'
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: D3DXMatrixPerspectiveFovRH-Funktion (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d48789bab9b968b6bcf657459c408abdba774b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109108"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="ab405-103">D3DXMatrixPerspectiveFovRH-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="ab405-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="ab405-104">Erstellt eine rechtshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.</span><span class="sxs-lookup"><span data-stu-id="ab405-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab405-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab405-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="ab405-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab405-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab405-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ab405-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab405-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab405-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab405-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="ab405-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ab405-110">*folow* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab405-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab405-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab405-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab405-112">Sichtfeld in y-Richtung im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="ab405-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="ab405-113">*Aspect* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab405-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab405-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab405-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab405-115">Seitenverhältnis, definiert als Ansichtsraumbreite dividiert durch Höhe.</span><span class="sxs-lookup"><span data-stu-id="ab405-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="ab405-116">*zn* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab405-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab405-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab405-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab405-118">Z-Wert der Nahansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab405-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="ab405-119">*( )* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ab405-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab405-120">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab405-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab405-121">Z-Wert der fernen Ansichtsebene.</span><span class="sxs-lookup"><span data-stu-id="ab405-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab405-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab405-122">Return value</span></span>

<span data-ttu-id="ab405-123">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab405-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ab405-124">Zeiger auf eine D3DXMATRIX-Struktur, bei der es sich um eine rechtshändige Perspektivprojektionsmatrix handelt.</span><span class="sxs-lookup"><span data-stu-id="ab405-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab405-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab405-125">Remarks</span></span>

<span data-ttu-id="ab405-126">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ab405-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ab405-127">Auf diese Weise kann die D3DXMatrixPerspectiveFovRH-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab405-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ab405-128">Diese Funktion berechnet die zurückgegebene Matrix wie gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab405-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="ab405-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab405-129">Requirements</span></span>



| <span data-ttu-id="ab405-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab405-130">Requirement</span></span> | <span data-ttu-id="ab405-131">Wert</span><span class="sxs-lookup"><span data-stu-id="ab405-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab405-132">Header</span><span class="sxs-lookup"><span data-stu-id="ab405-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ab405-133"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab405-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ab405-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab405-134">Library</span></span><br/> | <dl> <span data-ttu-id="ab405-135"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab405-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab405-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab405-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab405-137">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ab405-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
