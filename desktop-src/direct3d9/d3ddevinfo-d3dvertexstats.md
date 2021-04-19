---
description: Gibt die Anzahl der Dreiecke an, die von der Software Scheitelpunkt Verarbeitung der Laufzeit verarbeitet und abgeschnitten wurden.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: D3DDEVINFO_D3DVERTEXSTATS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3DVERTEXSTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3baa6738e5d90d2353beb6c7d7bf0ab85770af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350672"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>D3DDEVINFO \_ D3DVERTEXSTATS-Struktur

Gibt die Anzahl der Dreiecke an, die von der Software Scheitelpunkt Verarbeitung der Laufzeit verarbeitet und abgeschnitten wurden.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**Numrendereddreiecke**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Gesamtanzahl der Dreiecke, die in diesem Frame nicht abgeschnitten werden.

</dd> <dt>

**Numextraclippingdreiecke**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der neuen Dreiecke, die durch Clipping generiert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Debug-Laufzeit und die Verarbeitung von Software Scheitel Punkten, um die Anzahl der nicht geschnittenen und abgeschnittenen primitiven für eine bestimmte Szene zu erhalten. Primitive werden in der Regel basierend auf einem Wächter-Band (sofern vorhanden) abgeschnitten. Das Clipping Guard-Band wird mit Parametern wie "GuardBandLeft" in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
