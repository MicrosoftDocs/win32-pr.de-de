---
description: Durchsatzmetriken zum Besseren des Verständnisses der Leistung einer Anwendung.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f9c92a3eae10ef289e53764c7568f826640edf66c3351edaadf3d922515a3eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565030"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS-Struktur

Durchsatzmetriken zum Besseren des Verständnisses der Leistung einer Anwendung.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Member

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Bandbreite oder die maximale Datenübertragungsrate von der Host-CPU zur GPU. Dies ist in der Regel die Bandbreite des PCI- oder AGP-Buss, der die CPU und die GPU verbindet.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Arbeitsspeicherauslastung beim Hochladen von Daten von der Host-CPU auf die GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz des Vertexdurchsatzes. Dies ist die Anzahl der verarbeiteten Scheitelpunkte im Vergleich zur theoretischen maximalen Scheitelpunktverarbeitungsrate.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Durchsatz in Dreieckssatz in Prozent. Dies ist die Anzahl der Dreiecke, die für die Rasterung im Vergleich zur theoretischen maximalen Dreieckssatzrate eingerichtet werden.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz des Pixelfülldurchsatzes. Dies ist die Anzahl von Pixeln, die im Vergleich zur theoretischen Pixelfüllung gefüllt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
