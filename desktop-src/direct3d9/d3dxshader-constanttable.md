---
description: Hilfsstruktur zum Verwalten einer shaderkonstantentabelle. Dies kann auch mithilfe von ID3DXConstantTable erfolgen.
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: D3DXSHADER_CONSTANTTABLE-Struktur (D3dx9shader. h)
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
ms.openlocfilehash: ef4fe6cf9af924d9ae6c358f72bf49f93d85f29d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367363"
---
# <a name="d3dxshader_constanttable-structure"></a>D3DXSHADER \_ constanables-Struktur

Hilfsstruktur zum Verwalten einer shaderkonstantentabelle. Dies kann auch mithilfe von [**ID3DXConstantTable**](id3dxconstanttable.md)erfolgen.

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

Größe der Struktur. Siehe Hinweise.

</dd> <dt>

**Creator**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die den Namen des Erstellers enthält.

</dd> <dt>

**Version**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Shader-Version.

</dd> <dt>

**Konstanten**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Konstanten.

</dd> <dt>

**Constantinfo**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array konstanter Informationen, D3DXSHADER \_ constantinfo \[ *Konstanten* \] . Weitere Informationen finden Sie unter [**D3DXSHADER \_ constantinfo**](d3dxshader-constantinfo.md).

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die [D3DXSHADER Flags](d3dxshader-flags.md) -Flags, mit denen der Shader kompiliert wird.

</dd> <dt>

**Target**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset in der Zeichenfolge, die das Ziel enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Shader-konstanteninformationen sind in einer durch Tabstopps getrennten Tabelle mit Kommentaren enthalten. Alle Offsets werden in Bytes vom Anfang der Struktur gemessen. Einträge in der Konstanten Tabelle werden nach Ersteller in aufsteigender Reihenfolge sortiert.

Eine Shader-Konstante Tabelle kann mit den [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstellen verwaltet werden. Alternativ dazu können Sie die Konstante Tabelle mit **D3DXSHADER \_ CONSTAN/verwalten**.

Dieses Größen Element wird häufig mit folgendem initialisiert:


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
