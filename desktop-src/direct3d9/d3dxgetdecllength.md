---
description: Gibt die Anzahl der Elemente in der Vertex-Deklaration zurück.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: D3DXGetDeclLength-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5576b4b86d5238d4942e09d605f695c66136799a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353725"
---
# <a name="d3dxgetdecllength-function"></a><span data-ttu-id="fdd12-103">D3DXGetDeclLength-Funktion</span><span class="sxs-lookup"><span data-stu-id="fdd12-103">D3DXGetDeclLength function</span></span>

<span data-ttu-id="fdd12-104">Gibt die Anzahl der Elemente in der Vertex-Deklaration zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd12-104">Returns the number of elements in the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdd12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdd12-105">Syntax</span></span>


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a><span data-ttu-id="fdd12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd12-107">*pdecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdd12-107">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdd12-108">Typ: **Konstanten [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="fdd12-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="fdd12-109">Ein Zeiger auf die Vertexdeklaration.</span><span class="sxs-lookup"><span data-stu-id="fdd12-109">A pointer to the vertex declaration.</span></span> <span data-ttu-id="fdd12-110">Siehe [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="fdd12-110">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd12-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdd12-111">Return value</span></span>

<span data-ttu-id="fdd12-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdd12-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdd12-113">Die Anzahl der Elemente in der Vertex-Deklaration.</span><span class="sxs-lookup"><span data-stu-id="fdd12-113">The number of elements in the vertex declaration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd12-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fdd12-114">Requirements</span></span>



| <span data-ttu-id="fdd12-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fdd12-115">Requirement</span></span> | <span data-ttu-id="fdd12-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fdd12-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd12-117">Header</span><span class="sxs-lookup"><span data-stu-id="fdd12-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fdd12-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdd12-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fdd12-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fdd12-119">Library</span></span><br/> | <dl> <span data-ttu-id="fdd12-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdd12-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fdd12-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fdd12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd12-122">Mesh-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fdd12-122">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
