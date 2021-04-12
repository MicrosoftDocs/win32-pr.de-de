---
description: Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: 'ID3DXMATRIXStack:: rotateyawpitchrolllocal-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cffacf4129a711dece35fd581f6cfc9bc12c2f99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354327"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="a1dd3-103">ID3DXMATRIXStack:: rotateyawpitchrolllocal-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a1dd3-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="a1dd3-104">Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1dd3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1dd3-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="a1dd3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1dd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1dd3-107">Nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1dd3-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1dd3-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1dd3-109">Die-Achse um die y-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a1dd3-110">*Tonhöhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1dd3-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1dd3-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1dd3-112">Die Tonhöhe um die x-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a1dd3-113">*Rollout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1dd3-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1dd3-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1dd3-115">Der rollenum die z-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1dd3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1dd3-116">Return value</span></span>

<span data-ttu-id="a1dd3-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1dd3-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1dd3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1dd3-119">Remarks</span></span>

<span data-ttu-id="a1dd3-120">Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="a1dd3-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="a1dd3-121">Da die Drehung linksbündig mit dem Matrix Stapel multipliziert wird, ist die Drehung relativ zum lokalen Koordinaten Bereich des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1dd3-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dd3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1dd3-122">Requirements</span></span>



| <span data-ttu-id="a1dd3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1dd3-123">Requirement</span></span> | <span data-ttu-id="a1dd3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a1dd3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1dd3-125">Header</span><span class="sxs-lookup"><span data-stu-id="a1dd3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a1dd3-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1dd3-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a1dd3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a1dd3-127">Library</span></span><br/> | <dl> <span data-ttu-id="a1dd3-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1dd3-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1dd3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1dd3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1dd3-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a1dd3-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a1dd3-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a1dd3-132">**ID3DXMATRIXStack:: rotateaxis**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="a1dd3-133">**ID3DXMATRIXStack:: rotateaxislocal**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="a1dd3-134">**ID3DXMATRIXStack:: rotateyawpitchroll**</span><span class="sxs-lookup"><span data-stu-id="a1dd3-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
