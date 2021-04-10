---
description: Ruft den Scheitelpunkt Wert fester Funktion ab.
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'ID3DXBaseMesh:: getf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961642"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="891fe-103">ID3DXBaseMesh:: getf VF-Methode</span><span class="sxs-lookup"><span data-stu-id="891fe-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="891fe-104">Ruft den Scheitelpunkt Wert fester Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="891fe-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="891fe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="891fe-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="891fe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="891fe-106">Parameters</span></span>

<span data-ttu-id="891fe-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="891fe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="891fe-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="891fe-108">Return value</span></span>

<span data-ttu-id="891fe-109">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="891fe-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="891fe-110">Gibt die flexiblen Vertexformatcodes (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="891fe-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="891fe-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="891fe-111">Remarks</span></span>

<span data-ttu-id="891fe-112">Diese Methode kann 0 zurückgeben, wenn das Vertex-Format nicht direkt einem FVF-Code zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="891fe-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="891fe-113">Dies geschieht bei einem Mesh, das aus einer Scheitelpunkt Deklaration erstellt wurde, die nicht die gleiche Reihenfolge und dieselben Elemente hat, die von den f</span><span class="sxs-lookup"><span data-stu-id="891fe-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="891fe-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="891fe-114">Requirements</span></span>



| <span data-ttu-id="891fe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="891fe-115">Requirement</span></span> | <span data-ttu-id="891fe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="891fe-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="891fe-117">Header</span><span class="sxs-lookup"><span data-stu-id="891fe-117">Header</span></span><br/>  | <dl> <span data-ttu-id="891fe-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="891fe-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="891fe-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="891fe-119">Library</span></span><br/> | <dl> <span data-ttu-id="891fe-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="891fe-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="891fe-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="891fe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891fe-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="891fe-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
