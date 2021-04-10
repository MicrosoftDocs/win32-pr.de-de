---
description: Definiert ein Rechteck.
ms.assetid: a8590411-fd34-4048-a41f-b4155d955573
title: D3DRECT-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 9a22b74869afa16ca0c55ac50975eb36ba590c7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762099"
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

Type: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Koordinate der linken oberen Ecke des Rechtecks.

</dd> <dt>

**y1**
</dt> <dd>

Type: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Koordinate der linken oberen Ecke des Rechtecks.

</dd> <dt>

**x2**
</dt> <dd>

Type: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Die x-Koordinate der unteren rechten Ecke des Rechtecks.

</dd> <dt>

**Y2**
</dt> <dd>

Type: **[ **Long**](../winprog/windows-data-types.md)**

</dd> <dd>

Die y-Koordinate der unteren rechten Ecke des Rechtecks.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Klartext**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
</dt> </dl>

 

 
