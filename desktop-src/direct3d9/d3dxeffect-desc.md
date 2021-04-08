---
description: Beschreibt ein Effect-Objekt.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC-Struktur (D3dx9effect. h)
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
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762054"
---
# <a name="d3dxeffect_desc-structure"></a>D3DXEFFECT- \_ Struktur

Beschreibt ein Effect-Objekt.

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

Eine Zeichenfolge, die den Namen des Effekts Erstellers enthält.

</dd> <dt>

**Parameter**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Anzahl der Parameter, die für die Auswirkung verwendet werden.

</dd> <dt>

**O**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Techniken, die den Effekt darstellen können.

</dd> <dt>

**Funktionen**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl von Funktionen, die den Effekt darstellen können.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Effect-Objekt kann mehrere renderingtechniken und-Parameter für denselben Effekt enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
