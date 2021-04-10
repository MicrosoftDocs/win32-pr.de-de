---
description: Definiert Konstanten, die den Typ des Hintergrund Puffers beschreiben.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: D3DBACKBUFFER_TYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961569"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="49ecc-103">D3DBACKBUFFER- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="49ecc-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="49ecc-104">Definiert Konstanten, die den Typ des Hintergrund Puffers beschreiben.</span><span class="sxs-lookup"><span data-stu-id="49ecc-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ecc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49ecc-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="49ecc-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="49ecc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="49ecc-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER- \_ Typ \_ Mono**</span><span class="sxs-lookup"><span data-stu-id="49ecc-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="49ecc-108">Gibt eine nicht Stereo Austausch Kette an.</span><span class="sxs-lookup"><span data-stu-id="49ecc-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="49ecc-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER- \_ Typ \_ Links**</span><span class="sxs-lookup"><span data-stu-id="49ecc-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="49ecc-110">Gibt die linke Seite eines Stereo Paars in einer Swapkette an.</span><span class="sxs-lookup"><span data-stu-id="49ecc-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="49ecc-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ Type \_ right**</span><span class="sxs-lookup"><span data-stu-id="49ecc-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="49ecc-112">Gibt die Rechte Seite eines Stereo Paars in einer Swapkette an.</span><span class="sxs-lookup"><span data-stu-id="49ecc-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="49ecc-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ Type \_ \_ DWORD erzwingen**</span><span class="sxs-lookup"><span data-stu-id="49ecc-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="49ecc-114">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="49ecc-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="49ecc-115">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="49ecc-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="49ecc-116">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="49ecc-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49ecc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49ecc-117">Remarks</span></span>

<span data-ttu-id="49ecc-118">Direct3D 9 unterstützt keine Stereoansicht, deshalb verwendet Direct3D nicht die Werte D3DBACKBUFFER \_ Type \_ left und D3DBACKBUFFER \_ Type \_ right dieses enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="49ecc-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ecc-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49ecc-119">Requirements</span></span>



| <span data-ttu-id="49ecc-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49ecc-120">Requirement</span></span> | <span data-ttu-id="49ecc-121">Wert</span><span class="sxs-lookup"><span data-stu-id="49ecc-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49ecc-122">Header</span><span class="sxs-lookup"><span data-stu-id="49ecc-122">Header</span></span><br/> | <dl> <span data-ttu-id="49ecc-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ecc-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ecc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ecc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ecc-125">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="49ecc-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="49ecc-126">**IDirect3DDevice9:: GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="49ecc-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="49ecc-127">**IDirect3DSwapChain9:: GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="49ecc-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
