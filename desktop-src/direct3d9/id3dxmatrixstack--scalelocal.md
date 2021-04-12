---
description: Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.
ms.assetid: fe71da67-c8c9-4c78-9055-9bc3cadc0780
title: 'ID3DXMATRIXStack:: scalelocal-Methode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05b188e3f1b0322225584bc0ef7c194c52ef949f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219461"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx9mathh"></a><span data-ttu-id="8af9a-103">ID3DXMATRIXStack:: scalelocal-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8af9a-103">ID3DXMATRIXStack::ScaleLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="8af9a-104">Skalieren Sie die aktuelle Matrix über den Objekt Ursprung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-104">Scale the current matrix about the object origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8af9a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8af9a-105">Syntax</span></span>


```C++
HRESULT ScaleLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="8af9a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8af9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af9a-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8af9a-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af9a-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8af9a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8af9a-109">Die Skalierungs Komponente in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="8af9a-110">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8af9a-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af9a-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8af9a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8af9a-112">Die Skalierungs Komponente in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="8af9a-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8af9a-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8af9a-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8af9a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8af9a-115">Die Skalierungs Komponente in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="8af9a-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af9a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8af9a-116">Return value</span></span>

<span data-ttu-id="8af9a-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8af9a-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8af9a-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8af9a-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af9a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8af9a-119">Remarks</span></span>

<span data-ttu-id="8af9a-120">Diese Methode multipliziert die aktuelle Matrix Links mit der berechneten Skalierungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="8af9a-120">This method left-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="8af9a-121">Die Transformation ist der lokale Ursprung des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8af9a-121">The transformation is about the local origin of the object.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="8af9a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8af9a-122">Requirements</span></span>



| <span data-ttu-id="8af9a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8af9a-123">Requirement</span></span> | <span data-ttu-id="8af9a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8af9a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8af9a-125">Header</span><span class="sxs-lookup"><span data-stu-id="8af9a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8af9a-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8af9a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8af9a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8af9a-127">Library</span></span><br/> | <dl> <span data-ttu-id="8af9a-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8af9a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8af9a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8af9a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8af9a-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="8af9a-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="8af9a-131">**ID3DXMATRIXStack:: Scale**</span><span class="sxs-lookup"><span data-stu-id="8af9a-131">**ID3DXMATRIXStack::Scale**</span></span>](id3dxmatrixstack--scale.md)
</dt> </dl>

 

 
