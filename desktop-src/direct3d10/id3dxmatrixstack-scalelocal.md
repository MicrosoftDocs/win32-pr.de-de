---
description: 'ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h): Skaliert die aktuelle Matrix über den Objekt ursprung.'
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h)
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
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107778"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a><span data-ttu-id="0407f-103">ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="0407f-103">ID3DXMATRIXStack::ScaleLocal method (D3DX10.h)</span></span>

<span data-ttu-id="0407f-104">Skalieren Sie die aktuelle Matrix über den Objekt-Ursprung.</span><span class="sxs-lookup"><span data-stu-id="0407f-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0407f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0407f-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="0407f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0407f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0407f-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0407f-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0407f-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0407f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0407f-109">Die Skalierungskomponente in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0407f-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="0407f-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0407f-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0407f-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0407f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0407f-112">Die Skalierungskomponente in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0407f-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="0407f-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0407f-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0407f-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0407f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0407f-115">Die Skalierungskomponente in Z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="0407f-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0407f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0407f-116">Return value</span></span>

<span data-ttu-id="0407f-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0407f-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0407f-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0407f-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0407f-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0407f-119">Remarks</span></span>

<span data-ttu-id="0407f-120">Diese Methode multipliziert die aktuelle Matrix mit der berechneten Skalierungsmatrix.</span><span class="sxs-lookup"><span data-stu-id="0407f-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="0407f-121">Bei der Transformation geht es um den lokalen Ursprung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="0407f-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="0407f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0407f-122">Requirements</span></span>



| <span data-ttu-id="0407f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0407f-123">Requirement</span></span> | <span data-ttu-id="0407f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0407f-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0407f-125">Header</span><span class="sxs-lookup"><span data-stu-id="0407f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0407f-126"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="0407f-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0407f-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0407f-127">Library</span></span><br/> | <dl> <span data-ttu-id="0407f-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0407f-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0407f-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0407f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0407f-130">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="0407f-130">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0407f-131">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0407f-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
