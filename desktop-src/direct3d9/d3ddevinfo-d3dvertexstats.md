---
description: Gibt die Anzahl der Dreiecke an, die von der Softwarevertexverarbeitung der Runtime verarbeitet und abgeschnitten wurden.
ms.assetid: 280fb5c3-3048-4208-b352-0548b13ecba2
title: D3DDEVINFO_D3DVERTEXSTATS -Struktur (D3D9Types.h)
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
ms.openlocfilehash: 80edbdcdeea5df6ff020c0c4cc2179db5152c15cc4965efe6580db7fd7bdcc48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894530"
---
# <a name="d3ddevinfo_d3dvertexstats-structure"></a>D3DDEVINFO \_ D3DVERTEXSTATS-Struktur

Gibt die Anzahl der Dreiecke an, die von der Softwarevertexverarbeitung der Runtime verarbeitet und abgeschnitten wurden.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3DVERTEXSTATS {
  DWORD NumRenderedTriangles;
  DWORD NumExtraClippingTriangles;
} D3DDEVINFO_D3DVERTEXSTATS, *LPD3DDEVINFO_D3DVERTEXSTATS;
```



## <a name="members"></a>Member

<dl> <dt>

**NumRenderedTriangles**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Gesamtanzahl von Dreiecken, die in diesem Rahmen nicht abgeschnitten werden.

</dd> <dt>

**NumExtraClippingTriangles**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Anzahl der neuen Dreiecke, die durch Clipping generiert wurden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Verwenden Sie die Debuglaufzeit und die Softwarevertexverarbeitung, um die Anzahl der nicht abgeschnittenen und abgeschnittenen Primitiven für eine bestimmte Szene zu erhalten. Primitive werden in der Regel basierend auf einem Schutzband abgeschnitten (sofern vorhanden). Das Clipping Guard-Band wird mit Parametern wie GuardBandLeft in [**D3DCAPS9 festgelegt.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
