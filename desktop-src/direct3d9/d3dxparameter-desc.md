---
description: Beschreibt einen Parameter, der für ein Effektobjekt verwendet wird.
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: D3DXPARAMETER_DESC -Struktur (D3dx9effect.h)
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
ms.openlocfilehash: a12541e9bfb33979b11f8198e218a3eb474f948aeb8c74982a5369eed782eaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631150"
---
# <a name="d3dxparameter_desc-structure"></a>D3DXPARAMETER \_ DESC-Struktur

Beschreibt einen Parameter, der für ein Effektobjekt verwendet wird.

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

**Semantische**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Semantische Bedeutung, auch als Verwendung bezeichnet.

</dd> <dt>

**Klasse**
</dt> <dd>

Typ: **[ **D3DXPARAMETER-KLASSE \_**](./d3dxparameter-class.md)**

</dd> <dd>

Parameterklasse. Legen Sie dies auf einen der Werte in der [**D3DXPARAMETER-KLASSE \_ fest.**](./d3dxparameter-class.md)

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DXPARAMETER \_ TYPE**](./d3dxparameter-type.md)**

</dd> <dd>

Der Parametertyp. Legen Sie dies auf einen der Werte in [**D3DXPARAMETER \_ TYPE fest.**](./d3dxparameter-type.md)

</dd> <dt>

**Zeilen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Zeilen im Array.

</dd> <dt>

**Spalten**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Spalten im Array.

</dd> <dt>

**CreateUiDefinition-Elemente**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Elemente im Array.

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Anmerkungen.

</dd> <dt>

**StructMembers**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Strukturmitglieder.

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Parameterattribute. Weitere Informationen [finden Sie unter Effektkonst constants ( Effektkonst constants](dx9-graphics-reference-effects-constants.md)).

</dd> <dt>

**Byte**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Größe des Parameters in Bytes.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
