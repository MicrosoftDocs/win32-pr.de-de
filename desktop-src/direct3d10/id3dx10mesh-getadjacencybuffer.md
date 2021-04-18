---
description: Greifen Sie auf den zutreffungspuffer des Mesh zu.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'ID3DX10Mesh:: getaccessdencybuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355036"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a><span data-ttu-id="7f222-103">ID3DX10Mesh:: getaccessdencybuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="7f222-103">ID3DX10Mesh::GetAdjacencyBuffer method</span></span>

<span data-ttu-id="7f222-104">Greifen Sie auf den zutreffungspuffer des Mesh zu.</span><span class="sxs-lookup"><span data-stu-id="7f222-104">Access the mesh's adjacency buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f222-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f222-105">Syntax</span></span>


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="7f222-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f222-107">*ppency* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7f222-107">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f222-108">Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="7f222-108">Type: **[**ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***</span></span>

<span data-ttu-id="7f222-109">Der annäherungspuffer.</span><span class="sxs-lookup"><span data-stu-id="7f222-109">The adjacency buffer.</span></span> <span data-ttu-id="7f222-110">Siehe [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="7f222-110">See [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f222-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f222-111">Return value</span></span>

<span data-ttu-id="7f222-112">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7f222-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7f222-113">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="7f222-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f222-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f222-114">Requirements</span></span>



| <span data-ttu-id="7f222-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f222-115">Requirement</span></span> | <span data-ttu-id="7f222-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7f222-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f222-117">Header</span><span class="sxs-lookup"><span data-stu-id="7f222-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7f222-118"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f222-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f222-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f222-119">Library</span></span><br/> | <dl> <span data-ttu-id="7f222-120"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f222-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f222-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f222-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f222-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="7f222-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="7f222-123">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7f222-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




