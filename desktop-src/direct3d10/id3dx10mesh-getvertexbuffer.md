---
description: 'ID3DX10Mesh::GetVertexBuffer-Methode: Ruft den Vertexpuffer ab, der dem Gitternetz zugeordnet ist.'
ms.assetid: c69a712b-8964-4a5b-a136-3f24060b7fd8
title: ID3DX10Mesh::GetVertexBuffer-Methode (D3DX10.h)
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
ms.openlocfilehash: 8a63b08cf978a65e1fa9999c79b8033436b41fa2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108078"
---
# <a name="id3dx10meshgetvertexbuffer-method"></a><span data-ttu-id="f0c2a-103">ID3DX10Mesh::GetVertexBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="f0c2a-103">ID3DX10Mesh::GetVertexBuffer method</span></span>

<span data-ttu-id="f0c2a-104">Ruft den Vertexpuffer ab, der dem Gitternetz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-104">Retrieves the vertex buffer associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c2a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0c2a-105">Syntax</span></span>


```C++
HRESULT GetVertexBuffer(
  [in]  UINT              iBuffer,
  [out] ID3DX10MeshBuffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="f0c2a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0c2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c2a-107">*iBuffer* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f0c2a-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c2a-108">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f0c2a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f0c2a-109">Der abzurufende Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-109">The vertex buffer to get.</span></span> <span data-ttu-id="f0c2a-110">Dies ist ein Indexwert.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-110">This is an index value.</span></span>

</dd> <dt>

<span data-ttu-id="f0c2a-111">*ppVertexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f0c2a-111">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c2a-112">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0c2a-112">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="f0c2a-113">Der Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-113">The vertex buffer.</span></span> <span data-ttu-id="f0c2a-114">Siehe [ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f0c2a-114">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c2a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0c2a-115">Return value</span></span>

<span data-ttu-id="f0c2a-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0c2a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0c2a-117">Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.</span><span class="sxs-lookup"><span data-stu-id="f0c2a-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c2a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0c2a-118">Requirements</span></span>



| <span data-ttu-id="f0c2a-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0c2a-119">Requirement</span></span> | <span data-ttu-id="f0c2a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f0c2a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c2a-121">Header</span><span class="sxs-lookup"><span data-stu-id="f0c2a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f0c2a-122"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="f0c2a-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0c2a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0c2a-123">Library</span></span><br/> | <dl> <span data-ttu-id="f0c2a-124"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0c2a-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0c2a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f0c2a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c2a-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="f0c2a-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="f0c2a-127">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0c2a-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
