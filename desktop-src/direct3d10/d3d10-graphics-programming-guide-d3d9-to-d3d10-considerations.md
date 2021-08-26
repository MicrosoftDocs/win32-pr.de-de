---
description: Die folgende Seite enthält eine grundlegende Übersicht über die wichtigsten Unterschiede zwischen Direct3D 9 und Direct3D 10. Die folgende Gliederung bietet einige Einblicke, um Entwicklern mit Direct3D 9-Erfahrungen beim Untersuchen und Verknüpfen mit Direct3D 10 zu helfen.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Überlegungen zu Direct3D 9 zu Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6c2dac7da24184bb5cc6a78f8e7d391c7d0f8b7000107915ba5a606188dcf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120010"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Überlegungen zu Direct3D 9 zu Direct3D 10 (Direct3D 10)

Die folgende Seite enthält eine grundlegende Übersicht über die wichtigsten Unterschiede zwischen Direct3D 9 und Direct3D 10. Die folgende Gliederung bietet einige Einblicke, um Entwicklern mit Direct3D 9-Erfahrungen beim Untersuchen und Verknüpfen mit Direct3D 10 zu helfen.

Obwohl die Informationen in diesem Thema Direct3D 9 mit Direct3D 10 vergleichen, da Direct3D 11 auf den Verbesserungen in Direct3D 10 und 10.1 basiert, benötigen Sie diese Informationen auch für die Migration von Direct3D 9 zu Direct3D 11. Informationen zum Übergang von Direct3D 10 zu Direct3D 11 finden Sie unter [Migrieren zu Direct3D 11.](../direct3d11/d3d11-programming-guide-migrating.md)

