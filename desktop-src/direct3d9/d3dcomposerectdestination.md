---
description: Gibt das Quell Symbol und den Speicherort in einer Monochrom-Oberfläche an, in die Symbole kopiert werden sollen.
ms.assetid: eda6fc82-6a06-4a59-a3ab-9f7e5c5bb5a1
title: D3DCOMPOSERECTDESTINATION-Struktur (D3d9types. h)
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
ms.openlocfilehash: 56843bc78943a4c76fe4fe0f5e18242728a979c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355167"
---
# <a name="d3dcomposerectdestination-structure"></a>D3DCOMPOSERECTDESTINATION-Struktur

Gibt das Quell Symbol und den Speicherort in einer Monochrom-Oberfläche an, in die Symbole kopiert werden sollen.

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

**Srcrectindex**
</dt> <dd>

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Index bestimmtes Symbol aus dem Scheitelpunkt Puffer, der [**D3DCOMPOSERECTDESC**](d3dcomposerectdesc.md) -Strukturen enthält.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **[ **UShort**](../winprog/windows-data-types.md)**

</dd> <dd>

Reserviert zu Ausrichtungs Zwecken.

</dd> <dt>

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

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird in Aufrufen von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects) verwendet, um anzugeben, dass die Speicherort Symbole kopiert werden sollen und welches bestimmte Symbol kopiert werden soll. Ein Vertex-Puffer (siehe [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)), der mit diesen Strukturen gefüllt ist, wird erstellt, um die Symbol Speicherorte zu enthalten. Ushort-Mitglieder werden verwendet, um den Speicherbedarf so weit wie möglich zu reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
