---
description: ID3DXMATRIXStack::RotateAxisLocal-Methode (D3dx9math.h) – Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.
ms.assetid: c7ef11e9-f4c4-4801-8f25-190066baeb52
title: ID3DXMATRIXStack::RotateAxisLocal-Methode (D3dx9math.h)
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
ms.openlocfilehash: 0bfcfd7301f90dcf49b03e7bbb3fd7e3b0de6c3e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093468"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx9mathh"></a><span data-ttu-id="7514f-103">ID3DXMATRIXStack::RotateAxisLocal-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="7514f-103">ID3DXMATRIXStack::RotateAxisLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="7514f-104">Dreht (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="7514f-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7514f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7514f-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="7514f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7514f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7514f-107">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7514f-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7514f-108">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="7514f-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="7514f-109">Zeiger auf die beliebige Drehachse.</span><span class="sxs-lookup"><span data-stu-id="7514f-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="7514f-110">Siehe [**D3DXVECTOR3**](d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="7514f-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="7514f-111">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7514f-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7514f-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7514f-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7514f-113">Drehwinkel um die beliebige Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="7514f-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="7514f-114">Winkel werden gegen den Uhrzeigersinn gemessen, wenn entlang der beliebigen Achse zum Ursprung gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="7514f-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7514f-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7514f-115">Return value</span></span>

<span data-ttu-id="7514f-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7514f-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7514f-117">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7514f-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7514f-118">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="7514f-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7514f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7514f-119">Remarks</span></span>

<span data-ttu-id="7514f-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="7514f-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="7514f-121">Da die Drehung links multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.</span><span class="sxs-lookup"><span data-stu-id="7514f-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="7514f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7514f-122">Requirements</span></span>



| <span data-ttu-id="7514f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7514f-123">Requirement</span></span> | <span data-ttu-id="7514f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7514f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7514f-125">Header</span><span class="sxs-lookup"><span data-stu-id="7514f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7514f-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="7514f-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="7514f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7514f-127">Library</span></span><br/> | <dl> <span data-ttu-id="7514f-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7514f-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7514f-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7514f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7514f-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="7514f-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="7514f-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="7514f-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="7514f-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="7514f-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="7514f-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="7514f-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="7514f-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="7514f-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
