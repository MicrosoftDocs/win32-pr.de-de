---
description: Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: 'ID3DXMATRIXStack:: rotateaxislocal-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8488f6314eb926495baa2e42df9ea01616131507
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366444"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="519d1-103">ID3DXMATRIXStack:: rotateaxislocal-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="519d1-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="519d1-104">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="519d1-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="519d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="519d1-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="519d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="519d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="519d1-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="519d1-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519d1-108">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="519d1-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="519d1-109">Zeiger auf die beliebige Achse der Drehung.</span><span class="sxs-lookup"><span data-stu-id="519d1-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="519d1-110">Siehe [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="519d1-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="519d1-111">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="519d1-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="519d1-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="519d1-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="519d1-113">Drehwinkel für die beliebige Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="519d1-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="519d1-114">Winkel werden bei der Betrachtung der beliebigen Achse zum Ursprung gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="519d1-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="519d1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="519d1-115">Return value</span></span>

<span data-ttu-id="519d1-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="519d1-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="519d1-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="519d1-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="519d1-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="519d1-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="519d1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="519d1-119">Remarks</span></span>

<span data-ttu-id="519d1-120">Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="519d1-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="519d1-121">Da die Drehung linksbündig mit dem Matrix Stapel multipliziert wird, ist die Drehung relativ zum lokalen Koordinaten Bereich des Objekts.</span><span class="sxs-lookup"><span data-stu-id="519d1-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="519d1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="519d1-122">Requirements</span></span>



| <span data-ttu-id="519d1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="519d1-123">Requirement</span></span> | <span data-ttu-id="519d1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="519d1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="519d1-125">Header</span><span class="sxs-lookup"><span data-stu-id="519d1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="519d1-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="519d1-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="519d1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="519d1-127">Library</span></span><br/> | <dl> <span data-ttu-id="519d1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="519d1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="519d1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="519d1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="519d1-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="519d1-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="519d1-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="519d1-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="519d1-132">**ID3DXMATRIXStack:: rotateaxis**</span><span class="sxs-lookup"><span data-stu-id="519d1-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="519d1-133">**ID3DXMATRIXStack:: rotateyawpitchroll**</span><span class="sxs-lookup"><span data-stu-id="519d1-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="519d1-134">**ID3DXMATRIXStack:: rotateyawpitchrolllocal**</span><span class="sxs-lookup"><span data-stu-id="519d1-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
