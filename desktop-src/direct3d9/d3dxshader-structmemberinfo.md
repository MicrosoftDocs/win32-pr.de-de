---
description: Eine hilfsstruktur, die Informationen zur Elementstruktur enthält.
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: D3DXSHADER_STRUCTMEMBERINFO-Struktur (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 01782331459956c0878b46861db0d4f11e19c7dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354626"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>D3DXSHADER \_ structmembership Info-Struktur

Eine hilfsstruktur, die Informationen zur Elementstruktur enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser Struktur in Bytes zur Zeichenfolge, die den Namen des Strukturmembers enthält.

</dd> <dt>

**TypeInfo**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Offset vom Anfang dieser-Struktur in Bytes zur Zeichenfolge, die die Typinformationen enthält. Siehe [**D3DXSHADER \_ TypInfo**](d3dxshader-typeinfo.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TypInfo**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
