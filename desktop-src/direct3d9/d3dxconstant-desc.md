---
description: Eine Beschreibung einer Konstante in einer Konstanten Tabelle.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370464"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT- \_ Struktur

Eine Beschreibung einer Konstante in einer Konstanten Tabelle.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Name der Konstanten.

</dd> <dt>

**Register Set**
</dt> <dd>

Typ: **[ **D3DXREGISTER \_ set**](./d3dxregister-set.md)**

</dd> <dd>

Konstanter Datentyp. Siehe [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**Register Index**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

NULL basierter Index der Konstante in der Tabelle.

</dd> <dt>

**Register count**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Register, die Daten enthalten.

</dd> <dt>

**Klasse**
</dt> <dd>

Type: **[ **D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)**

</dd> <dd>

Parameter Klasse. Siehe [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md).

</dd> <dt>

**Type**
</dt> <dd>

Type: **[ **D3DXPARAMETER- \_ Typ**](./d3dxparameter-type.md)**

</dd> <dd>

Der Parametertyp. Siehe [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Zeilen.

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten.

</dd> <dt>

**Elemente**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Elemente im Array.

</dd> <dt>

**Structmembers**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der unter Parameter für Strukturmember.

</dd> <dt>

**Byte**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Datengröße in Byte Anzahl.

</dd> <dt>

**DefaultValue**
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf den Standardwert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE- \_ Abteilung**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
