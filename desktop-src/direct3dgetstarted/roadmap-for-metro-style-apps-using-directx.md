---
title: Roadmap für DirectX-Desktop-Apps
description: Im Folgenden finden Sie wichtige Ressourcen für die ersten Schritte mit DirectX und C++ zum Entwickeln grafikintensiver Desktop-Apps wie Spiele.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5940e775de65d6d22a9b244d1bd0b881240cf296b740c9a0be9c38f3ab0725a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983890"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roadmap für DirectX-Desktop-Apps

Hier finden Sie wichtige Ressourcen für die ersten Schritte mit DirectX und C++ zum Entwickeln grafikintensiver Desktop-Apps wie Spiele. Dies ist keine umfassende Liste aller Features oder verfügbaren Ressourcen.

## <a name="get-started"></a>Erste Schritte

Hier sind einige wichtige Themen. Einrichten Ihres DirectX-Projekts, Anpassen an Windows und Beispielanwendungen.

| Thema | BESCHREIBUNG |
|-|-|
| [Erstellen Ihrer ersten Windows-App mit DirectX](building-your-first-directx-app.md) | Verwenden Sie dieses grundlegende Tutorial, um mit der Entwicklung von DirectX-Apps zu beginnen, und verwenden Sie dann die Roadmap, um DirectX weiter zu erkunden. |
| [Erste Schritte mit DirectX für Windows](getting-started-with-a-directx-game.md) | Überprüfen Sie die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen. |
| [Vollständiger Code für ein DirectX-Framework](complete-code-sample-for-using-a-corewindow-with-directx.md) | Abrufen des Codes für ein einfaches DirectX-Renderingframework. |
| [Verwenden von Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | In diesem Abschnitt wird veranschaulicht, wie Sie die Microsoft Direct3D 11-API verwenden, um mehrere allgemeine Aufgaben auszuführen. |
| [Programmieranleitung für Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | Der Programmierleitfaden enthält Informationen zur Verwendung der programmierbaren Microsoft Direct3D 11-Pipeline zum Erstellen von 3D-Echtzeitgrafiken für Desktopanwendungen. |
| [Tools für DirectX-Grafiken](/windows/desktop/direct3dtools/dx-graphics-tools) | Dokumentation zu Tools, die zur Unterstützung der DirectX-Entwicklung verwendet werden. |
| [Neuerungen in Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Eine Aufschlüsselung aller Features, die in den neuesten Versionen von DirectX und Direct3D (derzeit 11.2) hinzugefügt wurden. |
| [Visual Studio 2013 herunterladen](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Sie müssen über Visual Studio Express 2013 für Windows Desktop verfügen, um Windows Store Spiele zu erstellen. Einen Überblick über Visual Studio finden Sie unter [Entwickeln von Windows Store-Apps mit Visual Studio 2012.](/previous-versions/windows/apps/br211384(v=win.10)) Weitere Informationen zu neuen Features in Visual Studio finden Sie unter [Product Highlights for Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Wo finde ich das DirectX SDK?](../directx-sdk--august-2009-.md) | Enthält Anleitungen für Entwickler, die ihre DirectX-Projekte in Microsoft Visual Studio bringen möchten. |

## <a name="sample-applications"></a>Beispielanwendungen

| Thema | BESCHREIBUNG |
|-|-|
| [Win32-Beispiel für Direct3D-Tutorial](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Einfaches Direct3D-Desktoptutorialbeispiel. |
| [DirectX-Videorenderingbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Ein Beispiel, das das benutzerdefinierte Videorendering mit Direct3D veranschaulicht. |

## <a name="review-key-direct3d-11-concepts"></a>Lesen Sie die wichtigsten Konzepte von Direct3D 11.

| Thema | BESCHREIBUNG |
|-|-|
| [Grafikpipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Behandelt die grundlegende Direct3D 11-Grafikpipeline. |
| [Rendering](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Behandelt die Direct3D-Renderingmodelle, -Komponenten, -Shader und den API-Aufrufflow. |
| [Ressourcen](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Behandelt Direct3D-"Ressourcen", z. B. Puffer und andere GPU-Ressourcentypen. |
| [Effekte](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Behandelt Direct3D-Multi-Shader-Instanziierung und Effekte.  |
| [Vorgehensweise: Erstellen einer Swapkette](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Erstellen der Swapkette, die zum Zeichnen von Pixeln in einen Bereich des Bildschirms verwendet wird. |
| [Vorgehensweise: Erstellen eines Geräts und des unmittelbaren Kontexts](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Erstellen einer Direct3D-Geräteabstraktion und eines unmittelbaren Kontexts zum Zeichnen |
| [Vorgehensweise: Erstellen eines Scheitelpunktpuffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Hier erfahren Sie, wie Sie eine einfache Liste von Gitternetzvertices für die Verarbeitung durch die GPU erstellen. |
| [Vorgehensweise: Erstellen eines Indexpuffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Erstellen eines Indexpuffers, sodass der Vertex-Shader die Reihenfolge der Scheitelpunkte in einem Gitternetz durchgehen kann. |
| [Vorgehensweise: Erstellen eines Konstantenpuffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Übergeben konstanter (einheitlicher) Daten zwischen CPU und GPU während des Renderings. |
| [Vorgehensweise: Erstellen einer Textur](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Erstellen einer Textur oder einer anderen Pufferressource, die von der GPU entnommen werden kann. |
| [Vorgehensweise: Initialisieren einer Textur aus einer Datei](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Hier erfahren Sie, wie Sie eine Textur aus einer Datei laden und für die Verwendung durch die Shaderpipeline verarbeiten. |
| [Vorgehensweise: Kompilieren eines Shaders](../direct3d11/how-to--compile-a-shader.md) | Kompilieren eines Shaders für die Verwendung in Ihrer Grafikanwendung. |

## <a name="graphics-apis"></a>Grafik-APIs

| Thema | BESCHREIBUNG |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Dokumentation der Kern-APIs für die Virtualisierung der GPU und ihrer Ressourcen sowie zum Zeichnen von Grafiken mithilfe eines einheitlichen Shadermodells. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Referenzdokumentation für High-Level Shadersprache, die Syntax und Regeln zum Definieren von Shaderprogrammen, die als Teil der Grafikpipeline in einem einheitlichen Shadermodell ausgeführt werden. |
| [DirectX-Grafikschnittstelle (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Dokumentation der low-level-APIs, die zum Abrufen der GPU-Schnittstelle und der Systemressourcen verwendet werden. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Dokumentation für die Direct2D-APIs, die das Zeichnen von 2D-Primitiven unterstützen. In der Regel wird Direct2D für benutzerdefinierte Benutzeroberflächen, Bildverarbeitung und Batchverarbeitung sowie einfache Spiele verwendet. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Dokumentation für die DirectWrite-APIs, die benutzerdefiniertes Rendern und Skalieren von Schriftarten unterstützen. |
| [Windows Imaging-Komponente (WIC)](/windows/desktop/wic/-wic-api) | Dokumentation für die WIC-APIs, die zum Lesen und Verwalten verschiedener Bitmapbildformate verwendet werden. |
| [DirectDraw Surfaces (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) für Texturen | Dokumentation zu den DDS-APIs, die für die 2D-Texturkomprimierung und -dekomprimierung in Verbindung mit den WIC-APIs verwendet werden. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Dokumentation für die DirectXMath-APIs, die Direct3D mit einer Reihe von Typen und Funktionen unterstützen, die für die 3D-Grafikentwicklung in Echtzeit geeignet sind. (ehemals XNAMath.) |
| [DirectCompute](https://walbourn.github.io/) | Dokumentation zu den DirectCompute-APIs, die für Compute- oder allgemeine Shaderfunktionen verwendet werden. |

## <a name="audio-media-and-input-apis"></a>Audio-, Medien- und Eingabe-APIs

| Thema | BESCHREIBUNG |
|-|-|
| [XAudio2-Programmieranleitung](/windows/desktop/xaudio2/programming-guide) | Knoten der obersten Ebene für die konzeptionelle Dokumentation zur XAudio2-Audio-API. |
| [XAudio2-Programmierreferenz](/windows/desktop/xaudio2/programming-reference) | Knoten der obersten Ebene für die XAudio2-Audio-API-Referenzdokumentation. |
| [XInput-Programmierhandbuch](/windows/desktop/xinput/programming-guide) | Knoten der obersten Ebene für die konzeptionelle Dokumentation zur XInput-Controller-API. |
| [XInput-Programmierreferenz](/windows/desktop/xinput/programming-reference) | Knoten der obersten Ebene für die Referenzdokumentation zur XInput-Controller-API. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Knoten der obersten Ebene für die API-Dokumentation zur Wiedergabe von Media Foundation -Medien (Audio/Video). In der Regel wird MF in Spielen für die Wiedergabe von Spielen verwendet, während XAudio2 für dynamische Audiodaten verwendet wird. |

## <a name="port-to-directx-11"></a>Portieren zu DirectX 11

| Thema | BESCHREIBUNG |
|-|-|
| [Migrieren zu Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Grundlegende Anleitung zum Verschieben Ihrer DirectX 9-Codebasis zu DirectX 11. |
| [Programmiertechniken mit dualer Verwendung für Spiele](https://walbourn.github.io/) | Ausführlicher Blogbeitrag zur Entwicklung für DirectX 9- \_ \* und DirectX 11-Featureebenen \_ \* in einer einzelnen Anwendung. |
| [Implementieren von Schattenpuffern für Direct3D-Featureebene 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Leitfaden für die Implementierung von Schattenkarten unter DirectX-Featureebene 9 \_ \* . |

## <a name="work-with-c"></a>Arbeiten mit C++

Wenn Sie ein Alter mit C++ auf Windows sind, sieht dies möglicherweise etwas anders aus. Im Folgenden finden Sie einige Zeiger auf Themen, die Ihnen helfen können, den Unterschied zu behandeln.

> [!NOTE]
> Einige dieser Themen unterstützen Sie bei der Wartung Ihrer C++/CX-Anwendung. Es wird jedoch empfohlen, [C++/WinRT für](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) neue Anwendungen zu verwenden. C++/WinRT ist eine vollständig standardisierte, moderne C++17-Programmiersprache für Windows-Runtime-APIs (WinRT), die als headerdateibasierte Bibliothek implementiert ist und Ihnen einen erstklassigen Zugriff auf die moderne Windows-API bietet.

| Thema | BESCHREIBUNG |
|-|-|
| [**Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Seite auf hoher Ebene, die links zu Inhalten im Zusammenhang mit C++ enthält. |
| [**Kurzreferenz (Windows Runtime und Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Die Tabelle enthält kurze Informationen zu Visual C++-Operatoren und Schlüsselwörtern für Komponentenerweiterungen (C++/CX). |
| [**Typsystem (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Referenzinhalt für die Typen, die von C++/CX unterstützt werden. |
| [**Namespaces (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Referenzinhalt für die Namespaces, die C++-spezifische Typen enthalten, die in Windows Store werden können. |

| Thema | BESCHREIBUNG |
|-|-|
| [Asynchrone Programmierung (DirectX und C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Erfahren Sie mehr über die asynchrone und Multithreadprogrammierung für DirectX-Apps und -Spiele. |
| [Asynchrone Programmierung in C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Beschreibt die grundlegenden Möglichkeiten, die Taskklasse zu verwenden, um asynchrone Windows Runtime zu nutzen. |
| [**task-Klasse (Concurrency Runtime)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Referenzdokumentation für die Aufgabenklasse. |
| [Taskparallelität (Concurrency Runtime)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Ausführliche Informationen zur Aufgabenklasse und deren Verwendung. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Zusätzliche nützliche Bibliotheken für Windows C++-Programmierung

| Thema | BESCHREIBUNG |
|-|-|
| [C++-Standardvorlagenbibliothek](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Laufzeittypen können gut mit Typen der Standardvorlagenbibliothek verwendet werden. Die meisten C++Windows Store-Apps verwenden Sammlungen und Algorithmen der Standardvorlagenbibliothek, mit Ausnahme der ABI-Grenze. |
| [Parallel Patterns Library](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL bietet Algorithmen und Typen, die die Aufgabenparallelität und Datenparallelität auf der CPU vereinfachen.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP bietet Zugriff auf die GPU für allgemeine Datenparallelität auf Grafikkarten, die DirectX 11 unterstützen. |

## <a name="blogs-and-other-resources"></a>Blogs und andere Ressourcen

| Thema | BESCHREIBUNG |
|-|-|
| [Blog zu Spielen für Windows und DirectX](https://walbourn.github.io/) | Regelmäßig aktualisierter Blog eines wichtigen DirectX-Entwicklers und eine hervorragende Ressource für DirectX-Entwickler. |
| [Windows DirectX-Entwicklerblog](https://devblogs.microsoft.com/directx/) | Der offizielle Windows DirectX-Blog. |
| [DirectX-Blog von Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Entwicklungsblog von einem anderen angesehenen Windows DirectX Dev Contributor. |
| [DirectX-Toolkit](https://directxtk.codeplex.com/) | CodePlex-Website für das DirectX Tool Kit (DxTK), die eine Reihe hilfreicher Unterstützungs-APIs zum Laden von Gittern, wiedergaben von Sounds und anderen gängigen Verhaltensweisen enthält. |
| [DirectXTex-Texturverarbeitungsbibliothek](https://directxtex.codeplex.com/) | Codeplex-Website für die DirectX Texture Processing Library (DxTEX), die Unterstützungs-APIs für Texturverarbeitung und Komprimierung/Dekomprimierung enthält. |