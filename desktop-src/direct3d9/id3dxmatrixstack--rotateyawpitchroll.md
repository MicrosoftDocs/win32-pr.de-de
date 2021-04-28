---
description: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h) – Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h)
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
ms.openlocfilehash: 8bb516e759e781ca3784e49253eeaddac68075bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107378"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a><span data-ttu-id="5663b-103">ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5663b-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3dx9math.h)</span></span>

<span data-ttu-id="5663b-104">Dreht (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="5663b-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5663b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5663b-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="5663b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5663b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5663b-107">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5663b-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5663b-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5663b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5663b-109">Das Gieren um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="5663b-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5663b-110">*Pitch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5663b-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5663b-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5663b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5663b-112">Die Tonhöhe um die X-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="5663b-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="5663b-113">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5663b-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5663b-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5663b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5663b-115">Der Roll um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="5663b-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5663b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5663b-116">Return value</span></span>

<span data-ttu-id="5663b-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5663b-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5663b-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5663b-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5663b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5663b-119">Remarks</span></span>

<span data-ttu-id="5663b-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="5663b-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="5663b-121">Da die Drehung rechts multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum Weltkoordinatenraum.</span><span class="sxs-lookup"><span data-stu-id="5663b-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5663b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5663b-122">Requirements</span></span>



| <span data-ttu-id="5663b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5663b-123">Requirement</span></span> | <span data-ttu-id="5663b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5663b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5663b-125">Header</span><span class="sxs-lookup"><span data-stu-id="5663b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5663b-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5663b-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5663b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5663b-127">Library</span></span><br/> | <dl> <span data-ttu-id="5663b-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5663b-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5663b-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5663b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5663b-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5663b-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5663b-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5663b-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5663b-132">**ID3DXMATRIXStack::RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="5663b-132">**ID3DXMATRIXStack::RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[<span data-ttu-id="5663b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="5663b-133">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="5663b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="5663b-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
