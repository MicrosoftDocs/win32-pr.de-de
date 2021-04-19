---
description: Versions Token, das einen prozeduralen Textur Fülleffekt in Effekten erzeugt. Dieses Makro wird von den D3DXFillxxxTX-Funktionen verwendet.
ms.assetid: b11b6229-27a3-4813-9642-9e33bcd0da7a
title: D3DXTX_VERSION (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTX_VERSION
api_type:
- HeaderDef
api_location:
- D3DX9Shader.h
ms.openlocfilehash: 05b034a48635e3a5a6d1a3dbdfbabd0fe2933b5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350678"
---
# <a name="d3dxtx_version"></a><span data-ttu-id="89c24-104">D3DXTX- \_ Version</span><span class="sxs-lookup"><span data-stu-id="89c24-104">D3DXTX\_VERSION</span></span>

<span data-ttu-id="89c24-105">Versions Token, das einen prozeduralen Textur Fülleffekt in Effekten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="89c24-105">Version token that creates a procedural texture filler in effects.</span></span> <span data-ttu-id="89c24-106">Dieses Makro wird von den D3DXFillxxxTX-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="89c24-106">This macro is used by the D3DXFillxxxTX functions.</span></span>

``` syntax
#define D3DXTX_VERSION (_Major, _Minor) (('T' << 24) | ('X' << 16) | ((_Major) << 8) | (_Minor))
```

## <a name="return-value"></a><span data-ttu-id="89c24-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89c24-107">Return Value</span></span>

<span data-ttu-id="89c24-108">Das-Makro gibt das prozedurale Textur Versions Token zurück.</span><span class="sxs-lookup"><span data-stu-id="89c24-108">The macro returns the procedural texture version token.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c24-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89c24-109">Requirements</span></span>



| <span data-ttu-id="89c24-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89c24-110">Requirement</span></span> | <span data-ttu-id="89c24-111">Wert</span><span class="sxs-lookup"><span data-stu-id="89c24-111">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c24-112">Header</span><span class="sxs-lookup"><span data-stu-id="89c24-112">Header</span></span><br/> | <dl> <span data-ttu-id="89c24-113"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c24-113"><dt>D3DX9Shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89c24-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c24-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c24-115">Makros</span><span class="sxs-lookup"><span data-stu-id="89c24-115">Macros</span></span>](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[<span data-ttu-id="89c24-116">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="89c24-116">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="89c24-117">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="89c24-117">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> <dt>

[<span data-ttu-id="89c24-118">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="89c24-118">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 




