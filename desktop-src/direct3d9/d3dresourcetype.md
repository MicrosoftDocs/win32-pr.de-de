---
description: Definiert Ressourcentypen.
ms.assetid: 6b360fb1-4a5a-47a2-bef9-d8234770bf0c
title: D3DRESOURCETYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecb6b0c84f884df6441f3272a585ee3e09928661
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489684"
---
# <a name="d3dresourcetype-enumeration"></a><span data-ttu-id="0759b-103">D3DRESOURCETYPE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0759b-103">D3DRESOURCETYPE enumeration</span></span>

<span data-ttu-id="0759b-104">Definiert Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="0759b-104">Defines resource types.</span></span>

## <a name="syntax"></a><span data-ttu-id="0759b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0759b-105">Syntax</span></span>


```C++
typedef enum D3DRESOURCETYPE { 
  D3DRTYPE_SURFACE        = 1,
  D3DRTYPE_VOLUME         = 2,
  D3DRTYPE_TEXTURE        = 3,
  D3DRTYPE_VOLUMETEXTURE  = 4,
  D3DRTYPE_CUBETEXTURE    = 5,
  D3DRTYPE_VERTEXBUFFER   = 6,
  D3DRTYPE_INDEXBUFFER    = 7,
  D3DRTYPE_FORCE_DWORD    = 0x7fffffff
} D3DRESOURCETYPE, *LPD3DRESOURCETYPE;
```



## <a name="constants"></a><span data-ttu-id="0759b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0759b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0759b-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE \_ SURFACE**</span><span class="sxs-lookup"><span data-stu-id="0759b-107"><span id="D3DRTYPE_SURFACE"></span><span id="d3drtype_surface"></span>**D3DRTYPE\_SURFACE**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-108">Surface-Ressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-108">Surface resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE-VOLUME \_**</span><span class="sxs-lookup"><span data-stu-id="0759b-109"><span id="D3DRTYPE_VOLUME"></span><span id="d3drtype_volume"></span>**D3DRTYPE\_VOLUME**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-110">Volumeressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-110">Volume resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE \_ TEXTURE**</span><span class="sxs-lookup"><span data-stu-id="0759b-111"><span id="D3DRTYPE_TEXTURE"></span><span id="d3drtype_texture"></span>**D3DRTYPE\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-112">Texturressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-112">Texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE \_ VOLUMETEXTURE**</span><span class="sxs-lookup"><span data-stu-id="0759b-113"><span id="D3DRTYPE_VOLUMETEXTURE"></span><span id="d3drtype_volumetexture"></span>**D3DRTYPE\_VOLUMETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-114">Volumetexturressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-114">Volume texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE \_ CUBETEXTURE**</span><span class="sxs-lookup"><span data-stu-id="0759b-115"><span id="D3DRTYPE_CubeTexture"></span><span id="d3drtype_cubetexture"></span><span id="D3DRTYPE_CUBETEXTURE"></span>**D3DRTYPE\_CUBETEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-116">Cubetexturressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-116">Cube texture resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE \_ VERTEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="0759b-117"><span id="D3DRTYPE_VERTEXBUFFER"></span><span id="d3drtype_vertexbuffer"></span>**D3DRTYPE\_VERTEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-118">Vertexpufferressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-118">Vertex buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE \_ INDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="0759b-119"><span id="D3DRTYPE_INDEXBUFFER"></span><span id="d3drtype_indexbuffer"></span>**D3DRTYPE\_INDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-120">Indexpufferressource.</span><span class="sxs-lookup"><span data-stu-id="0759b-120">Index buffer resource.</span></span>

</dd> <dt>

<span data-ttu-id="0759b-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0759b-121"><span id="D3DRTYPE_FORCE_DWORD"></span><span id="d3drtype_force_dword"></span>**D3DRTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0759b-122">Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0759b-122">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0759b-123">Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="0759b-123">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0759b-124">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0759b-124">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0759b-125">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0759b-125">Requirements</span></span>



| <span data-ttu-id="0759b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0759b-126">Requirement</span></span> | <span data-ttu-id="0759b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0759b-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0759b-128">Header</span><span class="sxs-lookup"><span data-stu-id="0759b-128">Header</span></span><br/> | <dl> <span data-ttu-id="0759b-129"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="0759b-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0759b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0759b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0759b-131">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0759b-131">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0759b-132">**IDirect3DResource9::GetType**</span><span class="sxs-lookup"><span data-stu-id="0759b-132">**IDirect3DResource9::GetType**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-gettype)
</dt> </dl>

 

 
