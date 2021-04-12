---
description: Erstellt eine rechtshändige perspektivische Projektionsmatrix.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: D3DXMatrixPerspectiveRH-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219441"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="7931e-103">D3DXMatrixPerspectiveRH-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7931e-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="7931e-104">Erstellt eine rechtshändige perspektivische Projektionsmatrix.</span><span class="sxs-lookup"><span data-stu-id="7931e-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7931e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7931e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="7931e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7931e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7931e-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7931e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7931e-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7931e-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7931e-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="7931e-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7931e-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7931e-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931e-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7931e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7931e-112">Breite des Ansichts Volumes auf der Nahsicht Ebene.</span><span class="sxs-lookup"><span data-stu-id="7931e-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="7931e-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7931e-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931e-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7931e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7931e-115">Höhe des Ansichts Volumes auf der nahen Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="7931e-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="7931e-116">*Zn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7931e-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931e-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7931e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7931e-118">Z-Wert der nahen Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="7931e-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="7931e-119">*ZF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7931e-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7931e-120">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7931e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7931e-121">Z-Wert der weit entfernten Ansichts Ebene.</span><span class="sxs-lookup"><span data-stu-id="7931e-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7931e-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7931e-122">Return value</span></span>

<span data-ttu-id="7931e-123">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="7931e-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7931e-124">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine rechts übergebene Perspektiven Projektions Matrix handelt.</span><span class="sxs-lookup"><span data-stu-id="7931e-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="7931e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7931e-125">Remarks</span></span>

<span data-ttu-id="7931e-126">Alle Parameter der **D3DXMatrixPerspectiveRH** -Funktion sind Abstände im Kamerabereich.</span><span class="sxs-lookup"><span data-stu-id="7931e-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="7931e-127">Die Parameter beschreiben die Dimensionen des Ansichts Volumes.</span><span class="sxs-lookup"><span data-stu-id="7931e-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="7931e-128">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7931e-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="7931e-129">Auf diese Weise kann die **D3DXMatrixPerspectiveRH** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7931e-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="7931e-130">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="7931e-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="7931e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7931e-131">Requirements</span></span>



| <span data-ttu-id="7931e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7931e-132">Requirement</span></span> | <span data-ttu-id="7931e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="7931e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7931e-134">Header</span><span class="sxs-lookup"><span data-stu-id="7931e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="7931e-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7931e-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7931e-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7931e-136">Library</span></span><br/> | <dl> <span data-ttu-id="7931e-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7931e-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7931e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7931e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7931e-139">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7931e-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="7931e-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="7931e-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="7931e-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="7931e-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="7931e-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="7931e-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="7931e-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="7931e-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="7931e-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="7931e-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
