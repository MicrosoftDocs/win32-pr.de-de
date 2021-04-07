---
title: High Fidelity-Grafiken mit DirectX
description: Windows-Anwendungsentwickler haben seit langem Microsoft DirectX verwendet, um hochwertige hardwarebeschleunigte 3D-Grafiken bereitzustellen.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda45f911293b9d31b9ae28d89c25ed93ce33696
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729857"
---
# <a name="high-fidelity-graphics-with-directx"></a>High Fidelity-Grafiken mit DirectX

Windows-Anwendungsentwickler haben seit langem Microsoft DirectX verwendet, um hochwertige hardwarebeschleunigte 3D-Grafiken bereitzustellen. Als die Technologie in 1995 debütierte, konnten Entwickler qualitativ hochwertige 3D-Grafiken für Spiele und Engineering-Anwendungen bereitstellen, die für Spieler und Fachkräfte bereit sind, die für ein 3D-Grafikboard extra bezahlen können. Die kostengünstigsten PCs enthalten jetzt auch eine leistungsfähige Hardware für 3D-Grafiken.

Um diese Grafikfunktionen nutzen zu können, wurde in Windows Vista die Windows Display Driver Model (WDDM)-Infrastruktur für DirectX eingeführt, die es mehreren Anwendungen und Diensten ermöglichte, die Ressourcen der Grafikverarbeitungseinheit (GPU) gemeinsam zu nutzen. Der Desktopfenster-Manager (DWM) verwendet diese Technologie zum Animieren des Aufgaben Wechsels in 3D, zum Bereitstellen dynamischer Miniaturbilder von Anwendungs Fenstern und zum Bereitstellen von Windows Aero-Glas Effekten für Desktop Anwendungen.

Windows 7 stellt den Anwendungsentwicklern noch mehr Grafikfunktionen zur Hand. Durch einen neuen Satz von directxapis können Microsoft Win32-Entwickler die neuesten Innovationen von GPUs nutzen, um Ihren Anwendungen schnelle, skalierbare, hochwertige 2D-und 3D-Grafiken, Text und Bilder hinzuzufügen. Auf den neuesten *LCD-* anzeigen können von directxapis Desktop-und Fenster Inhalte mit einer Farbtiefe von mehr als 8 Bits pro Farbkomponente angezeigt werden.

Mit DirectX können Win32-Entwickler auch die Parallelität von GPU für die allgemeine Berechnung verwenden, wie z. b. die Bildverarbeitung, und Sie können in DirectX 10-Hardware, DirectX 9-Hardware, CPU oder auf einem Windows-Remote Computer gerenden werden. Diese Technologien wurden entwickelt, um mit Windows Graphics Device Interface (GDI) und Windows GDI+ zusammenzuarbeiten, um sicherzustellen, dass Entwickler ihre vorhandenen Investitionen in Win32-Code problemlos erhalten können. (Weitere Informationen finden Sie [unter Neuigkeiten im DirectX SDK vom März 2009](/previous-versions//bb173043(v=vs.85)).)

Diese erweiterten Grafikfunktionen werden von den folgenden *com*-basierten APIs bereitgestellt:

-   [Direct2D](../direct2d/direct2d-portal.md) zum Zeichnen von 2D-Grafiken.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) zum Anordnen und Rendern von Text.
-   [Windows-Abbild](/windows/desktop/wic/-wic-lh) Erstellungs Komponente zum Verarbeiten und Anzeigen von Bildern.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) für das Zeichnen von 3D-Grafiken.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) zum Zeichnen von 3D-Grafiken und zum Bereitstellen des Zugriffs auf GPU-Technologien der nächsten Generation, z. b. Mosaik, eingeschränkte Unterstützung für Textur Streaming und allgemeines Computing.
-   [DirectX Graphics Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) zum Verwalten von lokalen und Remote Anzeigegeräten und GPU-Ressourcen und zur Bereitstellung von Interoperabilität zwischen DirectX und GDI.

## <a name="direct2d"></a>Direct2D

[Direct2D](../direct2d/direct2d-portal.md) ist auf Microsoft Direct3D 10 aufgebaut und bietet Win32-Entwicklern eine sofortige, auflösungsunabhängige, 2D-APIs, die die Leistungsfähigkeit der Next-Generation-Grafikhardware nutzen, aber gut mit den aktuellen GDI/GDI+-Anwendungen und Direct3D 10-Anwendungen interagieren. Direct2D bietet ein qualitativ hochwertiges 2D-Rendering mit der Leistung GDI und GDI+. Sie ermöglicht Win32-Entwicklern eine präzisere Kontrolle über Ressourcen und deren Verwaltung. (Siehe [Direct2D](../direct2d/direct2d-portal.md).)

