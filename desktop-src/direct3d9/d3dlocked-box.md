---
description: Beschreibt ein gesperrtes Feld (Volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX -Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLOCKED_BOX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: deb83c71eb9fe9fa5c69667e6dc48187144fa5c18e1daf084e4a04c1fd213744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750990"
---
# <a name="d3dlocked_box-structure"></a>D3DLOCKED \_ BOX-Struktur

Beschreibt ein gesperrtes Feld (Volume).

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DLOCKED_BOX {
  int  RowPitch;
  int  SlicePitch;
  void *pBits;
} D3DLOCKED_BOX, *LPD3DLOCKED_BOX;
```



## <a name="members"></a>Member

<dl> <dt>

**RowPitch**
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Byteoffset vom linken Rand einer Zeile bis zum linken Rand der nächsten Zeile.

</dd> <dt>

**SlicePitch**
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Byteoffset von der linken oberen Ecke eines Slices zur oberen linken Ecke des nächsten tiefen Slices.

</dd> <dt>

**pBits**
</dt> <dd>

Typ: **\* void**

</dd> <dd>

Zeiger auf den Anfang des Volumefelds. Wenn eine [**D3DBOX**](d3dbox.md) für den LockBox-Aufruf bereitgestellt wurde, werden pBits vom Anfang des Volumes entsprechend versetzt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Volumes können so visualisiert werden, dass sie in Segmente der Breite x Höhe 2D-Oberflächen organisiert sind, die gestapelt sind, um eine Breite x Höhe x Tiefenvolumen zu erstellen. Weitere Informationen finden Sie unter [VolumeTexturressourcen (Direct3D 9).](volume-texture-resources.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
