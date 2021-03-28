---
title: Direct3D 11-Features
description: Das-Programmier Handbuch enthält Informationen zur Verwendung der programmierbaren Direct3D 11-Pipeline zum Erstellen von Echt Zeit 3D-Grafiken für Spiele und für wissenschaftliche und Desktop Anwendungen.
ms.assetid: ee4dae04-1a52-4587-87c1-006abb687a91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b6ec64e315275ca6faaf513d04f996609615a2
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039817"
---
# <a name="direct3d-11-features"></a>Direct3D 11-Features

Das-Programmier Handbuch enthält Informationen zur Verwendung der programmierbaren Direct3D 11-Pipeline zum Erstellen von Echt Zeit 3D-Grafiken für Spiele und für wissenschaftliche und Desktop Anwendungen.

-   [Compute-Shader](#compute-shader)
-   [Dynamische shaderverknüpfung](#dynamic-shader-linking)
-   [Multithreading](#multithreading)
-   [Tessellation](#tessellation)
-   [Vollständige Auflistung der Features](#full-listing-of-features)
-   [In früheren Versionen hinzugefügte Features](#features-added-in-previous-releases)
-   [Zugehörige Themen](#related-topics)

## <a name="compute-shader"></a>Compute-Shader

Ein Compute-Shader ist ein programmierbarer Shader, der für die allgemeine Daten parallele Verarbeitung konzipiert ist. Das heißt, dass Compute-Shader eine GPU als allgemeinen parallelen Prozessor verwenden können. Der COMPUTE-Shader ähnelt den anderen programmierbaren Pipeline-Shadern (z. b. Vertex, Pixel, Geometrie), wie er auf Eingaben und Ausgaben zugreift. Die COMPUTE-Shader-Technologie wird auch als DirectCompute-Technologie bezeichnet. Ein Compute-Shader ist in Direct3D integriert und kann über ein Direct3D-Gerät aufgerufen werden. Mithilfe des Direct3D-Geräts können Speicherressourcen direkt mit Grafik-Shadern gemeinsam genutzt werden. Es ist jedoch nicht direkt mit anderen shaderphasen verbunden.

Ein Compute-Shader ist für Massenmarkt Anwendungen konzipiert, die Berechnungen zu interaktiven Tarifen ausführen, wenn die Kosten für den Übergang zwischen der API (und dem zugehörigen Software Stapel) und einer CPU zu viel mehr Aufwand beanspruchen würden.

Ein Compute-Shader verfügt über einen eigenen Satz von Zuständen. Ein Compute-Shader verfügt nicht unbedingt über eine erzwungene 1-1-Zuordnung zu Eingabedaten Sätzen (wie z. b. ein Vertexshader) oder Ausgabedaten Sätze (wie der Pixelshader). Einige Features des Grafik-Shaders werden zwar unterstützt, aber andere wurden entfernt, sodass neue Compute-Shader-spezifische Features hinzugefügt werden können.

Zur Unterstützung der COMPUTE-Shader-spezifischen Features sind nun mehrere neue Ressourcentypen verfügbar, z. b. Lese-/Schreibpuffer, Texturen und strukturierte Puffer.

Weitere Informationen finden Sie unter [Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) .

## <a name="dynamic-shader-linking"></a>Dynamische shaderverknüpfung

Renderingsysteme müssen mit erheblicher Komplexität umgehen, wenn Sie Shaders verwalten, und gleichzeitig die Möglichkeit zur Optimierung von Shader-Code bieten. Dies wird zu einer noch größeren Herausforderung, da Shader eine Vielzahl verschiedener Materialien in einer gerenderten Szene über verschiedene Hardware Konfigurationen hinweg unterstützen müssen. Um diese Herausforderung zu meistern, haben Shader-Entwickler häufig einen von zwei allgemeinen Ansätzen erreicht. Sie haben entweder voll ausgestattete große, allgemeine Shader erstellt, die von einer Vielzahl von Szenen Elementen verwendet werden können, die eine gewisse Flexibilität für die Flexibilität erzielen, oder einzelne Shader für jeden erforderlichen Geometry-Stream, Materialtyp oder leichte Typkombination erstellen.

Diese großen, allgemeinen Shader behandeln diese Aufgabe durch erneutes Kompilieren desselben Shader mit unterschiedlichen Präprozessordefinitionen, und die letztere Methode verwendet Brute-Force Developer Power, um das gleiche Ergebnis zu erzielen. Die Explosion der Shader-permutations war häufig ein Problem für Entwickler, die nun Tausende verschiedener shaderpermutationen innerhalb ihrer Spiel-und assetpipeline verwalten müssen.

Direct3D 11 und Shader Model 5 stellen objektorientierte Sprachkonstrukte vor und bieten Laufzeitunterstützung für Shader-Verknüpfungen, um Entwicklern beim Programmieren zu helfen.

Weitere Informationen finden Sie unter [dynamisches Verknüpfen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking) .

## <a name="multithreading"></a>Multithreading

Viele Grafikanwendungen sind aufgrund kostspieliger Aktivitäten, z. b. Szenen Diagramm Traversierung, Objekt Sortierung und Physik Simulationen, CPU-gebunden. Da mehr Kernsysteme immer mehr verfügbar sind, hat Direct3D 11 die Multithreading-Unterstützung verbessert, um eine effiziente Interaktion zwischen mehreren CPU-Threads und den D3D11-Grafik-APIs zu ermöglichen.

Direct3D 11 ermöglicht die Unterstützung von Multithreading durch die folgenden Funktionen:

-   Gleichzeitige Objekte werden nun in separaten Threads erstellt – durch das Erstellen von Einstiegspunkt Funktionen zum Erstellen von Objekten mit freiem Thread können viele Threads Objekte gleichzeitig erstellen. Beispielsweise kann eine Anwendung jetzt einen Shader kompilieren oder beim Rendern auf einem anderen Thread eine Textur in einem Thread laden.
-   Befehlslisten können für mehrere Threads erstellt werden – eine Befehlsliste ist eine aufgezeichnete Sequenz von Grafik Befehlen. Mit Direct3D 11 können Sie Befehlslisten für mehrere CPU-Threads erstellen, die eine parallele Durchquerung der Szene-oder Physik Verarbeitung in mehreren Threads ermöglichen. Dadurch wird der hauptrenderingthread freigegeben, um Befehls Puffer an die Hardware zu verteilen.

Weitere Informationen finden Sie unter [Multithreading](overviews-direct3d-11-render-multi-thread.md) .

## <a name="tessellation"></a>Mosaik

Das Mosaik kann verwendet werden, um ein einzelnes Modell mit unterschiedlichen Detailebenen zu erzeugen. Bei diesem Ansatz wird ein geometrisch genaueres Modell generiert, das von der für eine Szene benötigten Detailstufe abhängt. Verwenden Sie den Mosaik Prozess in einer Szene, in der die Detailebene ein niedrigeres Geometrie Modell zulässt, wodurch die Nachfrage nach der während des Renderings genutzten Speicherbandbreite verringert wird.

In Direct3D wird das Mosaik auf der GPU implementiert, um eine glättere gekrümmte Oberfläche von einem groben (weniger detaillierten) Eingabe Patch zu berechnen. Jedes (Quad-oder Dreieck)-patchgesicht wird in kleinere dreieckige Flächen unterteilt, die der gewünschten Oberfläche besser entsprechen.

Weitere Informationen zum Implementieren von Mosaik in der Grafik Pipeline finden Sie unter Mosaik [Übersicht](direct3d-11-advanced-stages-tessellation.md).

## <a name="full-listing-of-features"></a>Vollständige Auflistung der Features

Dies ist eine umfassende Liste der Features in Direct3D 11.

-   Sie können Direct3D 11 auf [downlevelhardware](overviews-direct3d-11-devices-downlevel.md) ausführen, indem Sie eine [featurestufe](overviews-direct3d-11-devices-downlevel-intro.md) angeben, wenn Sie ein Gerät erstellen.
-   Sie können den Mosaik Prozess (siehe Mosaik [Übersicht](direct3d-11-advanced-stages-tessellation.md)) mit den folgenden shadertypen ausführen:

    -   Rumpf-Shader
    -   Domain-Shader

-   Direct3D 11 unterstützt Multithreading (Weitere Informationen finden Sie unter [Multithreading](overviews-direct3d-11-render-multi-thread.md)).

    -   Multithread-Ressource/Shader/Objekt Erstellung
    -   Erstellung der Multithread-Anzeigeliste

-   Direct3D 11 erweitert Shader mit den folgenden Features (siehe [Shader Model 5](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl))

    -   Adressierbare Ressourcen: Texturen, Konstante Puffer und Samplern
    -   Zusätzliche Ressourcentypen, z. b. Lese-/Schreibpuffer und Texturen (siehe [neue Ressourcentypen](direct3d-11-advanced-stages-cs-resources.md)).
    -   Unterroutinen
    -   Compute-Shader (siehe [Übersicht über Compute-Shader](direct3d-11-advanced-stages-compute-shader.md)): ein Shader, der Berechnungen beschleunigt, indem der Problem Raum zwischen mehreren Softwarethreads oder Gruppen von Threads aufgeteilt wird, und das Freigeben von Daten zwischen shaderregistern, um die Datenmenge, die für die Eingabe in einen Shader erforderlich ist, erheblich zu reduzieren. Zu den Algorithmen, die der COMPUTE-Shader erheblich verbessern kann, gehören nach Verarbeitung, Animation, Physik und künstliche Intelligenz.
    -   Geometry-Shader (siehe [Geometry-Shader-Funktionen](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-gs-features))

        -   Instanziierung: ermöglicht dem Geometry-Shader das Ausgeben von maximal 1024 Scheitel Punkten oder einer beliebigen Kombination aus Instanzen und Scheitel Punkten bis 1024 (maximal 32 Instanzen von 32 Vertices).

    -   Pixel-Shader

        -   Abdeckung als PS-Eingabe
        -   Programmierbare interpolung von Eingaben: der Pixelshader kann Attribute innerhalb des Pixels (an beliebiger Stelle im Multisampling-Raster) auswerten.
        -   Bei der Centroid-Stichprobenentnahme von Attributen müssen folgende Regeln befolgt werden:

            -   Wenn alle Stichproben im primitiven behandelt werden, wird das Attribut im Pixel Center ausgewertet, unabhängig davon, ob das Beispiel Muster eine Beispiel Position im Pixel Center aufweist.
            -   Andernfalls wird das-Attribut im ersten behandelten Beispiel ausgewertet, d. h. das Beispiel mit dem niedrigsten Index zwischen allen Beispiel Indizes. In diesem Fall wird die Abtast Abdeckung nach dem Anwenden der logischen and-Operation auf die Abdeckung und den Status des Rasterizers für die Stichproben Maske bestimmt.
            -   Wenn keine Stichproben abgedeckt werden (z. b. in Hilfsskripts, die außerhalb der Grenzen eines primitiven ausgeführt werden, um 2 x 2 Pixel Stempel auszufüllen), wird das Attribut auf eine der folgenden Arten ausgewertet:

                -   Wenn der Zustand der "Sample-Mask Raster" eine Teilmenge der Stichproben im Pixel ist, ist das erste Beispiel, das durch den Zustand "Sample-Mask Raster" abgedeckt wird, der Auswertungs Punkt.
                -   Andernfalls ist das Pixel Center in der vollständigen Sample Mask-Bedingung der Auswertungs Punkt.

-   Direct3D 11 erweitert Texturen (siehe [Übersicht über Texturen](overviews-direct3d-11-resources-textures.md)) mit den folgenden Funktionen.

    -   Gather4

        -   Unterstützung für Texturen mit mehreren Komponenten: Geben Sie einen Kanal für den Ladevorgang an.
        -   Unterstützung für programmierbare Offsets

    -   Streaming

        -   Textur Klammern zum Einschränken des WDDM-Vorladens

    -   Werte für die Textur von 16K
    -   8 Bits von subtexund unter MIP-Genauigkeit bei der Textur Filterung erfordern
    -   Neue Textur Komprimierungs Formate (1 neues LDR-Format und 1 neues HDR-Format)

-   Direct3D 11 unterstützt die konservative otiefe: Dieser Algorithmus ermöglicht einem Pixelshader, den pro-Pixel-tiefen Wert des Pixel-Shaders mit dem im Rasterizer zu vergleichen. Das Ergebnis ermöglicht frühe Vorgänge bei der Wiedergabe und behält gleichzeitig die Möglichkeit, otiefe von einem Pixelshader auszugeben.
-   Direct3D 11 unterstützt großen Arbeitsspeicher

    -   Ressourcen > 4 GB zulassen
    -   Indizes von Ressourcen 32-Bit beibehalten, aber Ressource größer

-   Direct3D 11 unterstützt Datenstrom-Ausgabe Verbesserungen

    -   Adressierbare Datenstrom Ausgabe
    -   Erhöhen Sie die Anzahl von streamausgaben auf 4.
    -   Alle Datenstrom Ausgabepuffer in mehrere Elemente ändern

-   Direct3D 11 unterstützt Shader Model 5 (siehe [Shader Model 5](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5))

    -   Verdoppelt mit denorms
    -   Bits-Set-Anweisung zählen
    -   Erste Bitset-Anweisung suchen
    -   Behandlung von Durchläufen/Überlauf
    -   Bitumkehr Anweisungen für FFTs
    -   Bedingungs interner Austausch
    -   ResInfo für Puffer
    -   Gegenseitige Genauigkeit bei reduzierter Genauigkeit
    -   Shaderkonvertierungsanweisungen-FP16 zu FP32 und umgekehrt
    -   Strukturierter Puffer, bei dem es sich um einen neuen Puffertyp handelt, der strukturierte Elemente enthält.

-   Direct3D 11 unterstützt Lese-oder Schablonen Ansichten.

    -   Deaktiviert Schreibzugriffe auf den Teil, der schreibgeschützt ist, und ermöglicht die Verwendung von Textur als Eingabe und für Tiefe Berechnungen

-   Direct3D 11 unterstützt Draw indirekt-Direct3D 10 implementiert drawauto, das Inhalte (von der GPU generiert) annimmt und Sie (auf der GPU) rendert. Direct3D 11 generalisiert drawauto, sodass es von einem Compute-Shader mit drawinstanzierte und drawindexedinstangeleitet aufgerufen werden kann.
-   Direct3D 11 unterstützt verschiedene Features

    -   Gleit Komma-Viewports
    -   Pro-Ressourcen-MipMap-Klammer
    -   Tiefen Abweichung: Dieser Algorithmus aktualisiert das Verhalten der tiefen Verschiebung mithilfe des Raster-Zustands. Das Ergebnis beseitigt die Szenarien, in denen der berechnete Bias Nan sein könnte.
    -   Ressourcen Limits: Ressourcen Indizes müssen immer noch <= 32 Bits sein, aber Ressourcen können größer als 4 GB sein.
    -   Genauigkeit des Rasterizers
    -   MSAA-Anforderungen
    -   Reduzierte Leistungsindikatoren
    -   1-Bit-Format und Text Filter entfernt

## <a name="features-added-in-previous-releases"></a>In früheren Versionen hinzugefügte Features

Eine Liste der Features, die in früheren Versionen hinzugefügt wurden, finden Sie in den folgenden Themen:

-   [Neuerungen im SDK für Windows 7/Direct3D 11 vom August 2009](dx11-whats-new.md)
-   [Neuerungen in der Technical Preview-Version von November 2008 Direct3D 11](dx11-08nov-whats-new.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 