---
title: Neuerungen in der Technical Preview-Version von November 2008 Direct3D 11
description: Diese Version von Direct3D 11 enthält neue Features, Tools und Dokumentationen.
ms.assetid: 7d259764-b826-4609-b415-2093cc6df874
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a49529882eafaf092a866d1b172de62fe15c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390368"
---
# <a name="whats-new-in-the-nov-2008-direct3d-11-tech-preview"></a>Neuerungen in der Technical Preview-Version von November 2008 Direct3D 11

Diese Version von Direct3D 11 enthält neue Features, Tools und Dokumentationen.



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
<td><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>Mosaik<br/></td>
<td>Direct3D 11 bietet zusätzliche Pipeline Stufen, um das <a href="direct3d-11-advanced-stages-tessellation.md">Echt Zeit</a> Mosaik von hochwertigen primitiven zu unterstützen. Dank der umfangreichen programmierbaren Funktionen bietet dieses Feature viele verschiedene Methoden zum Auswerten von hochwertigen Oberflächen, einschließlich untergeordneter Oberflächen mithilfe von Näherungs Techniken, Bezier-Patches, adaptiver Mosaik-und Verschiebungs Zuordnung. Diese Funktion ist nur auf Direct3D 11-Klassen Hardware verfügbar. um dieses Feature zu evaluieren, müssen Sie daher den verweisrasterizer verwenden. Eine exemplarische Vorgehensweise finden Sie im <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> -Beispiel, das im Beispiel Browser verfügbar ist.<br/></td>
</tr>
<tr class="even">
<td><span id="Compute_Shader"></span><span id="compute_shader"></span><span id="COMPUTE_SHADER"></span>Compute-Shader<br/></td>
<td>Der <a href="direct3d-11-advanced-stages-compute-shader.md">Compute-Shader</a> ist eine zusätzliche Phase, die von der Direct3D 11-Pipeline unabhängig ist, die das allgemeine Computing auf der GPU ermöglicht. Zusätzlich zu allen shaderfeatures, die vom vereinheitlichten Shader-Kern bereitgestellt werden, unterstützt der COMPUTE-Shader auch verstreute Lese-und Schreibvorgänge in Ressourcen über ungeordnete Zugriffs Sichten, einen freigegebenen Speicherpool innerhalb einer Gruppe von ausgeführten Threads, Synchronisierungs primitiven, atomische Operatoren und viele andere erweiterte Daten parallele Features. In dieser Version wurde eine Variante des Direct3D 11-Compute-Shaders aktiviert, die auf Direct3D 10-Klassen-Hardware betrieben werden kann. Daher ist es möglich, COMPUTE-Shader auf tatsächlicher Hardware zu entwickeln, aber es ist ein aktualisierter Treiber erforderlich. Die vollständige Funktionalität des Direct3D 11-Compute-Shaders ist für die Unterstützung von Direct3D 11-Klassen-Hardware vorgesehen. um die vollständige Funktionalität zu evaluieren, müssen Sie daher den Verweis-Rasterizer verwenden, bis eine solche Hardware verfügbar ist. Eine Demo des Compute-Shaders in Aktion finden Sie im <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> -Beispiel, das im Beispiel Browser verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="Multithreaded_Rendering"></span><span id="multithreaded_rendering"></span><span id="MULTITHREADED_RENDERING"></span>Multithreaded-Rendering<br/></td>
<td>Der Schlüssel-API-Unterschied von Direct3D 10 in Direct3D 11 ist das Hinzufügen von <a href="overviews-direct3d-11-render-multi-thread.md">verzögerten Kontexten</a>, die eine skalierbare Ausführung von Direct3D-Befehlen ermöglichen, die über mehrere Kerne verteilt sind Ein verzögerter Kontext erfasst und assembliert Aktionen wie Zustandsänderungen und Zeichnen von Übermittlungen, die zu einem späteren Zeitpunkt auf dem eigentlichen Gerät ausgeführt werden können. Durch die Verwendung von verzögerten Kontexten für mehrere Threads kann eine Anwendung den CPU-Aufwand, der in der Direct3D11-Laufzeit und dem Treiber benötigt wird, auf mehrere Kerne verteilen, sodass die Computerkonfiguration eines Endbenutzers besser genutzt werden kann. Diese Funktion ist für die Verwendung mit der aktuellen Direct3D 10-Hardware und dem Referenz Raster verfügbar. Eine Demonstration der API-Nutzung finden Sie im <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> -Beispiel, das im Beispiel Browser verfügbar ist.<br/></td>
</tr>
<tr class="even">
<td><span id="Dynamic_Shader_Linkage_"></span><span id="dynamic_shader_linkage_"></span><span id="DYNAMIC_SHADER_LINKAGE_"></span>Dynamische shaderverknüpfung <br/></td>
<td>Um das combinatorisches Explosions Problem zu beheben, das in spezialisierten Shadern für die Leistung auftritt, führt Direct3D 11 eine begrenzte Form der Laufzeit- <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">shaderverknüpfung</a> ein, die eine nahezu optimale shaderspezialisierung während der Ausführung einer Anwendung ermöglicht. Dies wird erreicht, indem die Implementierungen spezifischer Funktionen im Shader-Code angegeben werden, wenn der Shader der Pipeline zugewiesen wird. Dadurch kann der Treiber schnell systemeigene shaderanweisungen Inline Inline aufrufen, anstatt den Treiber zu zwingen, die zwischen Sprache in systemeigene Anweisungen mit der neuen Konfiguration neu zu kompilieren. Die Shader-Entwicklung wird durch die Einführung von Klassen und Schnittstellen zu HLSL offengelegt. Eine Demonstration finden Sie im Beispiel <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">Dynamic Shader-Verknüpfung 11</a> , das über den Beispiel Browser verfügbar ist.<br/></td>
</tr>
<tr class="odd">
<td><span id="Windows_Advanced_Rasterizer__WARP_"></span><span id="windows_advanced_rasterizer__warp_"></span><span id="WINDOWS_ADVANCED_RASTERIZER__WARP_"></span>Windows Advanced Rasterizer (Warp)<br/></td>
<td>Warp ist in diesem SDK über Direct3D 11 und schließlich auch über Direct3D 10,1 verfügbar. Warp ist ein schnelles Skalierungsprogramm mit mehreren Kernen, das vollständig Direct3D 10,1-kompatibel ist. Die Verwendung dieser Technologie ist so einfach wie das Übergeben des D3D_DRIVER_TYPE_WARP-Flags bei der Erstellung des Geräts.<br/></td>
</tr>
<tr class="even">
<td><span id="Direct3D_10_and_Direct3D_11_on_Direct3D_9_Hardware__D3D10_Level_9_"></span><span id="direct3d_10_and_direct3d_11_on_direct3d_9_hardware__d3d10_level_9_"></span><span id="DIRECT3D_10_AND_DIRECT3D_11_ON_DIRECT3D_9_HARDWARE__D3D10_LEVEL_9_"></span>Direct3D 10 und Direct3D 11 auf Direct3D 9-Hardware (d3d10 Ebene 9)<br/></td>
<td>Die Direct3D-API ist in diesem SDK über Direct3D 11 und schließlich auch über Direct3D 10,1 verfügbar und kann auf die meisten Direct3D 9-Hardware und Direct3D 10, Direct3D 10,1 und Direct3D 11-Hardware abzielen. Dies wird erreicht, indem der Funktionsebenen-Mechanismus bereitgestellt wird, der Hardware je nach Funktionalität in sechs Kategorien gruppiert: 9_1, 9_2, 9_3, 10_0, 10_1 und 11_0. Eine Karte entspricht nur einer Funktionsebene, wenn Sie mit dieser Ebene vollständig kompatibel ist, und jede Ebene ist eine strikte Obermenge der darunter liegenden. Die Funktionalität wird minimal emuliert, um sicherzustellen, dass keine unerwarteten Leistungs Klippen gefunden werden. Folglich sind Features wie Geometry-Shader für Ziele der Direct3D 9-Ebene nicht verfügbar. <br/></td>
</tr>
<tr class="odd">
<td><span id="Runtime_Binaries"></span><span id="runtime_binaries"></span><span id="RUNTIME_BINARIES"></span>Lauf Zeit Binärdateien<br/></td>
<td>Alle Lauf Zeit Binärdateien, die in der Direct3D 11 Technical Preview bereitgestellt werden, die unter Windows 7 und Windows Vista SP1 verfügbar sein werden, werden mit dem SDK installiert und als &quot; Beta &quot; Komponenten (d. h. D3D11_beta.DLL) bezeichnet. Alle Komponenten der Beta-Bezeichnung werden Zeit bombardiert. Zum Erstellen von Projekten, um diese neuen Komponenten zu evaluieren, müssen Sie eine Verknüpfung mit der entsprechenden Beta-Bezeichnung importieren (d.h. D3D11_beta. lib). Wenn Sie über eine PDC-Kopie von Windows 7 verfügen, sind die Header, die LiCS und die pdsb, die in der Windows SDK mit dem Build bereitgestellt werden, für die Entwicklung mit den Direct3D 11-Komponenten von Windows 7 geeignet. Reservieren Sie die Verwendung der Header, der lisb und der pdsb in diesem SDK für die hier bereitgestellten Beta Komponenten.<br/></td>
</tr>
<tr class="even">
<td><span id="D3DX11"></span><span id="d3dx11"></span>Bibliothek d3dx11<br/></td>
<td>Bibliothek d3dx11 unterstützt derzeit das Textur laden, die Shader-Kompilierung, das Laden von Daten und Arbeits Thread Funktionen für Direct3D 11-Ressourcen. In Zukunft bietet diese Komponente weitere Technologien, die in d3dx10 verfügbar sind. Die Shader-Kompilierungs Funktionalität wird auch direkt über die Direct3D-Compilerkomponente bereitgestellt, wie im folgenden beschrieben<br/></td>
</tr>
<tr class="odd">
<td><span id="HLSL_and_Direct3D_Compiler"></span><span id="hlsl_and_direct3d_compiler"></span><span id="HLSL_AND_DIRECT3D_COMPILER"></span>HLSL-und Direct3D-Compiler<br/></td>
<td>Der HLSL-Compiler verfügt über mehrere neue Features für die Unterstützung der neuen Technologien, die in Direct3D 11 verfügbar sind. Dies umfasst die objektorientierte Programmierung über Schnittstellen und Klassen, eine direkte Indizierungs Syntax für Ressourcen Belastungen und das Schlüsselwort "präzise", um sicherzustellen, dass alle Vorgänge, die mit einer bestimmten Variablen ausgeführt werden, den strengen Gleit Komma Regeln entsprechen. Fast alle neuen linguistischen Features haben eine gültige Funktionalität für vorhandene Shader-Ziele. Zusätzlich zur Unterstützung aller Direct3D 9-, Direct3D 10-, Direct3D 10,1-und Direct3D 11-Shader unterstützt der HLSL-Compiler auch die speziellen Ziele, die zum Schreiben von Shader für Direct3D 10 Level 9-Ziele erforderlich sind. Der D3D-Compiler ist jetzt direkt außerhalb von d3dx10 und Bibliothek d3dx11 über D3DCompiler. H und D3DCompiler. lib zugänglich. Mit diesen neuen Dateien muss eine Anwendung nicht mit D3DX verknüpft werden, um die Lauf Zeit Kompilierung auszuführen, und eine Anwendung muss den Compiler nicht einschließen, wenn nur D3DX-Funktionalität benötigt wird.<br/></td>
</tr>
<tr class="even">
<td><span id="D3D11_Reference_Rasterizer"></span><span id="d3d11_reference_rasterizer"></span><span id="D3D11_REFERENCE_RASTERIZER"></span>D3D11-Referenz Raster<br/></td>
<td>Der Reference Rasterizer stellt eine Gold-Standard-rasterisierungsimplementierung für die Evaluierung der Direct3D 11-Features zur Verfügung, die noch nicht in der Hardware verfügbar waren Der verweisrasterizer wird auch als Möglichkeit bereitgestellt, eine bestimmte Hardware Implementierung für den rasterisierungsstandard zu überprüfen. Der Verweis Raster ist auf Richtigkeit, nicht auf Leistung ausgelegt. Um ein Referenzgerät zu erstellen, übergeben Sie einfach das D3D_DRIVER_TYPE_REFERENCE-Flag bei der Geräte Erstellung. <br/></td>
</tr>
<tr class="odd">
<td><span id="D3D11_SDK_Layers"></span><span id="d3d11_sdk_layers"></span><span id="D3D11_SDK_LAYERS"></span>D3D11-SDK-Ebenen<br/></td>
<td>Direct3D11-SDK-Ebenen bieten einen Mechanismus zum Überwachen des Betriebs der Direct3D 11-Laufzeit während der Entwicklung. Dies wird derzeit für die Bereitstellung nützlicher Debuginformationen verwendet, die nicht nur Fehler bei unsachgemäßer Verwendung enthalten, sondern auch Warnungen, die die empfohlene Verwendung der Laufzeit empfehlen und häufig ausführliche nützliche Informationen zum Debuggen bereitstellen. Es wird dringend empfohlen, dass die Debugausgabe von D3D11 SDK-Schichten während der Entwicklung jederzeit aktiviert ist und eine Anwendung während der Ausführung keine Debugausgaben generiert, bevor Sie für die Profilerstellung freigegeben oder mit pix für Windows verwendet wird. Das Aktivieren der Debugebene ist so einfach wie das Übergeben des D3D11_CREATE_DEVICE_DEBUG-Flags zum Zeitpunkt der Erstellung des Geräts. Entwicklern wird dringend empfohlen, Ebenen in Debugbuilds zu verwenden. Ebenen werden nicht für die Verwendung in Profil-oder Releasebuilds empfohlen.<br/></td>
</tr>
<tr class="even">
<td><span id="New_Samples"></span><span id="new_samples"></span><span id="NEW_SAMPLES"></span>Neue Beispiele<br/></td>
<td>Diese Version enthält vier neue Beispiele.<br/>
<ul>
<li>Das Beispiel <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">Dynamic Shader Linking 11</a> veranschaulicht die Verwendung von Shader Model 5-Shader-Schnittstellen und Direct3D 11-Unterstützung für das Verknüpfen von Shader-Schnittstellen Methoden zur Laufzeit.</li>
<li>Das <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> -Beispiel veranschaulicht, wie der COMPUTE-Shader (CS kurz später) eingerichtet und ausgeführt wird. dabei handelt es sich um eine der spannendsten neuen Features von Direct3D 11. Obwohl im Beispiel nur die CS verwendet werden, um die HDR-Audiozuordnung zu implementieren, sollte das Konzept problemlos auf andere nach Verarbeitungsalgorithmen und allgemeinere Berechnungen erweitert werden.</li>
<li>Das <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> -Beispiel veranschaulicht, wie das Rendering zwischen mehreren Threads mit sehr geringem mehr Aufwand aufgeteilt wird.</li>
<li>Das neue <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> -Beispiel ähnelt dem SubD10-Beispiel im DirectX SDK, mit dem Unterschied, dass es erweitert wurde, um drei neue Direct3D 11-Pipeline Phasen zu nutzen: den Hull-Shader, den Mosaik Dienst und den Domänen-Shader.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In früheren Versionen eingeführte Features](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

