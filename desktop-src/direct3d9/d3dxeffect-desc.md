---
description: Beschreibt ein Effektobjekt.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC-Struktur (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 0b30ad0348a5c799690d668e036724d30808c2998eee9d762fa2ad3fc8106c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298593"
---
# <a name="d3dxeffect_desc-structure"></a>D3DXEFFECT \_ DESC-Struktur

Beschreibt ein Effektobjekt.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Creator**
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeichenfolge, die den Namen des Effekterstellers enthält.

</dd> <dt>

**Parameter**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der für effect verwendeten Parameter.

</dd> <dt>

**Techniken**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Techniken, die den Effekt rendern können.

</dd> <dt>

**Funktionen**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Funktionen, die den Effekt rendern können.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Effektobjekt kann mehrere Renderingtechniken und Parameter für denselben Effekt enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
