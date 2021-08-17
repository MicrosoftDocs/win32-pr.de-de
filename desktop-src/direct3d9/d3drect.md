---
description: Definiert ein Rechteck.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: D3DRECT-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 5e202ae058cdc30b79e2cc579a064b597d0013f7447e70f0fd6d996d9740a830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732284"
---
# <a name="d3drect-structure"></a>D3DRECT-Struktur

Definiert ein Rechteck.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DRECT {
  LONG x1;
  LONG y1;
  LONG x2;
  LONG y2;
} D3DRECT;
```



## <a name="members"></a>Member

<dl> <dt>

**x1**
</dt> <dd>

Typ: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Koordinate der linken oberen Ecke des Rechtecks.

</dd> <dt>

**y1**
</dt> <dd>

Typ: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Koordinate der linken oberen Ecke des Rechtecks.

</dd> <dt>

**x2**
</dt> <dd>

Typ: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Koordinate der unteren rechten Ecke des Rechtecks.

</dd> <dt>

**y2**
</dt> <dd>

Typ: **[ **LONG**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Koordinate der unteren rechten Ecke des Rechtecks.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Klar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
