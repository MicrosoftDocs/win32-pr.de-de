---
description: Gibt das Rechteck an, das verwendet wird, um Glyphen auf einer monofarbenen Oberfläche einzuschließen.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: D3DCOMPOSERECTDESC-Struktur (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTDESC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8c23868e8759b98898013ea70d8d62768f1e648eb6e5019eb52dd21ba55905b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733203"
---
# <a name="d3dcomposerectdesc-structure"></a>D3DCOMPOSERECTDESC-Struktur

Gibt das Rechteck an, das verwendet wird, um Glyphen auf einer monofarbenen Oberfläche einzuschließen.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DCOMPOSERECTDESC {
  USHORT X;
  USHORT Y;
  USHORT Width;
  USHORT Height;
} D3DCOMPOSERECTDESC;
```



## <a name="members"></a>Member

<dl> <dt>

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

Die oberste Koordinate, an der mit dem Kopieren begonnen werden soll.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Texel von der linken Koordinate.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **USHORT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Texel aus der obersten Koordinate.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird in Aufrufen von [**ComposeRects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um Glyphen auf der Quelloberfläche einzuschließen. Ein Vertexpuffer (siehe [**IDirect3DVertexBuffer9),**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)der mit diesen Strukturen gefüllt ist, wird erstellt, um die Glyphenpositionen zu enthalten. USHORT-Member werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
