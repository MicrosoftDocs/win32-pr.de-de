---
title: Migrieren zu Direct3D 11
description: Dieser Abschnitt enthält Informationen für die Migration von einer früheren Version von Direct3D zu Direct3D 11.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316623"
---
# <a name="migrating-to-direct3d-11"></a>Migrieren zu Direct3D 11

Dieser Abschnitt enthält Informationen für die Migration von einer früheren Version von Direct3D zu Direct3D 11.

-   [Direct3D 9 bis Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 bis Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Enumerationen und Definitionen](#enumerations-and-defines)
    -   [Strukturen](#structures)
    -   [Schnittstellen](#interfaces)
    -   [Weitere verwandte Technologien](#other-related-technologies)
-   [Direct3D 10,1 bis Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Enumerationen und Definitionen](#enumerations-and-defines)
    -   [Strukturen](#structures)
    -   [Schnittstellen](#interfaces)
-   [Neue Features für Direct3D 11](#new-features-for-direct3d-11)
-   [Neue Features für DirectX 11,1](#new-features-for-directx-111)
-   [Neue Features für DirectX 11,2](#new-features-for-directx-112)
-   [Zugehörige Themen](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 bis Direct3D 11

Die Direct3D 11-API baut auf den Verbesserungen der Infrastruktur in Direct3D 10 und 10,1 auf. Das Portieren von Direct3D 9 auf Direct3D 11 ähnelt dem Wechsel zwischen Direct3D 9 und Direct3D 10. Im folgenden sind die wichtigsten Herausforderungen bei diesem Bemühen aufgeführt.

-   Entfernen der gesamten Verwendung fester Funktions Pipeline zugunsten von programmierbaren Shadern, die ausschließlich in HLSL erstellt wurden (kompiliert über D3DCompiler anstelle von D3DX9).
-   Zustands Verwaltung auf der Grundlage unveränderlicher Objekte anstelle einzelner Status umschalten.
-   Aktualisieren von, um strenge Verknüpfungs Anforderungen von Vertex-Puffer Eingabe Layouts und shadersignaturen einzuhalten.
-   Zuordnen von Shader-Ressourcen Sichten zu allen Textur Ressourcen.
-   Zuordnung des gesamten Bildinhalts zu einem DXGI \_ -Format, einschließlich des Entfernens aller 16-Bit-Farb Formate (5/5/5/1, 5/6/5, 4/4/4/4), des Entfernens aller 24-Bit-Farb Formate (8/8/8) und der strengen RGB-Farbreihen Folge.
-   Aufteilen der Verwendung des globalen Konstanten Zustands in mehrere kleine, effizienter aktualisierte Konstante Puffer.

Weitere Informationen zum Wechsel von Direct3D 9 zu Direct3D 10 finden Sie unter [Direct3D 9 bis Direct3D 10 Überlegungen](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 bis Direct3D 11

Das Umschreiben von Programmen, die zur Verwendung der API Direct3D 10 oder 10,1 geschrieben wurden, ist ein geradliniger Prozess, da Direct3D 11 eine Erweiterung der vorhandenen API ist. Mit nur einer kleinen Ausnahme (unten-monochrome Text Filterung) sind alle Methoden und Funktionen in Direct3D 10/10.1 in Direct3D 11 verfügbar. In der folgenden Gliederung werden die Unterschiede zwischen den beiden APIs zur Unterstützung beim Aktualisieren von vorhandenem Code beschrieben. Die wichtigsten Unterschiede sind hier:

-   Renderingvorgänge (Draw, State usw.) sind nicht mehr Teil der Geräteschnittstelle, sondern sind stattdessen ein Teil der neuen DeviceContext-Schnittstelle zusammen mit ressourcenmap/unmap-und Geräte Abfrage Methoden.
-   Direct3D 11 umfasst alle Verbesserungen und Änderungen, die zwischen Direct3D 10,0 und 10,1 vorgenommen wurden.

### <a name="enumerations-and-defines"></a>Enumerationen und Definitionen



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DXGI- \_ Format                           | [**DXGI \_ Das Formatieren**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)mehrerer neuer DXGI-Formate wurde definiert.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3d10 \_ Erstellen eines \_ Geräte \_ Wechsels \_ zu \_ Ref | [**D3D11 \_ Create \_ Device \_ Switch \_ to \_ ref**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)die Switch-to-REF-Funktion wird von Direct3D 11 nicht unterstützt.<br/>                                                                                                                                                                                                                                                                        |
| D3d10 \_ - \_ Treibertyp                    | [**D3D \_ \_Treibertyp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)beachten Sie, dass die Enumerationsbezeichner in [**D3D \_ Driver \_ Type**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) aus den bezeichlern im [**d3d10- \_ \_ Treibertyp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)neu definiert wurden. Daher sollten Sie sicherstellen, dass Sie die Enumerationsbezeichner anstelle von Literalzahlen verwenden.<br/> [**D3D \_ Der \_ Treibertyp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) ist in D3Dcommon. h definiert.<br/> |
| D3d10 \_ \_ ressourcenmisc- \_ Flag            | [**D3D11 \_ \_Ressourcenmisc \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)beachten Sie, dass viele dieser Flags neu definiert wurden. Achten Sie daher darauf, dass Sie enumerationsids anstelle von Literalzahlen verwenden.<br/>                                                                                                                                                                                                                                |
| D3d10- \_ Filter                          | [**D3D11 \_ Filter**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)beachten Sie, dass die Text Filterung d3d10 \_ Filter \_ Text \_ 1 Bit aus Direct3D 11 entfernt wurde. Siehe DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| D3D11- \_ Counter                         | [**D3D11 \_ Beachten Sie**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter), dass die herstellerneutralen Leistungsindikatoren für Direct3D 11 entfernt wurden, da Sie selten unterstützt wurden.<br/>                                                                                                                                                                                                                                                                          |
| D3d10 \_ x                               | D3D11 \_ x viele Enumerationen und Definitionen sind identisch, haben größere Grenzwerte oder verfügen über zusätzliche Werte.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Strukturen



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10 \_ so- \_ Deklarations \_ Eintrag            | [**D3D11 \_ Der \_ Deklarations \_ Eintrag fügt also**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)Stream hinzu.<br/>                                                                  |
| D3d10 \_ Blend- \_ Entsc                       | [**D3D11 \_ Blend- \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)Hinweis Diese Struktur hat sich von 10 auf 10,1 erheblich geändert, um den Blend-Status pro Renderziel anzugeben.<br/> |
| D3d10- \_ Puffer \_                      | [**D3D11 \_ Puffer- \_ Debugger**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)fügt einen structurebytestride zur Verwendung mit COMPUTE-Shaderressourcen hinzu.<br/>                                 |
| D3d10 \_ Shader- \_ Ressourcen \_ Ansicht \_ (Debug)      | [**D3D11 \_ Shader \_ - \_ Ressourcen \_ Ansicht**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc): die Struktur enthielt zusätzliche Union-Member, die für 10,1 hinzugefügt wurden.<br/>    |
| D3d10 \_ tiefen \_ Schablone \_ anzeigen \_        | [**D3D11 \_ Die Detailansicht für die tiefen \_ Schablone \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)weist einen neuen Flags-Member auf.<br/>                                                |
| D3d10 \_ Abfrage \_ Daten \_ Pipeline- \_ Statistik | [**D3D11 \_ Die Abfrage \_ Daten \_ Pipeline- \_ Statistik**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)fügt mehrere neue Shader-Stufen Indikatoren hinzu.<br/>                  |
| D3d10 \_ x                                 | D3D11 \_ x viele Strukturen sind zwischen den beiden APIs identisch.<br/>                                                                                     |



 

### <a name="interfaces"></a>Schnittstellen



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und [ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> Die Geräteschnittstelle wurde in diese beiden Teile aufgeteilt. Für die schnelle Portierung können Sie [**ID3D11Device:: getimmediatecontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)verwenden.<br/> Die Methoden "ID3D10Device:: gettextfiltersize" und "settextfilersize" sind nicht mehr vorhanden. Siehe DirectWrite.<br/> Create \* Shader übernimmt einen zusätzlichen optionalen Parameter für [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Setshader und \* getshader nehmen zusätzliche optionale Parameter für [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s) auf.<br/> " [**Kreategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) " nimmt ein Array und eine Anzahl für mehrere ausgabestreamschritte an.<br/> Der Grenzwert für den numentries-Parameter von " [**forategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) " wurde auf "D3D11" erweitert, sodass die Anzahl der \_ \_ \_ \* \_ \_ Ausgabe \_ Komponenten \_ in Direct3D 11 liegt.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) Switch-to-Ref-Funktionen werden in Direct3D 11 nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Die Map-und die unmap-Methode wurden zu [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)verschoben, und alle Zuordnungs Methoden verwenden die D3D11-zugeordnete unter [**\_ \_ geordnete Quelle**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) anstelle eines void-Ausdrucks \* \* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) BEGIN, End und GetData wurden in [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)verschoben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x viele Schnittstellen sind zwischen den beiden APIs identisch.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Weitere verwandte Technologien



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>10/10.1-Lösung</th>
<th>11 Lösung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>HLSL Complier (D3D10Compile *, D3DX10Compile*) und Shader Reflection-APIs</td>
<td>D3DCompiler (siehe D3DCompiler. h)
<blockquote>
[!Note]<br />
Für Windows Store-Apps werden die <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">D3DCompiler-APIs</a> nur für die Entwicklung und nicht für die Bereitstellung unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Auswirkungen 10</td>
<td>Die <a href="https://github.com/Microsoft/FX11">Auswirkungen 11</a> sind online als freigegebene Quelle verfügbar.
<blockquote>
[!Note]<br />
Diese Lösung eignet sich nicht für Windows Store-Apps, da Sie die <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">D3DCompiler-APIs</a> zur Laufzeit (Bereitstellung) erfordert.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DX9/d3dx10 math</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>Bibliothek d3dx11 im alten DirectX SDK <a href="https://github.com/Microsoft/DirectXTex">directxtex</a>, <a href="https://github.com/Microsoft/DirectXTK">directxtk</a>und <a href="https://github.com/Microsoft/DirectXMesh">directxmesh</a> bieten Alternativen zu vielen Technologien in den Legacy-d3dx10-und Bibliothek d3dx11-Bibliotheken.<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> und <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> bieten hochwertige Unterstützung für das Rendern von formatierten Linien und Schriftarten.<br/></td>
</tr>
</tbody>
</table>



 

Informationen zum Legacy-DirectX SDK finden Sie unter [wo ist das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10,1 bis Direct3D 11

Direct3D 10,1 ist eine Erweiterung der Direct3D 10-Schnittstelle, und alle Features von Direct3D 10,1 sind in Direct3D 11 verfügbar. Der größte Teil der Portierung von 10,1 auf 11 ist bereits über den Wechsel zwischen 10 und 11 adressiert.

### <a name="enumerations-and-defines"></a>Enumerationen und Definitionen



| Direct3D 10,1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10- \_ Funktion \_ Level1 | [**D3D \_ Funktions \_ Ebene**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)identisch, aber definiert in D3DCommon. h Plus Hinzufügen von \_ D3D \_ Featureebene \_ 11 \_ 0 für 11-Klassen Hardware zusammen mit D3D \_ Feature \_ Level \_ 9 \_ 1, D3D \_ Feature \_ Level \_ 9 \_ 2 und D3D \_ Feature \_ Level \_ 9 \_ 3 für 10level9<br/> (D3d10 \_ \_Die Featureebene \_ 9 \_ 1, d3d10 Featureebene \_ \_ \_ 9 \_ 2 und d3d10 \_ Feature \_ Level \_ 9 \_ 3 wurden ebenfalls für 10,1 bis d3d10 \_ 1. h hinzugefügt.)<br/> |



 

### <a name="structures"></a>Strukturen



| Direct3D 10,1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3d10 \_ Blend \_ DESC1                  | [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)die 11-Version ist identisch mit 10,1.<br/>                                 |
| D3d10- \_ Shader- \_ Ressourcen \_ Ansicht \_ DESC1 | [**D3D11 \_ Shader- \_ Ressourcen \_ Ansicht \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)die 11-Version ist identisch mit 10,1.<br/> |



 

### <a name="interfaces"></a>Schnittstellen



| Direct3D 10,1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und [ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> Die Geräteschnittstelle wurde in diese beiden Teile aufgeteilt. Für die schnelle Portierung können Sie [**ID3D11Device:: getimmediatecontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext)verwenden.<br/> Die Methoden "ID3D10Device:: gettextfiltersize" und "settextfilersize" sind nicht mehr vorhanden. Siehe DirectWrite.<br/> Create \* Shader übernimmt einen zusätzlichen optionalen Parameter für [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Setshader und \* getshader nehmen zusätzliche optionale Parameter für [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s) auf.<br/> " [**Kreategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) " nimmt ein Array und eine Anzahl für mehrere ausgabestreamschritte an.<br/> Der Grenzwert für den numentries-Parameter von " [**forategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) " wurde auf "D3D11" erweitert, sodass die Anzahl der \_ \_ \_ \* \_ \_ Ausgabe \_ Komponenten \_ in Direct3D 11 liegt.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Neue Features für Direct3D 11

Nachdem der Code für die Verwendung der Direct3D 11-API aktualisiert wurde, gibt es zahlreiche [neue Features](direct3d-11-features.md) , die berücksichtigt werden müssen.

-   Multithreaded-Rendering über Befehlslisten und mehrere Kontexte
-   Implementieren von erweiterten Algorithmen mithilfe von Compute-Shader (mit 4,0-, 4,1-oder 5,0-shaderprofilen)
-   Neue, 11-Klassen-Hardware Features:
    -   HLSL-Shader-Modell 5,0
    -   Dynamische shaderverknüpfung
    -   Mosaik durch Hülle und Domänen-Shader
    -   Neue Block Komprimierungs Formate: BC6H for HDR Images, bzw bc7 for höhere Fidelity Standard Images
-   Verwendung der [10 Level9-Technologie](overviews-direct3d-11-devices-downlevel.md) zum Rendern auf vielen Shader-Modell 2,0-und Shader-Modell 3,0-Geräten über die DIrect3D 11-API für die Unterstützung von niedrigerer Video Hardware unter Windows Vista und Windows 7.
-   Nutzung des Warp Software-renderinggeräts.

## <a name="new-features-for-directx-111"></a>Neue Features für DirectX 11,1

Windows 8 enthält weitere DirectX-Grafik Erweiterungen, die Sie bei der Implementierung Ihres DirectX-Grafik Codes berücksichtigen sollten. dazu gehören [Direct3D 11,1](direct3d-11-features.md), [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [Windows Display Driver Model (WDDM) 1,2](/windows-hardware/drivers/display/wddm-in-windows-8), [Feature Level](overviews-direct3d-11-devices-downlevel-intro.md) 11,1 Hardware, Direct2D Device Kontexte und andere Verbesserungen.

Teil Unterstützung für [Direct3D 11,1](direct3d-11-features.md) ist unter Windows 7 auch über das [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)verfügbar, das über das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar ist.

## <a name="new-features-for-directx-112"></a>Neue Features für DirectX 11,2

Die Windows 8.1 umfasst [Direct3D 11,2](direct3d-11-2-features.md), [DXGI 1,3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)und andere Verbesserungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

