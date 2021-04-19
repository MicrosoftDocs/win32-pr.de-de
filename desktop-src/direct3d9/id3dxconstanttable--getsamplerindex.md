---
description: Gibt den samplerindex zurück.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: 'ID3DXConstantTable:: getsamplerindex-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366651"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a><span data-ttu-id="a773a-103">ID3DXConstantTable:: getsamplerindex-Methode</span><span class="sxs-lookup"><span data-stu-id="a773a-103">ID3DXConstantTable::GetSamplerIndex method</span></span>

<span data-ttu-id="a773a-104">Gibt den samplerindex zurück.</span><span class="sxs-lookup"><span data-stu-id="a773a-104">Returns the sampler index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a773a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a773a-105">Syntax</span></span>


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a><span data-ttu-id="a773a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a773a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a773a-107">*hconstant* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a773a-107">*hConstant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a773a-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a773a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a773a-109">Der samplerhandle.</span><span class="sxs-lookup"><span data-stu-id="a773a-109">The sampler handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a773a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a773a-110">Return value</span></span>

<span data-ttu-id="a773a-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a773a-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a773a-112">Gibt die samplerindexnummer aus der Konstanten Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="a773a-112">Returns the sampler index number from the constant table.</span></span>

## <a name="requirements"></a><span data-ttu-id="a773a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a773a-113">Requirements</span></span>



| <span data-ttu-id="a773a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a773a-114">Requirement</span></span> | <span data-ttu-id="a773a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a773a-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a773a-116">Header</span><span class="sxs-lookup"><span data-stu-id="a773a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a773a-117"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a773a-117"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a773a-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a773a-118">Library</span></span><br/> | <dl> <span data-ttu-id="a773a-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a773a-119"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a773a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a773a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a773a-121">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a773a-121">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
