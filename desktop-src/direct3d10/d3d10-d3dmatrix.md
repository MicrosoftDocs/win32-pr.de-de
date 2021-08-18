---
description: Eine 4x4-Zeilen-Hauptmatrix.
ms.assetid: 2253f486-7bb6-4966-b3ec-dba47e53e372
title: D3DMATRIX-Struktur (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 7a8ba1b9d0aebf45ae376f6adbdf02dd4c3d8ff6590ecb49e5af8cd72d37a79f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498710"
---
# <a name="d3dmatrix-structure"></a>D3DMATRIX-Struktur

Eine 4x4-Zeilen-Hauptmatrix.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DMATRIX {
  float m[4][4];
} D3DMATRIX, *LPD3DMATRIX;
```



## <a name="members"></a>Member

<dl> <dt>

**m \[ 4 \] \[ 4\]**
</dt> <dd>

Typ: **float**

</dd> <dd>

Die 4x4-Zeilen-Hauptmatrix.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 




