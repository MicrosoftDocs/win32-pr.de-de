---
description: Eine 4 x 4-Zeilen hauptmatrix.
ms.assetid: 2253f486-7bb6-4966-b3ec-dba47e53e372
title: D3DMATRIX-Struktur (D3DX10Math. h)
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
ms.openlocfilehash: 1df0d2171e828b14fba87f6587c604146360d0e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355487"
---
# <a name="d3dmatrix-structure"></a>D3DMATRIX-Struktur

Eine 4 x 4-Zeilen hauptmatrix.

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

Die 4 x 4-Zeilen hauptmatrix.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 




