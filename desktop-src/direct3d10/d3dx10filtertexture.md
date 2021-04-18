---
description: Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.
ms.assetid: 19e651dd-dc34-405b-8769-00d91c097a1f
title: D3DX10FilterTexture-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10FilterTexture
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: e2f500bcd7f7465ca1c24f1adaab3a77dd5cb7b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365287"
---
# <a name="d3dx10filtertexture-function"></a><span data-ttu-id="3a2d4-103">D3DX10FilterTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a2d4-103">D3DX10FilterTexture function</span></span>

<span data-ttu-id="3a2d4-104">Generiert eine MipMap-Kette mithilfe eines bestimmten Textur Filters.</span><span class="sxs-lookup"><span data-stu-id="3a2d4-104">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a2d4-105">Syntax</span></span>


```C++
HRESULT D3DX10FilterTexture(
   ID3D10Resource *pTexture,
   UINT           SrcLevel,
   UINT           MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="3a2d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a2d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a2d4-107">*ptexture*</span><span class="sxs-lookup"><span data-stu-id="3a2d4-107">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2d4-108">Typ: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="3a2d4-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="3a2d4-109">Das zu filternde Textur Objekt.</span><span class="sxs-lookup"><span data-stu-id="3a2d4-109">The texture object to be filtered.</span></span> <span data-ttu-id="3a2d4-110">Siehe [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="3a2d4-110">See [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="3a2d4-111">*Srclevel*</span><span class="sxs-lookup"><span data-stu-id="3a2d4-111">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2d4-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a2d4-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a2d4-113">Die MipMap-Ebene, deren Daten verwendet werden, um den Rest der MipMap-Kette zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3a2d4-113">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="3a2d4-114">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="3a2d4-114">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3a2d4-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a2d4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a2d4-116">Flags, die Steuern, wie die einzelnen miplevel-Werte gefiltert werden (oder d3dx10 \_ default for d3dx10 \_ Filter \_ Box).</span><span class="sxs-lookup"><span data-stu-id="3a2d4-116">Flags controlling how each miplevel is filtered (or D3DX10\_DEFAULT for D3DX10\_FILTER\_BOX).</span></span> <span data-ttu-id="3a2d4-117">Siehe [**d3dx10 \_ Filter- \_ Flag**](d3dx10-filter-flag.md).</span><span class="sxs-lookup"><span data-stu-id="3a2d4-117">See [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a2d4-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a2d4-118">Return value</span></span>

<span data-ttu-id="3a2d4-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a2d4-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a2d4-120">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="3a2d4-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2d4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a2d4-121">Requirements</span></span>



| <span data-ttu-id="3a2d4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a2d4-122">Requirement</span></span> | <span data-ttu-id="3a2d4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3a2d4-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2d4-124">Header</span><span class="sxs-lookup"><span data-stu-id="3a2d4-124">Header</span></span><br/> | <dl> <span data-ttu-id="3a2d4-125"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a2d4-125"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2d4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a2d4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2d4-127">Textur Funktionen in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="3a2d4-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
