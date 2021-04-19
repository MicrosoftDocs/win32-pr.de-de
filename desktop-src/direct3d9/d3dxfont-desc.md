---
description: Definiert die Attribute einer Schriftart.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: D3DXFONT_DESC-Struktur (D3dx9core. h)
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
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351949"
---
# <a name="d3dxfont_desc-structure"></a>D3DXFONT- \_ Struktur

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

Typ: **[ **int**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe (in logischen Einheiten) der Zeichen Zelle oder des Zeichens der Schriftart.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite (in logischen Einheiten) der Zeichen in der Schriftart.

</dd> <dt>

**Weight**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Gewichtung der Schriftart im Bereich von 0 bis 1000.

</dd> <dt>

**MipLevels**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der angeforderten Mip-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt. Wenn der Wert 1 ist, wird der Textur Bereich identisch mit dem Bildschirmbereich zugeordnet.

</dd> <dt>

**Kursiv**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Legen Sie für eine kursiv Schrift auf **true** fest.

</dd> <dt>

**CharSet**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeichensatz.

</dd> <dt>

**Outputprecision**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Ausgabe Genauigkeit. Die Ausgabe Genauigkeit definiert, wie genau die Ausgabe der angeforderten Schrift Höhe, der Breite, der Zeichen Ausrichtung, dem Escapezeichen, der Tonhöhe und dem Schrifttyp entsprechen muss.

</dd> <dt>

**Qualität**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Ausgabequalität.

</dd> <dt>

**PitchAndFamily**
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)**

</dd> <dd>

Tonhöhe und Familie der Schriftart.

</dd> <dt>

**Fakename**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Eine mit NULL endenden Zeichenfolge oder Zeichen, die den Schriftart Namen der Schriftart angibt. Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des abschließenden NULL-Zeichens. Wenn "fakename" eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die mit den anderen angegebenen Attributen übereinstimmt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp "TCHAR" in "WCHAR;" aufgelöst. Andernfalls wird der-Datentyp in char aufgelöst. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, wird der D3DXFONT \_ DESC-Strukturtyp zu einem D3DXFONT- \_ descw aufgelöst; andernfalls wird der Strukturtyp in einen D3DXFONT \_ DeScA aufgelöst.

Mögliche Werte der obigen Member werden in der GDI- [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**GetDesc**](id3dxfont--getdesc.md)
</dt> </dl>

 

 
