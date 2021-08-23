---
title: High Fidelity-Grafiken mit DirectX
description: Windows Anwendungsentwickler haben Microsoft DirectX seit langem verwendet, um hochwertige, hardwarebeschleunigte 3D-Grafiken bereitzustellen.
ms.assetid: db555657-90b9-4db2-a0c2-bfaa526a8dd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9ecb5d6403745162f19b16eea15c22ef7f9676b14bd291226af2f8321483b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086643"
---
# <a name="high-fidelity-graphics-with-directx"></a>High Fidelity-Grafiken mit DirectX

Windows Anwendungsentwickler haben Microsoft DirectX seit langem verwendet, um hochwertige, hardwarebeschleunigte 3D-Grafiken bereitzustellen. Als die Technologie im Jahr 1995 entwickelt wurde, konnten Entwickler hochwertige 3D-Grafiken für Spiele und Entwicklungsanwendungen für Gamer und Experten bereitstellen, die bereit waren, zusätzliche Kosten für ein 3D-Grafikboard zu zahlen. Jetzt enthalten auch die kostengünstigsten PCs fähige 3D-Grafikhardware.

Um diese Grafikfunktionen nutzen zu können, hat Windows Vista die WDDM-Infrastruktur (Windows Display Driver Model) für DirectX eingeführt, die es mehreren Anwendungen und Diensten ermöglicht hat, die Ressourcen der Grafikverarbeitungseinheit (GRAPHICS Processing Unit, GPU) gemeinsam zu nutzen. Der Desktopfenster-Manager (DWM) verwendet diese Technologie, um Aufgabenwechsel in 3D zu animieren, dynamische Miniaturansichten von Anwendungsfenstern bereitzustellen und Windows Glass Effects für Desktopanwendungen bereitzustellen.

Windows 7 bietet Anwendungsentwicklern noch mehr Grafikfunktionen. Durch einen neuen Satz von DirectXAPIs können Microsoft Win32-Entwickler die neuesten Innovationen in GPUs nutzen, um ihren Anwendungen schnelle, skalierbare, hochwertige 2D- und 3D-Grafiken, Text und Bilder hinzuzufügen. Auf den neuesten *DISPLAYS können* DirectXAPIs Desktop- und Fensterinhalte mit einer Farbtiefe von mehr als 8 Bits pro Farbkomponente anzeigen.

