---
description: 'D3DXMatrixLookAtLH-Funktion (D3dx9math.h): Erstellt eine linkshändige Look-At-Matrix.'
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: D3DXMatrixLookAtLH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a423e700c4a42e2ae7f7e522d83a5a4bd9bf3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107588"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="c5880-103">D3DXMatrixLookAtLH-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c5880-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="c5880-104">Erstellt eine linkshändige Look-At-Matrix.</span><span class="sxs-lookup"><span data-stu-id="c5880-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5880-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5880-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="c5880-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5880-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c5880-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5880-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5880-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5880-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="c5880-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c5880-110">*pEye* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c5880-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5880-111">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5880-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5880-112">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Augenpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="c5880-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="c5880-113">Dieser Wert wird bei der Übersetzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c5880-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="c5880-114">*pAt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c5880-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5880-115">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5880-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5880-116">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die das Kamera-Look-at-Ziel definiert.</span><span class="sxs-lookup"><span data-stu-id="c5880-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="c5880-117">*pUp* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c5880-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5880-118">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c5880-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c5880-119">Zeiger auf die [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die den Up der aktuellen Welt definiert, in der Regel \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="c5880-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5880-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5880-120">Return value</span></span>

<span data-ttu-id="c5880-121">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5880-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5880-122">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine linkshändige Look-at-Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="c5880-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5880-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5880-123">Remarks</span></span>

<span data-ttu-id="c5880-124">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5880-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c5880-125">Auf diese Weise kann die **D3DXMatrixLookAtLH-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5880-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c5880-126">Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c5880-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="c5880-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5880-127">Requirements</span></span>



| <span data-ttu-id="c5880-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5880-128">Requirement</span></span> | <span data-ttu-id="c5880-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c5880-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5880-130">Header</span><span class="sxs-lookup"><span data-stu-id="c5880-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c5880-131"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c5880-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c5880-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5880-132">Library</span></span><br/> | <dl> <span data-ttu-id="c5880-133"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5880-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5880-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5880-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5880-135">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c5880-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c5880-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="c5880-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




