---
description: Beschreibt den Raster Status.
ms.assetid: f7b5b714-8fc8-47b8-adec-1089b8d07081
title: D3DRASTER_STATUS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: e77ab0e6ee164eadae862ed03df5652c21ba7040
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361215"
---
# <a name="d3draster_status-structure"></a>D3DRASTER- \_ Status Struktur

Beschreibt den Raster Status.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DRASTER_STATUS {
  BOOL InVBlank;
  UINT ScanLine;
} D3DRASTER_STATUS, *LPD3DRASTER_STATUS;
```



## <a name="members"></a>Member

<dl> <dt>

**Nicht angegeben**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** , wenn sich das Raster im vertikalen leeren Zeitraum befindet. **False** , wenn sich das Raster nicht im vertikalen leeren Zeitraum befindet.

</dd> <dt>

**Scanline**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Wenn "invblank" den Wert " **false**" hat, ist dieser Wert eine ganze Zahl, die ungefähr der aktuellen Scan Linie entspricht, die vom Raster gezeichnet wird Überprüfungs Zeilen werden auf die gleiche Weise wie Direct3D Surface-Koordinaten nummeriert: 0 ist der obere Teil der primären Oberfläche und erweitert auf den Wert (Höhe von Oberfläche-1) am unteren Rand der Anzeige.

Wenn "invblank" auf " **true**" festgelegt ist, wird dieser Wert auf NULL festgelegt und kann ignoriert werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetRasterStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrasterstatus)
</dt> </dl>

 

 
