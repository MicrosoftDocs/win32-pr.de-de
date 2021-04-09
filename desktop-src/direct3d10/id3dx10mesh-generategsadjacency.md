---
description: Fügt dem Index Puffer des Netzes Informationen hinzu. Wenn das Mesh an einen Geometry-Shader gesendet werden soll, der die Daten aufnimmt, ist es erforderlich, dass der Index Puffer des Netzes Informationen zu den Daten enthält.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh:: generategsadjacency-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050890"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a><span data-ttu-id="a8b1e-104">ID3DX10Mesh:: generategsadjacency-Methode</span><span class="sxs-lookup"><span data-stu-id="a8b1e-104">ID3DX10Mesh::GenerateGSAdjacency method</span></span>

<span data-ttu-id="a8b1e-105">Fügt dem Index Puffer des Netzes Informationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a8b1e-105">Adds adjacency data to the mesh's index buffer.</span></span> <span data-ttu-id="a8b1e-106">Wenn das Mesh an einen Geometry-Shader gesendet werden soll, der die Daten aufnimmt, ist es erforderlich, dass der Index Puffer des Netzes Informationen zu den Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="a8b1e-106">When the mesh is to be sent to a geometry shader that takes adjacency data, it is neccessary for the mesh's index buffer to contain adjacency data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b1e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8b1e-107">Syntax</span></span>


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a><span data-ttu-id="a8b1e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8b1e-108">Parameters</span></span>

<span data-ttu-id="a8b1e-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a8b1e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8b1e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8b1e-110">Return value</span></span>

<span data-ttu-id="a8b1e-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8b1e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8b1e-112">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a8b1e-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8b1e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8b1e-113">Requirements</span></span>



| <span data-ttu-id="a8b1e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8b1e-114">Requirement</span></span> | <span data-ttu-id="a8b1e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a8b1e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b1e-116">Header</span><span class="sxs-lookup"><span data-stu-id="a8b1e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a8b1e-117"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1e-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8b1e-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8b1e-118">Library</span></span><br/> | <dl> <span data-ttu-id="a8b1e-119"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1e-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8b1e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8b1e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b1e-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="a8b1e-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="a8b1e-122">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a8b1e-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




