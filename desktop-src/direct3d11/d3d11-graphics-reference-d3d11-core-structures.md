---
title: Direct3D 11 Core-Strukturen
description: Dieser Abschnitt enthält Informationen zu den Kern Strukturen.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- Strukturen, Direct3D 11 Kerne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390653"
---
# <a name="direct3d-11-core-structures"></a>Direct3D 11 Core-Strukturen

Dieser Abschnitt enthält Informationen zu den Kern Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a><br/></td>
<td>Beschreibt den Blend-Status, den Sie in einem Aufrufen von <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: kreateblendstate</strong></a> zum Erstellen eines Blend-State-Objekts verwenden. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt den Blend-Status, den Sie in einem <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> -Befehl verwenden, um ein Blend-State-Objekt zu erstellen. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a><br/></td>
<td>Definiert ein 3D-Feld.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a><br/></td>
<td>Beschreibt einen-Counter.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a><br/></td>
<td>Informationen zu den Leistungs Leistungsdaten der Grafikkarte.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a><br/></td>
<td>Beschreibt den Status der tiefen Schablone.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a><br/></td>
<td>Schablonen Vorgänge, die auf der Grundlage der Ergebnisse des Schablonen Tests ausgeführt werden können.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Argumente zum Zeichnen indizierter instanziierten, indirekt. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a><br/></td>
<td>Argumente für eine indirekte zeichnen-Instanz. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt Informationen zur Direct3D 11,1-Adapter Architektur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt Direct3D 9-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a><br/></td>
<td>Beschreibt Direct3D 9-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt die Direct3D 9-Schatten Unterstützung im aktuellen Grafiktreiber. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a><br/></td>
<td>Beschreibt, ob einfache Instanziierung unterstützt wird.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a><br/></td>
<td>Beschreibt die Unterstützung von Compute-Shader und der Rohund strukturierten Puffer im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt Direct3D 11,1-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a><br/></td>
<td>Beschreibt Direct3D 11,2-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a><br/></td>
<td>Beschreibt Direct3D 11,3-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a><br/></td>
<td>Beschreibt Direct3D 11,3-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a><br/></td>
<td>Beschreibt Direct3D 11,4-Funktions Optionen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a><br/></td>
<td>Beschreibt die Ebene der Unterstützung für freigegebene Ressourcen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a><br/></td>
<td>Beschreibt die Unterstützung doppelter Datentypen im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a><br/></td>
<td>Beschreibt, welche Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Beschreibt, welche Optionen für ungeordnete Ressourcen vom aktuellen Grafiktreiber für ein bestimmtes Format unterstützt werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a><br/></td>
<td>Beschreibt die Unterstützung der Unterstützung virtueller GPU-Adressen, einschließlich der maximalen Adress Bits pro Ressource und pro Prozess. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a><br/></td>
<td>Beschreibt, ob eine GPU-Profil Erstellungs Methode unterstützt wird.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a><br/></td>
<td>Beschreibt die Ebene der Shader-Zwischenspeicherung, die im aktuellen Grafiktreiber unterstützt wird.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt die Optionen für die Genauigkeits Unterstützung für Shader im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a><br/></td>
<td>Beschreibt die Multithreading-Funktionen, die vom aktuellen Grafiktreiber unterstützt werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a><br/></td>
<td>Eine Beschreibung eines einzelnen Elements für die Eingabe-Assembler-Stufe.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a><br/></td>
<td>Abfrage Informationen zur Grafik Pipeline Aktivität zwischen Aufrufen von <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>Verknüpfung id3d11devicecontext aus:: begin</strong></a> und <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>Verknüpfung id3d11devicecontext aus:: End</strong></a>.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a><br/></td>
<td>Abfrage Informationen über die Menge der Daten, die an die Stream-Ausgabepuffer zwischen <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>Verknüpfung id3d11devicecontext aus:: begin</strong></a> und <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>Verknüpfung id3d11devicecontext aus:: End</strong></a>gestreamt werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a><br/></td>
<td>Abfrage Informationen über die Zuverlässigkeit einer Zeitstempel-Abfrage.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a><br/></td>
<td>Beschreibt eine Abfrage.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a><br/></td>
<td>Beschreibt eine Abfrage.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a><br/></td>
<td>Beschreibt den Status des Rasterizers.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt den Status des Rasterizers.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a><br/></td>
<td>Beschreibt den Status des Rasterizers.<br/></td>
</tr>
<tr>
<td><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a><br/></td>
<td>D3D11_RECT wird wie folgt deklariert:<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a><br/></td>
<td>Beschreibt den Blend-Zustand für ein Renderziel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Struktur wird von der Direct3D 11,1-Laufzeit unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Beschreibt den Blend-Zustand für ein Renderziel.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a><br/></td>
<td>Beschreibt einen samplerzustand.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a><br/></td>
<td>Beschreibung eines Vertex-Elements in einem Vertex-Puffer in einem Ausgabe Slot.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a><br/></td>
<td>Definiert die Abmessungen eines Viewports.<br/></td>
</tr>
</tbody>
</table>

Außerdem gibt es eine 2D-Rechteck Struktur, die in D3D11. h definiert ist.

```cpp
typedef RECT D3D11_RECT;
```

Dokumentation finden Sie unter [Rect](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).

## <a name="related-topics"></a>Zugehörige Themen

[Kern Referenz](d3d11-graphics-reference-d3d11-core.md)