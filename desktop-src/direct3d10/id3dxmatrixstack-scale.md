---
description: Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.
ms.assetid: d0f4b341-b3b6-42e4-84df-78f203c3728e
title: 'ID3DXMATRIXStack:: Scale-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Scale
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 361c1fcbdc3f793bcf3e21d569eee740ca0b4ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367496"
---
# <a name="id3dxmatrixstackscale-method-d3dx10h"></a><span data-ttu-id="2b693-103">ID3DXMATRIXStack:: Scale-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="2b693-103">ID3DXMATRIXStack::Scale method (D3DX10.h)</span></span>

<span data-ttu-id="2b693-104">Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2b693-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b693-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b693-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="2b693-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b693-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b693-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b693-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b693-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b693-109">Die Skalierungs Komponente in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b693-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2b693-110">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b693-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b693-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b693-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b693-112">Die Skalierungs Komponente in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b693-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2b693-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b693-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b693-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b693-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b693-115">Die Skalierungs Komponente in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b693-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b693-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b693-116">Return value</span></span>

<span data-ttu-id="2b693-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b693-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b693-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b693-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b693-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b693-119">Remarks</span></span>

<span data-ttu-id="2b693-120">Mit dieser Methode wird die aktuelle Matrix mit der berechneten Skalierungs Matrix nach rechts multipliziert.</span><span class="sxs-lookup"><span data-stu-id="2b693-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="2b693-121">Die Transformation geht über den aktuellen Ursprung der Welt.</span><span class="sxs-lookup"><span data-stu-id="2b693-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="2b693-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b693-122">Requirements</span></span>



| <span data-ttu-id="2b693-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b693-123">Requirement</span></span> | <span data-ttu-id="2b693-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2b693-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b693-125">Header</span><span class="sxs-lookup"><span data-stu-id="2b693-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2b693-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b693-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b693-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b693-127">Library</span></span><br/> | <dl> <span data-ttu-id="2b693-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b693-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b693-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b693-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b693-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2b693-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2b693-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2b693-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
