---
description: Gibt an, wie die Symbol Daten von den Quell-und Ziel Oberflächen in einem Rückruf von composerects kombiniert werden.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: D3DCOMPOSERECTSOP-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370415"
---
# <a name="d3dcomposerectsop-enumeration"></a><span data-ttu-id="5ac43-103">D3DCOMPOSERECTSOP-Enumeration</span><span class="sxs-lookup"><span data-stu-id="5ac43-103">D3DCOMPOSERECTSOP enumeration</span></span>

<span data-ttu-id="5ac43-104">Gibt an, wie die Symbol Daten von den Quell-und Ziel Oberflächen in einem Rückruf von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects)kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="5ac43-104">Specifies how to combine the glyph data from the source and destination surfaces in a call to [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ac43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ac43-105">Syntax</span></span>


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a><span data-ttu-id="5ac43-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="5ac43-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ac43-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS \_ Kopieren**</span><span class="sxs-lookup"><span data-stu-id="5ac43-107"><span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS\_COPY**</span></span>
</dt> <dd>

<span data-ttu-id="5ac43-108">Kopieren Sie die Quelle in das Ziel.</span><span class="sxs-lookup"><span data-stu-id="5ac43-108">Copy the source to the destination.</span></span>

</dd> <dt>

<span data-ttu-id="5ac43-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ oder**</span><span class="sxs-lookup"><span data-stu-id="5ac43-109"><span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS\_OR**</span></span>
</dt> <dd>

<span data-ttu-id="5ac43-110">Bitweises OR-Quelle und-Ziel.</span><span class="sxs-lookup"><span data-stu-id="5ac43-110">Bitwise OR the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="5ac43-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ und**</span><span class="sxs-lookup"><span data-stu-id="5ac43-111"><span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS\_AND**</span></span>
</dt> <dd>

<span data-ttu-id="5ac43-112">Bitweises und die Quelle und das Ziel.</span><span class="sxs-lookup"><span data-stu-id="5ac43-112">Bitwise AND the source and the destination.</span></span>

</dd> <dt>

<span data-ttu-id="5ac43-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS- \_ netzb**</span><span class="sxs-lookup"><span data-stu-id="5ac43-113"><span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS\_NEG**</span></span>
</dt> <dd>

<span data-ttu-id="5ac43-114">Kopieren Sie die negiert-Quelle in das Ziel (DST & ~ src).</span><span class="sxs-lookup"><span data-stu-id="5ac43-114">Copy the negated source to the destination (Dst & ~Src).</span></span>

</dd> <dt>

<span data-ttu-id="5ac43-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ Erzwingen von \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="5ac43-115"><span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="5ac43-116">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="5ac43-116">Reserved.</span></span> <span data-ttu-id="5ac43-117">Wird verwendet, um die Enumeration auf eine Größe von 32 Bits zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="5ac43-117">Used to force enumeration to 32-bits in size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ac43-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ac43-118">Requirements</span></span>



| <span data-ttu-id="5ac43-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ac43-119">Requirement</span></span> | <span data-ttu-id="5ac43-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5ac43-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac43-121">Header</span><span class="sxs-lookup"><span data-stu-id="5ac43-121">Header</span></span><br/> | <dl> <span data-ttu-id="5ac43-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac43-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac43-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ac43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac43-124">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="5ac43-124">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




