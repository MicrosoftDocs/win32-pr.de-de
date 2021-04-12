---
description: Ruft den Scheitelpunkt Wert fester Funktion ab.
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: 'ID3DXSkinInfo:: getf VF-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6d48cd9cea6efd6cb43e6da6877a7aaf42909c71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354067"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="5e75e-103">ID3DXSkinInfo:: getf VF-Methode</span><span class="sxs-lookup"><span data-stu-id="5e75e-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="5e75e-104">Ruft den Scheitelpunkt Wert fester Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="5e75e-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e75e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e75e-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="5e75e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e75e-106">Parameters</span></span>

<span data-ttu-id="5e75e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5e75e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e75e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e75e-108">Return value</span></span>

<span data-ttu-id="5e75e-109">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e75e-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e75e-110">Gibt die flexiblen Vertexformatcodes (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="5e75e-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e75e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e75e-111">Remarks</span></span>

<span data-ttu-id="5e75e-112">Diese Methode kann 0 zurückgeben, wenn das Vertex-Format nicht direkt einem FVF-Code zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5e75e-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="5e75e-113">Dies geschieht bei einem Mesh, das aus einer Scheitelpunkt Deklaration erstellt wurde, die nicht die gleiche Reihenfolge und dieselben Elemente hat, die von den f</span><span class="sxs-lookup"><span data-stu-id="5e75e-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e75e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e75e-114">Requirements</span></span>



| <span data-ttu-id="5e75e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e75e-115">Requirement</span></span> | <span data-ttu-id="5e75e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5e75e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e75e-117">Header</span><span class="sxs-lookup"><span data-stu-id="5e75e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5e75e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e75e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5e75e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e75e-119">Library</span></span><br/> | <dl> <span data-ttu-id="5e75e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e75e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e75e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e75e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e75e-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5e75e-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="5e75e-123">**ID3DXSkinInfo:: setf VF**</span><span class="sxs-lookup"><span data-stu-id="5e75e-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
