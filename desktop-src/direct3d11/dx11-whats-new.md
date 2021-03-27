---
title: Neuerungen im SDK für Windows 7/Direct3D 11 vom August 2009
description: Diese Version von Windows 7/Direct3D 11 wird als Teil des DirectX SDK ausgeliefert und enthält neue Features, Tools und Dokumentationen.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103731560"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Neuerungen im SDK für Windows 7/Direct3D 11 vom August 2009

Diese Version von Windows 7/Direct3D 11 wird als Teil des DirectX SDK ausgeliefert und enthält neue Features, Tools und Dokumentationen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Bei Direct2D handelt es sich um eine hardwarebeschleunigte, 2D-Grafik-API, die leistungsstarke und qualitativ hochwertige Rendering für 2-d-Geometrie, Bitmaps und Text bereitstellt. Die Direct2D-API ist für die Zusammenarbeit mit Direct3D und GDI konzipiert. Mit diesem SDK können Entwickler die API auswerten und einfache Anwendungen schreiben, mit einigen der erweiterten Funktionen, die auf ordnungsgemäß konfigurierten Computern möglich sind. <br/> <a href="/windows/win32/direct2d/direct2d-portal">Dokumentation</a> und <a href="/previous-versions//dd372354(v=vs.85)">Beispiele</a> für Direct2D sind zurzeit auf MSDN verfügbar.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite bietet Unterstützung für hochwertige Text Rendering, auflösungsunabhängige Gliederungs Schriftarten, vollständige Unicode-Text-und Layoutunterstützung und vieles mehr:<br/>
<ul>
<li>Ein Geräte unabhängiges textlayoutsystem zur Verbesserung der Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche.<br/></li>
<li>Hochwertiges, unter Pixel-, ClearType-Text Rendering, das GDI-Direct3D, Direct2D oder anwendungsspezifische renderingtechnologie verwenden kann.<br/></li>
<li>Unterstützung für mehr formatieren Text. <br/></li>
<li>Unterstützung für die erweiterten Typografiefunktionen von OpenType-Schriftarten.<br/></li>
<li>Unterstützung für das Layout und Rendering von Text in allen Sprachen, die von Windows unterstützt werden.<br/></li>
</ul>
Mit diesem SDK können Entwickler die API auswerten und grundlegende Anwendungen nur zu Demonstrationszwecken schreiben.<br/> <a href="/windows/win32/directwrite/direct-write-portal">Dokumentation</a> und <a href="/windows/win32/directwrite/samples">Beispiele</a> für DirectWrite sind zurzeit auf MSDN verfügbar.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> baut auf DXGI 1,0 auf und ist für Windows Vista und Windows 7 verfügbar. DXGI 1,1 fügt mehrere neue Features hinzu:<br/>
<ul>
<li>Synchronisierte Unterstützung für freigegebene Oberflächen Dies ermöglicht eine effiziente Lese-und Schreib Oberflächen Freigabe zwischen mehreren D3D (möglicherweise zwischen d3d10-und D3D11-Geräten).<br/></li>
<li>BGRA-Formatunterstützung. Dies ermöglicht GDI das renderauf derselben DXGI-Oberfläche, die von einem Direct2D-, Direct3D 10,1-oder Direct3D 11-Gerät betroffen ist. <br/></li>
<li>Maximale Frame Latenz. Mithilfe von <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: setmaximumframelatency</strong></a> und <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: getmaximumframelatency</strong></a>können Titel die Anzahl der Frames steuern, die vor der Übermittlung für das Rendering in einer Warteschlange gespeichert werden dürfen. Latenz wird häufig verwendet, um zu steuern, wie die CPU zwischen der Reaktion auf Benutzereingaben und Frames in der geralteschlange auswählt.<br/></li>
<li>Adapterenumeration. Mithilfe von <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>können Titel lokale Adapter ohne angehängte Monitore oder Ausgaben sowie Adapter mit verbundenen Ausgaben auflisten.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Aktualisierte Beispiele<br/></td>
<td>Diese Version enthält mehrere neue und aktualisierte Beispiele.<br/>
<ul>
<li>Die neue <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> ist eine Abbildung erweiterter Verarbeitungsverfahren für Compute-Shader, die auf einer d3d10-oder D3D11-GPU ausgeführt werden können.</li>
<li>Das <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11-Beispiel</a> wurde erweitert, um aufgrund der Verwendung von Compute-Shader (zusätzlich zur Tabellen Zuordnung) weich-und Blüten Effekte zu implementieren, und stellt für Vergleiche Pixel-Shader-Implementierungen bereit.</li>
<li>Das <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11-Beispiel</a> wurde erheblich aktualisiert, mit komplexeren Kunst Ressourcen und einer intensiveren Thread bezogenen Verarbeitung.</li>
<li>Das <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11-Beispiel</a> wurde mit einem neuen Gesichts Modell aktualisiert, und das Beispiel nutzt nun das Feature "featureberechnung" des Samples Content Exporter.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In früheren Versionen eingeführte Features](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

