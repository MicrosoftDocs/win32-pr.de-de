---
description: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h) – Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 726a6d7092b95f53d17625f68884b92d347de3a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107838"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a><span data-ttu-id="2996f-103">ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="2996f-103">ID3DXMATRIXStack::RotateYawPitchRollLocal method (D3DX10.h)</span></span>

<span data-ttu-id="2996f-104">Dreht (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="2996f-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2996f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2996f-105">Syntax</span></span>


```C++
HRESULT RotateYawPitchRollLocal(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a><span data-ttu-id="2996f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2996f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2996f-107">*Yaw* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2996f-107">*Yaw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2996f-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2996f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2996f-109">Das Gieren um die y-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="2996f-109">The yaw around the y-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2996f-110">*Pitch* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2996f-110">*Pitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2996f-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2996f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2996f-112">Die Tonhöhe um die X-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="2996f-112">The pitch around the x-axis in radians.</span></span>

</dd> <dt>

<span data-ttu-id="2996f-113">*Roll* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="2996f-113">*Roll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2996f-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2996f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2996f-115">Der Roll um die Z-Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="2996f-115">The roll around the z-axis in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2996f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2996f-116">Return value</span></span>

<span data-ttu-id="2996f-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2996f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2996f-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2996f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2996f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2996f-119">Remarks</span></span>

<span data-ttu-id="2996f-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="2996f-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="2996f-121">Da die Drehung links multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.</span><span class="sxs-lookup"><span data-stu-id="2996f-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="2996f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2996f-122">Requirements</span></span>



| <span data-ttu-id="2996f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2996f-123">Requirement</span></span> | <span data-ttu-id="2996f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2996f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2996f-125">Header</span><span class="sxs-lookup"><span data-stu-id="2996f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2996f-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="2996f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2996f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2996f-127">Library</span></span><br/> | <dl> <span data-ttu-id="2996f-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="2996f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2996f-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2996f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2996f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2996f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2996f-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2996f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
