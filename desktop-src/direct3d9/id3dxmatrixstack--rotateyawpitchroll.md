---
description: Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: 'ID3DXMATRIXStack:: rotateyawpitchroll-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5020cb6ff3af41b9ef32ef77bb71607f6cd5ea6f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366628"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="8959e-103">ID3DXMATRIXStack:: rotateyawpitchroll-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8959e-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="8959e-104">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="8959e-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8959e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8959e-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="8959e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8959e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8959e-107">Nicht im  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8959e-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8959e-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8959e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8959e-109">Die-Achse um die y-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="8959e-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8959e-110">*Tonhöhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8959e-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8959e-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8959e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8959e-112">Die Tonhöhe um die x-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="8959e-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="8959e-113">*Rollout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8959e-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8959e-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8959e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8959e-115">Der rollenum die z-Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="8959e-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8959e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8959e-116">Return value</span></span>

<span data-ttu-id="8959e-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8959e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8959e-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8959e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8959e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8959e-119">Remarks</span></span>

<span data-ttu-id="8959e-120">Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="8959e-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="8959e-121">Da die Drehung mit dem Matrix Stapel rechts multipliziert ist, ist die Drehung relativ zum globalen Koordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="8959e-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="8959e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8959e-122">Requirements</span></span>



| <span data-ttu-id="8959e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8959e-123">Requirement</span></span> | <span data-ttu-id="8959e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8959e-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8959e-125">Header</span><span class="sxs-lookup"><span data-stu-id="8959e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8959e-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8959e-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8959e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8959e-127">Library</span></span><br/> | <dl> <span data-ttu-id="8959e-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8959e-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8959e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8959e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8959e-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="8959e-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8959e-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="8959e-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="8959e-132">**ID3DXMATRIXStack:: rotateaxis**</span><span class="sxs-lookup"><span data-stu-id="8959e-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="8959e-133">**ID3DXMATRIXStack:: rotateaxislocal**</span><span class="sxs-lookup"><span data-stu-id="8959e-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="8959e-134">**ID3DXMATRIXStack:: rotateyawpitchrolllocal**</span><span class="sxs-lookup"><span data-stu-id="8959e-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
