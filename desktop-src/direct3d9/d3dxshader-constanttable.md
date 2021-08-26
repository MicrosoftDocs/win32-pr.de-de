---
description: Hilfsstruktur zum Verwalten einer Shaderkonstantentabelle. Dies kann auch mit ID3DXConstantTable erfolgen.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE-Struktur (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027290"
---
# <a name="d3dxshader_constanttable-structure"></a>D3DXSHADER \_ CONSTANTTABLE-Struktur

Hilfsstruktur zum Verwalten einer Shaderkonstantentabelle. Dies kann auch mit [**id3DXConstantTable**](id3dxconstanttable.md)erfolgen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**Größe**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe der -Struktur. Siehe Hinweise.

</dd> <dt>

**Creator**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser Struktur in Bytes zu der Zeichenfolge, die den Namen des Erstellers enthält.

</dd> <dt>

**Version**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Shaderversion.

</dd> <dt>

**Konstanten**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Konstanten.

</dd> <dt>

**ConstantInfo**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array von Konstanteninformationen, D3DXSHADER \_ \[ *CONSTANTINFO-Konstanten.* \] Siehe [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md).

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die [D3DXSHADER-Flags,](d3dxshader-flags.md) die zum Kompilieren des Shaders verwendet werden.

</dd> <dt>

**Target**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset in die Zeichenfolge, die das Ziel enthält.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Shaderkonstanteninformationen sind in einer durch Tabstopps getrennten Tabelle mit Kommentaren enthalten. Alle Offsets werden ab dem Anfang der Struktur in Bytes gemessen. Einträge in der konstanten Tabelle werden in aufsteigender Reihenfolge nach Creator sortiert.

Eine Shaderkonstantentabelle kann mit den [**ID3DXConstantTable-Schnittstellen**](id3dxconstanttable.md) verwaltet werden. Alternativ können Sie die Konstantentabelle mit **D3DXSHADER \_ CONSTANTTABLE** verwalten.

Dieser Größenmember wird häufig mit folgendem Code initialisiert:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
