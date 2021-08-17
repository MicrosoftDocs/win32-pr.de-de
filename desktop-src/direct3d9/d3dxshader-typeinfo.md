---
description: Eine Hilfsstruktur, die Membertypinformationen enthält.
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: D3DXSHADER_TYPEINFO-Struktur (D3dx9shader.h)
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
ms.openlocfilehash: 2bd62cfc3531442f815a16148e23c281735f29e7097e5aa2b55fb03b0c0341c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731268"
---
# <a name="d3dxshader_typeinfo-structure"></a>D3DXSHADER \_ TYPEINFO-Struktur

Eine Hilfsstruktur, die Membertypinformationen enthält.

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

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Shaderobjekttyp. Siehe [**\_ D3DXPARAMETER-KLASSE.**](./d3dxparameter-class.md)

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Datentyp. Weitere Informationen finden Sie unter [**D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Matrixzeilen (Matrizen).

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten (Vektoren und Matrizen).

</dd> <dt>

**CreateUiDefinition-Elemente**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Arraydimension.

</dd> <dt>

**StructMembers**
</dt> <dd>

Typ: **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Strukturmember.

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Array von Strukturmemberinformationen, D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] . Siehe [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Typinformationen sind Teil von [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
