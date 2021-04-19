---
description: Definiert Schriftart Attribute.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373497"
---
# <a name="d3dx10_font_desc-structure"></a>D3dx10 \_ Font- \_ Struktur Struktur

Definiert Schriftart Attribute.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
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

Anzahl der angeforderten MipMap-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt. Wenn der Wert 1 ist, wird der Textur Bereich identisch mit dem Bildschirmbereich zugeordnet.

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

**Fakename \[ LF- \_ fakesisieren\]**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Eine NULL-terminierte Zeichenfolge, die den Schriftart Namen der Schriftart angibt. Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des abschließenden **null** -Zeichens. Wenn "fakename" eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die mit den anderen angegebenen Attributen übereinstimmt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp "TCHAR" in "WCHAR;" aufgelöst. Andernfalls wird der-Datentyp in char aufgelöst. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, wird der d3dx10 \_ Font \_ DESC-Strukturtyp in einen d3dx10 \_ Schriftart- \_ descw aufgelöst; andernfalls wird der Strukturtyp in eine d3dx10- \_ Schriftart \_ DeScA aufgelöst.

Mögliche Werte der obigen Member werden in der GDI- [LOGFONT](/previous-versions//ms533931(v=vs.85)) -Struktur angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
