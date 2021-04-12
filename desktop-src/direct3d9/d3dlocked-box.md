---
description: Beschreibt ein gesperrtes Feld (Volume).
ms.assetid: b371fb5e-2d65-453c-acd7-214de8aaa78a
title: D3DLOCKED_BOX-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 41fc5b0fd81405f9f12f65fca4fae53239110bfa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219568"
---
# <a name="d3dlocked_box-structure"></a>D3DLOCKED \_ Box-Struktur

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

**Rowpitch**
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Byte Offset vom linken Rand einer Zeile bis zum linken Rand der nächsten Zeile.

</dd> <dt>

**Slicepitch**
</dt> <dd>

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Byte Offset von der linken oberen Ecke eines Slice bis zum oberen linken Rand des nächst tiefsten Slice.

</dd> <dt>

**PBITS**
</dt> <dd>

Typ: **void \***

</dd> <dd>

Zeiger auf den Anfang des volumefelds. Wenn ein [**D3DBOX**](d3dbox.md) für den Lockbox-Befehl bereitgestellt wurde, ist PBITS entsprechend vom Start des Volumes abweicht.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Volumes können so visualisiert werden, dass Sie in Slices der Breite x Höhe 2D-Oberflächen angeordnet sind, um ein Volume mit einer Breite x-Tiefe zu bilden. Weitere Informationen finden Sie unter [volumetextur-Ressourcen (Direct3D 9)](volume-texture-resources.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DVolume9:: Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**IDirect3DVolumeTexture9:: Lockbox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)
</dt> </dl>

 

 
