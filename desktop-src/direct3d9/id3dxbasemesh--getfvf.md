---
description: 'ID3DXBaseMesh::GetFVF-Methode: Ruft den festen Vertexwert der Funktion ab.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: ID3DXBaseMesh::GetFVF-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115438"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="f891a-103">ID3DXBaseMesh::GetFVF-Methode</span><span class="sxs-lookup"><span data-stu-id="f891a-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="f891a-104">Ruft den festen Vertexwert der Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="f891a-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f891a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f891a-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="f891a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f891a-106">Parameters</span></span>

<span data-ttu-id="f891a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f891a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f891a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f891a-108">Return value</span></span>

<span data-ttu-id="f891a-109">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f891a-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f891a-110">Gibt die Codes des flexiblen Scheitelpunktformats (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="f891a-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="f891a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f891a-111">Remarks</span></span>

<span data-ttu-id="f891a-112">Diese Methode kann 0 zurückgeben, wenn das Scheitelpunktformat nicht direkt einem FVF-Code zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f891a-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="f891a-113">Dies tritt für ein Gitternetz auf, das aus einer Scheitelpunktdeklaration erstellt wurde, die nicht die gleiche Reihenfolge und die gleichen Elemente hat, die von den FVF-Codes unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f891a-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f891a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f891a-114">Requirements</span></span>



| <span data-ttu-id="f891a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f891a-115">Requirement</span></span> | <span data-ttu-id="f891a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f891a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f891a-117">Header</span><span class="sxs-lookup"><span data-stu-id="f891a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f891a-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="f891a-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f891a-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f891a-119">Library</span></span><br/> | <dl> <span data-ttu-id="f891a-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f891a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f891a-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f891a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f891a-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="f891a-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
