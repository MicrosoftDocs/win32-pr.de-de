---
description: Auswirkungen von Standardparametern.
ms.assetid: a8a24cf2-0ecd-4429-97d3-086ff49540a1
title: D3DXEFFECTDEFAULT-Struktur (D3dx9mesh.h)
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
ms.openlocfilehash: 41beda43807ace6b0f335dc1937f8843cbc11544e4842f86af98eb0e0bb0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731879"
---
# <a name="d3dxeffectdefault-structure"></a>D3DXEFFECTDEFAULT-Struktur

Auswirkungen von Standardparametern.

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

**pParamName**
</dt> <dd>

Typ: **LPSTR**

</dd> <dd>

Parametername.

</dd> <dt>

**Typ**
</dt> <dd>

Typ: **[ **D3DXEFFECTDEFAULTTYPE**](./d3dxeffectdefaulttype.md)**

</dd> <dd>

Datentyp in pValue. Weitere Informationen finden Sie unter [ **D3DXEFFECTDEFAULTTYPE.**](./d3dxeffectdefaulttype.md)

</dd> <dt>

**Numbytes**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Größe der Daten, auf die pValue verweist, in Bytes.

</dd> <dt>

**Pvalue**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf den Speicherort des Arbeitsspeichers, der die Daten enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effektstrukturen](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
