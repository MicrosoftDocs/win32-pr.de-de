---
description: Die Anzahl der Scheitel Punkte im Mesh.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh:: getvertexcount-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355035"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="e1967-103">ID3DX10Mesh:: getvertexcount-Methode</span><span class="sxs-lookup"><span data-stu-id="e1967-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="e1967-104">Die Anzahl der Scheitel Punkte im Mesh.</span><span class="sxs-lookup"><span data-stu-id="e1967-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="e1967-105">Ein Mesh kann mehrere Scheitelpunkt Puffer enthalten (d. h., ein Vertex-Puffer enthält möglicherweise alle Positionsdaten, eine andere enthält möglicherweise alle Texturkoordinaten Daten usw.), aber jeder Scheitelpunkt Puffer enthält die gleiche Anzahl von Elementen.</span><span class="sxs-lookup"><span data-stu-id="e1967-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1967-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1967-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="e1967-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1967-107">Parameters</span></span>

<span data-ttu-id="e1967-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e1967-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1967-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1967-109">Return value</span></span>

<span data-ttu-id="e1967-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1967-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1967-111">Die Anzahl der Scheitel Punkte im Mesh.</span><span class="sxs-lookup"><span data-stu-id="e1967-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1967-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1967-112">Requirements</span></span>



| <span data-ttu-id="e1967-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1967-113">Requirement</span></span> | <span data-ttu-id="e1967-114">Wert</span><span class="sxs-lookup"><span data-stu-id="e1967-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1967-115">Header</span><span class="sxs-lookup"><span data-stu-id="e1967-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e1967-116"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1967-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1967-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e1967-117">Library</span></span><br/> | <dl> <span data-ttu-id="e1967-118"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1967-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1967-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1967-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1967-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="e1967-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="e1967-121">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e1967-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
