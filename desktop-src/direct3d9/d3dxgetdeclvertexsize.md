---
description: Gibt die Größe eines Scheitel Punkts aus der Scheitelpunkt Deklaration zurück.
ms.assetid: a2524f96-103e-43ab-bdcb-b99e7402fd89
title: D3DXGetDeclVertexSize-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c962064faa61dc7045b0111c5efbf1d1bea9fd40
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354366"
---
# <a name="d3dxgetdeclvertexsize-function"></a><span data-ttu-id="48d73-103">D3DXGetDeclVertexSize-Funktion</span><span class="sxs-lookup"><span data-stu-id="48d73-103">D3DXGetDeclVertexSize function</span></span>

<span data-ttu-id="48d73-104">Gibt die Größe eines Scheitel Punkts aus der Scheitelpunkt Deklaration zurück.</span><span class="sxs-lookup"><span data-stu-id="48d73-104">Returns the size of a vertex from the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d73-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48d73-105">Syntax</span></span>


```C++
UINT D3DXGetDeclVertexSize(
  _In_ const D3DVERTEXELEMENT9 *pDecl,
  _In_       DWORD             Stream
);
```



## <a name="parameters"></a><span data-ttu-id="48d73-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48d73-107">*pdecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48d73-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48d73-108">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="48d73-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="48d73-109">Ein Zeiger auf die Vertexdeklaration.</span><span class="sxs-lookup"><span data-stu-id="48d73-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="48d73-110">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="48d73-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="48d73-111">*Stream* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48d73-111">*Stream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48d73-112">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48d73-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48d73-113">Der null basierte streamindex.</span><span class="sxs-lookup"><span data-stu-id="48d73-113">The zero-based stream index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48d73-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="48d73-114">Return value</span></span>

<span data-ttu-id="48d73-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48d73-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48d73-116">Die Vertex-Deklarations Größe in Byte.</span><span class="sxs-lookup"><span data-stu-id="48d73-116">The vertex declaration size, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d73-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48d73-117">Requirements</span></span>



| <span data-ttu-id="48d73-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48d73-118">Requirement</span></span> | <span data-ttu-id="48d73-119">Wert</span><span class="sxs-lookup"><span data-stu-id="48d73-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48d73-120">Header</span><span class="sxs-lookup"><span data-stu-id="48d73-120">Header</span></span><br/>  | <dl> <span data-ttu-id="48d73-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="48d73-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="48d73-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="48d73-122">Library</span></span><br/> | <dl> <span data-ttu-id="48d73-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48d73-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48d73-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48d73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d73-125">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="48d73-125">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
