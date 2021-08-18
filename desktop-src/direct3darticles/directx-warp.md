---
title: Windows Advanced Rasterization Platform (WARP) Guide
description: In diesem Artikel werden Windows Advanced Rasterization Platform (WARP) und die folgenden Aspekte von WARP beschrieben.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab76fd68985069e6114cd7bbb0901eeba5d911eba574332b1dd2008f0375a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745990"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Windows Advanced Rasterization Platform (WARP) Guide

In diesem Artikel werden Windows Advanced Rasterization Platform (WARP) und die folgenden Aspekte von WARP beschrieben.

-   [Was ist WARP?](#what-is-warp)
-   [WARP-Vorteile](#warp-benefits)
    -   [Entfernen der Notwendigkeit benutzerdefinierter Softwareraster](#removing-the-need-for-custom-software-rasterizers)
    -   [Aktivieren der maximalen Leistung von Grafikhardware](#enabling-maximum-performance-from-graphics-hardware)
    -   [Aktivieren des Renderings, wenn Direct3D-Hardware nicht verfügbar ist](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Nutzen vorhandener Ressourcen für softwarerendering](#leveraging-existing-resources-for-software-rendering)
    -   [Aktivieren von Szenarien, die keine Grafikhardware erfordern](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Abschließen der DirectX-Grafikplattform](#completing-the-directx-graphics-platform)
-   [WARP-Funktionen und -Anforderungen](#warp-capabilities-and-requirements)
-   [Verwenden von WARP](#how-to-use-warp)
-   [Empfohlene Anwendungstypen für WARP](#recommended-application-types-for-warp)
    -   [Lockere Spiele](#casual-games)
    -   [Vorhandene Nicht-Gaming-Anwendungen](#existing-non-gaming-applications)
    -   [Erweiterte Rendering-Spiele](#advanced-rendering-games)
    -   [Andere Anwendungen](#other-applications)
-   [WARP-Architektur und -Leistung](#warp-architecture-and-performance)
-   [WARP-Konformität](#warp-conformance)

## <a name="what-is-warp"></a>Was ist WARP?

WARP ist ein hochschneller, vollständig konformer Softwareraster. Es ist eine Komponente der DirectX-Grafiktechnologie, die von der Direct3D 11-Runtime eingeführt wurde. Die Direct3D 11-Runtime wird auf Windows 7, Windows Server 2008 R2 und Windows Vista mit dem \[ Update KB971644 \] installiert. Windows 8, Windows 10, Windows Server 2012 & und Windows RT enthalten die Direct3D 11.1-Runtime, die über eine aktualisierte Version von WARP verfügt. Windows 10 Fall Creators Update (1709) enthält eine Version von WARP, die sowohl Direct3D 11- als auch Direct3D 12-Runtimes unterstützt.

## <a name="warp-benefits"></a>WARP-Vorteile

WARP bietet die folgenden Vorteile:

-   [Entfernen der Notwendigkeit benutzerdefinierter Softwareraster](#removing-the-need-for-custom-software-rasterizers)
-   [Aktivieren der maximalen Leistung von Grafikhardware](#enabling-maximum-performance-from-graphics-hardware)
-   [Aktivieren des Renderings, wenn Direct3D-Hardware nicht verfügbar ist](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Nutzen vorhandener Ressourcen für softwarerendering](#leveraging-existing-resources-for-software-rendering)
-   [Aktivieren von Szenarien, die keine Grafikhardware erfordern](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Abschließen der DirectX-Grafikplattform](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Entfernen der Notwendigkeit benutzerdefinierter Softwareraster

WARP vereinfacht die Entwicklung, indem es nicht mehr erforderlich ist, einen benutzerdefinierten Softwareraster zu erstellen und Ihre Anwendung dafür zu optimieren, anstatt Ihre Anwendung auf Hardware zu optimieren. Durch die Bereitstellung eines einzelnen, allgemeinen Softwarerasters müssen Sie keine Bildrenderingalgorithmen mehr auf mehrere Arten schreiben, um auf Hardware oder Software mit unterschiedlichen Features und Funktionen ausgeführt zu werden. Sie können Algorithmen weiterhin auf mehrere Arten implementieren, um eine bessere Leistung oder Skalierung zu erzielen. Sie müssen jedoch nicht die API oder Renderingarchitektur ändern, die zum Implementieren dieser Algorithmen verwendet wird. Stattdessen können Sie sich auf die Erstellung einer großartigen Direct3D 10- oder höher-Anwendung konzentrieren, die auf Hardware oder Software gleich ausschaut und eine gute Leistung bietet.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Aktivieren der maximalen Leistung von Grafikhardware

Wenn eine Anwendung für die effiziente Ausführung auf Hardware optimiert ist, wird sie auch effizient auf WARP ausgeführt. Das Gegenteil trifft auch zu. Jede Anwendung, die für die Ausführung unter WARP optimiert ist, funktioniert gut auf Hardware. Anwendungen, die Direct3D 10 und höher ineffizient verwenden, können auf unterschiedlicher Hardware möglicherweise nicht effizient skaliert werden. WARP verfügt über ähnliche Leistungsprofile wie Hardware, sodass das Optimieren einer Anwendung für große Batches, das Minimieren von Zustandsänderungen, das Entfernen von Synchronisierungspunkten oder Sperren sowohl von Hardware als auch von WARP profitiert.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Aktivieren des Renderings, wenn Direct3D-Hardware nicht verfügbar ist

WARP ermöglicht schnelles Rendering in einer Vielzahl von Situationen, in denen Hardwareimplementierungen nicht erwünscht oder nicht verfügbar sind, einschließlich:

-   Wenn der Benutzer keine Direct3D-fähige Hardware hat
-   Wenn eine Anwendung als Dienst oder in einer Serverumgebung ausgeführt wird
-   Wenn eine Anwendung die Direct3D-Hardwareressourcen für andere Zwecke reservieren möchte
-   Wenn keine Grafikkarte installiert ist
-   Wenn ein Videotreiber nicht verfügbar ist oder nicht ordnungsgemäß funktioniert
-   Wenn auf einer Grafikkarte nicht genügend Arbeitsspeicher verfügbar ist, hängt oder zu viele Systemressourcen für die Initialisierung verwendet werden.

### <a name="leveraging-existing-resources-for-software-rendering"></a>Nutzen vorhandener Ressourcen für softwarerendering

Es gibt eine große Community, viele Bücher, Websites, SDKs, Beispiele, Whitepaper, Adressenlisten und andere Ressourcen, die Ihnen helfen können, die Vorteile von Direct3D 10 und höher shader-basiertem Bildrendering zu nutzen. Mit WARP als Softwarefallback können Sie vorhandene Hardwarekenntnisse nutzen, um die Leistung Ihrer Anwendung zu verbessern, wenn sie mit Hardware oder Software ausgeführt wird. Darüber hinaus können viele hervorragende Tools von den Grafikkartenanbietern und im DirectX SDK Ihnen helfen, Leistungsprobleme von Grafikanwendungen zu entwerfen, zu erstellen, zu entwickeln, zu debuggen und zu analysieren. Diese Tools und Kenntnisse können jetzt von der Anwendungsentwicklung profitieren, die sowohl auf Hardware als auch auf Software zielt, wenn Sie WARP verwenden.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Aktivieren von Szenarien, die keine Grafikhardware erfordern

Verschiedene Algorithmen und Anwendungen (Bildverarbeitungsalgorithmen, Drucken, Remoting, virtuelle PCs und andere Emulatoren, hochwertiges Rendern von Schriftarten, Diagramme, Diagramme und so weiter) wurden in der Regel für die CPU optimiert, da sie nicht von Hardware abhängig sind. Mit WARP können Sie eine einzelne Architektur verwenden, in der diese Algorithmen und Anwendungen ausgeführt werden und die vollständig in Software ausgeführt werden kann. Wenn jedoch die Hardwarebeschleunigung verfügbar ist, können Sie sie nutzen.

### <a name="completing-the-directx-graphics-platform"></a>Abschließen der DirectX-Grafikplattform

WARP ermöglicht Ihnen den Zugriff auf alle Direct3D 10- und höher-Grafikfeatures auch auf Computern ohne Direct3D 10 und höher Grafikhardware. Direct3D 10 hat Funktionsbits (Obergrenzen) entfernt; Das heißt, Sie müssen nicht mehr überprüfen, ob Grafikfunktionen von Grafikhardware verfügbar sind, da Direct3D 10 und höher diese Verfügbarkeit garantiert. Sie können jetzt alle Features einer Vielzahl von Grafikkarten verwenden, da Sie wissen, dass sich ihre Anwendung überall gleich verhält und gleich ausschaut. Sie können die Leistung dieser Anwendungen skalieren, indem Sie einfach teure Grafikfeatures auf Low-End-Grafikkarten deaktivieren oder auf kleinere Ziele rendern.

## <a name="warp-capabilities-and-requirements"></a>WARP-Funktionen und -Anforderungen

WARP unterstützt alle Direct3D 10- und 10.1-Features vollständig. WARP unterstützt beispielsweise die folgenden wichtigsten Features:

-   Alle Genauigkeitsanforderungen der Direct3D 10- und 10.1-Spezifikation
-   Direct3D 11 bei Verwendung mit den Featureebenen \_ 9 1, 9 \_ 2, 9 \_ 3, 10 0 und \_ 10 1 (weitere Informationen zu Featureebenen finden Sie unter \_ [**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)).
-   Alle optionalen Texturformate, z. B. Multisample-Renderziele und Sampling von float-Oberflächen
-   Antialiasing, hochwertiges Rendering bis zu 8x Multisample Antialiasing (MSAA)
-   Anisotrope Filterung
-   32-Bit- und 64-Bit-Anwendungen und 32-Bit-Anwendungen mit großen Adressen

Wenn Sie das Plattformupdate für [Windows 7](https://support.microsoft.com/kb/2670838) unter Windows 7 SP1 oder Windows Server 2008 R2 SP1 installieren, enthält dieses Betriebssystem dann die Direct3D 11.1-Runtime und eine WarP-Version, die Direct3D 11.x unterstützt, wenn sie mit den Featureebenen [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 1 und \_ 11 \_ 0 verwendet wird.

Windows 8, Windows 10, Windows Server 2012 & und Windows RT die Direct3D 11.1-Runtime und eine neue Version von WARP enthalten. Diese Version unterstützt Direct3D 11.x bei Verwendung mit den Featureebenen [9](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 0 und \_ 11 \_ 1.

Windows 10 Fall Creators Update (1709) enthält eine neue Version von WARP, die [die Direct3D 12-Featureebenen](../direct3d12/direct3d-12-graphics.md) 12 0 und \_ 12 \_ 1 unterstützt. 

Die mindesten Computeranforderungen für WARP sind identisch mit für Windows Vista, insbesondere:

-   CPU mit mindestens 800 MHz
-   MMX, SSE oder SSE2 ist nicht erforderlich.
-   Mindestens 512 MB RAM

## <a name="how-to-use-warp"></a>Verwenden von WARP

Direct3D 10-, 10.1-, 11- und 12-Komponenten können einen zusätzlichen Treibertyp verwenden, den Sie beim Erstellen des Geräts angeben können (z. B. wenn Sie die [**D3D11CreateDevice-Funktion**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) aufrufen). Dieser Treibertyp ist [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) oder [**D3D \_ DRIVER TYPE \_ \_ WARP.**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) Wenn Sie diesen Treibertyp angeben, erstellt die Runtime ein WARP-Gerät und initialisiert kein Hardwaregerät.

Da WARP dieselbe Softwareschnittstelle für Direct3D verwendet wie der Referenzraster, kann jede Direct3D-Anwendung, die die Ausführung mit dem Referenzraster unterstützen kann, mit WARP getestet werden. Um WARP zu verwenden, benennen Sie D3d10warp.dll in D3d10ref.dll um, und platzieren Sie es im gleichen Ordner wie das Beispiel oder die Anwendung. Wenn Sie als Nächstes zu ref wechseln, sehen Sie WARP-Rendering.

Wenn Sie WARP in D3d10ref.dll umbenennen und in C: Programme \\ (x86) \\ Microsoft DirectX SDK (Juni 2010) \\ Samples \\ C++ \\ Direct3D \\ Bin \\ x86 platzieren, können Sie alle DirectX-Beispiele für WARP ausführen, indem Sie entweder auf die Schaltfläche "Ref umschalten" im Beispiel klicken oder das Beispiel mit /ref in der Befehlszeile ausführen.

## <a name="recommended-application-types-for-warp"></a>Empfohlene Anwendungstypen für WARP

Alle Anwendungen, die Direct3D verwenden können, können WARP verwenden. Dies schließt die folgenden Anwendungstypen ein:

-   [Lockere Spiele](#casual-games)
-   [Vorhandene Nicht-Gaming-Anwendungen](#existing-non-gaming-applications)
-   [Erweiterte Rendering-Spiele](#advanced-rendering-games)
-   [Andere Anwendungen](#other-applications)

### <a name="casual-games"></a>Lockere Spiele

Spiele haben in der Regel einfache Renderinganforderungen. Sie erfordern jedoch auch die Verwendung beeindruckender visueller Effekte, die möglicherweise eine Hardwarebeschleunigung erfordern. Der Großteil der am besten verkauften Spieltitel für Windows sind Entweder-Simulationen oder lässige Spiele, von denen keines Hochleistungsgrafiken erfordert. Beide Spielestile profitieren jedoch in großem Umfang von modernen Shader-basierten Grafiken und der Möglichkeit, auf Hardware zu skalieren.

### <a name="existing-non-gaming-applications"></a>Vorhandene Nicht-Gaming-Anwendungen

Eine große Anzahl von grafischen Anwendungen erfordert eine minimale Anzahl von Codepfaden in ihrer Renderingebene. WARP ermöglicht es diesen Anwendungen, einen einzelnen Direct3D-Codepfad zu implementieren, der auf eine große Anzahl von Computerkonfigurationen zielen kann.

### <a name="advanced-rendering-games"></a>Erweiterte Rendering-Spiele

Spieleentwickler möchten möglicherweise Grafikkarten- oder treiberspezifische Renderingfehler isolieren. Daher können alle Spiele, selbst äußerst grafisch anspruchsvolle Spiele, davon profitieren, dass sie ihre Inhalte mit warp rendern können. Sie können WARP verwenden, um zu überprüfen, ob visuelle Artefakte, die Sie finden, Renderingfehler oder Probleme mit Hardware oder Treibern sind.

### <a name="other-applications"></a>Andere Anwendungen

Die Zielanwendungen für WARP enthalten auch anwendungen, die derzeit direct3D 10 oder Direct3D 10.1 möglicherweise nicht verwenden. Diese Zielanwendungen umfassen Anwendungen, die immer auf allen Computern funktionieren müssen, Bildverarbeitungsanwendungen, die keine CPU- und GPU-Versionen von Bildverarbeitungsalgorithmen schreiben, Bildverarbeitungsalgorithmen, bei denen geschwindigkeits- oder nutzungskritische GPU nicht wichtig ist, z. B. Drucken, sowie Emulatoren und virtuelle Umgebungen, die erweiterte 3D-Grafiken anzeigen.

## <a name="warp-architecture-and-performance"></a>WARP-Architektur und -Leistung

WARP basiert auf der Referenz-Rasterizer-Codebasis. Daher verwendet WARP die gleiche Softwareschnittstelle für Direct3D 10 und höher und DXGI. WARP ist in Windows 7 im D3d10warp.dll in Windows Systemordnern enthalten. Zwei Versionen von WARP sind auf 64-Bit-Computern installiert, eine x86- und x64-Version. Die x64-Version kann unter bestimmten Umständen schneller ausgeführt werden, da der in WARP enthaltene Codegenerator die zusätzlichen Register nutzen kann, die verfügbar sind, wenn Benutzer 64-Bit-Anwendungen ausführen.

WARP enthält die beiden folgenden Echtzeitcompiler mit hoher Geschwindigkeit:

-   Der High-Level Intermediate Language Compiler, der HLSL-Bytecode und den aktuellen Renderzustand in einen optimierten Stream von Vektorbefehlen für die Phasen Geometry Shader (GS), Vertex-Shader (VS) und Pixel-Shader (PS) der Pipeline konvertiert.
-   Der leistungsstarke Just-in-Time-Codegenerator, der diese Befehle verwenden und optimierten SSE2-, SSE4.1-, x86-, x64-, arm- und arm64-Assemblycode generieren kann.

WARP verwendet den Threadpool und die komplexe Aufgabenverwaltung und Abhängigkeitsnachverfolgung, die in Windows Vista eingeführt wurde, um eine effiziente Verteilung aller Teile der Renderingpipeline auf verfügbare CPU-Kerne zu ermöglichen.

WARP verwendet verzögertes Rendering. Das heißt, WARP kann Renderingbefehle in Batches ausführen, sodass die Rasterung nur erfolgt, wenn genügend Daten verfügbar sind, um alle CPU-Ressourcen effizient zu nutzen. Die Arbeit am Hauptanwendungsthread wird minimiert, damit die Anwendung Befehle so schnell wie möglich übermitteln kann. Wenn eine Anwendung auch multithreaded ist und den Threadpool verwendet, wird die Arbeit gleichmäßig zwischen WARP und der Anwendung verteilt.

Der WARP-Codegenerator wurde optimiert, um die moderne CPU-Architektur optimal zu nutzen. WARP wird auf allen Computern ausgeführt, auf denen Windows Vista und höher ausgeführt werden kann, auch wenn der Computer SSE nicht unterstützt. WARP wurde jedoch für Computer optimiert, die SSE2 unterstützen. Außerdem enthält es Optimierungen für bestimmte Architekturen von AMD- und Intel-Prozessoren sowie Unterstützung für die SSE 4.1-Erweiterungen.

Für WARP muss keine Grafikhardware ausgeführt werden. Sie kann auch in Situationen ausgeführt werden, in denen Hardware nicht verfügbar ist oder nicht initialisiert werden kann.

Anwendungen und Beispiele, die für die Ausführung auf Direct3D 10- und höher-Hardware entwickelt und erstellt wurden, ohne dass Sie mit WARP kenntnissen, werden wahrscheinlich mit WARP gut ausgeführt. Es wird jedoch empfohlen, die Qualitätseinstellungen und die Auflösung so weit wie möglich zu senken, um nutzbare Frameraten zu erzielen. Sie können WARP verwenden, um Anwendungen zu entwickeln und zu optimieren, die sowohl auf Hardware als auch auf Software gut ausgeführt werden.

Da WARP mehrere CPU-Kerne verwendet, ist die Leistung bei modernen CPUs mit vier Kernen am besten. WARP wird auch deutlich schneller auf Computern ausgeführt, auf denen SSE4.1-Erweiterungen installiert sind. Microsoft hat erhebliche Tests und Leistungsoptimierungen auf Computern mit acht oder mehr Kernen und SSE4.1 durchgeführt, da diese High-End-Computer während der Lebensdauer von betriebssystemen Windows 7 und höher häufiger werden.

Wenn WARP auf der CPU ausgeführt wird, ist es im Vergleich zu einer Grafikkarte auf verschiedene Arten beschränkt. Die Front-Side-Busgeschwindigkeit einer CPU liegt in der Regel bei oder unter 10 GB/s. Im Gegensatz dazu verfügt eine Grafikkarte häufig über dedizierten Arbeitsspeicher, der 20 bis 100 GB/s oder mehr Grafikbandbreite verwendet. Grafikhardware verfügt auch über Festfunktionseinheiten, die komplexe und teure Aufgaben wie Texturfilterung, Formatdekomprimierung oder Konvertierungen asynchron mit geringem Mehraufwand oder Stromkosten ausführen können. Das Ausführen dieser Vorgänge auf einer typischen CPU ist in Bezug auf den Energieverbrauch und die Leistungszyklen teuer.

Die typischen Leistungsnummern für einen Intel Penryn-basierten 3,0-GHz-Quad-Core-Computer zeigen, dass WARP in einigen Fällen in einer Reihe von Benchmarks die integrierten Direct3D 10- und höher-Grafik-GPUs übertrifft. Diskrete Low-End-Grafikhardware ist bei der Ausführung dieser Benchmarks in der Regel vier- bis fünfmal schneller als WARP. Diese integrierten oder diskreten LOW-End-GPUs verwenden nur minimale CPU-Ressourcen. Mid-Range- oder High-End-Grafikkarten sind für viele Anwendungen deutlich schneller als WARP, insbesondere wenn eine Anwendung die Parallelität und Arbeitsspeicherbandbreite nutzen kann, die diese Grafikkarten bereitstellen.

WARP ist kein Ersatz für Grafikhardware, insbesondere da eine angemessene Leistung von Low-End-Direct3D 10 und höher diskreter Hardware jetzt kostengünstig ist. Das Ziel von WARP ist es, Anwendungen zu ermöglichen, Direct3D 10-Hardware als Ziel zu verwenden, ohne dass sie erheblich unterschiedliche Codepfade oder Testanforderungen haben, unabhängig davon, ob sie auf Hardware oder in Software ausgeführt werden.

Die folgenden beiden Tabellen zeigen WARP-Beispieldaten mit verschiedenen CPUs und Grafikkarten.

Die erste Tabelle enthält WARP-Beispieldaten mit Direct3D 10-10-10-10-10-1000-Dateien mit allen Qualitätseinstellungen auf den niedrigsten Ebenen:

| CPU                         | Time   | Ave FPS | Min. FPS | Min. Frame | Max. FPS | Max. Frame |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Core mit 3,0 GHz     | 271.57 | 7.36    | 3,46    | 1966      | 15,01   | 995       |
| Penryn 4 Core mit 3,0 GHz      | 351.35 | 5,69    | 2.49    | 1967      | 10.95   | 980       |
| Penryn 2 Core mit 3,0 GHz      | 573.98 | 3.48    | 1,35    | 1964      | 6.61    | 988       |
| Core 2 Duo mit 2,6 GHz         | 707.19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo mit 2,4 GHz         | 763.25 | 2.62    | 0,76    | 1964      | 4.70    | 984       |
| Core 2 Duo mit 2,1 GHz         | 908.87 | 2,20    | 0.64    | 1965      | 3.72    | 986       |
| Xeon 8 Core mit 2,0 GHz        | 424.04 | 4.72    | 1,84    | 1967      | 9.56    | 988       |
| AMD FX74 4 Core mit 3,0 GHz    | 583.12 | 3.43    | 1,41    | 1967      | 5.78    | 986       |
| Phenom 9550 4 Core mit 2,2 GHz | 664.69 | 3,01    | 0.53    | 1959      | 5.46    | 987       |

Die zweite Tabelle zeigt Beispieldaten, die den gleichen Test auf einer Vielzahl von Grafikkarten ausführen:

| Grafikkarte         | Time   | Ave FPS | Min. FPS | Min. Frame | Max. FPS | Max. Frame |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23.58  | 84.80   | 60.78   | 1957      | 130.83  | 1022      |
| NVIDIA 8500 GT        | 47.63  | 41.99   | 25.67   | 1986      | 72.57   | 991       |
| NVIDIA Quadro 290     | 67.16  | 29.78   | 18.19   | 1969      | 49.87   | 1017      |
| NVIDIA 8400 GS        | 59.01  | 33.89   | 21.22   | 1962      | 51.82   | 1021      |
| ATI 3400              | 53.79  | 37.18   | 22.97   | 618       | 59.77   | 1021      |
| ATI 3200              | 67.19  | 29.77   | 18.91   | 1963      | 45.74   | 980       |
| ATI 2400 PRO          | 67.04  | 29.83   | 17.97   | 606       | 45.91   | 987       |
| Intel DX10 Integrated | 386.94 | 5.17    | 1,74    | 1974      | 16.22   | 995       |

## <a name="warp-conformance"></a>WARP-Konformität

WARP besteht alle Standardmäßigtests Windows Hardware Quality Labs (WHQL) zur Überprüfung von Direct3D-Hardwaregeräten.

WARP wurde für eine Suite von Direct3D 10- und Direct3D 10.1-Anwendungen und -Benchmarks sowie für SDK-Beispiele von DirectX, NVIDIA und AMD getestet.

WARP hat das [PIX-Debug-](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) und Analysetool für Windows beim Testen verwendet. Microsoft verfügt über eine große Bibliothek mit Singleframe-Erfassungen von Anwendungen, die zum Vergleichen zwischen Hardware und WARP verwendet werden. Die meisten Images werden zwischen Hardware und WARP nahezu identisch angezeigt. wenn manchmal kleine Unterschiede auftreten, befinden sie sich innerhalb der Toleranzen, die durch die Direct3D 10-Spezifikation definiert werden.