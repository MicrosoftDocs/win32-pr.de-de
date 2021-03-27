---
description: Gibt an, wie die Pipeline Vertex-Daten interpretiert, die an die Eingabe-Assembler-Phase gebunden sind. Diese primitiven topologiewerte bestimmen, wie die Scheitelpunkt Daten auf dem Bildschirm gerendert werden.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ primitive \_ topologieenumeration
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104995270"
---
# <a name="d3d11_primitive_topology-enumeration"></a>D3D11 \_ primitive \_ topologieenumeration

Gibt an, wie die Pipeline Vertex-Daten interpretiert, die an die Eingabe-Assembler-Phase gebunden sind. Diese primitiven topologiewerte bestimmen, wie die Scheitelpunkt Daten auf dem Bildschirm gerendert werden.

## <a name="syntax"></a>Syntax


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11 \_ primitive \_ Topologie nicht \_ definiert**
</dt> <dd>

Die IA-Phase wurde nicht mit einer primitiven Topologie initialisiert. Die IA-Phase funktioniert nur dann ordnungsgemäß, wenn eine primitive Topologie definiert ist.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ primitive \_ Topologie- \_ PointList**
</dt> <dd>

Interpretiert die Scheitelpunkt Daten als eine Liste von Punkten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ primitive \_ Topologie- \_ LineList**
</dt> <dd>

Interpretiert die Scheitelpunkt Daten als eine Liste von Zeilen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ primitive \_ Topologie ( \_ linestrip)**
</dt> <dd>

Interpretiert die Scheitelpunkt Daten als Zeilen Streifen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ primitive \_ Topologie ( \_ drei)**
</dt> <dd>

Interpretiert die Scheitelpunkt Daten als eine Liste von Dreiecken.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ primitive \_ Topologie ( \_ drei)**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Dreiecks Streifen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ primitive \_ Topologie \_ LineList \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Liste von Zeilen mit Daten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ primitive \_ Topologie ( \_ linestrip) \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Zeilen Streifen mit Daten der Daten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ primitive \_ Topologie \_ (in \_ TL)**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Liste von Dreiecken mit Daten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ primitive \_ Topologie, \_ \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Dreiecks Streifen mit Daten der Daten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 1 \_ - \_ Patchliste für Kontrollpunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 2 \_ - \_ Patchliste für Kontrollpunkte \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 3 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 4 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 5- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 6 \_ , \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 7 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ - \_ \_ \_ Kontroll \_ Punkt- \_ Patchliste für primitive Topologie 8**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 9 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 10 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 11 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 12- \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 13 \_ , \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 14 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 15- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 16- \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 17 \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 18- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 19- \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 20 \_ - \_ Patchliste für Kontrollpunkte \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 21 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 22 \_ - \_ Patchliste für Steuerungspunkt \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 23- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 24- \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 25 \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 26- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 27 \_ Kontroll \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 28- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 29- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 30- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 31- \_ Steuerungs \_ Punkt- \_ Patchliste**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ primitive \_ Topologie \_ 32 \_ - \_ Patchliste der Steuerungs Punkte \_**
</dt> <dd>

Interpretieren Sie die Scheitelpunkt Daten als Patchliste.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Bei der D3D11-Enumeration der **\_ primitiven \_ Topologie** handelt es sich um einen Typ, der in der D3D11. h-Header Datei als [**D3D \_ primitive \_ topologieenumeration**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) definiert ist, die vollständig in der Header Datei D3DCommon. h definiert ist.
