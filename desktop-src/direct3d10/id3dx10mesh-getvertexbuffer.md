---
description: Ruft den dem Mesh zugeordneten Vertex-Puffer ab.
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: 'ID3DX10Mesh:: getvertexbuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b78db368f2467c25b4bb4218a314a22027d5d3f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361228"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="0a3a6-103">ID3DX10Mesh:: getvertexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="0a3a6-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="0a3a6-104">Ruft den dem Mesh zugeordneten Vertex-Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="0a3a6-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a3a6-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0a3a6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a3a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a3a6-107">*ibuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a3a6-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3a6-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a3a6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a3a6-109">Der abzuzurufendene Vertex-Puffer.</span><span class="sxs-lookup"><span data-stu-id="0a3a6-109">The vertex buffer to get.</span></span> <span data-ttu-id="0a3a6-110">Dabei handelt es sich um einen Indexwert.</span><span class="sxs-lookup"><span data-stu-id="0a3a6-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="0a3a6-111">*ppvertexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a3a6-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3a6-112">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0a3a6-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="0a3a6-113">Der Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="0a3a6-113">The vertex buffer.</span></span> <span data-ttu-id="0a3a6-114">Siehe [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="0a3a6-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a3a6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a3a6-115">Return value</span></span>

<span data-ttu-id="0a3a6-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a3a6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a3a6-117">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="0a3a6-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3a6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a3a6-118">Requirements</span></span>



| <span data-ttu-id="0a3a6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a3a6-119">Requirement</span></span> | <span data-ttu-id="0a3a6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="0a3a6-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3a6-121">Header</span><span class="sxs-lookup"><span data-stu-id="0a3a6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0a3a6-122"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a3a6-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a3a6-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a3a6-123">Library</span></span><br/> | <dl> <span data-ttu-id="0a3a6-124"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a3a6-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3a6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a3a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3a6-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="0a3a6-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="0a3a6-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="0a3a6-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
