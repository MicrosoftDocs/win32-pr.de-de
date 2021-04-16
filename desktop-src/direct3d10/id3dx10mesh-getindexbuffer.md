---
description: Ruft die Daten in einem Index Puffer ab.
ms.assetid: 7e25ad67-7f9d-4c23-a029-a2262034ef38
title: 'ID3DX10Mesh:: getindexbuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c2777a9d530ac7217b1cc0f3c0f148998cc70ffe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394133"
---
# <a name="id3dx10meshgetindexbuffer-method"></a><span data-ttu-id="e48a9-103">ID3DX10Mesh:: getindexbuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="e48a9-103">ID3DX10Mesh::GetIndexBuffer method</span></span>

<span data-ttu-id="e48a9-104">Ruft die Daten in einem Index Puffer ab.</span><span class="sxs-lookup"><span data-stu-id="e48a9-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e48a9-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out] ID3DX10MeshBuffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e48a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e48a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e48a9-107">*ppindexbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e48a9-107">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e48a9-108">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e48a9-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="e48a9-109">Adresse eines Zeigers auf eine ID3DX10MeshBuffer-Schnittstelle, die den dem Mesh zugeordneten Index Puffer darstellt.</span><span class="sxs-lookup"><span data-stu-id="e48a9-109">Address of a pointer to a ID3DX10MeshBuffer interface, representing the index buffer associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e48a9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e48a9-110">Return value</span></span>

<span data-ttu-id="e48a9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e48a9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e48a9-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e48a9-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e48a9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e48a9-113">Requirements</span></span>



| <span data-ttu-id="e48a9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e48a9-114">Requirement</span></span> | <span data-ttu-id="e48a9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e48a9-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e48a9-116">Header</span><span class="sxs-lookup"><span data-stu-id="e48a9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e48a9-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48a9-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e48a9-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e48a9-118">Library</span></span><br/> | <dl> <span data-ttu-id="e48a9-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e48a9-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48a9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e48a9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48a9-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e48a9-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e48a9-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e48a9-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




