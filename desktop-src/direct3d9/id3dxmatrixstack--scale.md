---
description: Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: 'ID3DXMATRIXStack:: Scale-Methode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ed926a55c0dba6f74e819cd89a7fa75f6d087c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132297"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="a7d81-103">ID3DXMATRIXStack:: Scale-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a7d81-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="a7d81-104">Skalieren Sie die aktuelle Matrix über den Ursprung der Welt Koordinate.</span><span class="sxs-lookup"><span data-stu-id="a7d81-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7d81-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a7d81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7d81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d81-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7d81-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d81-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d81-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7d81-109">Die Skalierungs Komponente in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a7d81-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a7d81-110">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7d81-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d81-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d81-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7d81-112">Die Skalierungs Komponente in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a7d81-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a7d81-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7d81-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7d81-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7d81-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7d81-115">Die Skalierungs Komponente in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a7d81-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d81-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7d81-116">Return value</span></span>

<span data-ttu-id="a7d81-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7d81-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7d81-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7d81-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d81-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7d81-119">Remarks</span></span>

<span data-ttu-id="a7d81-120">Mit dieser Methode wird die aktuelle Matrix mit der berechneten Skalierungs Matrix nach rechts multipliziert.</span><span class="sxs-lookup"><span data-stu-id="a7d81-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="a7d81-121">Die Transformation geht über den aktuellen Ursprung der Welt.</span><span class="sxs-lookup"><span data-stu-id="a7d81-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="a7d81-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7d81-122">Requirements</span></span>



| <span data-ttu-id="a7d81-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7d81-123">Requirement</span></span> | <span data-ttu-id="a7d81-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a7d81-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d81-125">Header</span><span class="sxs-lookup"><span data-stu-id="a7d81-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d81-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d81-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a7d81-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a7d81-127">Library</span></span><br/> | <dl> <span data-ttu-id="a7d81-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7d81-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a7d81-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7d81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d81-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a7d81-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a7d81-131">**ID3DXMATRIXStack:: scalelocal**</span><span class="sxs-lookup"><span data-stu-id="a7d81-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
