---
description: Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: 'ID3DXMATRIXStack:: scalelocal-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 868aae418ebedbc54cb8f15ba4fa4e11d47c7f50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870192"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="10c1e-103">ID3DXMATRIXStack:: scalelocal-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="10c1e-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="10c1e-104">Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.</span><span class="sxs-lookup"><span data-stu-id="10c1e-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10c1e-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="10c1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10c1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c1e-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10c1e-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c1e-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c1e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c1e-109">Die Skalierungs Komponente in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="10c1e-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="10c1e-110">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10c1e-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c1e-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c1e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c1e-112">Die Skalierungs Komponente in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="10c1e-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="10c1e-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10c1e-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c1e-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c1e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c1e-115">Die Skalierungs Komponente in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="10c1e-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c1e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10c1e-116">Return value</span></span>

<span data-ttu-id="10c1e-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="10c1e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="10c1e-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="10c1e-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c1e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10c1e-119">Remarks</span></span>

<span data-ttu-id="10c1e-120">Diese Methode multipliziert die aktuelle Matrix Links mit der berechneten Skalierungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="10c1e-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="10c1e-121">Die Transformation ist der lokale Ursprung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="10c1e-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="10c1e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10c1e-122">Requirements</span></span>



| <span data-ttu-id="10c1e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10c1e-123">Requirement</span></span> | <span data-ttu-id="10c1e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="10c1e-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10c1e-125">Header</span><span class="sxs-lookup"><span data-stu-id="10c1e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="10c1e-126"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c1e-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="10c1e-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10c1e-127">Library</span></span><br/> | <dl> <span data-ttu-id="10c1e-128"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10c1e-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c1e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10c1e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c1e-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="10c1e-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="10c1e-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="10c1e-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
