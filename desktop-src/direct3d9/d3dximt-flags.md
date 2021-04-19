---
description: Textur Wrapping Optionen für IMT-Berechnungs-APIs.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: D3DXIMT Flags-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366640"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="66265-103">D3DXIMT Flags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="66265-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="66265-104">Textur Wrapping Optionen für IMT-Berechnungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="66265-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="66265-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66265-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="66265-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="66265-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66265-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="66265-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="66265-108">Die Textur wird in die U-Richtung umschlossen.</span><span class="sxs-lookup"><span data-stu-id="66265-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="66265-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="66265-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="66265-110">Die Textur wird in die Richtung V umschlossen.</span><span class="sxs-lookup"><span data-stu-id="66265-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="66265-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT \_ Wrap \_ -UV**</span><span class="sxs-lookup"><span data-stu-id="66265-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="66265-112">Die Textur umschließt sowohl die Richtung "Sie" als auch "V".</span><span class="sxs-lookup"><span data-stu-id="66265-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66265-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66265-113">Requirements</span></span>



| <span data-ttu-id="66265-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66265-114">Requirement</span></span> | <span data-ttu-id="66265-115">Wert</span><span class="sxs-lookup"><span data-stu-id="66265-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66265-116">Header</span><span class="sxs-lookup"><span data-stu-id="66265-116">Header</span></span><br/> | <dl> <span data-ttu-id="66265-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="66265-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66265-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66265-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66265-119">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="66265-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="66265-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="66265-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="66265-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="66265-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="66265-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="66265-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="66265-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="66265-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




