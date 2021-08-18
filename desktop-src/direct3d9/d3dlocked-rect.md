---
description: Beschreibt einen gesperrten rechteckigen Bereich.
ms.assetid: ee5d2ea6-bf98-4b09-bc67-b808ffcb23c6
title: D3DLOCKED_RECT -Struktur (D3D9Types.h)
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
ms.openlocfilehash: b419483329e5461de5bc98b3a37b556e37138a055932b1d6c80d3a19b13ae516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988900"
---
# <a name="d3dlocked_rect-structure"></a>D3DLOCKED \_ RECT-Struktur

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

Typ: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Bytes in einer Zeile der Oberfläche.

</dd> <dt>

**pBits**
</dt> <dd>

Typ: **\* void**

</dd> <dd>

Zeiger auf die gesperrten Bits. Wenn ein [**RECT für**](/previous-versions//dd162897(v=vs.85)) den [**LockRect-Aufruf**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) bereitgestellt wurde, werden pBits vom Anfang der Oberfläche entsprechend versetzt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Tonhöhe für DXTn-Formate ist anders als die, die in DirectX 7 zurückgegeben wurde. Er bezieht sich jetzt auf die Anzahl der Bytes in einer Zeile von Blöcken. Wenn Sie beispielsweise eine Breite von 16 haben, haben Sie eine Tonhöhe von 4 Blöcken (4 8 für \* DXT1, 4 \* 16 für DXT2-5).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**IDirect3DSurface9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect)
</dt> <dt>

[**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
</dt> </dl>

 

 
