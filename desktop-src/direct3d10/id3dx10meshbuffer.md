---
description: Ein Gitter Puffer ist ein Puffer, der Daten zu einem Mesh enthält.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: ID3DX10MeshBuffer-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366644"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="6f830-103">ID3DX10MeshBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6f830-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="6f830-104">Ein Gitter Puffer ist ein Puffer, der Daten zu einem Mesh enthält.</span><span class="sxs-lookup"><span data-stu-id="6f830-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="6f830-105">Sie kann einen von fünf verschiedenen Datentypen enthalten: Vertex-Daten, Indexdaten, Daten der Daten, Attributdaten oder Punkt-Rep-Daten.</span><span class="sxs-lookup"><span data-stu-id="6f830-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="6f830-106">Die-Struktur wird für den Zugriff auf diese fünf Datenelemente über die folgenden fünf APIs verwendet: [**ID3DX10Mesh:: getvertexbuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: getindexbuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: gettribuencybuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: getattributebuffer**](id3dx10mesh-getattributebuffer.md)oder [**ID3DX10Mesh:: getpointrepbuffer**](id3dx10mesh-getpointrepbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6f830-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="6f830-107">Member</span><span class="sxs-lookup"><span data-stu-id="6f830-107">Members</span></span>

<span data-ttu-id="6f830-108">Die **ID3DX10MeshBuffer** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6f830-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6f830-109">**ID3DX10MeshBuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6f830-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="6f830-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6f830-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f830-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="6f830-111">Methods</span></span>

<span data-ttu-id="6f830-112">Die **ID3DX10MeshBuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6f830-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="6f830-113">Methode</span><span class="sxs-lookup"><span data-stu-id="6f830-113">Method</span></span>                                       | <span data-ttu-id="6f830-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f830-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="6f830-115">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="6f830-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="6f830-116">Gibt die Größe des Gitter Puffers in Bytes an.</span><span class="sxs-lookup"><span data-stu-id="6f830-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="6f830-117">**Bilden**</span><span class="sxs-lookup"><span data-stu-id="6f830-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="6f830-118">Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6f830-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="6f830-119">**Unmap**</span><span class="sxs-lookup"><span data-stu-id="6f830-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="6f830-120">Aufheben der Zuordnung eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="6f830-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="6f830-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f830-121">Requirements</span></span>



| <span data-ttu-id="6f830-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f830-122">Requirement</span></span> | <span data-ttu-id="6f830-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6f830-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f830-124">Header</span><span class="sxs-lookup"><span data-stu-id="6f830-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6f830-125"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f830-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f830-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f830-126">Library</span></span><br/> | <dl> <span data-ttu-id="6f830-127"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f830-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f830-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f830-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f830-129">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6f830-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
