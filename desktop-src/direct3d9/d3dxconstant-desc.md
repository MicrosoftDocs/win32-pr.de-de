---
description: Eine Beschreibung einer Konstante in einer konstanten Tabelle.
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: D3DXCONSTANT_DESC-Struktur (D3dx9shader.h)
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
ms.openlocfilehash: bdb3b8276711f3165c0c138155eb6e628c19a124d6f9301de7638e5be24d1c1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952450"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT \_ DESC-Struktur

Eine Beschreibung einer Konstante in einer konstanten Tabelle.

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

Name der Konstante.

</dd> <dt>

**RegisterSet**
</dt> <dd>

Typ: **[ **D3DXREGISTER \_ SET**](./d3dxregister-set.md)**

</dd> <dd>

Konstanter Datentyp. Siehe [**D3DXREGISTER \_ SET**](./d3dxregister-set.md).

</dd> <dt>

**RegisterIndex**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Nullbasierter Index der Konstante in der Tabelle.

</dd> <dt>

**RegisterCount**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Register, die Daten enthalten.

</dd> <dt>

**Klasse**
</dt> <dd>

Typ: **[ **D3DXPARAMETER-KLASSE \_**](./d3dxparameter-class.md)**

</dd> <dd>

Parameterklasse. Siehe [**\_ D3DXPARAMETER-KLASSE.**](./d3dxparameter-class.md)

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md)**

</dd> <dd>

Der Parametertyp. Weitere Informationen finden Sie unter [**D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md).

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Zeilen.

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten.

</dd> <dt>

**CreateUiDefinition-Elemente**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Elemente im Array.

</dd> <dt>

**StructMembers**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Unterparameter des Strukturmembers.

</dd> <dt>

**Byte**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Datengröße in Byteanzahl.

</dd> <dt>

**Defaultvalue**
</dt> <dd>

Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf den Standardwert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
