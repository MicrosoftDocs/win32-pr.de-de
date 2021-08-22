---
description: Gibt das Quellglyph und die Position in einer monofarbigen Oberfläche an, in die Glyphen kopiert werden.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: D3DCOMPOSERECTDESTINATION-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESTINATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e6d859cb0bfd47c9be21f37feef287b38cdce4cc64360dd312b2b52bb825a23e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123310"
---
# <a name="d3dcomposerectdestination-structure"></a>D3DCOMPOSERECTDESTINATION-Struktur

Gibt das Quellglyph und die Position in einer monofarbigen Oberfläche an, in die Glyphen kopiert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DCOMPOSERECTDESTINATION {
  USHORT SrcRectIndex;
  USHORT Reserved;
  USHORT X;
  USHORT Y;
} D3DCOMPOSERECTDESTINATION;
```



## <a name="members"></a>Member

<dl> <dt>

**SrcRectIndex**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Index eines bestimmten Glyphen aus dem Scheitelpunktpuffer, der [**D3DCOMPOSERECTDESC-Strukturen**](d3dcomposerectdesc.md) enthält.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Für Ausrichtungszwecke reserviert.

</dd> <dt>

**X**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Linke Koordinate, um mit dem Kopieren zu beginnen.

</dd> <dt>

**J**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Obere Koordinate, an der mit dem Kopieren begonnen werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in Aufrufen von [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um anzugeben, in welche Position glyphen kopiert werden sollen und welches bestimmte Glyph kopiert werden soll. Ein Mit diesen Strukturen gefüllter Scheitelpunktpuffer (siehe [**IDirect3DVertexBuffer9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)wird erstellt, um die Glyphenpositionen zu enthalten. USHORT-Member werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