## <a name="directwrite"></a>DirectWrite

Viele der heutigen Anwendungen müssen ein qualitativ hochwertiges Text Rendering, auflösungsunabhängige Gliederungs Schriftarten und vollständige Unterstützung für Unicode-Text und-Layouts unterstützen. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), eine neue DirectX-Komponente, bietet diese Features und mehr:

-   Ein Geräte unabhängiges textlayoutsystem zur Verbesserung der Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche.
-   Hochwertiges, unter Pixel-, *ClearType* -Text Rendering, das GDI, [Direct2D](../direct2d/direct2d-portal.md)oder anwendungsspezifische renderingtechnologie verwenden kann.
-   Hardware beschleunigter Text, bei Verwendung mit [Direct2D](../direct2d/direct2d-portal.md).
-   Unterstützung für mehr formatieren Text.
-   Unterstützung für die erweiterten Typografiefunktionen von *OpenType* -Schriftarten.
-   Unterstützung für Layout und Rendering von Text in allen unterstützten Sprachen.
-   GDI-kompatibles Layout und Rendering.

Das Schriftart System " [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) " aktiviert die Schriftart "beliebige Schriftart überall", in der Benutzer keinen separaten Installationsschritt ausführen müssen, um eine Schriftart zu verwenden, und eine verbesserte strukturelle Hierarchie der Schriftart Gruppierung, um die manuelle oder programmgesteuerte Schriftart Ermittlung zu unterstützen. Die APIs unterstützen das Messen, zeichnen und Treffer Tests von Text mit mehreren Formaten. DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen, die auf der Schlüssel sprach Infrastruktur von Windows 7 aufbauen. DirectWrite bietet auch auf Low-Level-Glyphe-renderingapis für Entwickler, die ihre eigene Layout-und Unicode-zu-Glyphe-Verarbeitung durchführen möchten. (Weitere Informationen finden Sie unter [DirectWrite](../directwrite/direct-write-portal.md).)

## <a name="windows-imaging-component"></a>Windows-Bilderstellungskomponente

