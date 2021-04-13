---
description: Datentyp zum Verwalten eines Satzes von Standardeffekt Parametern.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: D3DXEFFECTINSTANCE-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354886"
---
# <a name="d3dxeffectinstance-structure"></a>D3DXEFFECTINSTANCE-Struktur

Datentyp zum Verwalten eines Satzes von Standardeffekt Parametern.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Member

<dl> <dt>

**"Peer Name"**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Der Name der Effekt Datei.

</dd> <dt>

**Numdefaults**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der Standardparameter.

</dd> <dt>

**pdefaults**
</dt> <dd>

Typ: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

Ein Zeiger auf ein Array von [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) -Elementen, die jeweils einen Effektparameter enthalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
