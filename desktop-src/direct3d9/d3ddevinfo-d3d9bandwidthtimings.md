---
description: Durchsatz Metriken, um die Leistung einer Anwendung besser zu verstehen.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219473"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS-Struktur

Durchsatz Metriken, um die Leistung einer Anwendung besser zu verstehen.

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

**Maxbandwidthausgelastet**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Bandbreite oder maximale Datenübertragungsrate von der Host-CPU zur GPU. Dabei handelt es sich in der Regel um die Bandbreite des PCI-oder AGP-Busses, der die CPU und die GPU verbindet.

</dd> <dt>

**Frontenduploadmemoryutilizedprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Arbeitsspeicher Auslastung in Prozent beim Hochladen von Daten von der Host-CPU auf die GPU.

</dd> <dt>

**Vertexrateutilizedprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Vertex-Durchsatz Prozentsatz. Dies ist die Anzahl der verarbeiteten Scheitel Punkte im Vergleich zur theoretischen maximalen Vertex-Verarbeitungsrate.

</dd> <dt>

**"" "" ".**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Dreiecks Einrichtung in Prozent. Dies ist die Anzahl der Dreiecke, die für die rasterisierung im Vergleich zur theoretischen maximalen Dreiecks Einrichtung festgelegt sind.

</dd> <dt>

**Fillrateutilizedprozent**
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Prozentsatz der Pixel Füll Durchsatz. Dies ist die Anzahl der Pixel, die im Vergleich zur theoretischen Pixel Füllung aufgefüllt werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
