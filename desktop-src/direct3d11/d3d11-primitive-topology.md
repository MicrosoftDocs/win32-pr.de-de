---
description: So interpretiert die Pipeline Scheitelpunktdaten, die an die Eingabeassembliererphase gebunden sind. Diese primitiven Topologiewerte bestimmen, wie die Scheitelpunktdaten auf dem Bildschirm gerendert werden.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ PRIMITIVE \_ TOPOLOGY-Enumeration
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 7c899d738b2a80036eaea61352f5e8aa82c73ddbeb48433d275d74506a478d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990010"
---
# <a name="d3d11_primitive_topology-enumeration"></a>D3D11 \_ PRIMITIVE \_ TOPOLOGY-Enumeration

So interpretiert die Pipeline Scheitelpunktdaten, die an die Eingabeassembliererphase gebunden sind. Diese primitiven Topologiewerte bestimmen, wie die Scheitelpunktdaten auf dem Bildschirm gerendert werden.

## <a name="syntax"></a>Syntax


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**D3D11 \_ PRIMITIVE TOPOLOGIE NICHT \_ \_ DEFINIERT**
</dt> <dd>

Die IA-Phase wurde nicht mit einer primitiven Topologie initialisiert. Die IA-Phase funktioniert nur dann ordnungsgemäß, wenn eine primitive Topologie definiert ist.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIEPUNKTLISTE**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Liste von Punkten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ LINELIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Eine Liste von Zeilen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIELINIENTRIP**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Linienstreifen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIEDREIECKLISTE**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Eine Liste von Dreiecken.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIEDREIECKSTRIP**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Dreiecksstreifen.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ LINELIST \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Liste von Zeilen mit Adjazenzdaten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIELINIENTRIP \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Linienstreifen mit Adjazenzdaten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIEDREIECKLISTE \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Liste von Dreiecken mit Adjazenzdaten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ \_ TOPOLOGIEDREIECKSTRIP \_ ADJ**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Dreiecksstreifen mit Adjazenzdaten.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 1 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 2 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 3 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 4 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 5 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 6 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 7 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 8 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ \_ 9, \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 10 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 11 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 12 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 13 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 14 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 15 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 16 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 17 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 18 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 19 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 20 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 21 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 22 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 23 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 24 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 25 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 26 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 27 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 28 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 29 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 30 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 31 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGIE \_ 32 \_ \_ STEUERUNGSPUNKT \_ PATCHLIST**
</dt> <dd>

Interpretieren Sie die Scheitelpunktdaten als Patchliste.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **D3D11 \_ PRIMITIVE \_ TOPOLOGY-Enumeration** ist in der D3D11.h-Headerdatei als [**D3D \_ PRIMITIVE \_ TOPOLOGY-Enumeration**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) definiert, die vollständig in der Headerdatei D3DCommon.h definiert ist.
