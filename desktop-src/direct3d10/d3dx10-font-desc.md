---
description: Definiert Schriftartattribute.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: D3DX10_FONT_DESC -Struktur (D3DX10.h)
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
ms.openlocfilehash: f3ee6dea032475eb94a723229751d9523c12d118f7319da8f0296cc8c8c42a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634950"
---
# <a name="d3dx10_font_desc-structure"></a>D3DX10 \_ FONT \_ DESC-Struktur

Definiert Schriftartattribute.

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

Typ: **[ **INT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Zeichenzelle oder des Zeichens der Schriftart in logischen Einheiten.

</dd> <dt>

**Width**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Zeichen in der Schriftart in logischen Einheiten.

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

Anzahl der angeforderten Mipmap-Ebenen. Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt. Wenn der Wert 1 ist, wird der Texturraum identisch mit dem Bildschirmbereich zugeordnet.

</dd> <dt>

**Kursiv**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Legen Sie für eine italische Schriftart auf **TRUE** fest.

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

Tonhöhe und Schriftfamilie der Schriftart.

</dd> <dt>

**FaceName \[ LF \_ FACESIZE\]**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Eine auf NULL beendete Zeichenfolge, die den Schriftartnamen der Schriftart angibt. Die Länge der Zeichenfolge darf 32 Zeichen nicht überschreiten, einschließlich des beendenden **NULL-Zeichens.** Wenn FaceName eine leere Zeichenfolge ist, wird die erste Schriftart verwendet, die den anderen angegebenen Attributen entspricht. Wenn die Compilereinstellungen Unicode erfordern, wird der TCHAR-Datentyp in WCHARauflöset. Andernfalls wird der Datentyp in CHAR auflösen. Siehe Hinweise.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch den Strukturtyp. Wenn Unicode definiert ist, wird der D3DX10 FONT DESC-Strukturtyp in eine D3DX10-SCHRIFTART DESCWauflöst. Andernfalls wird der Strukturtyp in eine \_ \_ \_ \_ D3DX10-SCHRIFTART \_ \_ DESCAauflöset.

Mögliche Werte der oben genannten Member sind in der GDI [LOGFONT-Struktur](/previous-versions//ms533931(v=vs.85)) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
