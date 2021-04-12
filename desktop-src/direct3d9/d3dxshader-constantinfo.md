---
description: D3DXSHADER \_ constantinfo-Struktur
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: D3DXSHADER_CONSTANTINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219496"
---
# <a name="d3dxshader_constantinfo-structure"></a>D3DXSHADER \_ constantinfo-Struktur

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die die Konstanten Informationen enthält.

</dd> <dt>

**Register Set**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Register Satz. Siehe [**D3DXREGISTER \_ set**](./d3dxregister-set.md).

</dd> <dt>

**Register Index**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Registrierungs Index.

</dd> <dt>

**Register count**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Register.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Reserviert.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die die [**D3DXSHADER \_ TypeInfo**](d3dxshader-typeinfo.md) -Informationen enthält.

</dd> <dt>

**DefaultValue**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die den Standardwert enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
