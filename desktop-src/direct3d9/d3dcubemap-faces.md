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
# <a name="d3dcubemap_faces-enumeration"></a>D3DCUBEMAP \_ Gesichter-Enumeration

Definiert die Gesichter einer cubemap.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_X"></span><span id="d3dcubemap_face_positive_x"></span>**D3DCUBEMAP \_ Gesicht \_ positiv \_ X**
</dt> <dd>

Positive x-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_X"></span><span id="d3dcubemap_face_negative_x"></span>**D3DCUBEMAP \_ Gesicht \_ negativ \_ X**
</dt> <dd>

Negative x-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_Y"></span><span id="d3dcubemap_face_positive_y"></span>**D3DCUBEMAP \_ Gesicht \_ positiv \_ Y**
</dt> <dd>

Positive y-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_Y"></span><span id="d3dcubemap_face_negative_y"></span>**D3DCUBEMAP \_ \_ negative \_ Y-Fläche**
</dt> <dd>

Negative y-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_POSITIVE_Z"></span><span id="d3dcubemap_face_positive_z"></span>**D3DCUBEMAP \_ \_ positive \_ Z**
</dt> <dd>

Positive z-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_NEGATIVE_Z"></span><span id="d3dcubemap_face_negative_z"></span>**D3DCUBEMAP \_ Gesicht \_ negativ \_ Z**
</dt> <dd>

Negative z-Fläche der cubemap.

</dd> <dt>

<span id="D3DCUBEMAP_FACE_FORCE_DWORD"></span><span id="d3dcubemap_face_force_dword"></span>**D3DCUBEMAP \_ Face \_ Force \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DCubeTexture9:: AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
</dt> <dt>

[**IDirect3DCubeTexture9:: getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
</dt> <dt>

[**IDirect3DCubeTexture9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DCubeTexture9:: unlockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-unlockrect)
</dt> </dl>

 

 
