---
description: Beschreibt den Rasterstatus.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRASTER_STATUS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: fc8a1e2995a9353a02df120b109eb32ad0914821e5690440c7228fbc8e7b6c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676400"
---
# <a name="d3draster_status-structure"></a>D3DRASTER \_ STATUS-Struktur

Beschreibt den Rasterstatus.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**InVBlank**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE,** wenn sich das Raster im vertikalen Leerzeitraum befindet. **FALSE,** wenn sich das Raster nicht im vertikalen Leerzeitraum befindet.

</dd> <dt>

**ScanLine**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Wenn InVBlank **false** ist, ist dieser Wert eine ganze Zahl, die ungefähr der aktuellen Scanzeile entspricht, die vom Raster gezeichnet wird. Scanlinien werden auf die gleiche Weise nummeriert wie Direct3D-Oberflächenkoordinaten: 0 ist der obere Rand der primären Oberfläche und erstreckt sich auf den Wert (Höhe der Oberfläche – 1) am unteren Rand der Anzeige.

Wenn InVBlank **true** ist, wird dieser Wert auf 0 festgelegt und kann ignoriert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
