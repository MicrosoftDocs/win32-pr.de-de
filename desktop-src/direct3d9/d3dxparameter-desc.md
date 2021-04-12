---
description: Beschreibt einen Parameter, der für ein Effect-Objekt verwendet wird.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC-Struktur (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 2256e24daa6dc8b6e5da1528e9a5e5aefce8ec99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219437"
---
# <a name="d3dxparameter_desc-structure"></a>D3DXPARAMETER- \_ Struktur

Beschreibt einen Parameter, der für ein Effect-Objekt verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Name des Parameters.

</dd> <dt>

**Tischer**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Semantik Bedeutung, auch als Verwendung bezeichnet.

</dd> <dt>

**Klasse**
</dt> <dd>

Type: **[ **D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)**

</dd> <dd>

Parameter Klasse. Legen Sie diesen Wert auf einen der Werte in der [**D3DXPARAMETER- \_ Klasse**](./d3dxparameter-class.md)fest.

</dd> <dt>

**Type**
</dt> <dd>

Type: **[ **D3DXPARAMETER- \_ Typ**](./d3dxparameter-type.md)**

</dd> <dd>

Der Parametertyp. Legen Sie diesen Wert auf einen der Werte in [**D3DXPARAMETER \_ Type**](./d3dxparameter-type.md)fest.

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Zeilen im Array.

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten im Array.

</dd> <dt>

**Elemente**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Elemente im Array.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Anmerkungen.

</dd> <dt>

**Structmembers**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Strukturmembern.

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Parameter Attribute. Siehe [Wirkungs Konstanten](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

**Byte**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Größe des Parameters in Byte.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
