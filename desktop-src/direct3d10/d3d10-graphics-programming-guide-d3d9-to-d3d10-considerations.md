---
description: Auf der folgenden Seite finden Sie eine grundlegende Übersicht über die wichtigsten Unterschiede zwischen Direct3D 9 und Direct3D 10. Der folgende Umriss bietet einige Einblicke, die Entwicklern bei der Direct3D 9-Unterstützung bei der Unterstützung von Direct3D 10 helfen.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Überlegungen zu Direct3D 9 bis Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467ceefe7784a9b408bb36c8bed13217cb6de7c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748024"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Überlegungen zu Direct3D 9 bis Direct3D 10 (Direct3D 10)

Auf der folgenden Seite finden Sie eine grundlegende Übersicht über die wichtigsten Unterschiede zwischen Direct3D 9 und Direct3D 10. Der folgende Umriss bietet einige Einblicke, die Entwicklern bei der Direct3D 9-Unterstützung bei der Unterstützung von Direct3D 10 helfen.

Obwohl die Informationen in diesem Thema Direct3D 9 mit Direct3D 10 vergleichen, da Direct3D 11 auf den Verbesserungen in Direct3D 10 und 10,1 aufbaut, benötigen Sie diese Informationen auch für die Migration von Direct3D 9 zu Direct3D 11. Informationen zum überschreiten von Direct3D 10 nach Direct3D 11 finden Sie unter [Migrieren zu Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Übersicht über die wesentlichen strukturellen Änderungen in Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Entfernen der Fixed-Funktion](#removal-of-fixed-function)
    -   [Validierung der Erstellungszeit des Geräte Objekts](#device-object-creation-time-validation)
-   [Engine-Abstraktionen/-Trennung](/windows)
    -   [Direktes Entfernen von Direct3D 9-Abhängigkeiten](#direct-removal-of-direct3d-9-dependencies)
-   [Tricks zum schnellen Beheben von Problemen mit der Anwendungs Erstellung](#tricks-for-quickly-resolving-application-build-issues)
    -   [Überschreiben von Direct3D 9-Typen](#overriding-direct3d-9-types)
    -   [Beheben von Link Problemen](#resolving-link-issues)
    -   [Simulieren von Geräte Deckeln](#simulating-device-caps)
-   [Antreiben der Direct3D 10-API](#driving-the-direct3d-10-api)
    -   [Erstellen von Ressourcen](#resource-creation)
    -   [Ansichten](#views)
    -   [Statischer und dynamischer Ressourcen Zugriff](#static-versus-dynamic-resource-access)
    -   [Direct3D 10 Effekte](#direct3d-10-effects)
    -   [HLSL ohne Auswirkungen](#hlsl-without-effects)
    -   [Shader-Kompilierung](#shader-compilation)
    -   [Erstellen von Shaderressourcen](#creation-of-shader-resources)
    -   [Shader Reflection Layer-Schnittstelle](#shader-reflection-layer-interface)
    -   [Layouts des Eingabe Assemblers-Vertexshader/Eingabedaten Strom Verknüpfung](/windows)
    -   [Auswirkungen des Entfernens von Shader-Toten Code](#impact-of-shader-dead-code-removal)
    -   [Beispiel für Vertex-Shader-Eingabe Struktur](#vertex-shader-input-structure-example)
    -   [Zustands Objekt Erstellung](#state-object-creation)
-   [Portieren von Texturen](#porting-textures)
    -   [Unterstützte Dateiformate](#file-formats-supported)
    -   [Mapping-Textur Formate](#mapping-texture-formats)
-   [Portieren von Shadern](#porting-shaders)
    -   [Direct3D 10-Shader werden in HLSL erstellt.](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Shadersignaturen und Verknüpfungen](#shader-signatures-and-linkage)
    -   [HLSL-Shader-Phasen Verknüpfungen](#hlsl-shader-stage-linkages)
    -   [Konstantenpuffer](#constant-buffers)
    -   [Benutzer Clip Flächen in HLSL auf Featureebene 9 und höher](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Weitere Direct3D 10-Unterschiede bei der Überwachung](#additional-direct3d-10-differences-to-watch-for)
    -   [Ganze Zahlen als Eingabe](#integers-as-input)
    -   [Maus Cursor](#mouse-cursors)
    -   [Zuordnung von Texels zu Pixeln in Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Verhaltensänderungen der Verweis Zählung](#reference-counting-behavior-changes)
    -   [Test kooperative Ebene](#test-cooperative-level)
    -   [Stretchrect](#stretchrect)
-   [Weitere Direct3D 10,1-Unterschiede](#additional-direct3d-101-differences)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Übersicht über die wesentlichen strukturellen Änderungen in Direct3D 10

-   [Entfernen der Fixed-Funktion](#removal-of-fixed-function)
-   [Validierung der Erstellungszeit des Geräte Objekts](#device-object-creation-time-validation)

Der Renderingvorgang mit dem Direct3D 10-Gerät ist strukturell ähnlich wie bei Direct3D 9.

-   Festlegen einer vertexstreamquelle
-   Festlegen des Eingabe Layouts in Direct3D 10 (Festlegen der vertexstreamdeklaration in Direct3D 9)
-   Primitive Topologie deklarieren
-   Festlegen von Texturen
-   Festlegen von Zustands Objekten
-   Shader festlegen
-   Draw

Der [**Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) -Befehl verknüpft die Vorgänge. die Reihenfolge der Aufrufe vor dem Zeichnen-Aufruf ist willkürlich. Die wichtigsten Unterschiede im Direct3D 10-API-Design lauten wie folgt:

-   Entfernen der Fixed-Funktion
-   Entfernen von Caps Bits Direct3D die Basis Funktionsgruppe von 10 ist garantiert.
-   Strengere Verwaltung von: Ressourcen Zugriff, Gerätestatus, shaderkonstanten, shaderverknüpfung (Eingaben und Ausgaben für Shader) Zwischenstufen
-   Die Namensänderungen von API-Einstiegspunkten entsprechen der Verwendung des virtuellen GPU-Speichers (Map () anstelle von Lock ()).
-   Dem Gerät kann zum Zeitpunkt der Erstellung eine debugschicht hinzugefügt werden.
-   Die primitive Topologie ist nun ein expliziter Zustand (getrennt vom [**Zeichnen**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) -Befehl).
-   Explizite shaderkonstanten werden nun in konstanten Puffern gespeichert.
-   Die Shader-Erstellung erfolgt vollständig in HLSL. Der HLSL-Compiler befindet sich nun in der primären Direct3D 10-dll.
-   Neue programmierbare Phase: der Geometrie-Shader
-   Entfernen von BeginScene ()/EndScene ()
-   Allgemeine 2D-, Fokus-und Adapter Verwaltungsfunktionen, die in einer neuen Komponente implementiert werden: DXGI

### <a name="removal-of-fixed-function"></a>Entfernen der Fixed-Funktion

Manchmal ist es überraschend, dass auch in einer Direct3D 9-Engine, die die programmierbare Pipeline voll ausgenutzt hat, eine Reihe von Bereichen vorhanden sind, die von der Pipeline mit fester Funktions Dauer (FF) abhängen. Die häufigsten Bereiche beziehen sich normalerweise auf das auf dem Bildschirm ausgerichtete Rendering für die Benutzeroberfläche. Aus diesem Grund ist es wahrscheinlich, dass Sie einen FF-Emulations-Shader oder eine Reihe von Shadern erstellen müssen, die das erforderliche Austausch Verhalten bereitstellen.

Diese Dokumentation enthält ein Whitepaper, das Ersatz-shaderquellen für die gängigsten FF-Verhaltensweisen enthält (siehe Beispiel für eine [Fixed-Funktion](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Einige Pixel Verhalten fester Funktionen, einschließlich des Alpha Tests, wurden in Shader verschoben.

### <a name="device-object-creation-time-validation"></a>Validierung der Erstellungszeit des Geräte Objekts

Die Pipeline "Direct3D 10" wurde von Grund auf in Hardware und Software neu entworfen, um den CPU-mehr Aufwand (zur Zeichnen der Zeit) zu verringern. Um die Kosten zu senken, wurden allen Arten von Gerätedaten ein Objekt mit expliziten Erstellungs Methoden zugewiesen, die vom Gerät selbst bereitgestellt werden. Dies ermöglicht eine strikte Datenüberprüfung zur Objekt Erstellungszeit anstelle von während des Draw-Aufrufes, wie dies häufig bei Direct3D 9 der Fall ist.

## <a name="engine-abstractions--separation"></a>Engine-Abstraktionen/-Trennung

Bei Anwendungen, einschließlich spielen, die sowohl Direct3D 9 als auch Direct3D 10 unterstützen möchten, müssen die renderingschichten vom Rest der Codebasis abstrahiert werden. Es gibt viele Möglichkeiten, dies zu erreichen, aber der Schlüssel für alle diese ist das Design der Abstraktionsschicht für das Direct3D-Gerät auf niedrigerer Ebene. Alle Systeme sollten über die allgemeine Ebene mit der Hardware kommunizieren, die für die Bereitstellung von GPU-Ressourcen und Low-Level-typverwaltung entwickelt wurde.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Direktes Entfernen von Direct3D 9-Abhängigkeiten

Beim Portieren umfangreicher, zuvor getesteter Codebasen ist es wichtig, die Menge an Codeänderungen zu minimieren, die unbedingt erforderlich sind, um bereits getestete Verhalten im Code beizubehalten. Zu den bewährten Methoden zählen die eindeutige Dokumentierung von Elementen mithilfe von Kommentaren. Häufig ist es sinnvoll, einen Kommentar Standard für diese Arbeit zu haben, der eine schnelle Navigation durch die Codebasis ermöglicht.

Im folgenden finden Sie eine Beispielliste mit Standard Kommentaren für einzelne Zeilen/Startblöcke, die für diese Arbeit verwendet werden könnten.



| Element                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 entfernt<br/>                     | Verwenden Sie dies, wenn Zeilen/Code Blöcke entfernt werden.<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 benötigt Update<br/> | Das Hinzufügen zusätzlicher Hinweise zum Update Update erforderlich, das vorschlägt, welche work/New-API für spätere Besuche im Code für die Verhaltens Konvertierung verwendet werden soll. Die intensive Verwendung von Assert (**false**) sollte auch verwendet werden, wenn für \\ \\ Direct3D 10 Updates erforderlich sind, um sicherzustellen, dass Sie keinen unwissentlich ausgeirrten Code ausführen.<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 geändert<br/>                     | Bereiche, in denen wesentliche Änderungen aufgetreten sind, sollten für den zukünftigen Verweis aufbewahrt, aber auskommentiert werden.<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 Ende<br/>                                     | Endcode Block-Qualifizierer<br/>                                                                                                                                                                                                                                                                                            |



 

Für mehrere Quellzeilen sollten Sie auch die C-Formatvorlagen/ \* \* -Kommentare verwenden, aber die relevanten Start-/endkommentare zu diesen Bereichen hinzufügen.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Tricks zum schnellen Beheben von Problemen mit der Anwendungs Erstellung

-   [Überschreiben von Direct3D 9-Typen](#overriding-direct3d-9-types)
-   [Beheben von Link Problemen](#resolving-link-issues)
-   [Simulieren von Geräte Deckeln](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Überschreiben von Direct3D 9-Typen

Es kann sinnvoll sein, eine übergeordnete Header Datei einzufügen, die Typdefinitionen/über Schreibungen für Direct3D 9-Basis Typen enthält, die von den Direct3D 10-Headern nicht mehr unterstützt werden. Auf diese Weise können Sie die Menge der Änderungen im Code und Schnittstellen minimieren, wenn eine direkte Zuordnung von einem Direct3D 9-Typ zum neu definierten Direct3D 10-Typ vorliegt. Diese Vorgehensweise ist auch nützlich, wenn Code Verhalten in einer Quelldatei zusammengehalten werden soll. In diesem Fall empfiehlt es sich, Versions neutrale/allgemein benannte Typen zu definieren, die allgemeine Konstrukte beschreiben, die für das Rendering verwendet werden, aber noch über die APIs Direct3D 9 und Direct3D 10 verfügen. Beispiel:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Weitere Direct3D 10 spezifische Beispiele hierfür sind:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Beheben von Link Problemen

Es empfiehlt sich, Direct3D 10-und Windows Vista-Anwendungen mit der neuesten Version von Microsoft Visual Studio zu entwickeln. Es ist jedoch möglich, eine Windows Vista-Anwendung zu erstellen, die mit der früheren Version 2003 von Visual Studio von Direct3D 10 abhängig ist. Bei Direct3D 10 handelt es sich um eine Windows Vista-Platt Form Komponente, die in der folgenden lib Abhängigkeiten aufweist (wie beim Server 2003 SP1 Platform SDK): "bufferoverflowu. lib" ist erforderlich, um alle Linker-Probleme bei der Puffer \_ Sicherheitsüberprüfung zu lösen.

### <a name="simulating-device-caps"></a>Simulieren von Geräte Deckeln

Viele Anwendungen enthalten Code Bereiche, die von verfügbaren geräteregistrierungs Daten abhängen. Umgehen Sie dieses Problem, indem Sie die Geräte Enumeration überschreiben und Geräte Limits auf sinnvolle Werte erzwingen. Planen Sie den erneuten Besuch von Bereichen, in denen später Abhängigkeiten von Caps vorhanden sind, um die Obergrenzen nach Möglichkeit vollständig zu entfernen.

## <a name="driving-the-direct3d-10-api"></a>Antreiben der Direct3D 10-API

Dieser Abschnitt konzentriert sich auf die Verhaltensänderungen, die durch die Direct3D 10-API verursacht werden.

-   [Erstellen von Ressourcen](#resource-creation)
-   [Ansichten](#views)
-   [Statischer und dynamischer Ressourcen Zugriff](#static-versus-dynamic-resource-access)
-   [Direct3D 10 Effekte](#direct3d-10-effects)
-   [HLSL ohne Auswirkungen](#hlsl-without-effects)
-   [Shader-Kompilierung](#shader-compilation)
-   [Erstellen von Shaderressourcen](#creation-of-shader-resources)
-   [Shader Reflection Layer-Schnittstelle](#shader-reflection-layer-interface)
-   [Layouts des Eingabe Assemblers-Vertexshader/Eingabedaten Strom Verknüpfung](/windows)
-   [Auswirkungen des Entfernens von Shader-Toten Code](#impact-of-shader-dead-code-removal)
-   [Beispiel für Vertex-Shader-Eingabe Struktur](#vertex-shader-input-structure-example)
-   [Zustands Objekt Erstellung](#state-object-creation)

### <a name="resource-creation"></a>Erstellen von Ressourcen

Die Direct3D 10-API hat Ressourcen als generische Puffer Typen entworfen, die spezifische Bindungsflags gemäß der geplanten Verwendung aufweisen. Dieser Entwurfspunkt wurde gewählt, um einen nahezu universellen Zugriff auf Ressourcen in der Pipeline zu ermöglichen, z. b. zum Rendern eines Vertex-Puffers und zum sofortigen Zeichnen der Ergebnisse, ohne die CPU zu unterbrechen. Das folgende Beispiel veranschaulicht die Zuordnung von Scheitelpunkt Puffern und Index Puffern, in denen Sie sehen können, dass die Ressourcen Beschreibung nur von den GPU-ressourcenbindungsflags abweicht

Die Direct3D 10-API hat Textur Hilfsobjekte zum expliziten Erstellen von Textur typressourcen bereitgestellt, aber wie Sie sich vorstellen können, sind dies wirklich Hilfsfunktionen.

-   CreateTexture2D()
-   "Kreatetexturecube ()"
-   CreateTexture3D()

Wenn Sie Direct3D 10 als Ziel verwenden, möchten Sie wahrscheinlich mehr Elemente während der Erstellung der Ressourcen zuweisen, als Sie mit Direct3D 9 verwendet werden. Dies wird bei der Erstellung von renderzielpuffern und Texturen, bei denen Sie außerdem eine Ansicht für den Zugriff auf den Puffer und das Festlegen der Ressource auf dem Gerät erstellen müssen, am offensichtlichsten.

[Tutorial 1: Direct3D 10-Grundlagen](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 und höhere Versionen von Direct3D erweitern das DDS-Dateiformat, um neue DXGI-Formate, Textur Arrays und cubemaparrays zu unterstützen. Weitere Informationen zur DDS-Dateiformat Erweiterung finden Sie im [Programmier Handbuch für DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Sichten

Eine Sicht ist eine speziell typisierte Schnittstelle zu Daten, die in einem Pixel Puffer gespeichert werden. Auf eine Ressource können mehrere Ansichten gleichzeitig zugeordnet werden. diese Funktion wird im Einzel Pass-to-cubemap-Beispiel in diesem SDK hervorgehoben.

[Programmierer-Führungs Seite für den Ressourcen Zugriff](d3d10-graphics-programming-guide-resources-access-views.md)

[Cubemap-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Statischer und dynamischer Ressourcen Zugriff

Um eine optimale Leistung zu erzielen, sollten Anwendungen ihre Datenverwendung im Hinblick auf die statische und dynamische Verwendung der Daten partitionieren. Direct3D 10 wurde entwickelt, um diesen Ansatz nutzen zu können. Daher wurden die Zugriffsregeln für Ressourcen erheblich auf Direct3D 9 hochskalieren. Bei statischen Ressourcen sollten Sie die Ressource im Idealfall während der Erstellungszeit mit Ihren Daten füllen. Wenn Sie die Engine um den Erstellungs-, Sperrungs-, Fill-und entsperrungs Entwurfspunkt von Direct3D 9 entworfen haben, können Sie die Auffüllung von der Erstellungszeit mithilfe einer stagingressource und der updatesubresource-Methode auf der Ressourcen Schnittstelle verzögern.

### <a name="direct3d-10-effects"></a>Direct3D 10 Effekte

Die Verwendung des Direct3D 10 Effects-Systems ist nicht der Rahmen dieses Artikels. Das System wurde so geschrieben, dass die von Direct3D 10 bereitgestellten architektonischen Vorteile vollständig genutzt werden. Weitere Details zur Verwendung finden Sie im Abschnitt [Effekte (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) .

### <a name="hlsl-without-effects"></a>HLSL ohne Auswirkungen

Die Direct3D 10-shaderpipeline kann ohne Verwendung des Direct3D 10 Effects-Systems gesteuert werden. Beachten Sie, dass in dieser Instanz alle Konstanten Puffer, Shader, Sampler und Textur Bindungen von der Anwendung selbst verwaltet werden müssen. Weitere Informationen finden Sie im Beispiel Link und in den folgenden Abschnitten dieses Dokuments:

[Beispiel für HLSL ohne Effekte](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Shader-Kompilierung

Der Direct3D 10 HLSL-Compiler bringt Erweiterungen zur HLSL-Sprachdefinition und hat daher die Möglichkeit, in zwei Modi zu arbeiten. Zur umfassenden Unterstützung der intrinsischen Funktionen und Semantik im Stil von Direct3D 9 muss die Kompilierung mithilfe des Kompatibilitätsmodus-Flags aufgerufen werden, das auf Kompilierungs Basis angegeben werden kann.

Das Shader-Modell 4,0 spezifische HLSL-sprach Semantik und intrinsische Funktionen für Direct3D 10 finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Wichtige Änderungen in der Syntax von Direct3D 9 HLSL, um die meisten Hinweise zu finden, liegen im Bereich des Textur Zugriffs. Die neue Syntax ist die einzige Form, die vom Compiler außerhalb des Kompatibilitätsmodus unterstützt wird.

> [!Note]  
> Die Direct3D 10-Compilertyp-APIs ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) und [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) werden von den Laufzeiten Direct3D 10, 10,1 und 11 bereitgestellt, die unter Windows Vista und höher ausgeführt werden. Die Direct3D 10-Compilertyp-APIs verfügen über die gleiche Funktionalität wie der HLSL-Compiler, der im DirectX SDK (Dezember 2006) enthalten ist. Dieser HLSL-Compiler unterstützt die Direct3D 10,1-profile nicht (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1, FX \_ 4 \_ 1), und es fehlen eine Reihe von Optimierungen und Verbesserungen. Sie können einen HLSL-Compiler erhalten, der die Direct3D 10,1-Profile aus der neuesten [Version des DirectX SDK von SDK](/previous-versions/windows/apps/hh452744(v=win.10))unterstützt. Informationen zum Legacy-DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md). Sie können den neuesten HLSL-Fxc.exe Befehlszeilen Compiler und [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) -APIs aus dem Windows SDK erhalten.

 

### <a name="creation-of-shader-resources"></a>Erstellen von Shaderressourcen

Die Erstellung kompilierter Shader-Instanzen außerhalb des Direct3D 10 Effects-Systems erfolgt auf eine sehr ähnliche Weise wie Direct3D 9. in Direct3D 10 ist es jedoch wichtig, die Shader-Eingabe Signatur für die spätere Verwendung beizubehalten. Die Signatur wird standardmäßig als Teil des Shader-BLOB zurückgegeben, kann jedoch extrahiert werden, um die Arbeitsspeicher Anforderungen bei Bedarf zu verringern. Weitere Informationen finden Sie unter [Verwenden von Shadern in Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Shader Reflection Layer-Schnittstelle

Die Shader-reflektionsebene ist die Schnittstelle, mit der Informationen zu den shaderanforderungen abgerufen werden können. Dies ist besonders nützlich, wenn eingabeassemblyverknüpfungen erstellt werden (siehe unten), in denen Sie möglicherweise die Shader-Eingabe Anforderungen durchlaufen müssen, um sicherzustellen, dass Sie dem Shader die richtige Eingabe Struktur bereitstellen Sie können eine Instanz der reflektionsebenenschnittstelle gleichzeitig erstellen, indem Sie eine Instanz eines kompilierten Shaders erstellen.

Die Shader-reflektionsebene ersetzt D3DX9-Methoden, die ähnliche Funktionen bereitstellen. Beispielsweise wird [**isparameterused**](../direct3d9/id3dxeffect--isparameterused.md) durch die [**getdesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) -Methode ersetzt.

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layouts des Eingabe Assemblers-Vertexshader/Eingabedaten Strom Verknüpfung

Der Eingabe Assembler (IA) ersetzt die vertexstreamdeklaration des Direct3D 9-Stils, und die Beschreibungs Struktur ist in Form sehr ähnlich. Der Hauptunterschied besteht darin, dass das erstellte IA-Layoutobjekt direkt einem bestimmten Format der Shader-Eingabe Signatur zugeordnet werden muss. Das Zuordnungsobjekt, das erstellt wird, um den Eingabedaten Strom mit Shader zu verknüpfen, kann über eine beliebige Anzahl von Shadern verwendet werden, bei denen die shadereingabesignatur mit der des Shader übereinstimmt, der zum Erstellen

Zum optimalen Steuern der Pipeline mit statischen Daten sollten Sie die Permutationen des eingabestreamformats auf mögliche shadereingabesignaturen berücksichtigen und die IA-layoutobjektinstanzen so früh wie möglich erstellen und nach Möglichkeit wieder verwenden.

### <a name="impact-of-shader-dead-code-removal"></a>Auswirkungen des Entfernens von Shader-Toten Code

Im folgenden Abschnitt wird ein signifikanter Unterschied zwischen Direct3D 9 und Direct3D 10 erläutert, bei dem wahrscheinlich eine sorgfältige Behandlung in Ihrem Engine-Code erforderlich ist. Shader, die bedingte Ausdrücke enthalten, verfügen häufig über bestimmte Codepfade, die im Rahmen des Kompilierungsprozesses entfernt werden. In Direct3D 9 können zwei Arten von Eingaben entfernt werden (zum Entfernen markiert), wenn Sie nicht verwendet werden: Signatur Eingaben (wie im folgenden Beispiel) und Konstante Eingaben. Wenn das Ende des Konstanten Puffers nicht verwendete Einträge enthält, spiegelt die Größen Deklaration im Shader die Größe des Konstanten Puffers ohne die nicht verwendeten Einträge am Ende wider. Beide Arten von Eingaben verbleiben in Signaturen oder konstantenpuffern Direct3D 10 mit einer besonderen Ausnahme im Fall von nicht verwendeten Konstanten Eingaben am Ende eines konstanten Puffers. Dies hat möglicherweise Auswirkungen auf die Engine, wenn große Shader verarbeitet und Eingabe Layouts erstellt werden. Elemente, die von nicht reagierender Code Optimierungen im Compiler entfernt werden, müssen in der Eingabe Struktur weiterhin deklariert werden. Dies wird im folgenden Beispiel veranschaulicht:

### <a name="vertex-shader-input-structure-example"></a>Beispiel für Vertex-Shader-Eingabe Struktur


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* Direct3D 9 beim Entfernen von unzustellbaren Code wird die Deklaration im Shader entfernt, da der bedingte Code entfernt wurde.


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



Oder Sie könnten noch deutlicher erkennen, dass die Konstante eine Kompilierzeit Konstante mit der folgenden Deklaration ist:


```
#define LIGHT_MAPPED false
```



Im obigen Beispiel wird unter Direct3D 9 das uv2-Element aufgrund von unzustellbaren Code Optimierungen im Compiler entfernt. Unter Direct3D 10 wird der unzustellbare Code trotzdem entfernt, aber das Layout des Shader-Eingabe Assemblers erfordert, dass die Definition der Eingabedaten vorhanden ist. Die Shader-reflektionsebene bietet die Möglichkeit, diese Situation auf generische Weise zu behandeln, wobei Sie die Eingabe Anforderungen des Shaders durchlaufen und sicherstellen können, dass Sie eine vollständige Beschreibung des Eingabedaten Stroms für die Shader-Signatur Zuordnung bereitstellen.

Im folgenden finden Sie eine Beispiel Funktion, mit der erkannt wird, dass ein semantischer Name/Index in einer Funktions Signatur vorhanden ist:


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>Zustands Objekt Erstellung

Beim Portieren von Engine-Code kann es hilfreich sein, anfänglich einen Standardsatz von Zustands Objekten zu verwenden und alle Direct3D 9 Device Rendering State/Textur State-Einstellungen zu deaktivieren. Dies führt zum Rendern von Artefakten, ist aber die schnellste Möglichkeit, die Dinge zu erledigen. Sie können später ein Zustands Objekt-Verwaltungssystem erstellen, das einen Verbund Schlüssel verwenden kann, um die maximale Wiederverwendung der Anzahl der verwendeten Zustands Objekte zu ermöglichen.

## <a name="porting-textures"></a>Portieren von Texturen

### <a name="file-formats-supported"></a>Unterstützte Dateiformate

Die **D3DXxxCreateXXX** -Funktion und die **D3DXxxSaveXXX** -Funktion, die eine Textur aus oder in einer Grafikdatei (z. b. [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) erstellen oder speichern, unterstützen einen anderen Satz von Dateiformaten in Direct3D 10 als in Direct3D 9:



| Dateiformat | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| BMP        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| . ppm        | x          |             |
| DIB        | x          |             |
| . HDR        | x          |             |
| . PFM        | x          |             |
| TIFF       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Weitere Informationen finden Sie unter Vergleichen der Direct3D 9 [**D3DXIMAGE \_ FileFormat**](../direct3d9/d3dximage-fileformat.md) -Enumerationen mit den [**d3dx10- \_ Bild \_ Datei \_ Format**](d3dx10-image-file-format.md) -Enumerationen für Direct3D 10.

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet. Für die Verarbeitung von Textur Dateien empfiehlt sich die Verwendung von [directxtex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mapping-Textur Formate

Die folgende Tabelle zeigt die Zuordnung von Textur Formaten von Direct3D 9 zu Direct3D 10. Alle Inhalte in Formaten, die in DXGI nicht verfügbar sind, müssen von hilfsprogrammroutinen konvertiert werden.



| Direct3D 9-Format                   | Direct3D 10-Format                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ unbekannt                     | DXGI- \_ Format \_ unbekannt                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | DXGI- \_ Format \_ B8G8R8A8 \_ unorm & DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | DXGI- \_ Format \_ B8G8R8X8 \_ unorm & DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | DXGI- \_ Format \_ B5G6R5 \_ unorm ²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | DXGI- \_ Format \_ B5G5R5A1 \_ unorm ²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | DXGI- \_ Format \_ B4G4R4A4 \_ unorm ³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ a8                          | DXGI- \_ Format \_ a8 \_ unorm                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | DXGI- \_ Format \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | DXGI- \_ Format \_ R8G8B8A8 \_ unorm & DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI- \_ Format \_ R16G16 \_ unorm                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI- \_ Format \_ R16G16B16A16 \_ unorm                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | DXGI- \_ Format \_ R8 \_ unorm Hinweis: Verwenden Sie. r Swizzle in Shader, um rot zu anderen Komponenten zu duplizieren, um das d3d9-Verhalten zu erhalten.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI- \_ Format \_ R8G8 \_ unorm Note: Verwenden Sie Swizzle. rrrg im Shader, um rot zu duplizieren, und bewegen Sie grün zu den Alpha-Komponenten, um d3d9-Verhalten zu erhalten.                                                                                                            |
| D3DFMT \_ A4L4                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | DXGI- \_ Format \_ R8G8 \_ snorm                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | DXGI- \_ Format \_ R8G8B8A8 \_ snorm                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | DXGI- \_ Format \_ R16G16 \_ snorm                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI- \_ Format \_ G8R8 \_ G8B8 \_ unorm (in DX9 die Daten wurden um 255.0 f zentral hochskaliert, dies kann jedoch im Shader-Code behandelt werden).                                                                                                                                   |
| D3DFMT \_ im YUY2                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI- \_ Format \_ R8G8 \_ B8G8 \_ unorm (in DX9 die Daten wurden um 255.0 f zentral hochskaliert, dies kann jedoch im Shader-Code behandelt werden).                                                                                                                                   |
| D3DFMT \_ DXT1                        | DXGI- \_ Format \_ BC1 \_ unorm & DXGI- \_ Format \_ BC1 \_ unorm \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI- \_ Format \_ BC1 \_ unorm & DXGI- \_ Format \_ BC1 \_ unorm \_ sRGB Hinweis: DXT1 und DXT2 sind identisch mit der API/Hardware-Perspektive... der einzige Unterschied war "prämultipliziertes Alpha", das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt. |
| D3DFMT \_ DXT3                        | DXGI- \_ Format \_ BC2 \_ unorm & DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI- \_ Format \_ BC2 \_ unorm & DXGI- \_ Format \_ BC2 \_ unorm \_ sRGB Hinweis: DXT3 und DXT4 sind identisch mit der API/Hardware-Perspektive... der einzige Unterschied war "prämultipliziertes Alpha", das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt. |
| D3DFMT \_ DXT5                        | DXGI- \_ Format \_ BC3 \_ unorm & DXGI- \_ Format \_ BC3 \_ unorm \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ Lockable | DXGI- \_ Format \_ D16 \_ unorm                                                                                                                                                                                                                             |
| D3DFMT \_ d32                         | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | DXGI- \_ Format \_ D16 \_ unorm                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ Lockable              | DXGI- \_ Format \_ d32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI- \_ Format \_ D24 \_ unorm \_ S8 \_ uint                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI- \_ Format \_ R16 \_ unorm Hinweis: Verwenden Sie. r Swizzle in Shader, um rot zu anderen Komponenten zu duplizieren, um das d3d9-Verhalten zu erhalten.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI- \_ Format \_ R16 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI- \_ Format \_ R32 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | DXGI- \_ Format \_ R16G16B16A16 \_ snorm                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI- \_ Format \_ R16 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI- \_ Format \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI- \_ Format \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI- \_ Format \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI- \_ Format \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | DXGI- \_ Format \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI- \_ Format \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI- \_ Format \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI- \_ Format \_ R32G32B32 \_ float                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ float4                 | DXGI- \_ Format \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI- \_ Format \_ R8G8B8A8 \_ uint-Hinweis: der Shader ruft uint-Werte ab, aber wenn die ganzzahligen Gleit Komma Zahlen von Direct3D 9 (0,0 f, 1.0 f... 255. f), uint kann einfach im Shader in float32 konvertiert werden.                                                               |
| D3DDECLTYPE \_ SHORT2                 | DXGI- \_ Format \_ R16G16 \_ Sint Hinweis: der Shader ruft Sint-Werte ab, aber wenn die ganzzahligen Gleit Komma Werte Direct3D 9 im Stil erforderlich sind, kann Sint einfach in float32 in Shader konvertiert werden.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI- \_ Format \_ R16G16B16A16 \_ Sint Hinweis: der Shader ruft Sint-Werte ab, aber wenn die ganzzahligen Gleit Komma Werte Direct3D 9 im Stil erforderlich sind, kann Sint einfach in float32 in Shader konvertiert werden.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI- \_ Format \_ R8G8B8A8 \_ unorm                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | DXGI- \_ Format \_ R16G16 \_ snorm                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | DXGI- \_ Format \_ R16G16B16A16 \_ snorm                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI- \_ Format \_ R16G16 \_ unorm                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | DXGI- \_ Format \_ R16G16B16A16 \_ unorm                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI- \_ Format \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI- \_ Format \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | DXGI- \_ Format \_ BC4 \_ unorm                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | DXGI- \_ Format \_ BC5 \_ unorm                                                                                                                                                                                                                             |



 

¹ DXGI 1,1, das in der Direct3D 11-Laufzeit enthalten ist, enthält BGRA-Formate. Die Unterstützung für diese Formate ist jedoch für Direct3D 10-und 10,1-Geräte mit Treibern optional, die für das Windows-Anzeigetreiber Modell (WDDM) für Windows Vista (WDDM 1,0) implementiert sind. Verwenden Sie stattdessen DXGI- \_ Format \_ R8G8B8A8 \_ unorm. Alternativ dazu können Sie Ihr Gerät mit [**d3d10 \_ Create \_ Device \_ BGRA- \_ Unterstützung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) erstellen, um sicherzustellen, dass nur Computer mit der Laufzeitversion Direct3D 11,0 und einem WDDM 1,1-Treiber unterstützt werden.

² DXGI 1,0 definierte 5:6:5-und 5:5:5:1-Formate, aber Sie wurden von der Direct3D 10. x-oder Direct3D 11,0-Laufzeit nicht unterstützt. Diese Formate werden optional mit DXGI 1,2 in der DirectX 11,1-Laufzeit unterstützt, die für die Featureebene 11,1-Videoadapter und WDDM 1,2 (Anzeigetreiber Modell beginnend mit Windows 8) erforderlich ist und bereits auf 10 Level9-Funktionsebenen unterstützt wird.

³ DXGI 1,2 hat das 4:4:4:4-Format eingeführt. Dieses Format wird optional in der DirectX 11,1-Runtime unterstützt, die für die Featureebene 11,1-Videoadapter und WDDM 1,2-Treiber erforderlich ist und bereits auf 10 Level9-Funktionsebenen unterstützt wird.

Für nicht komprimierte Formate hat DXGI die Unterstützung für beliebige Pixel Format Muster eingeschränkt. alle nicht komprimierten Formate müssen den Typ "RGBA" aufweisen. Dies erfordert möglicherweise das Schwenken vorhandener Assets-Pixel Formate, die Sie nach Möglichkeit als offline-Vorverarbeitungs Durchlauf berechnen.

## <a name="porting-shaders"></a>Portieren von Shadern

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Direct3D 10-Shader werden in HLSL erstellt.

Direct3D 10 schränkt die Verwendung von Assemblysprache nur zu Debuggingzwecken ein. Daher müssen alle in Direct3D 9 verwendeten handschriftlichen assemblyshader in HLSL konvertiert werden.

### <a name="shader-signatures-and-linkage"></a>Shadersignaturen und Verknüpfungen

Weiter oben in diesem Dokument wurden die Anforderungen für die eingabeassemblyverknüpfung mit Vertexshader-Eingabe Signaturen erläutert (siehe oben). Beachten Sie, dass die Direct3D 10-Laufzeit auch die Anforderungen für die Bereitstellung von Verknüpfungen zwischen Shadern verschärft hat. Diese Änderung wirkt sich auf Shader-Quellen aus, bei denen die Bindung Zwischenstufen unter Direct3D 9 möglicherweise nicht vollständig beschrieben wurde. Beispiel:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Unterbrochene vs-PS-Verknüpfung: Obwohl der Pixelshader möglicherweise nicht an der vollständigen Matrix interessiert ist, muss die Verknüpfung die vollständige float4x3 angeben.

Beachten Sie, dass die Verknüpfungs Semantik Zwischenstufen genau übereinstimmen muss. die Eingaben der zielstufen können jedoch ein Präfix der Werte sein, die ausgegeben werden. Im obigen Beispiel könnte der Pixelshader die Position und die texcoord1 als die einzigen Eingaben haben, er kann jedoch nicht die Position und texcoord2 aufgrund der Bestellungs Einschränkungen als einzige Eingabe aufweisen.

### <a name="hlsl-shader-stage-linkages"></a>HLSL-Shader-Phasen Verknüpfungen

Die Verknüpfung zwischen Shadern kann an einem der folgenden Punkte in der Pipeline auftreten:

-   Eingabe Assembler in Scheitelpunkt-Shader
-   Vertex-Shader an Pixel-Shader
-   Vertex-Shader zu Geometry-Shader
-   Vertex-Shader zum Streamen der Ausgabe
-   Geometry-Shader in Pixel-Shader
-   Geometry-Shader zum Streamen

### <a name="constant-buffers"></a>Konstantenpuffer

Um das Portieren von Inhalten aus Direct3D 9 zu vereinfachen, kann ein anfänglicher Ansatz zur konstanten Verwaltung außerhalb des Effekten Systems das Erstellen eines einzelnen Konstanten Puffers mit allen erforderlichen Konstanten einschließen. Es ist wichtig für die Leistung, Konstanten mit der erwarteten Aktualisierungshäufigkeit in Puffer zu ordnen. Diese Organisation verringert die Menge redundanter konstanter Mengen auf ein Minimum.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Benutzer Clip Flächen in HLSL auf Featureebene 9 und höher

Ab Windows 8 können Sie das **clipplane** -Funktions Attribut in einer HLSL- [Funktionsdeklaration](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) anstelle von [SV \_ clipdistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) verwenden, damit Ihr Shader auf [Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x und auf Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](../direct3dhlsl/user-clip-planes-on-10level9.md).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Weitere Direct3D 10-Unterschiede bei der Überwachung

### <a name="integers-as-input"></a>Ganze Zahlen als Eingabe

In Direct3D 9 gab es keine wirkliche Hardwareunterstützung für integer-Datentypen. Direct3D 10-Hardware unterstützt jedoch explizite ganzzahlige Typen. Wenn Sie über Gleit Komma Daten im Scheitelpunkt Puffer verfügen, müssen Sie über eine float-Eingabe verfügen. Andernfalls ist ein ganzzahliger Typ die Bitmuster Darstellung des Gleit Komma Werts. Ein ganzzahliger Typ ist für eine Pixel-Shadereingabe nicht zulässig, es sei denn, der Wert ist für keine interpolung markiert (siehe [interpolationmodifizierer](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Maus Cursor

In früheren Versionen von Windows wurden die Standard-GDI-Maus Cursor Routinen auf allen voll Bild exklusiven Geräten nicht ordnungsgemäß ausgeführt. Die [**setcursorproperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)-, [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)-und [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) -APIs wurden hinzugefügt, um diese Fälle zu behandeln. Da die Version von GDI von Windows Vista die [DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) -Oberflächen vollständig versteht, ist diese spezialisierte Mauszeiger-API nicht erforderlich, sodass es keine Entsprechung von Direct3D 10 gibt. Direct3D 10-Anwendungen sollten stattdessen die Standard- [GDI](../menurc/cursors.md) -mousorcursorroutinen für Maus Cursor verwenden.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Zuordnung von Texels zu Pixeln in Direct3D 10

In Direct3D 9 war der textebereich und die Pixel zentriert eine halbe Einheit voneinander entfernt (Weitere Informationen finden [Sie unter Direktes Mapping von Texels zu Pixeln (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). In Direct3D 10 befinden sich die textezentren bereits in halben Einheiten, sodass es nicht erforderlich ist, Scheitelpunkt Koordinaten zu verschieben.

Das Rendern von voll Bild-Quads ist mit Direct3D 10 geradliniger. Voll Bildschirme sollten in clipspace (-1, 1) definiert und einfach durch den Vertex-Shader ohne Änderungen geleitet werden. Auf diese Weise ist es nicht erforderlich, den Vertex-Puffer jedes Mal neu zu laden, wenn sich die Bildschirmauflösung ändert, und es gibt keine zusätzliche Arbeit im Pixelshader, um die Texturkoordinaten zu bearbeiten.

### <a name="reference-counting-behavior-changes"></a>Verhaltensänderungen der Verweis Zählung

Im Gegensatz zu früheren Direct3D-Versionen enthalten die verschiedenen Set-Funktionen keinen Verweis auf die Geräte Objekte. Dies bedeutet, dass die Anwendung sicherstellen muss, dass Sie einen Verweis auf das Objekt enthält, solange dieses Objekt an die Pipeline gebunden werden soll. Wenn die Verweis Anzahl des Objekts auf 0 (null) fällt, wird das Objekt an die Pipeline gebunden, wenn es zerstört wird. Diese Art der Verweis Speicherung wird auch als "schwache Verweis" bezeichnet. Daher enthält jeder Bindungs Speicherort im Geräte Objekt einen schwachen Verweis auf die Schnittstelle/das Objekt. Sofern nicht explizit angegeben, sollte dieses Verhalten für alle Set-Methoden angenommen werden. Wenn die Zerstörung eines Objekts bewirkt, dass ein Bindungspunkt auf **null** festgelegt wird, wird von der debugschicht eine Warnung ausgegeben. Beachten Sie, dass Aufrufe von Geräte Abruf Methoden, wie z. b. [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) , den Verweis Zähler der zurückgegebenen Objekte erhöhen.

### <a name="test-cooperative-level"></a>Test kooperative Ebene

Die Funktionalität der Direct3D 9-API [**testkooperativelevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) ist analog zum Festlegen des [vorhandenen DXGI- \_ \_ Tests](../direct3ddxgi/dxgi-present.md) beim Aufrufen von " [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present)".

### <a name="stretchrect"></a>Stretchrect

Eine Funktion, die der Direct3D 9 [**IDirect3DDevice9:: stretchrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) -Methode ähnelt, ist in Direct3D 10 und 10,1 nicht verfügbar. Verwenden Sie [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), um Ressourcen Oberflächen zu kopieren. Zum Ändern der Größe von Vorgängen können Sie eine Textur mithilfe der Textur Filterung in eine Textur darstellen. Verwenden Sie zum Umrechnen von MSAA-Oberflächen in nicht-MSAA-Oberflächen [**ID3D10Device:: resolvesubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Weitere Direct3D 10,1-Unterschiede

Windows Vista mit Service Pack 1 (SP1) enthielt ein kleineres Update für Direct3D 10 und Direct3D 10,1, das die folgenden zusätzlichen Hardware Features verfügbar gemacht hat:

-   MSAA pro Sample-Shader
-   MSAA-Tiefe Read-Back
-   Unabhängige Blend-Modi pro Renderziel
-   Cube-Karten Arrays
-   In Block komprimierte Formate (BC) Renderingformate

Das Direct3D 10,1-Update hat Unterstützung für die folgenden neuen Schnittstellen hinzugefügt, die von vorhandenen Schnittstellen abgeleitet sind:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

Das Update Direct3D 10,1 enthält auch die folgenden zusätzlichen Strukturen:

-   [**D3d10 \_ \_ Renderziel \_ Blend \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3d10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**D3d10- \_ Shader- \_ Ressourcen \_ Ansicht \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

Die Direct3D 10,1-API umfasst ein neues Konzept mit dem Namen Funktionsebene. Dieses Konzept bedeutet, dass Sie die Direct3D 10,1-API verwenden können, um Direct3D 10,0 ([**d3d10 \_ Feature \_ Level \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) oder Direct3D 10,1 ([**d3d10 \_ Feature \_ Level \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) Hardware zu steuern. Da die Direct3D 10,1-API von den Direct3D 10-Schnittstellen abgeleitet ist, können Anwendungen ein Direct3D 10,1-Gerät erstellen und dann als Direct3D 10,0-Gerät verwenden, außer wenn neue 10,1-spezifische Features benötigt werden (vorausgesetzt, dass die Funktionsebene " **d3d10 \_ Feature \_ Level \_ 10 \_ 1** " vorhanden ist und diese Features unterstützt).

> [!Note]  
> Direct3D 10,1-Geräte können die vorhandenen 10,0 HLSL-Shader-profile (vs \_ 4 \_ 0, PS \_ 4 \_ 0, GS \_ 4 \_ 0) und die neuen 10,1-profile (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1) mit zusätzlichen HLSL-Anweisungen und-Funktionen verwenden.

 

Windows 7 enthielt ein kleineres Update der Direct3D 10,1-API, die in der Direct3D 11-Laufzeit enthalten ist. Dieses Update bietet Unterstützung für die folgenden featureebenen:

-   [**D3d10 \_ \_ Featureebene \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3d10 \_ \_ Featureebene \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3d10 \_ \_ Featureebene \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 hat auch Unterstützung für Direct3D 10,1 für [Windows Advanced rasterization Platform (Warp)](../direct3darticles/directx-warp.md)hinzugefügt. Sie können einen Warp-Treiber mithilfe von [**d3d10 \_ Driver \_ Type \_ Warp**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)angeben.

Weitere Informationen zu Direct3D 10,1 finden Sie unter [Direct3D 10,1 Features](d3d10-graphics-programming-guide-10-1.md) und [**d3d10 \_ Feature \_ Level1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) Enumeration.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
