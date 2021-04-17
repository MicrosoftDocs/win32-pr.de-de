---
description: Definiert die Gesichter einer cubemap.
ms.assetid: 6d18b410-6f22-4202-86ae-6b3ef85e6f69
title: D3DCUBEMAP_FACES-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCUBEMAP_FACES
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: eaf482f6f98d695f3aea3198948616c05ed01f72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354406"
---
# <a name="d3dcubemap_faces-enumeration"></a><span data-ttu-id="11bca-103">D3DCUBEMAP \_ Gesichter-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11bca-103">D3DCUBEMAP\_FACES enumeration</span></span>

<span data-ttu-id="11bca-104">Definiert die Gesichter einer cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-104">Defines the faces of a cubemap.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11bca-105">Syntax</span></span>


```C++
typedef enum D3DCUBEMAP_FACES { 
  D3DCUBEMAP_FACE_POSITIVE_X   = 0,
  D3DCUBEMAP_FACE_NEGATIVE_X   = 1,
  D3DCUBEMAP_FACE_POSITIVE_Y   = 2,
  D3DCUBEMAP_FACE_NEGATIVE_Y   = 3,
  D3DCUBEMAP_FACE_POSITIVE_Z   = 4,
  D3DCUBEMAP_FACE_NEGATIVE_Z   = 5,
  D3DCUBEMAP_FACE_FORCE_DWORD  = 0xffffffff
} D3DCUBEMAP_FACES, *LPD3DCUBEMAP_FACES;
```



## <a name="constants"></a><span data-ttu-id="11bca-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="11bca-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11bca-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ Gesicht \_ positiv \_ X**</span><span class="sxs-lookup"><span data-stu-id="11bca-107"><span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-108">Positive x-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-108">Positive x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ Gesicht \_ negativ \_ X**</span><span class="sxs-lookup"><span data-stu-id="11bca-109"><span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_X**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-110">Negative x-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-110">Negative x-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ Gesicht \_ positiv \_ Y**</span><span class="sxs-lookup"><span data-stu-id="11bca-111"><span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-112">Positive y-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-112">Positive y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP \_ \_ negative \_ Y-Fläche**</span><span class="sxs-lookup"><span data-stu-id="11bca-113"><span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-114">Negative y-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-114">Negative y-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ \_ positive \_ Z**</span><span class="sxs-lookup"><span data-stu-id="11bca-115"><span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP\_FACE\_POSITIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-116">Positive z-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-116">Positive z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ Gesicht \_ negativ \_ Z**</span><span class="sxs-lookup"><span data-stu-id="11bca-117"><span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP\_FACE\_NEGATIVE\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-118">Negative z-Fläche der cubemap.</span><span class="sxs-lookup"><span data-stu-id="11bca-118">Negative z-face of the cubemap.</span></span>

</dd> <dt>

<span data-ttu-id="11bca-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP \_ Face \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="11bca-119"><span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP\_FACE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="11bca-120">Erzwingt die Kompilierung dieser Enumeration in 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="11bca-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="11bca-121">Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="11bca-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="11bca-122">Dieser Wert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="11bca-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11bca-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11bca-123">Requirements</span></span>



| <span data-ttu-id="11bca-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11bca-124">Requirement</span></span> | <span data-ttu-id="11bca-125">Wert</span><span class="sxs-lookup"><span data-stu-id="11bca-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11bca-126">Header</span><span class="sxs-lookup"><span data-stu-id="11bca-126">Header</span></span><br/> | <dl> <span data-ttu-id="11bca-127"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="11bca-127"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11bca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11bca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11bca-129">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="11bca-129">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="11bca-130">**IDirect3DCubeTexture9:: AddDirtyRect**</span><span class="sxs-lookup"><span data-stu-id="11bca-130">**IDirect3DCubeTexture9::AddDirtyRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[<span data-ttu-id="11bca-131">**IDirect3DCubeTexture9:: getcubemapsurface**</span><span class="sxs-lookup"><span data-stu-id="11bca-131">**IDirect3DCubeTexture9::GetCubeMapSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[<span data-ttu-id="11bca-132">**IDirect3DCubeTexture9:: lockrect**</span><span class="sxs-lookup"><span data-stu-id="11bca-132">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="11bca-133">**IDirect3DCubeTexture9:: unlockrect**</span><span class="sxs-lookup"><span data-stu-id="11bca-133">**IDirect3DCubeTexture9::UnlockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
