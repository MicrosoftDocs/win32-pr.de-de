---
description: Gibt das Rechteck an, das verwendet wird, um Symbole auf eine monochrome Oberfläche einzuschließen.
ms.assetid: ce5d492f-38d1-4e7b-a9c2-68c791c84d0c
title: D3DCOMPOSERECTDESC-Struktur (D3d9types. h)
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
ms.openlocfilehash: cf9ad5f1c075f4dc52d68b894b37c7d0f0a7b310
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394078"
---
# <a name="d3dcomposerectdesc-structure"></a>D3DCOMPOSERECTDESC-Struktur

Gibt das Rechteck an, das verwendet wird, um Symbole auf eine monochrome Oberfläche einzuschließen.

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

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Linke Koordinate, um mit dem Kopieren bei zu beginnen.

</dd> <dt>

**J**
</dt> <dd>

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Die obere Koordinate, an der der Kopiervorgang beginnt.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von texeln von linker Koordinate.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl von texeln aus der oberen Koordinate.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in Aufrufen von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um Symbole auf der Quell Oberfläche einzuschließen. Ein Vertex-Puffer (siehe [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), der mit diesen Strukturen gefüllt ist, wird erstellt, um die Symbol Speicherorte zu enthalten. Ushort-Mitglieder werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
