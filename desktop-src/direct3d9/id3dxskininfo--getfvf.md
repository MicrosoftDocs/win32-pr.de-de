---
description: 'ID3DXSkinInfo::GetFVF-Methode: Ruft den festen Vertexwert der Funktion ab.'
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: ID3DXSkinInfo::GetFVF-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107158"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="fe3d4-103">ID3DXSkinInfo::GetFVF-Methode</span><span class="sxs-lookup"><span data-stu-id="fe3d4-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="fe3d4-104">Ruft den vertex-Wert der festen Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe3d4-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="fe3d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe3d4-106">Parameters</span></span>

<span data-ttu-id="fe3d4-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe3d4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe3d4-108">Return value</span></span>

<span data-ttu-id="fe3d4-109">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe3d4-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe3d4-110">Gibt die Codes des flexiblen Vertexformats (FVF) zurück.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3d4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe3d4-111">Remarks</span></span>

<span data-ttu-id="fe3d4-112">Diese Methode kann 0 zurückgeben, wenn das Scheitelpunktformat nicht direkt einem FVF-Code zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="fe3d4-113">Dies tritt bei einem Gitternetz auf, das aus einer Scheitelpunktdeklaration erstellt wurde, die nicht die gleiche Reihenfolge und dieselben Elemente aufwies, die von den FVF-Codes unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fe3d4-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3d4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe3d4-114">Requirements</span></span>



| <span data-ttu-id="fe3d4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe3d4-115">Requirement</span></span> | <span data-ttu-id="fe3d4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fe3d4-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3d4-117">Header</span><span class="sxs-lookup"><span data-stu-id="fe3d4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fe3d4-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe3d4-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe3d4-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe3d4-119">Library</span></span><br/> | <dl> <span data-ttu-id="fe3d4-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe3d4-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe3d4-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe3d4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe3d4-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fe3d4-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="fe3d4-123">**ID3DXSkinInfo::SetFVF**</span><span class="sxs-lookup"><span data-stu-id="fe3d4-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
