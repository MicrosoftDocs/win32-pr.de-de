---
title: Direct3D 11 Core-Enumerationen
description: Dieser Abschnitt enthält Informationen zu den kernenumerationen.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- Enumerationen, Direct3D 11 Kerne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b012ae34367ef849bebf3fb25780310fcb924ba9
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391193"
---
# <a name="direct3d-11-core-enumerations"></a>Direct3D 11 Core-Enumerationen

Dieser Abschnitt enthält Informationen zu den kernenumerationen.

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
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a><br/></td>
<td>Optionale Flags, die das Verhalten von <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>Verknüpfung id3d11devicecontext aus:: GetData</strong></a>steuern.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a><br/></td>
<td>Blend-Faktoren, die Werte für den Pixelshader und das Renderziel modulieren.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a><br/></td>
<td>RGB-oder Alpha-Mischungs Vorgang.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a><br/></td>
<td>Gibt die zu löschenden Teile der tiefen Schablone an. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a><br/></td>
<td>Identifizieren Sie, welche Komponenten jedes Pixels eines Renderziels während der Mischung geschrieben werden können.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a><br/></td>
<td>Vergleichs Optionen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a><br/></td>
<td>Gibt an, ob die konservative rasterisierung ein-oder ausgeschaltet ist.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a><br/></td>
<td>Gibt an, ob die Hardware und der Treiber die konservative rasterisierung unterstützen und auf welcher Ebene.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a><br/></td>
<td>Gibt den Kontext an, in dem eine Abfrage auftritt.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Enumeration wird von der Direct3D 11,1-Runtime unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Gibt an, wie der vorhandene Inhalt einer Ressource während eines Kopier-oder Aktualisierungs Vorgangs eines Bereichs innerhalb dieser Ressource behandelt werden soll.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a><br/></td>
<td>Optionen für Leistungsindikatoren.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a><br/></td>
<td>Datentyp eines Leistungs Zählers.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a><br/></td>
<td>Beschreibt die Parameter, die zum Erstellen eines Geräts verwendet werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a><br/></td>
<td>Beschreibt Flags, die verwendet werden, um ein Gerätekontext-Zustands Objekt (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) mit der <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1:: samatedevicecontextstate</strong></a> -Methode zu erstellen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a><br/></td>
<td>Gibt an, dass Dreiecke mit einer bestimmten Richtung nicht gezeichnet werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a><br/></td>
<td>Identifizieren Sie den Teil eines tiefen Schablonen Puffers zum Schreiben von Tiefendaten.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a><br/></td>
<td>Gerätekontext Optionen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a><br/></td>
<td>Direct3D 11 Feature-Optionen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a><br/></td>
<td>Gibt Optionen für die Fence an. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a><br/></td>
<td>Bestimmt den Füll Modus, der beim Rendern von Dreiecken verwendet wird.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a><br/></td>
<td>Filteroptionen während der Textur Stichprobe.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a><br/></td>
<td>Typen von Vergrößerungs-oder minierungs-samplerfiltern.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a><br/></td>
<td>Gibt den Typ der samplerfilterreduzierung an. <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a><br/></td>
<td>Welche Ressourcen für ein bestimmtes Format und ein bestimmtes Gerät unterstützt werden (siehe <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device:: checkformatsupport</strong></a> und <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: checkfeaturesupport</strong></a>).<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a><br/></td>
<td>Optionen für die Unterstützung nicht geordneter Ressourcen für eine COMPUTE-Shader-Ressource (siehe <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: checkfeaturesupport</strong></a>). <br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a><br/></td>
<td>Der Typ der Daten, die in einem Eingabe Slot enthalten sind.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Enumeration wird von der Direct3D 11,1-Runtime unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Gibt logische Vorgänge an, die für ein Renderziel konfiguriert werden sollen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a><br/></td>
<td>Gibt an, wie die Pipeline Geometry-oder Hull-Shader-Eingabe primitive interpretiert. <br/></td>
</tr>
<tr>
<td><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a><br/></td>
<td>Gibt an, wie die Pipeline Vertex-Daten interpretiert, die an die Eingabe-Assembler-Phase gebunden sind. Diese primitiven topologiewerte bestimmen, wie die Scheitelpunkt Daten auf dem Bildschirm gerendert werden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a><br/></td>
<td>Abfrage Typen.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a><br/></td>
<td>Flags, die verschiedene Abfrage Verhalten beschreiben.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a><br/></td>
<td>Option (e) zum auslöst eines Fehlers auf eine nicht fort Setz Bare Ausnahme.<br/></td>
</tr>
<tr>
<td><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a><br/></td>
<td>Beschreibt die Ebene der Unterstützung für das Shader-Caching im aktuellen Grafiktreiber.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Diese Enumeration wird von der Direct3D 11,1-Runtime unterstützt, die unter Windows 8 und höheren Betriebssystemen verfügbar ist.
</blockquote>
<br/> Werte, die minimale Genauigkeits Stufen in Shader-Stufen angeben.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a><br/></td>
<td>Definiert Konstanten, die eine Ebene für die Unterstützung von freigegebenen Ressourcen angeben.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a><br/></td>
<td>Die Schablonen Vorgänge, die während der tiefen Schablone getestet werden können.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a><br/></td>
<td>Identifizieren Sie eine Technik zum Auflösen von Texturkoordinaten, die sich außerhalb der Grenzen einer Textur befinden.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a><br/></td>
<td>Die verschiedenen Gesichter einer Cube-Textur.<br/></td>
</tr>
<tr>
<td><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a><br/></td>
<td>Gibt die Ebene an, auf der die gekachelten Ressourcen unterstützt werden.<br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a>Zugehörige Themen

[Core-Referenz](d3d11-graphics-reference-d3d11-core.md)