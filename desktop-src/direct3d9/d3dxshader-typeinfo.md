---
description: Eine hilfsstruktur, die Member-Typinformationen enthält.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: D3DXSHADER_TYPEINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354716"
---
# <a name="d3dxshader_typeinfo-structure"></a>D3DXSHADER \_ TypInfo-Struktur

Eine hilfsstruktur, die Member-Typinformationen enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Klasse**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Shader-Objekttyp. Siehe [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md).

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Datentyp. Siehe [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Matrix Zeilen (Matrizen).

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten (Vektoren und Matrizen).

</dd> <dt>

**Elemente**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Array Dimension.

</dd> <dt>

**Structmembers**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Strukturmembern.

</dd> <dt>

**Structmembership Info**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array von Strukturmember-Informationen, D3DXSHADER \_ structmembership Info \[ *structmembers* \] . Weitere Informationen finden Sie unter [**D3DXSHADER \_ structmembership Info**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Typinformationen sind Teil von [**D3DXSHADER \_ structmembership Info**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ constantinfo**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
