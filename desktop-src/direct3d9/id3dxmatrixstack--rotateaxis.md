---
description: 'ID3DXMATRIXStack::RotateAxis-Methode (D3dx9math.h): Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.'
ms.assetid: b7ae5195-a2af-429f-9a0d-51cd7e955362
title: ID3DXMATRIXStack::RotateAxis-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ea62b65bca73eb3fe7b2cd962e1afd9b35d53bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093488"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx9mathh"></a><span data-ttu-id="5117c-103">ID3DXMATRIXStack::RotateAxis-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5117c-103">ID3DXMATRIXStack::RotateAxis method (D3dx9math.h)</span></span>

<span data-ttu-id="5117c-104">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="5117c-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5117c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5117c-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="5117c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5117c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5117c-107">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5117c-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5117c-108">Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5117c-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5117c-109">Zeiger auf die beliebige Drehachse.</span><span class="sxs-lookup"><span data-stu-id="5117c-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="5117c-110">Siehe [**D3DXVECTOR3.**](d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="5117c-110">See [**D3DXVECTOR3**](d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="5117c-111">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5117c-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5117c-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5117c-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5117c-113">Drehwinkel um die beliebige Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="5117c-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="5117c-114">Winkel werden gegen den Uhrzeigersinn gemessen, wenn entlang der beliebigen Achse zum Ursprung gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="5117c-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5117c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5117c-115">Return value</span></span>

<span data-ttu-id="5117c-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5117c-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5117c-117">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5117c-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5117c-118">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5117c-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5117c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5117c-119">Remarks</span></span>

<span data-ttu-id="5117c-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Drehungsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="5117c-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="5117c-121">Da die Drehung mit dem Matrixstapel rechts multipliziert wird, ist die Drehung relativ zum Weltkoordinatenraum.</span><span class="sxs-lookup"><span data-stu-id="5117c-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="5117c-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5117c-122">Requirements</span></span>



| <span data-ttu-id="5117c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5117c-123">Requirement</span></span> | <span data-ttu-id="5117c-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5117c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5117c-125">Header</span><span class="sxs-lookup"><span data-stu-id="5117c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5117c-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5117c-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5117c-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5117c-127">Library</span></span><br/> | <dl> <span data-ttu-id="5117c-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5117c-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5117c-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5117c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5117c-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5117c-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5117c-131">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="5117c-131">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="5117c-132">**ID3DXMATRIXStack::RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="5117c-132">**ID3DXMATRIXStack::RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[<span data-ttu-id="5117c-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="5117c-133">**ID3DXMATRIXStack::RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> <dt>

[<span data-ttu-id="5117c-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="5117c-134">**ID3DXMATRIXStack::RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