In Windows Vista wurde von der [Windows-Abbild](/windows/desktop/wic/-wic-lh) Erstellungs Komponente ein erweiterbares Framework zum Arbeiten mit Bildern und Bild Metadaten eingeführt. Zu den von der Windows Imaging-Komponente unterstützten Bildformaten gehören *JPEG*, *PNG* und *TIFF*, und die unterstützten Metadatenformate sind *XMP* und *EXIF*. Mit Windows 7 wird die Einhaltung von Standards von der Windows-Abbild Komponente erweitert, indem die Unterstützung für die progressive Bild Decodierung, erweiterte *PNG* -Features, *GIF* -Metadaten und Metadaten, die sich auf *APPN* -Segmente (Weitere Informationen finden Sie [unter What es New for WIC in Windows 7](/previous-versions//ee720061(v=vs.85)).)

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 erweitert die Funktionalität der Direct3D 10-Pipeline und bietet Windows 7-spielen und High-End-3D-Anwendungen einen effizienten, stabilen, skalierbaren Zugriff auf die bevorstehende Generierung von GPUs und Multi-Core-CPUs. Zusätzlich zu den in Direct3D 10 gefundenen Funktionen führt Direct3D 11 mehrere neue Features ein.

Geometrie-und hochwertige Oberflächen können nun im Mosaik Prozess unterstützt werden, um skalierbare, dynamische Inhalte in der Oberflächendarstellung von Patches und Unterteilungen zu unterstützen.

Um die von mehreren CPU-Kernen verfügbare parallele Verarbeitungsleistung optimal zu nutzen, erhöht Multithreading die Anzahl potenzieller renderingaufrufe pro Frame, indem die Anwendungs-, Lauf Zeit-und Treiber Aufrufe über mehrere Kerne verteilt werden. Außerdem wurde die Ressourcen Erstellung und-Verwaltung für die Multithread-Verwendung optimiert, sodass eine effizientere dynamische Textur Verwaltung für das Streaming ermöglicht wird.

Für Direct3D 11 wurden neue Compute-Shader für allgemeine Zwecke erstellt. Anders als vorhandene Shader sind dies Erweiterungen der programmierbaren Pipeline, mit denen Ihre Anwendung unabhängig von der CPU mehr Arbeit auf der GPU ausführen kann. [**Drawauto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), das in Direct3D 10 eingeführt wurde, wurde für die Interaktion mit einem Compute-Shader erweitert.

Es wurden mehrere Verbesserungen an der High-Level Schattierung Language ([HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)) vorgenommen, z. b. in einer begrenzten Form dynamischer Verknüpfungen in Shadern zur Verbesserung der Spezialisierungs Komplexität und objektorientierter Programmierkonstrukte wie Klassen und Schnittstellen. (Weitere Informationen finden Sie [unter Neuigkeiten im DirectX SDK vom März 2009](/previous-versions//bb173043(v=vs.85)).)

## <a name="direct3d-10-improvements"></a>Direct3D 10 Verbesserungen

Direct3D 10 enthält eine neu gestaltete Grafik Pipeline mit programmierbaren Shader-Stufen und unveränderlichen Zustands Objekten für die Initialisierung der Phasen mit fester Funktionsweise. Die Zustands Objekte vereinfachen die Pipeline und verbessern die Leistung, indem die Anzahl der erforderlichen Zustandsänderungen minimiert wird. Die Programmierbarkeit der Shader-Stufen bietet nun allgemeine Schattierungs Spracherweiterungen zur Unterstützung unbegrenzter shaderanweisungen, generalisierter Shaderressourcen sowie ganzzahlige und bitweise Berechnungen.

Die Pipeline führt außerdem die Geometrie-Shader-Stufe ein, die die Arbeit vollständig von der CPU auf die GPU verlagert. Diese neue Phase ermöglicht Ihnen das Erstellen von Geometrie, das Streamen der Daten in den Arbeitsspeicher und das Rendering der Geometrie ohne CPU-Interaktion.

Einige weitere Verbesserungen wurden speziell für eine schnellere Leistung entwickelt. Ein Prädikat Rendering führt die Okklusion aus, um die Menge der gerenderten Geometrie zu verringern. Instanziierungsapis können die Geometrie Menge, die an die GPU übertragen werden muss, drastisch reduzieren, indem Sie mehrere Instanzen ähnlicher Objekte zeichnen. Textur Arrays ermöglichen es der GPU, Textur Austausch Vorgänge ohne CPU-Eingriff durchzuführen.

Es wurden mehrere Ergänzungen an Direct3D 10 und Direct3D 11 vorgenommen, um den Umfang der Konfigurationen zu erweitern, die diese APIs als Ziel haben können. Die [Windows Advanced rasterization Platform (Warp)](/windows/desktop/direct3darticles/directx-warp) implementiert schnelles, skalierbares CPU-Rendering (Multi-Core) für Direct3D 10 und ermöglicht das Rendering von Grafiken auf Systemen ohne Grafikhardware. Durch das Hinzufügen neuer "featureebenen", die speziell [Direct3D 10 Level 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9)genannt werden, können die Direct3D 10-und Direct3D 11-APIs die Microsoft Direct3D 9-Klassen Hardware Steuern und so die Anzahl der Konfigurationen erweitern, die eine Direct3D 10-oder Direct3D 11-Anwendung auf fast alle Computersysteme auf dem Markt ausrichten kann. (Siehe [Direct3D 10 graphics](../direct3d10/d3d10-graphics.md).)

## <a name="directxgdi-interoperability"></a>DirectX/GDI-Interoperabilität

In Windows Vista unterscheidet sich das Verhalten einer Anwendung, die sowohl DirectX als auch GDI zum Renderingverhalten verwendet, in Abhängigkeit davon, ob DWM aktiviert oder deaktiviert ist. Wenn DWM aktiviert ist, Verhalten sich Anwendungen, die sowohl DirectX als auch GDI verwenden, unter Windows Vista anders als Windows XP. Dies hat dazu geführt, dass viele ISVs DWM beim Ausführen von Anwendungen unter Windows Vista deaktiviert haben, um ein konsistentes Verhalten sicherzustellen. Dank der Verbesserungen an DirectX in Windows 7 kann eine Anwendung DirectX und GDI nun frei mischen, ohne DWM zu deaktivieren. Windows 7 bietet auch eine verbesserte Leistung für Szenarien, die eine Interoperation zwischen DirectX und GDI erfordern, indem die effizienteren Direct3D 10-APIs genutzt werden. (Siehe [Übersicht über die Zusammenarbeit zwischen Direct2D und GDI](../direct2d/direct2d-and-gdi-interoperation-overview.md).)

 

 