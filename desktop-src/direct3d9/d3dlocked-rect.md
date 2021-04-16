---
description: Beschreibt einen gesperrten rechteckigen Bereich.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_RECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 9242a267085579cce52e66f2b9326a8e6298c87c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530956"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ Rect-Struktur

Beschreibt einen gesperrten rechteckigen Bereich.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DLOCKED_RECT {
  INT  Pitch;
  void *pBits;
} D3DLOCKED_RECT, *LPD3DLOCKED_RECT;
```



## <a name="members"></a>Member

<dl> <dt>

**Neigung**
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Bytes in einer Zeile der-Oberfläche.

</dd> <dt>

**PBITS**
</dt> <dd>

Typ: **void \***

</dd> <dd>

Zeiger auf die gesperrten Bits. Wenn ein [**Rect**](/previous-versions//dd162897(v=vs.85)) für den [**lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) -Befehl bereitgestellt wurde, ist PBITS entsprechend dem Anfang der Oberfläche ausgeglichen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Tonhöhe für DXTn-Formate unterscheidet sich von dem, was in DirectX 7 zurückgegeben wurde. Sie verweist jetzt auf die Anzahl der Bytes in einer Zeile von Blöcken. Wenn Sie z. b. eine Breite von 16 haben, verfügen Sie über eine Höhe von 4 Blöcken (4 \* 8 für DXT1, 4 \* 16 für DXT2-5).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
