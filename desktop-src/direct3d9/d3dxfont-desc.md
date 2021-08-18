---
description: Definiert die Attribute einer Schriftart.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC-Struktur (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: b458d9c3575993dd3d478f886d0b71b3cd5c1af0a53330b0813deafa188ac4c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728540"
---
# <a name="d3dxfont_desc-structure"></a>D3DXFONT \_ DESC-Struktur

Definiert die Attribute einer Schriftart.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Height**
</dt> <dd>

Typ: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Zeichenzelle oder des Zeichens der Schriftart in logischen Einheiten.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite von Zeichen in der Schriftart in logischen Einheiten.

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Gewichtung der Schriftart im Bereich von 0 bis 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der angeforderten MIP-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt. Wenn der Wert 1 ist, wird der Texturraum dem Bildschirmbereich identisch zugeordnet.

</dd> <dt>

**Kursiv**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Legen Sie für eine italische Schriftart **true** fest.

</dd> <dt>

**Charset**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeichensatz.

</dd> <dt>

**OutputPrecision**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Ausgabegenauigkeit. Die Ausgabegenauigkeit definiert, wie genau die Ausgabe mit der angeforderten Schrifthöhe, Breite, Zeichenausrichtung, Escapezeichen, Tonhöhe und Schrifttyp übereinstimmen muss.

</dd> <dt>

**Qualität**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Ausgabequalität.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)**

</dd> <dd>

Tonhöhe und Schriftfamilie.

</dd> <dt>

**GesichtsName**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Eine auf NULL endende Zeichenfolge oder Zeichen, die den Schriftartnamen der Schriftart angibt. Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des abschließenden NULL-Zeichens. Wenn FaceName eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die mit den anderen angegebenen Attributen übereinstimmt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp TCHAR in WCHAR aufgelöst. Andernfalls wird der Datentyp in CHAR aufgelöst. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, wird der D3DXFONT \_ DESC-Strukturtyp in einen D3DXFONT \_ DESCW aufgelöst. Andernfalls wird der Strukturtyp in einen D3DXFONT-DESCA \_ aufgelöst.

Mögliche Werte der oben genannten Member werden in der GDI [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
