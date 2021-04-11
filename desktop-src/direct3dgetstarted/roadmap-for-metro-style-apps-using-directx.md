---
title: Roadmap für DirectX-Desktop-Apps
description: Hier finden Sie wichtige Ressourcen, die Ihnen bei den ersten Schritten mit der Verwendung von DirectX und C++ zum entwickeln Grafik intensiver Desktop-Apps wie Spielen helfen.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104039885"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Roadmap für DirectX-Desktop-Apps

Hier finden Sie wichtige Ressourcen, die Ihnen bei den ersten Schritten mit der Verwendung von DirectX und C++ zum entwickeln Grafik intensiver Desktop-Apps, z. b. Spiele, helfen. Dabei handelt es sich nicht um eine umfassende Liste aller Features oder verfügbaren Ressourcen.

## <a name="get-started"></a>Erste Schritte

Im folgenden finden Sie einige wichtige Themen. Einrichten Ihres DirectX-Projekts, Einrichten von Windows und Beispielanwendungen.

| Thema | BESCHREIBUNG |
|-|-|
| [Erstellen Ihrer ersten Windows-App mit DirectX](building-your-first-directx-app.md) | Verwenden Sie dieses grundlegende Tutorial für den Einstieg in die Entwicklung von DirectX-apps |
| [Einstieg in DirectX für Windows](getting-started-with-a-directx-game.md) | Überprüfen Sie die Schritte, die Sie ausführen müssen, um mit der Entwicklung eines Spiels mit DirectX und C++ zu beginnen |
| [Vervollständigen von Code für ein DirectX-Framework](complete-code-sample-for-using-a-corewindow-with-directx.md) | Den Code für ein grundlegendes DirectX-Renderingframework zu erhalten. |
| [Verwendung von Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | In diesem Abschnitt wird veranschaulicht, wie die Microsoft Direct3D 11-API verwendet wird, um mehrere häufige Aufgaben auszuführen. |
| [Programmieranleitung für Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews) | Das-Programmier Handbuch enthält Informationen zur Verwendung der programmierbaren Microsoft Direct3D 11-Pipeline zum Erstellen von Echt Zeit 3D-Grafiken für Desktop Anwendungen. |
| [Tools für DirectX-Grafiken](/windows/desktop/direct3dtools/dx-graphics-tools) | Dokumentation für Tools, mit denen die DirectX-Entwicklung unterstützt wird. |
| [Neuerungen in Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Eine Aufschlüsselung aller Features, die in den neuesten Versionen von DirectX und Direct3D hinzugefügt wurden (zurzeit 11,2). |
| [Visual Studio 2013 herunterladen](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Sie müssen über Visual Studio Express 2013 für Windows Desktop verfügen, um Windows Store-Spiele erstellen zu können. Eine Tour durch Visual Studio finden Sie unter [entwickeln von Windows Store-Apps mit Visual Studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Informationen zu neuen Funktionen in Visual Studio finden Sie unter [Product Highlights for Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [Wo finde ich das DirectX SDK?](../directx-sdk--august-2009-.md) | Enthält Anleitungen für Entwickler, die Ihre DirectX-Projekte in Microsoft Visual Studio bringen möchten. |

## <a name="sample-applications"></a>Beispielanwendungen

| Thema | BESCHREIBUNG |
|-|-|
| [Direct3D Tutorial Win32-Beispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Basic Desktop Direct3D Tutorial-Beispiel. |
| [Beispiel für DirectX-Video Rendering](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Ein Beispiel, das benutzerdefiniertes Video Rendering mit Direct3D veranschaulicht. |

## <a name="review-key-direct3d-11-concepts"></a>Review Key Direct3D 11 Konzepte

| Thema | BESCHREIBUNG |
|-|-|
| [Grafik Pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Behandelt die grundlegende Direct3D 11-Grafik Pipeline. |
| [Darstellung](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Behandelt die Direct3D-Renderingmodelle,-Komponenten,-Shader und API-Aufrufe. |
| [Ressourcen](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Behandelt Direct3D "Resources" (z. b. Puffer und andere GPU-Ressourcentypen). |
| [Effekte](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Umfasst Direct3D-multishader-Instanziierung und-Auswirkungen.  |
| [Gewusst wie: Erstellen einer SwapChain](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Erstellen der Austausch Kette zum Zeichnen von Pixeln in einem Bereich des Bildschirms. |
| [Gewusst wie: Erstellen eines Geräts und eines unmittelbaren Kontexts](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | So erstellen Sie eine Direct3D-Geräte Abstraktion und einen unmittelbaren Kontext zum Zeichnen. |
| [Vorgehensweise: Erstellen eines Scheitelpunkt Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | So erstellen Sie eine einfache Liste von Mesh-Scheitel Punkten für die Verarbeitung durch die GPU. |
| [Vorgehensweise: Erstellen eines Index Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Erstellen eines Index Puffers, der es dem Vertexshader ermöglicht, die Reihenfolge der Scheitel Punkte in einem Mesh zu durchlaufen. |
| [Vorgehensweise: Erstellen eines konstanten Puffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Übergeben konstanter (einheitlicher) Daten zwischen der CPU und der GPU während des Renderings. |
| [Vorgehensweise: Erstellen einer Textur](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Erstellen einer Textur oder einer anderen Puffer Ressource, die von der GPU als Stichprobe erstellt werden kann. |
| [Gewusst wie: Initialisieren einer Textur aus einer Datei](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | So laden Sie eine Textur aus einer Datei und verarbeiten Sie für die Verwendung durch die Shader-Pipeline. |
| [Gewusst wie: Kompilieren eines Shaders](../direct3d11/how-to--compile-a-shader.md) | So kompilieren Sie einen Shader für die Verwendung in der Grafikanwendung |

## <a name="graphics-apis"></a>Grafik-APIs

| Thema | BESCHREIBUNG |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Dokumentation der Kern-APIs für die Virtualisierung der GPU und der zugehörigen Ressourcen sowie zum Zeichnen von Grafiken mithilfe eines Unified Shader-Modells. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Referenz Dokumentation für High-Level Shader-Sprache, die Syntax und die Regeln, die zum Definieren von shaderprogrammen verwendet werden, die als Teil der Grafik Pipeline in einem vereinheitlichten Shader-Modell ausgeführt werden. |
| [DirectX-Grafikschnittstelle (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Dokumentation der Low-Level-APIs, mit denen die GPU-Schnittstelle und die Systemressourcen abgerufen werden. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Dokumentation für die Direct2D-APIs, die das Zeichnen von 2D-primitiven unterstützen. In der Regel wird Direct2D für benutzerdefinierte Benutzeroberflächen, Bildverarbeitung und Batch Verarbeitung und einfache Spiele verwendet. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Dokumentation für die DirectWrite-APIs, die die benutzerdefinierte Schriftart Rendering und-Skalierung unterstützen. |
| [Windows Imaging-Komponente (WIC)](/windows/desktop/wic/-wic-api) | Dokumentation für die WIC-APIs, die zum Lesen und Verwalten von unterschiedlichen Bitmap-Bildformaten verwendet werden. |
| [DirectDraw-Oberflächen (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) für Texturen | Dokumentation für die DDS-APIs, die für die 2D-Textur Komprimierung und-Komprimierung in Verbindung mit den WIC-APIs verwendet werden. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Dokumentation für die directxmath-APIs, die Direct3D mit einer Reihe von Typen und Funktionen unterstützen, die für die 3D-Grafik Entwicklung in Echtzeit geeignet sind. (Ehemals xnamath.) |
| [DirectCompute](https://walbourn.github.io/) | Dokumentation für die DirectCompute-APIs, die für Compute-oder allgemeine Shader-Funktionen verwendet werden. |

## <a name="audio-media-and-input-apis"></a>Audio-, Medien-und Eingabe-APIs

| Thema | BESCHREIBUNG |
|-|-|
| [XAudio2-Programmieranleitung](/windows/desktop/xaudio2/programming-guide) | Der Knoten der obersten Ebene für die konzeptionelle Dokumentation der XAudio2-audioapi. |
| [XAudio2-Programmierreferenz](/windows/desktop/xaudio2/programming-reference) | Der Knoten der obersten Ebene für die XAudio2-audioapi-Referenz Dokumentation. |
| [Leitfaden für die xinput-Programmierung](/windows/desktop/xinput/programming-guide) | Der Knoten der obersten Ebene für die konzeptionelle Dokumentation der xinput-Controller-API. |
| [Xinput-Programmier Referenz](/windows/desktop/xinput/programming-reference) | Knoten der obersten Ebene für die Referenz Dokumentation zur xinput-Controller-API. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Der Knoten der obersten Ebene für die API für die Wiedergabe von Media Foundation (MF) (Audiodateien). In der Regel wird MF in spielen für die Wiedergabe von Soundgeräten verwendet, während XAudio2 für dynamisches Audiomaterial verwendet wird. |

## <a name="port-to-directx-11"></a>Port zu DirectX 11

| Thema | BESCHREIBUNG |
|-|-|
| [Migrieren zu Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Grundlegender Leitfaden zum Verschieben Ihrer DirectX 9-Codebasis in DirectX 11. |
| [Dual-Use-Codierungstechniken für Spiele](https://walbourn.github.io/) | Ausführlicher Blogbeitrag zum entwickeln für die featureebenen DirectX 9 \_ \* und DirectX 11 \_ \* in einer einzigen Anwendung. |
| [Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10)) | Leitfaden zum Implementieren von Schatten Zuordnungen unter DirectX-Funktionsebene 9 \_ \* . |

## <a name="work-with-c"></a>Arbeiten mit C++

Wenn Sie mit C++ auf Windows-Plattformen arbeiten, können die Dinge etwas anders aussehen. Hier finden Sie einige Hinweise zu Themen, die Ihnen helfen, den Unterschied zu beheben.

> [!NOTE]
> Einige dieser Themen sind vorhanden, um Sie bei der Verwaltung Ihrer C++/CX-Anwendung zu unterstützen. Es wird jedoch empfohlen, [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) für neue Anwendungen zu verwenden. C++/WinRT ist eine vollständig standardisierte, moderne C++17-Programmiersprache für Windows-Runtime-APIs (WinRT), die als headerdateibasierte Bibliothek implementiert ist und Ihnen einen erstklassigen Zugriff auf die moderne Windows-API bietet.

| Thema | BESCHREIBUNG |
|-|-|
| [**Visual C++-Sprachreferenz (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Auf hoher Ebene, die mit Inhalten verknüpft ist, die mit C++ verknüpft sind. |
| [**Kurzreferenz (Windows Runtime und Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabelle, die QuickInfo zu Visual C++ Komponenten Erweiterungen (C++/CX)-Operatoren und-Schlüsselwörtern bereitstellt. |
| [**Typsystem (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Referenz Inhalt für die Typen, die von C++ unterstützt werden/CX. |
| [**Namespaces (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Referenz Inhalte für die Namespaces, die C++-spezifische Typen enthalten, die in Windows Store-Apps verwendet werden können. |

| | |
|-|-|
| [Asynchrone Programmierung (DirectX und C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Erfahren Sie mehr über die asynchrone und Multithreadprogrammierung für DirectX-apps und Spiele. |
| [Asynchrone Programmierung in C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Beschreibt die grundlegenden Methoden zum Verwenden der Task-Klasse, um Windows-Runtime asynchrone Methoden zu verarbeiten. |
| [**Task-Klasse (Concurrency Runtime)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Referenz Dokumentation für die Task-Klasse. |
| [Aufgaben Parallelität (Concurrency Runtime)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Ausführliche Erörterung der Aufgaben Klasse und deren Verwendung. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Weitere nützliche Bibliotheken für Windows C++ programmieren

| | |
|-|-|
| [C++-Standard Vorlagen Bibliothek](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows-Runtime Typen sind bei Standard Vorlagen-Bibliothekstypen gut gegeben. Die meisten C++-Windows Store-Apps verwenden Standard Vorlagen Bibliothekssammlungen und-Algorithmen, außer an der ABI-Grenze. |
| [Parallel Patterns Library](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL stellt Algorithmen und Typen bereit, die die Aufgaben Parallelität und Daten Parallelität auf der CPU vereinfachen.  |
| [C++ Accelerated massive parallelism (C++ amp)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ amp bietet Zugriff auf die GPU für allgemeine Daten Parallelität auf Videokarten, die DirectX 11 unterstützen. |

## <a name="blogs-and-other-resources"></a>Blogs und andere Ressourcen

| Thema | BESCHREIBUNG |
|-|-|
| [Blog zu spielen für Windows und DirectX](https://walbourn.github.io/) | Regelmäßig aktualisierter Blog von einem wichtigen DirectX dev-Mitwirkenden und einer rundum nützlichen Ressource für DirectX-Entwickler. |
| [Windows DirectX-Entwickler Blog](https://devblogs.microsoft.com/directx/) | Der offizielle Windows DirectX-Blog. |
| [Der DirectX-Blog von Shawn hargreave](https://www.shawnhargreaves.com/blogindex.html)) | Dev-Blog von einem anderen gut anerkannten Windows DirectX dev-Mitwirkenden. |
| [DirectX-Toolkit](https://directxtk.codeplex.com/) | CodePlex-Website für das DirectX-Toolkit (dxtk), das eine Reihe hilfreicher Support-APIs für das Laden von Meshes, das Abspielen von Sounds und andere gängige Verhalten enthält. |
| [DirectXTex-Texturverarbeitungsbibliothek](https://directxtex.codeplex.com/) | Code Plex-Website für die DirectX-Textur Verarbeitungs Bibliothek (dxtex), die Unterstützung-APIs für die Textur Verarbeitung und Komprimierung/Dekomprimierung enthält. |