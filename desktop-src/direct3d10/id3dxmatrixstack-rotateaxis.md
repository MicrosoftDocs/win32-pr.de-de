---
description: 'ID3DXMATRIXStack::RotateAxis-Methode (D3DX10.h): Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.'
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: ID3DXMATRIXStack::RotateAxis-Methode (D3DX10.h)
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
ms.openlocfilehash: 0a2e52eed1c1957de9a0fcfed4ba3d3d05f89cb9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107909"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a><span data-ttu-id="c2556-103">ID3DXMATRIXStack::RotateAxis-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="c2556-103">ID3DXMATRIXStack::RotateAxis method (D3DX10.h)</span></span>

<span data-ttu-id="c2556-104">Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.</span><span class="sxs-lookup"><span data-stu-id="c2556-104">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2556-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2556-105">Syntax</span></span>


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a><span data-ttu-id="c2556-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2556-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2556-107">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c2556-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2556-108">Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2556-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c2556-109">Zeiger auf die beliebige Drehachse.</span><span class="sxs-lookup"><span data-stu-id="c2556-109">Pointer to the arbitrary axis of rotation.</span></span> <span data-ttu-id="c2556-110">Siehe [**D3DXVECTOR3.**](d3d10-d3dxvector3.md)</span><span class="sxs-lookup"><span data-stu-id="c2556-110">See [**D3DXVECTOR3**](d3d10-d3dxvector3.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2556-111">*Winkel* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c2556-111">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2556-112">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2556-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2556-113">Drehwinkel um die beliebige Achse im Bogenmaß.</span><span class="sxs-lookup"><span data-stu-id="c2556-113">Rotation angle about the arbitrary axis, in radians.</span></span> <span data-ttu-id="c2556-114">Winkel werden gegen den Uhrzeigersinn gemessen, wenn entlang der beliebigen Achse zum Ursprung gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="c2556-114">Angles are measured counterclockwise when looking along the arbitrary axis toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2556-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2556-115">Return value</span></span>

<span data-ttu-id="c2556-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2556-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2556-117">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2556-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c2556-118">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="c2556-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2556-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2556-119">Remarks</span></span>

<span data-ttu-id="c2556-120">Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Drehungsmatrix ähnlich der folgenden hinzu:</span><span class="sxs-lookup"><span data-stu-id="c2556-120">This method adds the rotation to the matrix stack with the computed rotation matrix similar to the following:</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



<span data-ttu-id="c2556-121">Da die Drehung mit dem Matrixstapel rechts multipliziert wird, ist die Drehung relativ zum Weltkoordinatenraum.</span><span class="sxs-lookup"><span data-stu-id="c2556-121">Because the rotation is right-multiplied to the matrix stack, the rotation is relative to world coordinate space.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2556-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2556-122">Requirements</span></span>



| <span data-ttu-id="c2556-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2556-123">Requirement</span></span> | <span data-ttu-id="c2556-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c2556-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2556-125">Header</span><span class="sxs-lookup"><span data-stu-id="c2556-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c2556-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c2556-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2556-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2556-127">Library</span></span><br/> | <dl> <span data-ttu-id="c2556-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2556-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2556-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c2556-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2556-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="c2556-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c2556-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c2556-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
