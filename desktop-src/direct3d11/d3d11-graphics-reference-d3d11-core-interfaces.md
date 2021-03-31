---
title: Direct3D 11 Kern Schnittstellen
description: Dieser Abschnitt enthält Informationen zu den Kern Schnittstellen.
ms.assetid: e96804db-0987-49ca-b1b1-321f36c13024
keywords:
- Schnittstellen, Direct3D 11 Kerne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c578d84a7a9f223cb81285b69f5b5d1baed4e6
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104474525"
---
# <a name="direct3d-11-core-interfaces"></a>Direct3D 11 Kern Schnittstellen

Dieser Abschnitt enthält Informationen zu den Kern Schnittstellen.

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
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a><br/></td>
<td>Diese Schnittstelle kapselt Methoden zum asynchronen Abrufen von Daten aus der GPU.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate"><strong>ID3D11BlendState</strong></a><br/></td>
<td>Die Blend-State-Schnittstelle enthält eine Beschreibung des Mischungs Zustands, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11blendstate1"><strong>ID3D11BlendState1</strong></a><br/></td>
<td>Die Blend-State-Schnittstelle enthält eine Beschreibung des Mischungs Zustands, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können. Diese Blend-State-Schnittstelle unterstützt logische Vorgänge und Mischungs Vorgänge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist"><strong>ID3D11CommandList</strong></a> -Schnittstelle kapselt eine Liste von Grafik Befehlen für die Wiedergabe.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11counter"><strong>ID3D11Counter</strong></a><br/></td>
<td>Diese Schnittstelle kapselt Methoden zum Messen der GPU-Leistung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate"><strong>ID3D11DepthStencilState</strong></a><br/></td>
<td>Die Schnittstelle "tiefen Schablone-Status" enthält eine Beschreibung für den Status der tiefen Schablone, die Sie an die <a href="d3d10-graphics-programming-guide-output-merger-stage.md">Ausgabe-Fusion-Phase</a>binden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a> fügt den in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11device1"><strong>ID3D11Device1</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen. <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11device2"><strong>ID3D11Device2</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a> fügt in <a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11device3"><strong>ID3D11Device3</strong></a>neue Methoden hinzu, z. b. <strong>registerdeviceremovedevent</strong> und <strong>unregisterdeviceremoved</strong>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a><br/></td>
<td>Die Geräteschnittstelle stellt einen virtuellen Adapter dar. Sie wird verwendet, um Ressourcen zu erstellen. <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5"><strong>ID3D11Device5</strong></a> fügt den in <a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4"><strong>ID3D11Device4</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><br/></td>
<td>Eine Geräte untergeordnete Schnittstelle greift auf Daten zu, die von einem Gerät verwendet werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a> -Schnittstelle stellt einen Gerätekontext dar, der renderingbefehle generiert.<br/>
<blockquote>
[!Note]<br />
Die neueste Version dieser Schnittstelle ist <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> , die in Windows 10 Creators Update eingeführt wurde. Anwendungen, die das Windows 10 Creators Update verwenden, sollten anstelle von <strong>ID3D11Device</strong>die <strong>ID3D11DeviceContext4</strong> -Schnittstelle verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a><br/></td>
<td>Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet. <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a> fügt den in <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>Verknüpfung id3d11devicecontext aus</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a><br/></td>
<td>Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet. <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11devicecontext1"><strong>ID3D11DeviceContext1</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a><br/></td>
<td>Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a> fügt den in <a href="/windows/desktop/api/D3D11_2/nn-d3d11_2-id3d11devicecontext2"><strong>ID3D11DeviceContext2</strong></a>neue Methoden hinzu. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a><br/></td>
<td>Die Gerätekontext Schnittstelle stellt einen Gerätekontext dar. Sie wird zum Rendering von Befehlen verwendet. <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4"><strong>ID3D11DeviceContext4</strong></a> fügt den in <a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3"><strong>ID3D11DeviceContext3</strong></a>neue Methoden hinzu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a><br/></td>
<td>Die <a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a> -Schnittstelle stellt ein Kontext Zustands Objekt dar, das Zustands-und Verhaltens Informationen zu einem Microsoft Direct3D-Gerät enthält.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence"><strong>ID3D11Fence</strong></a><br/></td>
<td>Stellt einen Fence dar, ein Objekt, das für die Synchronisierung der CPU und eines oder mehrerer GPUs verwendet wird.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11inputlayout"><strong>ID3D11InputLayout</strong></a><br/></td>
<td>Eine Eingabe Layout-Schnittstelle enthält eine Definition, wie Vertex-Daten, die im Arbeitsspeicher angeordnet sind, in die <a href="d3d10-graphics-programming-guide-input-assembler-stage.md">Eingabe-Assembler-Phase</a> der <a href="overviews-direct3d-11-graphics-pipeline.md">Grafik Pipeline</a>eingegeben werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread"><strong>ID3D11Multithread</strong></a><br/></td>
<td>Bietet Threading Schutz für kritische Abschnitte einer Multithreadanwendung.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate"><strong>ID3D11Predicate</strong></a><br/></td>
<td>Eine Prädikat Schnittstelle bestimmt, ob die Geometrie abhängig von den Ergebnissen eines vorherigen zeichnen-Aufrufes verarbeitet werden soll.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a><br/></td>
<td>Eine Abfrage Schnittstelle fragt Informationen von der GPU ab.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11query1"><strong>ID3D11Query1</strong></a><br/></td>
<td>Stellt ein Abfrageobjekt zum Abfragen von Informationen aus der GPU (Graphics Processing Unit) dar.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11rasterizerstate"><strong>ID3D11RasterizerState</strong></a><br/></td>
<td>Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11_1/nn-d3d11_1-id3d11rasterizerstate1"><strong>ID3D11RasterizerState1</strong></a><br/></td>
<td>Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können. Diese Rasterizer-State-Schnittstelle unterstützt die erzwungene Stichproben Anzahl.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11rasterizerstate2"><strong>ID3D11RasterizerState2</strong></a><br/></td>
<td>Die Raster-State-Schnittstelle enthält eine Beschreibung für den Status des Rasterizers, den Sie an die <a href="d3d10-graphics-programming-guide-rasterizer-stage.md">Raster-Stufe</a>binden können. Diese Rasterizer-State-Schnittstelle unterstützt die erzwungene Stichproben Anzahl und den konservativen rasterisierungsmodus.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate"><strong>ID3D11SamplerState</strong></a><br/></td>
<td>Die samplerstatusschnittstelle enthält eine Beschreibung für den samplerstatus, den Sie an jede Shader-Stufe der <a href="overviews-direct3d-11-graphics-pipeline.md">Pipeline</a> binden können, um Sie durch Textur Beispiel Vorgänge zu verweisen.<br/></td>
</tr>
</tbody>
</table>



 

Direct3D 11 implementiert Schnittstellen für:

-   [Ressourcen](d3d11-graphics-reference-resource-interfaces.md)
-   [Shader](d3d11-graphics-reference-d3d11-shader-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kern Referenz](d3d11-graphics-reference-d3d11-core.md)
</dt> </dl>

