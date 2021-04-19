---
description: Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: 'ID3DXMATRIXStack:: rotateaxislocal-Methode (d3dx10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5b00e1fd5b678d89d6b5ca4680499f6fde723c12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364398"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="729ff-103">ID3DXMATRIXStack:: rotateaxislocal-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="729ff-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="729ff-104">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="729ff-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="729ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="729ff-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="729ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="729ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="729ff-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="729ff-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="729ff-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="729ff-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="729ff-109">Zeiger auf die beliebige Achse der Drehung.</span><span class="sxs-lookup"><span data-stu-id="729ff-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="729ff-110">Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="729ff-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="729ff-111">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="729ff-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="729ff-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="729ff-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="729ff-113">Drehwinkel für die beliebige Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="729ff-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="729ff-114">Winkel werden bei der Betrachtung der beliebigen Achse zum Ursprung gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="729ff-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="729ff-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="729ff-115">Return value</span></span>

<span data-ttu-id="729ff-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="729ff-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="729ff-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="729ff-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="729ff-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="729ff-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="729ff-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="729ff-119">Remarks</span></span>

<span data-ttu-id="729ff-120">Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="729ff-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="729ff-121">Da die Drehung linksbündig mit dem Matrix Stapel multipliziert wird, ist die Drehung relativ zum lokalen Koordinaten Bereich des Objekts.</span><span class="sxs-lookup"><span data-stu-id="729ff-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="729ff-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="729ff-122">Requirements</span></span>



| <span data-ttu-id="729ff-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="729ff-123">Requirement</span></span> | <span data-ttu-id="729ff-124">Wert</span><span class="sxs-lookup"><span data-stu-id="729ff-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="729ff-125">Header</span><span class="sxs-lookup"><span data-stu-id="729ff-125">Header</span></span><br/>  | <dl> <span data-ttu-id="729ff-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="729ff-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="729ff-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="729ff-127">Library</span></span><br/> | <dl> <span data-ttu-id="729ff-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="729ff-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="729ff-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="729ff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729ff-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="729ff-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="729ff-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="729ff-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
