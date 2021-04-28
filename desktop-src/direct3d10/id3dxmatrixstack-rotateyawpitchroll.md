---
description: 'ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h): Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.'
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8c4f167f769a1ed46404028916477d6784e4a436
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107828"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a><span data-ttu-id="b7853-103">ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="b7853-103">ID3DXMATRIXStack::RotateYawPitchRoll method (D3DX10.h)</span></span>

<span data-ttu-id="b7853-104">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="b7853-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7853-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7853-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="b7853-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7853-107">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b7853-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7853-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7853-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7853-109">Das Gähnen um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="b7853-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b7853-110">*Tonhöhe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b7853-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7853-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7853-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7853-112">Die Tonhöhe um die x-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="b7853-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b7853-113">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="b7853-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7853-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7853-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7853-115">Das Rollback um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="b7853-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7853-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7853-116">Return value</span></span>

<span data-ttu-id="b7853-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7853-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7853-118">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7853-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7853-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7853-119">Remarks</span></span>

<span data-ttu-id="b7853-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Drehungsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="b7853-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="b7853-121">Da die Drehung mit dem Matrixstapel rechts multipliziert wird, ist die Drehung relativ zum Weltkoordinatenraum.</span><span class="sxs-lookup"><span data-stu-id="b7853-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7853-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7853-122">Requirements</span></span>



| <span data-ttu-id="b7853-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7853-123">Requirement</span></span> | <span data-ttu-id="b7853-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b7853-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7853-125">Header</span><span class="sxs-lookup"><span data-stu-id="b7853-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b7853-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7853-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7853-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7853-127">Library</span></span><br/> | <dl> <span data-ttu-id="b7853-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7853-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7853-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b7853-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7853-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="b7853-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="b7853-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b7853-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
