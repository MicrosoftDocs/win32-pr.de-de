---
description: Standardparameter beeinflussen.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: D3DXEFFECTDEFAULT-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: fee415cbd7d8ec28daa079dd2f224949402a813b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361866"
---
# <a name="d3dxeffectdefault-structure"></a>D3DXEFFECTDEFAULT-Struktur

Standardparameter beeinflussen.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXEFFECTDEFAULT {
  LPSTR                 pParamName;
  D3DXEFFECTDEFAULTTYPE Type;
  DWORD                 NumBytes;
  LPVOID                pValue;
} D3DXEFFECTDEFAULT, *LPD3DXEFFECTDEFAULT;
```



## <a name="members"></a>Member

<dl> <dt>

**pparamname**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Parametername.

</dd> <dt>

**Type**
</dt> <dd>

Typ: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Datentyp in pValue. Weitere Informationen finden Sie unter [ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**NumBytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe (in Bytes) der Daten, auf die von pValue verwiesen wird.

</dd> <dt>

**pValue**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Zeiger auf den Speicherort, der die Daten enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Effekt Strukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
