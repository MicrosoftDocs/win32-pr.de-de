---
description: 'ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h): Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.'
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h)
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
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107878"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a><span data-ttu-id="e7f09-103">ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="e7f09-103">ID3DXMATRIXStack::RotateAxisLocal method (D3DX10.h)</span></span>

<span data-ttu-id="e7f09-104">Dreht (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="e7f09-104">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f09-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7f09-105">Syntax</span></span>


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="e7f09-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7f09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f09-107">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e7f09-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f09-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7f09-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e7f09-109">Zeiger auf die beliebige Drehachse.</span><span class="sxs-lookup"><span data-stu-id="e7f09-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="e7f09-110">Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="e7f09-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7f09-111">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e7f09-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f09-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7f09-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7f09-113">Drehwinkel um die beliebige Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="e7f09-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="e7f09-114">Winkel werden gegen den Uhrzeigersinn gemessen, wenn entlang der beliebigen Achse zum Ursprung gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="e7f09-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f09-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7f09-115">Return value</span></span>

<span data-ttu-id="e7f09-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7f09-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7f09-117">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7f09-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7f09-118">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="e7f09-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f09-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7f09-119">Remarks</span></span>

<span data-ttu-id="e7f09-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="e7f09-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



<span data-ttu-id="e7f09-121">Da die Drehung links multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.</span><span class="sxs-lookup"><span data-stu-id="e7f09-121">Because the rotation is left-multiplied to the matrix stack, the rotation is relative to the object's local coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f09-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7f09-122">Requirements</span></span>



| <span data-ttu-id="e7f09-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7f09-123">Requirement</span></span> | <span data-ttu-id="e7f09-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e7f09-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f09-125">Header</span><span class="sxs-lookup"><span data-stu-id="e7f09-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f09-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f09-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7f09-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7f09-127">Library</span></span><br/> | <dl> <span data-ttu-id="e7f09-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f09-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f09-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e7f09-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f09-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="e7f09-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e7f09-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e7f09-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
