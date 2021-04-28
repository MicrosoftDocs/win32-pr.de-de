---
description: 'D3DXMatrixRotationQuaternion-Funktion (D3dx9math.h): Erstellt eine Rotationsmatrix aus einer Quaternion.'
ms.assetid: e590058c-772b-4eef-aab0-a12bb04c299a
title: D3DXMatrixRotationQuaternion-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationQuaternion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b30de0c45c8d78b2e07d6ff57a4e94b9753298a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118198"
---
# <a name="d3dxmatrixrotationquaternion-function-d3dx9mathh"></a><span data-ttu-id="1da85-103">D3DXMatrixRotationQuaternion-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="1da85-103">D3DXMatrixRotationQuaternion function (D3dx9math.h)</span></span>

<span data-ttu-id="1da85-104">Erstellt eine Rotationsmatrix aus einer Quaternion.</span><span class="sxs-lookup"><span data-stu-id="1da85-104">Builds a rotation matrix from a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1da85-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationQuaternion(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="1da85-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1da85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da85-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1da85-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1da85-108">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1da85-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1da85-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1da85-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1da85-110">*pQ* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1da85-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da85-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="1da85-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1da85-112">Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="1da85-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da85-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1da85-113">Return value</span></span>

<span data-ttu-id="1da85-114">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="1da85-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1da85-115">Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die aus der Quell quaternion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1da85-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure built from the source quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da85-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1da85-116">Remarks</span></span>

<span data-ttu-id="1da85-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="1da85-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1da85-118">Auf diese Weise kann die **D3DXMatrixRotationQuaternion-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1da85-118">In this way, the **D3DXMatrixRotationQuaternion** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="1da85-119">Informationen zum Berechnen von Quaternionswerten aus einem Richtungsvektor ( x, y, z ) und einem Drehwinkel finden Sie unter [**D3DXQUATERNION**](d3dxquaternion.md).</span><span class="sxs-lookup"><span data-stu-id="1da85-119">For information about how to calculate quaternion values from a direction vector ( x, y, z ) and an angle of rotation, see [**D3DXQUATERNION**](d3dxquaternion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1da85-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1da85-120">Requirements</span></span>



| <span data-ttu-id="1da85-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1da85-121">Requirement</span></span> | <span data-ttu-id="1da85-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1da85-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1da85-123">Header</span><span class="sxs-lookup"><span data-stu-id="1da85-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1da85-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1da85-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1da85-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1da85-125">Library</span></span><br/> | <dl> <span data-ttu-id="1da85-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1da85-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1da85-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1da85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da85-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1da85-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="1da85-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="1da85-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="1da85-130">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="1da85-130">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="1da85-131">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="1da85-131">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="1da85-132">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="1da85-132">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="1da85-133">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="1da85-133">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> </dl>

 

 