Mit DirectX können Win32-Entwickler auch die Parallelität der GPU für allgemeine Berechnungen wie Bildverarbeitung verwenden und auf DirectX 10-Hardware, DirectX 9-Hardware, CPU oder auf einem Remotecomputer Windows rendern. Diese Technologien wurden für die Zusammenarbeit mit Windows Graphics Device Interface (GDI) und Windows GDI+ entwickelt, um sicherzustellen, dass Entwickler ihre vorhandenen Investitionen in Win32-Code problemlos aufrechterhalten können. (Weitere Informationen finden Sie [unter Neuerungen im DirectX SDK vom März 2009.)](/previous-versions//bb173043(v=vs.85))

Diese erweiterten Grafikfunktionen werden von den folgenden COM-basierten APIs bereitgestellt:

-   [Direct2D](../direct2d/direct2d-portal.md) zum Zeichnen von 2D-Grafiken.
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) zum Anordnen und Rendern von Text.
-   [Windows Imaging Component](/windows/desktop/wic/-wic-lh) für die Verarbeitung und Anzeige von Bildern.
-   [Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics) zum Zeichnen von 3D-Grafiken.
-   [Direct3D 11](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) zum Zeichnen von 3D-Grafiken und Bereitstellen des Zugriffs auf GPU-Technologien der nächsten Generation, z. B. Mosaik, eingeschränkte Unterstützung für Texturstreaming und allgemeines Computing.
-   [DirectX Graphic Infrastructure (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) zum Verwalten lokaler und Remoteanzeigegeräte und GPU-Ressourcen sowie zur Bereitstellung von Interoperabilität zwischen DirectX und GDI.

## <a name="direct2d"></a>Direct2D

[Direct2D](../direct2d/direct2d-portal.md) basiert auf Microsoft Direct3D 10 und bietet Win32-Entwicklern sofort modusunabhängige, auflösungsunabhängige 2D-APIs, die die Leistungsfähigkeit der Grafikhardware der nächsten Generation nutzen und dennoch gut mit den heutigen GDI-/GDI+- und Direct3D 10-Anwendungen zusammenarbeiten. Direct2D bietet hochwertiges 2D-Rendering mit einer Leistung, die GDI und GDI+ überlegen ist. Es bietet Win32-Entwicklern eine feineren Kontrolle über Ressourcen und ihre Verwaltung. (Siehe [Direct2D](../direct2d/direct2d-portal.md).)

## <a name="directwrite"></a>DirectWrite

Viele der heutigen Anwendungen müssen qualitativ hochwertiges Textrendering, auflösungsunabhängige Gliederungsschriftarten und vollständige Unicode-Text- und Layoutunterstützung unterstützen. [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), eine neue DirectX-Komponente, bietet diese Features und vieles mehr:

-   Ein geräteunabhängiges Textlayoutsystem, das die Lesbarkeit von Text in Dokumenten und in der Benutzeroberfläche verbessert.
-   Qualitativ *hochwertiges,* subpixeliges ClearType-Textrendering, das GDI, [Direct2D](../direct2d/direct2d-portal.md)oder anwendungsspezifische Renderingtechnologie verwenden kann.
-   Hardwarebeschleunigte Text, wenn er mit [Direct2D](../direct2d/direct2d-portal.md)verwendet wird.
-   Unterstützung für mehrformatigen Text.
-   Unterstützung für die erweiterten Typografiefeatures von *OpenType-Schriftarten.*
-   Unterstützung für das Layout und Rendering von Text in allen unterstützten Sprachen.
-   GDI-kompatibles Layout und Rendering.

Das [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) Schriftartsystem ermöglicht die Verwendung von Schriftarten "beliebiger Schriftart überall", bei der Benutzer keinen separaten Installationsschritt ausführen müssen, nur um eine Schriftart zu verwenden, und eine verbesserte strukturelle Hierarchie der Schriftartgruppierung zur Unterstützung der manuellen oder programmgesteuerten Schriftartermittlung. Die APIs unterstützen das Messen, Zeichnen und Treffertesten von mehrformatigem Text. DirectWrite verarbeitet Text in allen unterstützten Sprachen für globale und lokalisierte Anwendungen und baut auf der Schlüsselsprachinfrastruktur in Windows 7 auf. DirectWrite bietet auch Glyphenrendering-APIs auf niedriger Ebene für Entwickler, die ein eigenes Layout und unicode-to-glyph-Verarbeitung durchführen möchten. (Siehe [DirectWrite](../directwrite/direct-write-portal.md).)

## <a name="windows-imaging-component"></a>Windows-Bilderstellungskomponente

In Windows Vista wurde mit [der Windows Imaging Component](/windows/desktop/wic/-wic-lh) ein erweiterbares Framework für die Arbeit mit Bildern und Bildmetadaten eingeführt. Die von Windows Imaging Component unterstützten Bildformate umfassen *JPEG,* *PNG* und *TIFF,* und die unterstützten Metadatenformate umfassen *XMP* und *EXIF.* Mit Windows 7 erweitert Windows Imaging Component die Standardskonformität durch Unterstützung für die progressive Bilddecodierung, erweiterte *PNG-Features,* *GIF-Metadaten* und Metadaten, die *APPn-Segmente* umfassen. (Weitere Informationen finden Sie [unter What es New for WIC in Windows 7](/previous-versions//ee720061(v=vs.85)).)

## <a name="direct3d-11"></a>Direct3D 11

Microsoft Direct3D 11 erweitert die Funktionalität der Direct3D 10-Pipeline und bietet Windows 7 Spiele und High-End-3D-Anwendungen mit effizientem, stabilem und skalierbarem Zugriff auf die bevorstehende Generation von GPUs und CPUs mit mehreren Kernen. Zusätzlich zu den Funktionen in Direct3D 10 führt Direct3D 11 mehrere neue Features ein.

Geometrie und Oberflächen mit hoher Ordnung können jetzt mosaikiert werden, um skalierbare, dynamische Inhalte in Darstellungen von Patch- und Unterteilungsoberflächen zu unterstützen.

Um die parallele Verarbeitungsleistung mehrerer CPU-Kerne nutzen zu können, erhöht Multithreading die Anzahl potenzieller Renderingaufrufe pro Frame, indem die Anwendungs-, Laufzeit- und Treiberaufrufe auf mehrere Kerne verteilt werden. Darüber hinaus wurde die Ressourcenerstellung und -verwaltung für die Verwendung mit Multithread optimiert, wodurch eine effizientere dynamische Texturverwaltung für das Streaming ermöglicht wird.

Für Direct3D 11 wurden neue allgemeine Compute-Shader erstellt. Im Gegensatz zu vorhandenen Shadern sind dies Erweiterungen der programmierbaren Pipeline, die es Ihrer Anwendung ermöglichen, unabhängig von der CPU vollständig mehr Arbeit auf der GPU zu erledigen. [**DrawAuto**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto), das in Direct3D 10 eingeführt wurde, wurde für die Interaktion mit einem Compute-Shader erweitert.

Es wurden mehrere Verbesserungen an der Schattierungssprache auf hoher Ebene[(HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)vorgenommen, z. B. eine eingeschränkte Form der dynamischen Verknüpfung in Shadern zur Verbesserung der Spezialisierungskomplexität und objektorientierte Programmierkonstrukte wie Klassen und Schnittstellen. (Weitere Informationen finden Sie [unter Neuerungen im DirectX SDK vom März 2009.)](/previous-versions//bb173043(v=vs.85))

## <a name="direct3d-10-improvements"></a>Direct3D 10-Verbesserungen

Direct3D 10 enthält eine neu gestaltete Grafikpipeline mit programmierbaren Shaderstufen und unveränderlichen Zustandsobjekten zum Initialisieren der Stufen fester Funktionen. Die Zustandsobjekte vereinfachen die Pipeline und verbessern die Leistung, indem sie die Anzahl der erforderlichen Zustandsänderungen minimieren. Die Programmierbarkeit von Shaderstufen bietet jetzt allgemeine Schattierungsspracherweiterungen zur Unterstützung unbegrenzter Shaderanweisungen, generalisierter Shaderressourcen sowie ganzzahliger und bitweiser Berechnungen.

Die Pipeline führt auch die Geometry-Shaderphase ein, die die Arbeit vollständig von der CPU auf die GPU auslagert. Mit dieser neuen Phase können Sie Geometrie erstellen, die Daten in den Arbeitsspeicher streamen und die Geometrie ohne CPU-Interaktion rendern.

Mehrere weitere Verbesserungen wurden speziell für eine schnellere Leistung entwickelt. Prädikatrendering führt Okklusions-Culling aus, um die Menge der gerenderten Geometrie zu reduzieren. Instanziierungs-APIs können die Menge der Geometrie, die auf die GPU übertragen werden muss, erheblich reduzieren, indem mehrere Instanzen ähnlicher Objekte gezeichnet werden. Texturarrays ermöglichen der GPU den Texturaustausch ohne CPU-Eingriff.

Es wurden mehrere Ergänzungen zu Direct3D 10 und Direct3D 11 vorgenommen, um die Gamut der Konfigurationen zu erweitern, die mit diesen APIs als Ziel verwendet werden können. Die [Windows Advanced Rasterization Platform (WARP)](/windows/desktop/direct3darticles/directx-warp) implementiert schnelles skalierbares CPU-Rendering mit mehreren Kernen für Direct3D 10 und ermöglicht das Rendern von Grafiken mit vollem Funktionsumfang auf Systemen ohne Grafikhardware. Durch das Hinzufügen neuer "Featureebenen", insbesondere [Direct3D 10 Level 9](/windows/desktop/direct3d11/d3d11-graphics-reference-10level9)genannt, können direct3D 10 und Direct3D 11APIs Microsoft Direct3D 9-Klassenhardware antreiben, wodurch die Anzahl der Konfigurationen erweitert wird, die eine Direct3D 10- oder Direct3D 11-Anwendung auf fast jedes Computersystem auf dem Markt anwenden kann. (Siehe [Direct3D 10 Graphics](../direct3d10/d3d10-graphics.md).)

## <a name="directxgdi-interoperability"></a>DirectX/GDI-Interoperabilität

In Windows Vista unterscheidet sich das Verhalten einer Anwendung, die sowohl DirectX als auch GDI zum Rendern auf einer freigegebenen Oberfläche verwendet, je nachdem, ob DWM ein- oder ausgeschaltet ist. Wenn DWM aktiviert ist, verhalten sich Anwendungen, die sowohl DirectX als auch GDI verwenden, auf Windows Vista anders als auf Windows XP. Dies hat dazu geführt, dass viele ISVs DWM deaktivieren, wenn sie ihre Anwendungen auf Windows Vista ausführen, um ein konsistentes Verhalten sicherzustellen. Mit den Verbesserungen an DirectX in Windows 7 kann eine Anwendung jetzt DirectX und GDI frei mischen, ohne DWM zu deaktivieren. Windows 7 bietet auch verbesserte Leistung für Szenarien, die eine Interoperation zwischen DirectX und GDI erfordern, indem die effizienteren Direct3D 10-APIs verwendet werden. (Siehe [Direct2D und GDI Interoperation Overview](../direct2d/direct2d-and-gdi-interoperation-overview.md).)

 

 