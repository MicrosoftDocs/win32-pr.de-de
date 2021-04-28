---
description: 'ID3DXMATRIXStack::Scale-Methode (D3dx9math.h): Skaliert die aktuelle Matrix über den Ursprung der Weltkoordinaten.'
ms.assetid: 6c4ef625-736e-41a0-8a79-4d71e8685754
title: ID3DXMATRIXStack::Scale-Methode (D3dx9math.h)
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
ms.openlocfilehash: 6d877fccf5bfebfdc1f9cf3943c4334e5b8c7fff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093368"
---
# <a name="id3dxmatrixstackscale-method-d3dx9mathh"></a><span data-ttu-id="a0981-103">ID3DXMATRIXStack::Scale-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="a0981-103">ID3DXMATRIXStack::Scale method (D3dx9math.h)</span></span>

<span data-ttu-id="a0981-104">Skalieren Sie die aktuelle Matrix über den Ursprung der Weltkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="a0981-104">Scale the current matrix about the world coordinate origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0981-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0981-105">Syntax</span></span>


```C++
HRESULT Scale(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="a0981-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0981-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0981-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0981-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0981-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0981-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0981-109">Die Skalierungskomponente in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a0981-109">The scaling component in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a0981-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0981-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0981-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0981-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0981-112">Die Skalierungskomponente in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a0981-112">The scaling component in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="a0981-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0981-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0981-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a0981-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a0981-115">Die Skalierungskomponente in Z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="a0981-115">The scaling component in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0981-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0981-116">Return value</span></span>

<span data-ttu-id="a0981-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a0981-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a0981-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0981-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0981-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0981-119">Remarks</span></span>

<span data-ttu-id="a0981-120">Diese Methode multipliziert die aktuelle Matrix mit der berechneten Skalierungsmatrix.</span><span class="sxs-lookup"><span data-stu-id="a0981-120">This method right-multiplies the current matrix with the computed scale matrix.</span></span> <span data-ttu-id="a0981-121">Bei der Transformation geht es um den aktuellen Ursprung der Welt.</span><span class="sxs-lookup"><span data-stu-id="a0981-121">The transformation is about the current world origin.</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="a0981-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0981-122">Requirements</span></span>



| <span data-ttu-id="a0981-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0981-123">Requirement</span></span> | <span data-ttu-id="a0981-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a0981-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0981-125">Header</span><span class="sxs-lookup"><span data-stu-id="a0981-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a0981-126"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0981-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a0981-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0981-127">Library</span></span><br/> | <dl> <span data-ttu-id="a0981-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a0981-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a0981-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a0981-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0981-130">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="a0981-130">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="a0981-131">**ID3DXMATRIXStack::ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="a0981-131">**ID3DXMATRIXStack::ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)
</dt> </dl>

 

 
