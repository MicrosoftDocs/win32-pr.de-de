---
description: Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'ID3DXMATRIXStack:: rotateaxis-Methode (d3dx10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: badd26d61fa6580b0193039e29a8fceedabe2d3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355997"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="c0cdd-103">ID3DXMATRIXStack:: rotateaxis-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="c0cdd-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="c0cdd-104">Rotiert (relativ zum globalen Koordinaten Bereich) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cdd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0cdd-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="c0cdd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0cdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0cdd-107">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0cdd-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0cdd-108">Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0cdd-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c0cdd-109">Zeiger auf die beliebige Achse der Drehung.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="c0cdd-110">Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span><span class="sxs-lookup"><span data-stu-id="c0cdd-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0cdd-111">*Winkel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0cdd-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0cdd-112">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0cdd-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0cdd-113">Drehwinkel für die beliebige Achse im Bogenmaße.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="c0cdd-114">Winkel werden bei der Betrachtung der beliebigen Achse zum Ursprung gegen den Uhrzeigersinn gemessen.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0cdd-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0cdd-115">Return value</span></span>

<span data-ttu-id="c0cdd-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0cdd-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0cdd-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0cdd-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0cdd-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0cdd-119">Remarks</span></span>

<span data-ttu-id="c0cdd-120">Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="c0cdd-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="c0cdd-121">Da die Drehung mit dem Matrix Stapel rechts multipliziert ist, ist die Drehung relativ zum globalen Koordinaten Bereich.</span><span class="sxs-lookup"><span data-stu-id="c0cdd-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0cdd-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0cdd-122">Requirements</span></span>



| <span data-ttu-id="c0cdd-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0cdd-123">Requirement</span></span> | <span data-ttu-id="c0cdd-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0cdd-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0cdd-125">Header</span><span class="sxs-lookup"><span data-stu-id="c0cdd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0cdd-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0cdd-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0cdd-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0cdd-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0cdd-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0cdd-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0cdd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0cdd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0cdd-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="c0cdd-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c0cdd-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c0cdd-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