-   [Übersicht über die wichtigsten strukturellen Änderungen in Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Entfernen der festen Funktion](#removal-of-fixed-function)
    -   [Überprüfung der Erstellungszeit von Geräteobjekten](#device-object-creation-time-validation)
-   [Engine-Abstraktionen/Trennung](/windows)
    -   [Direktes Entfernen von Direct3D 9-Abhängigkeiten](#direct-removal-of-direct3d-9-dependencies)
-   [Tricks zum schnellen Beheben von Problemen beim Erstellen von Anwendungen](#tricks-for-quickly-resolving-application-build-issues)
    -   [Überschreiben von Direct3D 9-Typen](#overriding-direct3d-9-types)
    -   [Beheben von Linkproblemen](#resolving-link-issues)
    -   [Simulieren von Geräte-CAPs](#simulating-device-caps)
-   [Fahren mit der Direct3D 10-API](#driving-the-direct3d-10-api)
    -   [Ressourcenerstellung](#resource-creation)
    -   [Ansichten](#views)
    -   [Statischer und dynamischer Ressourcenzugriff](#static-versus-dynamic-resource-access)
    -   [Direct3D 10-Effekte](#direct3d-10-effects)
    -   [HLSL ohne Effekte](#hlsl-without-effects)
    -   [Shaderkompilierung](#shader-compilation)
    -   [Erstellen von Shaderressourcen](#creation-of-shader-resources)
    -   [Shader-Reflektionsebenenschnittstelle](#shader-reflection-layer-interface)
    -   [Eingabeassemblierungslayouts – Vertex-Shader/Eingabestreamverknüpfung](/windows)
    -   [Auswirkungen der Entfernung von shader dead code](#impact-of-shader-dead-code-removal)
    -   [Vertex-Shadereingabestruktur – Beispiel](#vertex-shader-input-structure-example)
    -   [Erstellung von Zustandsobjekten](#state-object-creation)
-   [Portieren von Texturen](#porting-textures)
    -   [Unterstützte Dateiformate](#file-formats-supported)
    -   [Zuordnen von Texturformaten](#mapping-texture-formats)
-   [Portieren von Shadern](#porting-shaders)
    -   [Direct3D 10-Shader werden in HLSL erstellt.](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Shadersignaturen und -verknüpfung](#shader-signatures-and-linkage)
    -   [HLSL Shader Stage-Verknüpfungen](#hlsl-shader-stage-linkages)
    -   [Konstantenpuffer](#constant-buffers)
    -   [Benutzerclipebenen in HLSL auf Featureebene 9 und höher](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Zusätzliche Direct3D 10-Unterschiede, die überwacht werden müssen](#additional-direct3d-10-differences-to-watch-for)
    -   [Ganze Zahlen als Eingabe](#integers-as-input)
    -   [Mauscursor](#mouse-cursors)
    -   [Zuordnen von Texels zu Pixeln in Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Änderungen des Referenzzählverhaltens](#reference-counting-behavior-changes)
    -   [Testen der kooperativen Ebene](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Zusätzliche Direct3D 10.1-Unterschiede](#additional-direct3d-101-differences)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Übersicht über die wichtigsten strukturellen Änderungen in Direct3D 10

-   [Entfernen der festen Funktion](#removal-of-fixed-function)
-   [Überprüfung der Erstellungszeit von Geräteobjekten](#device-object-creation-time-validation)

Das Rendern mit dem Direct3D 10-Gerät ähnelt strukturell Direct3D 9.

-   Festlegen einer Vertexstreamquelle
-   Festlegen des Eingabelayouts in Direct3D 10 (Festlegen der Vertexstreamdeklaration in Direct3D 9)
-   Deklarieren der primitiven Topologie
-   Festlegen von Texturen
-   Festlegen von Zustandsobjekten
-   Festlegen von Shadern
-   Draw

Der [**Draw-Aufruf**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) verbindet die Vorgänge. Die Reihenfolge der Aufrufe vor dem Draw-Aufruf ist willkürlich. Die wichtigsten Unterschiede im Direct3D 10-API-Design sind wie folgt:

-   Entfernen der festen Funktion
-   Entfernen von CAPS-Bits: Der Basisfunktionssatz von Direct3D 10 ist garantiert.
-   Strengere Verwaltung von: Ressourcenzugriff, Gerätestatus, Shaderkonstanten, Shaderbindung (Eingaben und Ausgaben an Shader) zwischen Phasen
-   Änderungen des API-Einstiegspunktnamens spiegeln die Verwendung des virtuellen GPU-Speichers (Map() anstelle von Lock()) wider.
-   Zum Zeitpunkt der Erstellung kann dem Gerät eine Debugebene hinzugefügt werden.
-   Die primitive Topologie ist jetzt ein expliziter Zustand (getrennt vom [**Draw-Aufruf).**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw)
-   Explizite Shaderkonstanten werden jetzt in Konstantenpuffern gespeichert.
-   Die Shadererstellung erfolgt vollständig in HLSL. Der HLSL-Compiler befindet sich jetzt in der primären Direct3D 10-DLL.
-   Neue programmierbare Phase– der Geometrie-Shader
-   Entfernen von BeginScene()/EndScene()
-   Allgemeine 2D-, Fokus- und Adapterverwaltungsfunktionen, die in einer neuen Komponente implementiert sind: DXGI

### <a name="removal-of-fixed-function"></a>Entfernen der festen Funktion

Es ist manchmal überraschend, dass selbst in einer Direct3D 9-Engine, die die programmierbare Pipeline vollständig ausnutzt, eine Reihe von Bereichen vorhanden ist, die von der FF-Pipeline (Fixed-Function) abhängen. Die gängigsten Bereiche beziehen sich in der Regel auf das bildschirmraumorientierte Rendering für die Benutzeroberfläche. Aus diesem Grund müssen Sie wahrscheinlich einen FF-Emulations-Shader oder eine Gruppe von Shadern erstellen, die das erforderliche Ersetzungsverhalten bereitstellen.

Diese Dokumentation enthält ein Whitepaper mit Ersatz-Shaderquellen für die gängigsten FF-Verhaltensweisen (siehe [Fixed Function EMU Sample](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Einige Pixelverhalten mit fester Funktion, einschließlich Alphatest, wurden in Shader verschoben.

### <a name="device-object-creation-time-validation"></a>Überprüfung der Erstellungszeit von Geräteobjekten

Die Direct3D 10-Pipeline wurde von Grund auf neu in Hardware und Software mit der primären Absicht umgestaltet, den CPU-Mehraufwand (zur Zeichnen-Zeit) zu reduzieren. Um Kosten zu senken, wurde allen Arten von Gerätedaten ein Objekt mit expliziten Erstellungsmethoden zugewiesen, die vom Gerät selbst bereitgestellt werden. Dies ermöglicht eine strenge Datenvalidierung zum Zeitpunkt der Objekterstellung anstatt während des Draw-Aufrufs, wie dies häufig bei Direct3D 9 derFall ist.

## <a name="engine-abstractions--separation"></a>Engine-Abstraktionen/Trennung

Für Anwendungen, einschließlich Games, die sowohl Direct3D 9 als auch Direct3D 10 unterstützen möchten, müssen die Renderingebenen aus der restlichen Codebasis abstrahiert werden. Es gibt viele Möglichkeiten, dies zu erreichen, aber entscheidend für alle ist das Design der Abstraktionsschicht für das Direct3D-Gerät auf niedrigerer Ebene. Alle Systeme sollten mit der Hardware über die gemeinsame Ebene kommunizieren, die für gpu-Ressourcen- und Typverwaltung auf niedriger Ebene konzipiert ist.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Direktes Entfernen von Direct3D 9-Abhängigkeiten

Beim Portieren großer, zuvor getesteter Codebasen ist es wichtig, die Menge der Codeänderungen an denen zu minimieren, die unbedingt erforderlich sind, um zuvor getestete Verhaltensweisen im Code beizubehalten. Zu den bewährten Methoden gehört die eindeutige Dokumentation, wo sich Elemente mithilfe von Kommentaren ändern. Es ist häufig hilfreich, einen Kommentarstandard für diese Arbeit zu haben, der eine schnelle Navigation durch die Codebasis ermöglicht.

Im Folgenden finden Sie eine Beispielliste mit Standardkommentaren für einzelne Zeilen/Startblöcke, die für diese Arbeit verwendet werden können.



| Element                                                                                                                                                                             | Beschreibung                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 ENTFERNT<br/>                     | Verwenden Sie diese Option, wenn Zeilen/Codeblöcke entfernt werden.<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 MUSS AKTUALISIERT WERDEN<br/> | Es hilft, dem NEED UPDATE-Kommentar zusätzliche Hinweise hinzuzufügen, die vorschlagen, welche Arbeit/neue API für spätere Aufrufe des Codes für die Verhaltenskonvertierung verwendet werden soll. Es sollte auch eine starke Verwendung von assert(**false**) verwendet werden, wenn \\ \\ Direct3D 10 NEEDS UPDATE auftritt, um sicherzustellen, dass Sie nicht unwissentlich fehlerhaften Code ausführen.<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 CHANGED<br/>                     | Bereiche, in denen wichtige Änderungen vorgenommen wurden, sollten für zukünftige Verweise beibehalten, aber auskommentiert werden.<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 END<br/>                                     | Endcodeblockqualifizierer<br/>                                                                                                                                                                                                                                                                                            |



 

Für mehrere Quellzeilen sollten Sie auch den C-Stil //Kommentare verwenden, aber die \* \* relevanten Start-/Endkommentare um diese Bereiche herum hinzufügen.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Tricks zum schnellen Beheben von Problemen beim Erstellen von Anwendungen

-   [Überschreiben von Direct3D 9-Typen](#overriding-direct3d-9-types)
-   [Beheben von Linkproblemen](#resolving-link-issues)
-   [Simulieren von Geräte-CAPs](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Überschreiben von Direct3D 9-Typen

Es kann nützlich sein, eine Headerdatei auf hoher Ebene mit Typdefinitionen/-außerkraftsetzungen für Direct3D 9-Basistypen einfügungen, die von den Direct3D 10-Headern nicht mehr unterstützt werden. Dadurch können Sie die Menge der Änderungen im Code und den Schnittstellen minimieren, bei denen eine direkte Zuordnung von einem Direct3D 9-Typ zum neu definierten Direct3D 10-Typ besteht. Dieser Ansatz ist auch nützlich, um Codeverhalten in einer Quelldatei zusammen zu halten. In diesem Fall ist es eine gute Idee, versionsneutrale/allgemein benannte Typen zu definieren, die allgemeine Konstrukte beschreiben, die für das Rendering verwendet werden, aber sowohl Direct3D 9- als auch Direct3D 10-APIs umfassen. Beispiel:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Weitere Direct3D 10-spezifische Beispiele hierfür sind:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Beheben von Linkproblemen

Es empfiehlt sich, Direct3D 10- und Windows Vista-Anwendungen mit der neuesten Version von Microsoft Visual Studio. Es ist jedoch möglich, eine Windows Vista-Anwendung zu erstellen, die von Direct3D 10 mithilfe der früheren Version von 2003 von Visual Studio. Direct3D 10 ist eine Windows Vista-Plattformkomponente, die abhängigkeiten (wie beim Server 2003 SP1 Platform SDK) von der folgenden Bibliothek aufweist: BufferOverflowU.lib ist erforderlich, um alle Probleme mit \_ Linkern für puffersicherheitsprüfung zu lösen.

### <a name="simulating-device-caps"></a>Simulieren von Geräte-CAPs

Viele Anwendungen enthalten Codebereiche, die von verfügbaren CAPS-Daten des Geräts abhängen. Sie können dies durch Überschreiben der Geräteenumeration und Erzwingen von Caps für Geräte auf sinnvolle Werte umschreiben. Planen Sie, Bereiche, in denen es später Abhängigkeiten von CAPS gibt, erneut zu besuchen, um CAPS nach Möglichkeit vollständig zu entfernen.

## <a name="driving-the-direct3d-10-api"></a>Verwenden der Direct3D 10-API

Dieser Abschnitt konzentriert sich auf die Verhaltensänderungen, die durch die Direct3D 10-API verursacht werden.

-   [Ressourcenerstellung](#resource-creation)
-   [Ansichten](#views)
-   [Statischer und dynamischer Ressourcenzugriff](#static-versus-dynamic-resource-access)
-   [Direct3D 10-Effekte](#direct3d-10-effects)
-   [HLSL ohne Effekte](#hlsl-without-effects)
-   [Shaderkompilierung](#shader-compilation)
-   [Erstellen von Shaderressourcen](#creation-of-shader-resources)
-   [Shader-Reflektionsschichtschnittstelle](#shader-reflection-layer-interface)
-   [Layouts des Eingabe-Assemblers – Vertex-Shader/Eingabestreamverknüpfung](/windows)
-   [Auswirkungen der Entfernung von shader dead code](#impact-of-shader-dead-code-removal)
-   [Vertex-Shader-Eingabestruktur – Beispiel](#vertex-shader-input-structure-example)
-   [Erstellung von Zustandsobjekten](#state-object-creation)

### <a name="resource-creation"></a>Ressourcenerstellung

Die Direct3D 10-API hat Ressourcen als generische Puffertypen entworfen, die bestimmte Bindungsflags gemäß der geplanten Verwendung haben. Dieser Entwurfspunkt wurde ausgewählt, um den nahezu überall verfügbaren Zugriff auf Ressourcen in der Pipeline für Szenarien wie das Rendern in einen Scheitelpunktpuffer und das anschließende sofortige Zeichnen der Ergebnisse zu ermöglichen, ohne die CPU zu unterbrechen. Im folgenden Beispiel wird die Zuordnung von Scheitelpunktpuffern und Indexpuffern veranschaulicht, bei denen Sie sehen können, dass sich die Ressourcenbeschreibung nur durch die GPU-Ressourcenbindungsflags unterscheidet.

Die Direct3D 10-API stellt Textur-Hilfsmethoden zum expliziten Erstellen von Texturtypressourcen bereit, aber wie Sie sich vorstellen können, handelt es sich hierbei um Hilfsfunktionen.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Wenn Sie Direct3D 10 als Ziel verwenden, sollten Sie während der Ressourcenerstellung wahrscheinlich mehr Elemente zuordnen, als Sie es bei Direct3D 9 gewohnt sind. Dies wird am deutlichsten bei der Erstellung von Renderzielpuffern und Texturen, bei denen Sie auch eine Ansicht für den Zugriff auf den Puffer und das Festlegen der Ressource auf dem Gerät erstellen müssen.

[Tutorial 1: Grundlagen zu Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 und neuere Versionen von Direct3D erweitern das DDS-Dateiformat, um neue DXGI-Formate, Texturarrays und Cubezuordnungsarrays zu unterstützen. Weitere Informationen zur DDS-Dateiformaterweiterung finden Sie im [Programmierhandbuch für DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Sichten

Eine Ansicht ist eine speziell typierte Schnittstelle zu Daten, die in einem Pixelpuffer gespeichert sind. Einer Ressource können mehrere Ansichten gleichzeitig zugeordnet werden, und dieses Feature wird im Beispiel Single Pass Render to Cubemap in diesem SDK hervorgehoben.

[Seite "Leitfaden für Programmierer" zum Ressourcenzugriff](d3d10-graphics-programming-guide-resources-access-views.md)

[CubeMap-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Statischer und dynamischer Ressourcenzugriff

Um eine optimale Leistung zu erzielen, sollten Anwendungen ihre Datennutzung hinsichtlich der statischen und dynamischen Natur der Daten partitionieren. Direct3D 10 wurde entwickelt, um diesen Ansatz zu nutzen. Daher wurden die Zugriffsregeln für Ressourcen gegenüber Direct3D 9 erheblich verbessert. Für statische Ressourcen sollten Sie die Ressource idealerweise während der Erstellung mit ihren Daten auffüllen. Wenn Ihre Engine für den Entwurfspunkt Erstellen, Sperren, Füllen und Entsperren von Direct3D 9 entworfen wurde, können Sie die Auffüllung von Erstellungszeit mithilfe einer Stagingressource und der UpdateSubResource-Methode auf der Ressourcenschnittstelle zurückversetzen.

### <a name="direct3d-10-effects"></a>Direct3D 10-Effekte

Die Verwendung des Direct3D 10 Effects-Systems wird in diesem Artikel nicht behandelt. Das System wurde geschrieben, um die Vorteile der Architektur von Direct3D 10 voll zu nutzen. Weitere Informationen zur Verwendung finden Sie im Abschnitt Effekte [(Direct3D 10).](d3d10-graphics-programming-guide-effects.md)

### <a name="hlsl-without-effects"></a>HLSL ohne Effekte

Die Direct3D 10-Shaderpipeline kann ohne verwendung des Direct3D 10 Effects-Systems gesteuert werden. Beachten Sie, dass in dieser Instanz alle konstanten Puffer-, Shader-, Sampler- und Texturbindungen von der Anwendung selbst verwaltet werden müssen. Ausführlichere Informationen finden Sie unter dem Beispiellink und den folgenden Abschnitten dieses Dokuments:

[BEISPIEL FÜR HLSL ohne Effekte](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Shaderkompilierung

Der Direct3D 10 HLSL-Compiler bietet Verbesserungen an der HLSL-Sprachdefinition und bietet daher die Möglichkeit, in zwei Modi zu arbeiten. Zur vollständigen Unterstützung von systeminternen Funktionen und Semantik im Direct3D 9-Stil sollte die Kompilierung mit dem Kompatibilitätsmodusflag aufgerufen werden, das pro Kompilierung angegeben werden kann.

Die Shadermodell 4.0-spezifische HLSL-Sprachsemantik und systeminterne Funktionen für Direct3D 10 finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Wichtige Änderungen an der Syntax von Direct3D 9 HLSL, die am meisten zu beachten sind, liegen im Bereich des Texturzugriffs. Die neue Syntax ist die einzige Form, die vom Compiler außerhalb des Kompatibilitätsmodus unterstützt wird.

> [!Note]  
> Die Direct3D 10-Compilertyp-APIs ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) und [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) werden von den Runtimes Direct3D 10, 10.1 und 11 bereitgestellt, die in Windows Vista und höher ausgeführt werden. Die Compiler-APIs von Direct3D 10 verfügen über die gleiche Funktionalität wie der HLSL-Compiler, der im DirectX SDK (Dezember 2006) enthalten ist. Dieser HLSL-Compiler unterstützt keine Direct3D 10.1-Profile (im Vergleich \_ zu 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 \_ 1, fx \_ 4 \_ 1), und es fehlen eine Reihe von Optimierungen und Verbesserungen. Sie können einen HLSL-Compiler, der direct3D 10.1-Profile unterstützt, aus der neuesten [älteren DirectX SDK-Version erhalten.](/previous-versions/windows/apps/hh452744(v=win.10)) Informationen zum älteren DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md). Sie können die neuesten HLSL-Fxc.exe-Befehlszeilencompiler und [D3DCompiler-APIs](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) aus dem Windows SDK herunterladen.

 

### <a name="creation-of-shader-resources"></a>Erstellen von Shaderressourcen

Die Erstellung kompilierter Shaderinstanzen außerhalb des Direct3D 10 Effects-Systems erfolgt auf sehr ähnliche Weise wie Direct3D 9. In Direct3D 10 ist es jedoch wichtig, die Shadereingabesignatur für die spätere Verwendung zu behalten. Die Signatur wird standardmäßig als Teil des Shaderblobs zurückgegeben, kann jedoch extrahiert werden, um die Arbeitsspeicheranforderungen bei Bedarf zu reduzieren. Weitere Informationen finden Sie unter [Verwenden von Shadern in Direct3D 10.](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)

### <a name="shader-reflection-layer-interface"></a>Shader-Reflektionsschichtschnittstelle

Die Shader-Reflektionsebene ist die Schnittstelle, über die Informationen zu den Shaderanforderungen erhalten werden können. Dies ist besonders nützlich beim Erstellen von Eingabe-Assemblyverknüpfungen (siehe unten), bei denen Sie möglicherweise die Shadereingabeanforderungen durchlaufen müssen, um sicherzustellen, dass Sie die richtige Eingabestruktur für den Shader verwenden. Sie können eine Instanz der Reflektionsebenenschnittstelle gleichzeitig mit dem Erstellen einer Instanz eines kompilierten Shaders erstellen.

Die Shader-Reflektionsebene ersetzt D3DX9-Methoden, die ähnliche Funktionen bereitstellen. Beispielsweise wird [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) durch die [**GetDesc-Methode**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) ersetzt.

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layouts des Eingabe-Assemblers – Vertex-Shader/Eingabestreamverknüpfung

Der Eingabe-Assembler (IA) ersetzt die Vertexstreamdeklaration im Direct3D 9-Stil, und die Beschreibungsstruktur ist in der Form sehr ähnlich. Der Hauptunterschied, den die IA mit sich bringt, besteht in der direkten Zuordnung des erstellten IA-Layoutobjekts zu einem bestimmten Format der Shadereingabesignatur. Das Zuordnungsobjekt, das zum Verknüpfen des Eingabestreams mit dem Shader erstellt wurde, kann für eine beliebige Anzahl von Shadern verwendet werden, bei denen die Shadereingabesignatur mit der des Shaders zum Erstellen des Eingabelayouts abgleicht.

Um die Pipeline am besten mit statischen Daten zu fördern, sollten Sie die Permutationen des Eingabestreamformats auf mögliche Shader-Eingabesignaturen berücksichtigen und die IA-Layoutobjektinstanzen so früh wie möglich erstellen und nach Möglichkeit wiederverwenden.

### <a name="impact-of-shader-dead-code-removal"></a>Auswirkungen der Entfernung von shader dead code

Im folgenden Abschnitt wird ein signifikanter Unterschied zwischen Direct3D 9 und Direct3D 10 beschrieben, der wahrscheinlich eine sorgfältige Behandlung in Ihrem Engine-Code erfordert. Bei Shadern, die bedingte Ausdrücke enthalten, werden im Rahmen des Kompilierungsprozesses häufig bestimmte Codepfade entfernt. In Direct3D 9 können zwei Arten von Eingaben entfernt (zum Entfernen markiert) werden, wenn sie nicht verwendet werden: Signatureingaben (wie das folgende Beispiel) und konstante Eingaben. Wenn das Ende des Konstantenpuffers nicht verwendete Einträge enthält, spiegelt die Größendeklaration im Shader die Größe des konstanten Puffers ohne die nicht verwendeten Einträge am Ende wider. Beide Arten von Eingaben verbleiben in Signaturen oder konstanten Puffern Direct3D 10 mit einer besonderen Ausnahme im Fall von nicht verwendeten konstanten Eingaben am Ende eines konstanten Puffers. Dies kann sich auf die Engine auswirken, wenn große Shader und Eingabelayouts erstellt werden. Elemente, die durch Optimierungen in dead code im Compiler entfernt werden, müssen weiterhin in der Eingabestruktur deklariert werden. Dies wird im folgenden Beispiel veranschaulicht:

### <a name="vertex-shader-input-structure-example"></a>Vertex-Shader-Eingabestruktur – Beispiel


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* Direct3D 9 dead code removal would remove the declaration in the shader due to conditional dead code removal


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



Oder Sie können es noch offensichtlicher machen, dass die Konstante eine Kompilierzeitkonst constant mit der folgenden Deklaration ist:


```
#define LIGHT_MAPPED false
```



Im obigen Beispiel würde unter Direct3D 9 das uv2-Element aufgrund von Optimierungen in dead code im Compiler entfernt. Unter Direct3D 10 wird der in dead-Code weiterhin entfernt, aber für das Layout des Shadereingabe-Assemblers muss die Definition der Eingabedaten vorhanden sein. Die Shader-Reflektionsebene bietet die Möglichkeit, diese Situation auf generische Weise zu behandeln, wobei Sie die Shadereingabeanforderungen durchlaufen und sicherstellen können, dass Sie eine vollständige Beschreibung der Zuordnung von Eingabestream zu Shadersignatur bereitstellen.

Hier ist eine Beispielfunktion zum Erkennen des Vorhandenseins eines semantischen Namens/Indexes in einer Funktionssignatur:


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



### <a name="state-object-creation"></a>Erstellung von Zustandsobjekten

Beim Portieren von Engine-Code kann es helfen, zunächst einen Standardsatz von Zustandsobjekten zu verwenden und alle Renderzustands-/Texturzustandseinstellungen des Direct3D 9-Geräts zu deaktivieren. Dies verursacht Renderingartefakte, ist aber die schnellste Möglichkeit, die Dinge in Betrieb zu nehmen. Sie können später ein Zustandsobjekt-Verwaltungssystem erstellen, das einen Verbundschlüssel verwenden kann, um die maximale Wiederverwendung der Anzahl der verwendeten Zustandsobjekte zu ermöglichen.

## <a name="porting-textures"></a>Portieren von Texturen

### <a name="file-formats-supported"></a>Unterstützte Dateiformate

Die **Funktionen D3DXxxCreateXXX** und **D3DXxxSaveXXX,** die eine Textur aus oder in einer Grafikdatei erstellen oder speichern (z. B. [**D3DX10CreateTextureFromFile),**](d3dx10createtexturefromfile.md)unterstützen einen anderen Satz von Dateiformaten in Direct3D 10 als in Direct3D 9:



| Dateiformat | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| BMP        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| .ppm        | x          |             |
| DIB        | x          |             |
| .hdr        | x          |             |
| PFM        | x          |             |
| TIFF       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Weitere Informationen finden Sie unter Vergleichen der Direct3D 9 [**D3DXIMAGE \_ FILEFORMAT-Enumerationen**](../direct3d9/d3dximage-fileformat.md) mit den [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT-Enumerationen**](d3dx10-image-file-format.md) für Direct3D 10.

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8. Für die Verarbeitung von Texturdatei empfiehlt es sich, [DirectXTex zu verwenden.](https://github.com/Microsoft/DirectXTex)

 

### <a name="mapping-texture-formats"></a>Zuordnen von Texturformaten

Die folgende Tabelle zeigt die Zuordnung von Texturformaten von Direct3D 9 zu Direct3D 10. Alle Inhalte in Formaten, die in DXGI nicht verfügbar sind, müssen von Hilfsprogrammroutinen konvertiert werden.



| Direct3D 9-Format                   | Direct3D 10-Format                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                     | DXGI \_ FORMAT \_ UNKNOWN                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM & DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM & DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | DXGI \_ FORMAT \_ B5G6R5 \_ UNORMNORM                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORMFORMAT                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | DXGI \_ FORMAT \_ A8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | DXGI \_ FORMAT \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM & DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | DXGI FORMAT R8 UNORM Hinweis: Verwenden Sie .r swizzle im Shader, um Rot auf andere Komponenten zu duplizieren, um \_ \_ das \_ D3D9-Verhalten zu erhalten.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ FORMAT \_ R8G8 \_ UNORM Hinweis: Verwenden Sie swizzle .rrrg im Shader, um Rot zu duplizieren, und verschieben Sie Grün auf die Alphakomponenten, um das D3D9-Verhalten zu erhalten.                                                                                                            |
| D3DFMT \_ A4L4                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | \_DXGI-FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ FORMAT \_ G8R8 \_ G8B8 \_ UNORM (in DX9 wurden die Daten um 255,0f hochskaliert, aber dies kann im Shadercode behandelt werden).                                                                                                                                   |
| D3DFMT \_ YUY2                        | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ FORMAT \_ R8G8 \_ B8G8 \_ UNORM (in DX9 wurden die Daten um 255,0f hochskaliert, aber dies kann im Shadercode verarbeitet werden).                                                                                                                                   |
| D3DFMT \_ DXT1                        | DXGI \_ FORMAT \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ FORMAT \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB Hinweis: DXT1 und DXT2 sind aus API-/Hardwareperspektive identisch... Der einzige Unterschied war "prämultipliziertes Alpha", das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt. |
| D3DFMT \_ DXT3                        | DXGI \_ FORMAT \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ FORMAT \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB Hinweis: DXT3 und DXT4 sind aus API-/Hardwareperspektive identisch... Der einzige Unterschied war "prämultipliziertes Alpha", das von einer Anwendung nachverfolgt werden kann und kein separates Format benötigt. |
| D3DFMT \_ DXT5                        | DXGI \_ FORMAT \_ BC3 \_ UNORM & DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ LOCKABLE | DXGI \_ FORMAT \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | DXGI \_ FORMAT \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ LOCKABLE              | DXGI \_ FORMAT \_ D32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI \_ FORMAT \_ R16 \_ UNORM Hinweis: Verwenden Sie .r swizzle im Shader, um Rot auf andere Komponenten zu duplizieren, um das D3D9-Verhalten zu erhalten.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI \_ FORMAT \_ R16 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI \_ FORMAT \_ R32 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | \_DXGI-FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI \_ FORMAT \_ R16 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | \_DXGI-FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI \_ FORMAT \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | \_DXGI-FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT Hinweis: Shader ruft UINT-Werte ab, aber wenn ganzzahlige Gleitkommawerte im Direct3D 9-Stil benötigt werden (0,0f, 1,0f... 255.f), UINT kann einfach in float32 im Shader konvertiert werden.                                                               |
| D3DDECLTYPE \_ SHORT2                 | DXGI \_ FORMAT \_ R16G16 \_ SINT Hinweis: Shader ruft SINT-Werte ab, aber wenn integrale Gleitkommawerte im Direct3D 9-Stil benötigt werden, kann SINT einfach im Shader in float32 konvertiert werden.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT Hinweis: Shader ruft SINT-Werte ab, aber wenn ganzzahlige Gleitkommawerte im Direct3D 9-Stil benötigt werden, kann SINT einfach im Shader in float32 konvertiert werden.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | \_DXGI-FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | \_DXGI-FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | \_DXGI-FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | \_DXGI-FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Nicht verfügbar                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | \_DXGI-FORMAT \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | \_DXGI-FORMAT \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹DXGI 1.1, das in der Direct3D 11-Runtime enthalten ist, enthält BGRA-Formate. Die Unterstützung für diese Formate ist jedoch optional für Direct3D 10- und 10.1-Geräte mit Treibern, die im Windows Display Driver Model (WDDM) für Windows Vista (WDDM 1.0) implementiert sind. Erwägen Sie stattdessen die Verwendung von DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM. Alternativ können Sie Ihr Gerät mit [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) erstellen, um sicherzustellen, dass Sie nur Computer unterstützen, auf denen die Direct3D 11.0-Runtime und ein WDDM 1.1-Treiber oder höher installiert sind.

²DXGI 1.0 definierte die Formate 5:6:5 und 5:5:5:1, aber sie wurden von der Direct3D 10.x- oder Direct3D 11.0-Runtime nicht unterstützt. Diese Formate werden optional mit DXGI 1.2 in der DirectX 11.1-Runtime unterstützt. Dies ist für Grafikkarten auf Featureebene 11.1 und WDDM 1.2 -Treiber (Anzeigetreibermodell ab Windows 8) erforderlich und wird bereits auf 10Level9-Featureebenen unterstützt.

Mit gisXGI 1.2 wurde das Format 4:4:4:4 eingeführt. Dieses Format wird optional in der DirectX 11.1-Runtime unterstützt, die für Grafikkarten auf Featureebene 11.1 und WDDM 1.2-Treiber erforderlich ist und bereits auf 10level9-Featureebenen unterstützt wird.

Bei nicht komprimierten Formaten hat DXGI die Unterstützung für beliebige Pixelformatmuster eingeschränkt. alle nicht komprimierten Formate müssen vom Typ RGBA sein. Dies kann eine Swizzling vorhandener Medienressourcen-Pixelformate erfordern. Es wird empfohlen, nach Möglichkeit als Offlinevorverarbeitungsdurchlauf zu berechnen.

## <a name="porting-shaders"></a>Portieren von Shadern

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Direct3D 10-Shader werden in HLSL erstellt.

Direct3D 10 beschränkt die Verwendung der Assemblysprache auf die Verwendung von Debugzwecken. Daher müssen alle in Direct3D 9 verwendeten handgeschriebenen Assembly-Shader in HLSL konvertiert werden.

### <a name="shader-signatures-and-linkage"></a>Shadersignaturen und -verknüpfung

Wir haben die Anforderungen für die Verknüpfung der Eingabeassembly mit Vertex-Shader-Eingabesignaturen weiter oben in diesem Dokument erläutert (siehe oben). Beachten Sie, dass die Direct3D 10-Runtime auch die Anforderungen für die Stage-to-Stage-Verknüpfung zwischen Shadern verstärkt hat. Diese Änderung wirkt sich auf Shaderquellen aus, bei denen die Bindung zwischen Phasen möglicherweise nicht vollständig unter Direct3D 9 beschrieben wurde. Beispiel:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Fehlerhafte VS - PS-Verknüpfung : Obwohl der Pixelshader möglicherweise nicht an der vollständigen Matrix interessiert ist, muss die Verknüpfung den vollständigen float4x3 angeben.

Beachten Sie, dass die Bindungssemantik zwischen Phasen genau übereinstimmen muss. Die Eingaben der Zielstufen können jedoch ein Präfix der ausgegebenen Werte sein. Im obigen Beispiel könnte der Pixel-Shader position und texcoord1 als einzige Eingaben haben, aber nicht die Position und texcoord2 als einzige Eingaben aufgrund der Sortierungseinschränkungen.

### <a name="hlsl-shader-stage-linkages"></a>HLSL Shader Stage-Verknüpfungen

Die Verknüpfung zwischen Shadern kann an einem der folgenden Punkte in der Pipeline auftreten:

-   Eingabeassemblierer zu Vertex-Shader
-   Vertex-Shader zu Pixel-Shader
-   Vertex-Shader zu Geometry-Shader
-   Vertex-Shader zu Streamausgabe
-   Geometry-Shader in Pixel-Shader
-   Geometry-Shader zum Streamen

### <a name="constant-buffers"></a>Konstantenpuffer

Zur Vereinfachung des Portierens von Inhalten aus Direct3D 9 kann ein erster Ansatz zur konstanten Verwaltung außerhalb des Effects-Systems die Erstellung eines einzelnen konstanten Puffers mit allen erforderlichen Konstanten beinhalten. Es ist wichtig, dass die Leistung Konstanten nach der erwarteten Aktualisierungshäufigkeit in Puffer sortiert. Diese Organisation reduziert die Anzahl redundanter Konstantensätze auf ein Minimum.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Benutzerclipebenen in HLSL auf Featureebene 9 und höher

Ab Windows 8 können Sie das **Clipplanes-Funktionsattribut** in einer HLSL-Funktionsdeklaration anstelle von [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) verwenden, damit Ihr Shader sowohl auf [Featureebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x als auch auf [](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) \_ Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User clip planes on feature level 9 hardware (Benutzer clip planes on feature level 9 hardware ( Benutzer clip planes on feature level 9 hardware](../direct3dhlsl/user-clip-planes-on-10level9.md)).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Zusätzliche Direct3D 10-Unterschiede, die überwacht werden müssen

### <a name="integers-as-input"></a>Ganze Zahlen als Eingabe

In Direct3D 9 gab es keine echte Hardwareunterstützung für ganzzahlige Datentypen, aber Direct3D 10-Hardware unterstützt explizite ganzzahlige Typen. Wenn der Scheitelpunktpuffer Gleitkommadaten enthält, müssen Sie über eine float-Eingabe verfügen. Andernfalls ist ein ganzzahliger Typ die Bitmusterdarstellung des Gleitkommawerts. Ein ganzzahliger Typ ist für eine Pixel-Shadereingabe nicht zulässig, es sei denn, der Wert ist für keine Interpolation markiert (siehe [Interpolationsmodifizierer](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Mauscursor

In früheren Versionen von Windows funktionierten die standardmäßigen GDI-Mauscursorroutinen nicht auf allen exklusiven Vollbildgeräten ordnungsgemäß. Die [**APIs SetCursorProperties,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties) [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)und [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) wurden hinzugefügt, um diese Fälle zu behandeln. Da Windows Vista-Version von GDI [DXGI-Oberflächen](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) vollständig versteht, ist diese spezialisierte Mauscursor-API nicht erforderlich, sodass keine Direct3D 10-Entsprechung vorhanden ist. Direct3D 10-Anwendungen sollten stattdessen die [GDI-Standard-Mauscursorroutinen](../menurc/cursors.md) für Mauscursor verwenden.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Zuordnen von Texels zu Pixeln in Direct3D 10

In Direct3D 9 waren texel-Center und Pixelcenter eine halbe Einheit voneinander entfernt (siehe [Direktes Zuordnen von Texels zu Pixeln (Direct3D 9).](../direct3d9/directly-mapping-texels-to-pixels.md) In Direct3D 10 befinden sich texel-Center bereits in halber Einheit, sodass keine Vertexkoordinaten verschoben werden müssen.

Das Rendern von Vollbild-Quadern ist mit Direct3D 10 einfacher. Vollbild-Quader sollten in Clipspace (-1,1) definiert und einfach ohne Änderungen durch den Vertex-Shader übergeben werden. Auf diese Weise ist es nicht erforderlich, den Scheitelpunktpuffer jedes Mal neu zu laden, wenn sich die Bildschirmauflösung ändert, und es ist kein zusätzlicher Aufwand im Pixelshader erforderlich, um die Texturkoordinaten zu bearbeiten.

### <a name="reference-counting-behavior-changes"></a>Änderungen des Referenzzählverhaltens

Im Gegensatz zu früheren Direct3D-Versionen enthalten die verschiedenen Set-Funktionen keinen Verweis auf die Geräteobjekte. Dies bedeutet, dass die Anwendung sicherstellen muss, dass sie einen Verweis auf das Objekt enthält, solange das Objekt an die Pipeline gebunden werden soll. Wenn die Ref-Anzahl des Objekts auf 0 (null) fällt, wird die Gebundene des Objekts an die Pipeline aufgehoben, wenn es zerstört wird. Diese Art der Verweisaufbewahrung wird auch als schwache Verweisaufbewahrung bezeichnet, sodass jede Bindungsposition im Device-Objekt einen schwachen Verweis auf die Schnittstelle/das Objekt enthält. Sofern nicht explizit anders angegeben, sollte dieses Verhalten für alle Set-Methoden angenommen werden. Wenn die Zerstörung eines Objekts bewirkt, dass ein Bindungspunkt auf **NULL** festgelegt wird, gibt die Debugebene eine Warnung aus. Beachten Sie, dass Durch Aufrufe von Get-Gerätemethoden wie [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) die Verweisanzahl der zurückgegebenen Objekte erhöht wird.

### <a name="test-cooperative-level"></a>Testen der kooperativen Ebene

Die Funktionalität der Direct3D 9-API [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) entspricht dem Festlegen von [DXGI \_ PRESENT \_ TEST](../direct3ddxgi/dxgi-present.md) beim Aufrufen von [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Eine Funktion ähnlich der Direct3D 9 [**IDirect3DDevice9::StretchRect-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) ist in Direct3D 10 und 10.1 nicht verfügbar. Um Ressourcenoberflächen zu kopieren, verwenden Sie [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Rendern Sie für Größenänderungsvorgänge mithilfe der Texturfilterung in eine Textur. Verwenden Sie zum Konvertieren von MSAA-Oberflächen in Nicht-MSAA-Oberflächen [**ID3D10Device::ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Zusätzliche Direct3D 10.1-Unterschiede

Windows Vista mit Service Pack 1 (SP1) enthielt ein kleineres Update auf Direct3D 10 und Direct3D 10.1, das die folgenden zusätzlichen Hardwarefeatures verfügbar gemacht hat:

-   MSAA-Shader pro Beispiel
-   MSAA-Tiefenlesedauer
-   Unabhängige Mischungsmodi pro Renderziel
-   Cubezuordnungsarrays
-   Rendern in blockkomprimierte Formate (BC)

Das Direct3D 10.1-Update hat Unterstützung für die folgenden neuen Schnittstellen hinzugefügt, die von vorhandenen Schnittstellen abgeleitet werden:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

Das Direct3D 10.1-Update enthielt auch die folgenden zusätzlichen Strukturen:

-   [**D3D10 \_ RENDER \_ TARGET \_ BLEND \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**D3D10 \_ \_ SHADER-RESSOURCENANSICHT \_ \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

Die Direct3D 10.1-API enthält ein neues Konzept namens Featureebene. Dieses Konzept bedeutet, dass Sie die Direct3D 10.1-API verwenden können, um Direct3D 10.0 ([**D3D10 \_ FEATURE \_ LEVEL \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) oder Direct3D 10.1 ([**D3D10 \_ FEATURE LEVEL \_ \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) zu verwenden. Da die Direct3D 10.1-API von den Direct3D 10-Schnittstellen abgeleitet wird, können Anwendungen ein Direct3D 10.1-Gerät erstellen und es dann als Direct3D 10.0-Gerät verwenden, es sei denn, es sind neue 10.1-spezifische Features erforderlich (vorausgesetzt, dass **D3D10 \_ FEATURE \_ LEVEL \_ 10 \_ 1** vorhanden ist und diese Features unterstützt).

> [!Note]  
> Direct3D 10.1-Geräte können die vorhandenen 10.0 HLSL-Shaderprofile \_ (vs. 4 \_ 0, ps \_ 4 \_ 0, gs 4 0) und die neuen \_ \_ 10.1-Profile \_ (vs. 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 1) \_ mit zusätzlichen HLSL-Anweisungen und -Funktionen verwenden.

 

Windows 7 enthielt ein kleineres Update der Direct3D 10.1-API, die in der Direct3D 11-Runtime enthalten ist. Dieses Update fügt Unterstützung für die folgenden Featureebenen hinzu:

-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 wurde auch Unterstützung für Direct3D 10.1 für [Windows Advanced Rasterization Platform (WARP) hinzugefügt.](../direct3darticles/directx-warp.md) Sie können einen WARP-Treiber angeben, indem [**Sie D3D10 \_ DRIVER TYPE \_ \_ WARP verwenden.**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)

Weitere Informationen zu Direct3D 10.1 finden Sie unter [Direct3D 10.1-Features](d3d10-graphics-programming-guide-10-1.md) und die [**Enumeration D3D10 \_ FEATURE \_ LEVEL1.**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
