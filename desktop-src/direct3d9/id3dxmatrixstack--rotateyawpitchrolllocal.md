---
description: 'ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h): Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.'
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h)
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
ms.openlocfilehash: 1d104676b6d346afd527552dbfba4bac23ed09cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093448"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a><span data-ttu-id="a5fa6-103">ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a5fa6-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="a5fa6-104">Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fa6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5fa6-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="a5fa6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5fa6-107">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa6-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5fa6-109">Das Gähnen um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a5fa6-110">*Tonhöhe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa6-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5fa6-112">Die Tonhöhe um die x-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="a5fa6-113">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5fa6-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5fa6-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5fa6-115">Das Rollback um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5fa6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5fa6-116">Return value</span></span>

<span data-ttu-id="a5fa6-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5fa6-118">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5fa6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5fa6-119">Remarks</span></span>

<span data-ttu-id="a5fa6-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Drehungsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="a5fa6-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="a5fa6-121">Da die Drehung mit dem Matrixstapel nach links multipliziert wird, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a5fa6-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fa6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5fa6-122">Requirements</span></span>



| <span data-ttu-id="a5fa6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5fa6-123">Requirement</span></span> | <span data-ttu-id="a5fa6-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a5fa6-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fa6-125">Header</span><span class="sxs-lookup"><span data-stu-id="a5fa6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a5fa6-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a5fa6-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5fa6-127">Library</span></span><br/> | <dl> <span data-ttu-id="a5fa6-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5fa6-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5fa6-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5fa6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fa6-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a5fa6-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a5fa6-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="a5fa6-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="a5fa6-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="a5fa6-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="a5fa6-134">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
