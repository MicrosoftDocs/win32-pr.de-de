---
description: Gibt die Größe eines Scheitel Punkts für ein flexibles Vertex-Format (FVF) zurück.
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: D3DXGetFVFVertexSize-Funktion (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd5dbe5a58faf385d6f9f50f2fcb4a01a7c01dc5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353724"
---
# <a name="d3dxgetfvfvertexsize-function"></a><span data-ttu-id="3bd24-103">D3DXGetFVFVertexSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="3bd24-103">D3DXGetFVFVertexSize function</span></span>

<span data-ttu-id="3bd24-104">Gibt die Größe eines Scheitel Punkts für ein flexibles Vertex-Format (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="3bd24-104">Returns the size of a vertex for a flexible vertex format (FVF).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bd24-105">Syntax</span></span>


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="3bd24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bd24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd24-107">*F-VF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bd24-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd24-108">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd24-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bd24-109">FVF, die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3bd24-109">FVF to be queried.</span></span> <span data-ttu-id="3bd24-110">Eine Kombination aus [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="3bd24-110">A combination of [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd24-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bd24-111">Return value</span></span>

<span data-ttu-id="3bd24-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bd24-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bd24-113">Die vertexgröße des-Vertex in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3bd24-113">The FVF vertex size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd24-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bd24-114">Requirements</span></span>



| <span data-ttu-id="3bd24-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bd24-115">Requirement</span></span> | <span data-ttu-id="3bd24-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3bd24-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd24-117">Header</span><span class="sxs-lookup"><span data-stu-id="3bd24-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3bd24-118"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bd24-118"><dt>D3dx9mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3bd24-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3bd24-119">Library</span></span><br/> | <dl> <span data-ttu-id="3bd24-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bd24-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bd24-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bd24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd24-122">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3bd24-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
