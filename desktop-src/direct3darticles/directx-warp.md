---
title: Leitfaden für die Windows Advanced rasterization Platform (Warp)
description: In diesem Artikel werden die Windows Advanced rasterization Platform (Warp) und die folgenden Aspekte von Warp beschrieben.
ms.assetid: C40A96EB-64AA-46EB-85A9-7C996ABC8BFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c09c29dd7b935542f0238cde0a71cbc97fce23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729241"
---
# <a name="windows-advanced-rasterization-platform-warp-guide"></a>Leitfaden für die Windows Advanced rasterization Platform (Warp)

In diesem Artikel werden die Windows Advanced rasterization Platform (Warp) und die folgenden Aspekte von Warp beschrieben.

-   [Was ist Warp?](#what-is-warp)
-   [Warp-Vorteile](#warp-benefits)
    -   [Entfernen von benutzerdefinierten Software rasterizern](#removing-the-need-for-custom-software-rasterizers)
    -   [Aktivieren der maximalen Leistung von Grafik Hardware](#enabling-maximum-performance-from-graphics-hardware)
    -   [Aktivieren von Rendering, wenn Direct3D-Hardware nicht verfügbar ist](#enabling-rendering-when-direct3d-hardware-is-not-available)
    -   [Nutzen vorhandener Ressourcen für das Software Rendering](#leveraging-existing-resources-for-software-rendering)
    -   [Aktivieren von Szenarios, für die keine Grafik Hardware erforderlich ist](#enabling-scenarios-that-do-not-require-graphics-hardware)
    -   [Abschließen der DirectX-Grafik Plattform](#completing-the-directx-graphics-platform)
-   [Warp-Funktionen und-Anforderungen](#warp-capabilities-and-requirements)
-   [Verwenden von Warp](#how-to-use-warp)
-   [Empfohlene Anwendungs Typen für Warp](#recommended-application-types-for-warp)
    -   [Ungezwungene Spiele](#casual-games)
    -   [Vorhandene nicht-Gaming-Anwendungen](#existing-non-gaming-applications)
    -   [Erweiterte renderingspiele](#advanced-rendering-games)
    -   [Andere Anwendungen](#other-applications)
-   [Warp-Architektur und-Leistung](#warp-architecture-and-performance)
-   [Warp-Konformität](#warp-conformance)

## <a name="what-is-warp"></a>Was ist Warp?

Warp ist ein hoch Geschwindigkeits, vollständig konformitäter Software Rasterizer. Dabei handelt es sich um eine Komponente der DirectX-Grafiktechnologie, die von der Direct3D 11-Laufzeit eingeführt wurde. Die Direct3D 11-Laufzeit wird auf Windows 7, Windows Server 2008 R2 und Windows Vista mit dem \[ KB971644- \] Update installiert. Windows 8, Windows 10, Windows Server 2012 & oben und Windows RT enthalten die Direct3D 11,1-Laufzeit, die eine aktualisierte Version von Warp enthält. Windows 10 Fall Creators Update (1709) enthält eine Version von Warp, die sowohl Direct3D 11-als auch Direct3D 12-Laufzeiten unterstützt.

## <a name="warp-benefits"></a>Warp-Vorteile

Warp bietet die folgenden Vorteile:

-   [Entfernen von benutzerdefinierten Software rasterizern](#removing-the-need-for-custom-software-rasterizers)
-   [Aktivieren der maximalen Leistung von Grafik Hardware](#enabling-maximum-performance-from-graphics-hardware)
-   [Aktivieren von Rendering, wenn Direct3D-Hardware nicht verfügbar ist](#enabling-rendering-when-direct3d-hardware-is-not-available)
-   [Nutzen vorhandener Ressourcen für das Software Rendering](#leveraging-existing-resources-for-software-rendering)
-   [Aktivieren von Szenarios, für die keine Grafik Hardware erforderlich ist](#enabling-scenarios-that-do-not-require-graphics-hardware)
-   [Abschließen der DirectX-Grafik Plattform](#completing-the-directx-graphics-platform)

### <a name="removing-the-need-for-custom-software-rasterizers"></a>Entfernen von benutzerdefinierten Software rasterizern

Warp vereinfacht die Entwicklung, da es nicht mehr notwendig ist, ein benutzerdefiniertes Software Raster zu erstellen und die Anwendung dafür zu optimieren, anstatt die Anwendung auf Hardware zu optimieren. Durch die Bereitstellung eines einzelnen, allgemeinen Software Rasterizers müssen Sie renderingalgorithmen nicht mehr auf verschiedene Weise schreiben, um auf Hardware oder Software mit unterschiedlichen Features und Funktionen auszuführen. Algorithmen können weiterhin auf verschiedene Weise implementiert werden, um eine bessere Leistung oder Skalierung zu erzielen. Es ist jedoch nicht erforderlich, die API oder die renderingarchitektur zu ändern, die zum Implementieren dieser Algorithmen verwendet wird. Stattdessen können Sie sich auf das Erstellen einer großartigen Direct3D 10-Anwendung konzentrieren, die auf dem gleichen Stand ist, und sich auf Hardware oder in der Software gut aneignen.

### <a name="enabling-maximum-performance-from-graphics-hardware"></a>Aktivieren der maximalen Leistung von Grafik Hardware

Wenn eine Anwendung für die effiziente Verwendung auf Hardware optimiert ist, wird Sie auch effizient auf der Warp ausgeführt. Der umgekehrte Wert ist ebenfalls true. jede Anwendung, die für die Ausführung in Warp optimiert ist, wird auf Hardware gut funktionieren. Anwendungen, die Direct3D 10 und höher verwenden, werden möglicherweise nicht effizient auf unterschiedlichen Hardware skaliert. Warp weist ähnliche Leistungsprofile für Hardware auf, sodass die Optimierung einer Anwendung für große Batches, das Minimieren von Zustandsänderungen, das Entfernen von Synchronisierungs Punkten oder Sperren sowohl für Hardware als auch für Warp vorteilhaft ist.

### <a name="enabling-rendering-when-direct3d-hardware-is-not-available"></a>Aktivieren von Rendering, wenn Direct3D-Hardware nicht verfügbar ist

Warp ermöglicht schnelles Rendering in einer Vielzahl von Situationen, in denen Hardware Implementierungen nicht erwünscht oder nicht verfügbar sind, darunter:

-   Wenn der Benutzer keine Direct3D-fähige Hardware hat
-   Wenn eine Anwendung als Dienst oder in einer Serverumgebung ausgeführt wird
-   Wenn eine Anwendung die Direct3D-Hardware Ressourcen für andere Verwendungszwecke reservieren möchte
-   Wenn eine Grafikkarte nicht installiert ist
-   Wenn ein Videotreiber nicht verfügbar ist oder nicht ordnungsgemäß funktioniert
-   Wenn eine Grafikkarte nicht über genügend Arbeitsspeicher verfügt, reagiert oder zu viele Systemressourcen für die Initialisierung benötigen

### <a name="leveraging-existing-resources-for-software-rendering"></a>Nutzen vorhandener Ressourcen für das Software Rendering

Es gibt eine riesige Community, viele Bücher, Websites, sdche, Beispiele, Whitepaper, Mailinglisten und weitere Ressourcen, mit denen Sie das auf Shader basierende Image Rendering von Direct3D 10 und höher nutzen können. Mithilfe von Warp als Software Fallback können Sie vorhandenes Wissen über Hardware verwenden, um die Leistung Ihrer Anwendung zu verbessern, wenn Sie mit Hardware oder Software ausgeführt wird. Darüber hinaus können viele hervorragende Tools von den Grafikkarten Anbietern und dem DirectX SDK Ihnen helfen, Leistungsprobleme von Grafikanwendungen zu entwerfen, zu entwickeln, zu entwickeln, zu Debuggen und zu analysieren. Diese Tools und Kenntnisse können nun von der Anwendungsentwicklung profitieren, die bei der Verwendung von Warp sowohl auf Hardware als auch auf Software abzielt.

### <a name="enabling-scenarios-that-do-not-require-graphics-hardware"></a>Aktivieren von Szenarios, für die keine Grafik Hardware erforderlich ist

Verschiedene Algorithmen und Anwendungen (Bildverarbeitungsalgorithmen, Druck, Remoting, virtuelle PCs und andere Emulatoren, qualitativ hochwertige Schriftart Rendering, Diagramme, Diagramme usw.) wurden in der Regel für die CPU optimiert, da Sie nicht von der Hardware abhängig sind. Mit Warp können Sie eine einzelne Architektur verwenden, die diese Algorithmen und Anwendungen ausführt und vollständig in der Software ausgeführt werden kann. Wenn jedoch die Hardwarebeschleunigung verfügbar ist, können Sie Sie nutzen.

### <a name="completing-the-directx-graphics-platform"></a>Abschließen der DirectX-Grafik Plattform

Warp ermöglicht den Zugriff auf alle Direct3D 10 und spätere Grafik Features, auch auf Computern ohne Direct3D 10 und höhere Grafikhardware. Direct3D 10 entfernte Funktionsbits (Caps); Das heißt, Sie müssen nicht mehr überprüfen, ob Grafikfunktionen von der Grafikhardware verfügbar sind, da Direct3D 10 und höher diese Verfügbarkeit gewährleistet. Sie können jetzt alle Features einer großen Bandbreite von Grafikkarten verwenden, wenn Sie wissen, dass sich Ihre Anwendung verhält und überall gleich aussieht. Sie können die Leistung dieser Anwendungen skalieren, indem Sie einfach teure Grafik Features auf Low-End-Videokarten oder auf kleinere Ziele deaktivieren.

## <a name="warp-capabilities-and-requirements"></a>Warp-Funktionen und-Anforderungen

Warp unterstützt vollständig alle Direct3D 10-und 10,1-Features. Beispielsweise unterstützt Warp die folgenden wichtigsten Features:

-   Alle Genauigkeits Anforderungen der Spezifikation "Direct3D 10" und "10,1"
-   Direct3D 11 bei Verwendung mit featureebenen 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0 und 10 \_ 1 (Weitere Informationen zu featureebenen finden Sie unter [**D3D \_ Feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level))
-   Alle optionalen Textur Formate, wie z. b. Multisampling-Renderziele und Sampling von Gleit Komma Oberflächen
-   Antialiasing, hochwertiges Rendering bis zu 8X Multisampling Antialiasing (MSAA)
-   Anisotrope Filterung
-   32-Bit-und 64-Bit-Anwendungen und große Adress abhängige 32-Bit-Anwendungen

Wenn Sie das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838) unter Windows 7 SP1 oder Windows Server 2008 R2 SP1 installieren, umfasst dieses Betriebssystem dann die Direct3D 11,1 Runtime und eine Version von Warp, die Direct3D 11. x unterstützt, wenn Sie mit den featureebenen 9 [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1 und 11 \_ 0 verwendet wird.

Windows 8, Windows 10, Windows Server 2012 & oben und Windows RT enthalten die Direct3D 11,1-Laufzeit und eine neue Version von Warp. Diese Version unterstützt Direct3D 11. x, wenn Sie mit [featureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ 1, 9 \_ 2, 9 \_ 3, 10 \_ 0, 10 \_ 1, 11 \_ 0 und 11 \_ 1 verwendet wird.

Windows 10 Fall Creators Update (1709) enthält eine neue Version von Warp, die [Direct3D 12](../direct3d12/direct3d-12-graphics.md) -Funktionsebenen 12 \_ 0 und 12 1 unterstützt \_ . 

Die Mindestanforderungen an die Computer für Warp sind identisch mit denen für Windows Vista, insbesondere:

-   Mindestens 800 MHz CPU
-   MMX, SSE oder SSE2 ist nicht erforderlich.
-   Mindestens 512 MB RAM

## <a name="how-to-use-warp"></a>Verwenden von Warp

Die Komponenten Direct3D 10, 10,1, 11 und 12 können einen zusätzlichen Treibertyp verwenden, den Sie beim Erstellen des Geräts angeben können (z. b. Wenn Sie die [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) -Funktion aufgerufen haben). Dieser Treibertyp ist [**d3d10 \_ Driver \_ Type \_ Warp**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type) oder [**D3D \_ Driver \_ Type \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type). Wenn Sie diesen Treibertyp angeben, erstellt die Laufzeit ein Warp-Gerät und initialisiert kein Hardware Gerät.

Da Warp die gleiche Softwareschnittstelle wie der Verweis Raster für Direct3D verwendet, kann jede Direct3D-Anwendung, die die Ausführung mit dem Verweis Raster unterstützen kann, mithilfe von Warp getestet werden. Um Warp zu verwenden, benennen Sie D3d10warp.dll um D3d10ref.dll, und platzieren Sie es im selben Ordner wie das Beispiel oder die Anwendung. Wenn Sie dann zu Ref wechseln, sehen Sie das Warp-Rendering.

Wenn Sie "Warp" in "D3d10ref.dll" umbenennen und in "C: \\ Programme (x86) \\ Microsoft DirectX SDK (Juni 2010) \\ Samples \\ C++ \\ Direct3D \\ bin \\ x86" platzieren, können Sie alle DirectX-Beispiele für Warp ausführen, indem Sie entweder auf die Schaltfläche "Ref umschalten" im Beispiel klicken oder das Beispiel mit/Ref ausführen, das in der Befehlszeile angegeben ist.

## <a name="recommended-application-types-for-warp"></a>Empfohlene Anwendungs Typen für Warp

Alle Anwendungen, die Direct3D verwenden können, können Warp verwenden. Dies umfasst die folgenden Anwendungs Typen:

-   [Ungezwungene Spiele](#casual-games)
-   [Vorhandene nicht-Gaming-Anwendungen](#existing-non-gaming-applications)
-   [Erweiterte renderingspiele](#advanced-rendering-games)
-   [Andere Anwendungen](#other-applications)

### <a name="casual-games"></a>Ungezwungene Spiele

Spiele verfügen in der Regel über einfache Renderinganforderungen. Sie erfordern jedoch auch die Verwendung beeindruckender visueller Effekte, die möglicherweise eine Hardwarebeschleunigung erfordern. Die Mehrzahl der besten verkauften Spieltitel für Windows sind entweder Simulationen oder Gelegenheitsspiele, von denen keine Hochleistungs Grafiken erfordert. Beide Spielstile profitieren jedoch erheblich von modernen shaderbasierten Grafiken und der Möglichkeit, Hardware zu skalieren.

### <a name="existing-non-gaming-applications"></a>Vorhandene nicht-Gaming-Anwendungen

Eine große Menge grafischer Anwendungen erfordert eine minimale Anzahl von Codepfade in ihrer renderingschicht. Mithilfe von Warp können diese Anwendungen einen einzelnen Direct3D-Codepfad implementieren, der auf eine große Anzahl von Computerkonfigurationen abzielen kann.

### <a name="advanced-rendering-games"></a>Erweiterte renderingspiele

Spieleentwickler möchten möglicherweise Grafikkarten-oder Treiber spezifische Renderingfehler isolieren. Daher können alle Spiele, sogar extrem grafisch anspruchsvolle Spiele, von der Möglichkeit profitieren, ihre Inhalte mithilfe von Warp zu erzeugen. Mithilfe von Warp können Sie überprüfen, ob visuelle Artefakte, die Sie finden, Fehler oder Probleme mit Hardware oder Treibern rendern.

### <a name="other-applications"></a>Andere Anwendungen

Zu den Zielanwendungen für Warp zählen auch diejenigen, die derzeit nicht Direct3D 10 oder Direct3D 10,1 verwenden. Zu diesen Zielanwendungen zählen Anwendungen, die immer auf allen Computern funktionieren müssen, Abbild Verarbeitungsanwendungen, die keine CPU-und GPU-Versionen von Bildverarbeitungsalgorithmen schreiben, Bildverarbeitungsalgorithmen, bei denen Geschwindigkeit oder Verwendung der GPU nicht wichtig ist, wie z. b. Drucken, Emulatoren und virtuelle Umgebungen, in denen erweiterte 3D-Grafiken angezeigt werden.

## <a name="warp-architecture-and-performance"></a>Warp-Architektur und-Leistung

Warp basiert auf der verweisrasterizer-CodeBase. Daher verwendet Warp dieselbe Softwareschnittstelle sowohl für Direct3D 10 als auch für höhere Versionen und für dxgi. Warp ist in Windows 7 in den D3d10warp.dll enthalten, der sich in Windows-Systemordnern befindet. Auf 64-Bit-Computern sind zwei Versionen von Warp installiert, eine x86-und x64-Version. Die x64-Version kann unter bestimmten Umständen schneller ausgeführt werden, da der in Warp enthaltene Code-Generator die zusätzlichen Register nutzen kann, die verfügbar sind, wenn Benutzer 64-Bit-Anwendungen ausführen.

Warp enthält die folgenden zwei hoch Geschwindigkeits Echt Zeit Compiler:

-   Der Compiler der mittleren Sprache auf hoher Ebene, der HLSL-Bytecode und den aktuellen renderzustand in einen optimierten Datenstrom von Vektor Befehlen für den Geometry-Shader (GS), den Vertex-Shader (VS) und die Pixel-Shader-Stufen (PS) der Pipeline konvertiert.
-   Der leistungsstarke Just-in-Time-Code-Generator, der diese Befehle ausführen und optimierten SSE2-, SSE 4.1-, x86-, x64-, Arm-und arm64-Assemblycode generieren kann.

Warp verwendet den Thread Pool und die komplexe Aufgaben Verwaltung sowie die Abhängigkeits Nachverfolgung, die in Windows Vista eingeführt wurde, um die effiziente Verteilung aller Teile der Renderingpipeline über verfügbare CPU-Kerne zuzulassen.

Warp verwendet verzögertes Rendering. Das heißt, Warp kann das Rendern von Befehlen in Batches ausführen, sodass die rasterisierung nur dann erfolgt, wenn genügend Daten verfügbar sind, um alle CPU-Ressourcen effizient zu nutzen. Die Arbeit am Hauptanwendungs Thread ist minimiert, damit die Anwendung Befehle so schnell wie möglich übermitteln kann. Wenn eine Anwendung auch Multithreadvorgänge verwendet und der Thread Pool verwendet wird, wird die Arbeit gleichmäßig zwischen den Warp-und der Anwendung verteilt.

Der Warp Code-Generator wurde optimiert, um die moderne CPU-Architektur optimal zu nutzen. Warp wird auf allen Computern ausgeführt, auf denen Windows Vista und spätere Betriebssysteme ausgeführt werden können. Dies gilt auch, wenn der Computer SSE nicht unterstützt. Warp wurde jedoch für Computer optimiert, die SSE2 unterstützen. Sie enthält auch Optimierungen für bestimmte Architekturen von AMD-und Intel-Prozessoren sowie Unterstützung für die SSE 4,1-Erweiterungen.

Die Ausführung von Warp erfordert keine auszuführende Grafikhardware. Sie kann auch in Situationen ausgeführt werden, in denen Hardware nicht verfügbar ist oder nicht initialisiert werden kann.

Anwendungen und Beispiele, die entwickelt und entwickelt wurden, um auf Direct3D 10-und spätere Hardware ohne Wissen von Warp ausgeführt zu werden, werden wahrscheinlich problemlos mithilfe von Warp ausgeführt. Es wird jedoch empfohlen, die Qualitätseinstellungen und die Lösung so weit wie möglich zu verringern, um verwendbare Frameraten zu erzielen. Sie können Warp verwenden, um Anwendungen zu entwickeln und zu optimieren, die sowohl auf Hardware als auch auf Software gut ausgeführt werden.

Da Warp mehrere CPU-Kerne verwendet, erfolgt die beste Leistung bei modernen Quad-Core-CPUs. Warp ist auf Computern mit installiertem SSE 4.1-Erweiterungen ebenfalls erheblich schneller. Microsoft hat eine beträchtliche Test-und Leistungsoptimierung auf Computern mit acht oder mehr Kernen und SSE 4.1 durchgeführt, da diese High-End-Computer während der Lebensdauer von Windows 7 und höheren Betriebssystemen häufiger verwendet werden.

Wenn Warp auf der CPU ausgeführt wird, ist Sie auf verschiedene Weise auf eine Grafikkarte beschränkt. Die Front-Side-Busgeschwindigkeit einer CPU beträgt in der Regel ungefähr oder weniger als 10 GB/s. Im Gegensatz dazu verfügt eine Grafikkarte häufig über dedizierten Arbeitsspeicher, der 20 bis 100 GB/s oder mehr Grafik Bandbreite verwendet. Grafikhardware verfügt auch über Einheiten fester Funktionseinheiten, die komplexe und aufwändige Aufgaben ausführen können, wie z. b. Textur Filterung, Format Dekomprimierung oder Konvertierungen, mit geringem Aufwand oder Stromkosten asynchron. Die Ausführung dieser Vorgänge für eine typische CPU ist in Bezug auf Stromverbrauch und Leistungs Zyklen aufwendig.

Die typischen Leistungszahlen für einen Intel pryn-basierten Prozessor mit 3,0 GHz Quad Core zeigen, dass Warp in manchen Fällen einen Outdo-fähigen Direct3D 10-und spätere Grafik-GPUs für eine Reihe von Benchmarks durchführen kann. Eine diskrete Hardware Hardware ist in der Regel 4 bis fünfmal schneller als Warp bei der Ausführung dieser Benchmarks. Diese integrierten oder diskreten GPUs mit geringem Ende können CPU-Ressourcen nur minimal nutzen. Mittel-oder High-End-Grafikkarten sind für viele Anwendungen deutlich schneller als Warp, insbesondere dann, wenn eine Anwendung von der Parallelität und der Arbeitsspeicher Bandbreite profitieren kann, die diese Grafikkarten bereitstellen.

Warp ist kein Ersatz für Grafikhardware. vor allem, wenn die Leistung von Low-End-Direct3D 10 und höher möglich ist, ist jetzt ein kostengünstiger. Das Ziel von Warp besteht darin, dass Anwendungen Direct3D 10-stufige Hardware als Ziel haben, ohne dass Sie unterschiedliche Codepfade oder Testanforderungen haben, unabhängig davon, ob Sie auf Hardware oder Software ausgeführt werden.

In den folgenden beiden Tabellen werden Warp-Beispiel Daten mit verschiedenen CPUs und Grafikkarten angezeigt.

Die erste Tabelle zeigt Warp-Beispiel Daten mit Direct3D 10-Crysis, die auf 800 x 600 ausgeführt werden, und alle Qualitätseinstellungen auf den niedrigsten Stufen:

| CPU                         | Time   | Ave-fps | Minimale fps | Min. Rahmen | Max. fps | Maximaler Frame |
|-----------------------------|--------|---------|---------|-----------|---------|-----------|
| Core i7 8 Kerne mit 3,0 GHz     | 271,57 | 7.36    | 3,46    | 1966      | 15,01   | 995       |
| Pryn 4 Kerne mit 3,0 GHz      | 351,35 | 5,69    | 2.49    | 1967      | 10,95   | 980       |
| Pryn 2 Kerne mit 3,0 GHz      | 573,98 | 3.48    | 1,35    | 1964      | 6,61    | 988       |
| Core 2 Duo mit 2,6 GHz         | 707,19 | 2.83    | 0.81    | 1959      | 5.18    | 982       |
| Core 2 Duo mit 2,4 GHz         | 763,25 | 2.62    | 0,76    | 1964      | 4.70    | 984       |
| Core 2 Duo mit 2,1 GHz         | 908,87 | 2,20    | 0,64    | 1965      | 3.72    | 986       |
| Xeon 8 Kerne mit 2,0 GHz        | 424,04 | 4.72    | 1,84    | 1967      | 9,56    | 988       |
| AMD FX74 4 Kerne mit 3,0 GHz    | 583,12 | 3.43    | 1,41    | 1967      | 5,78    | 986       |
| Phenom 9550 4 Kerne mit 2,2 GHz | 664,69 | 3,01    | 0,53    | 1959      | 5.46    | 987       |

Die zweite Tabelle zeigt Beispiel Daten, die denselben Test über eine Vielzahl von Grafikkarten ausführen:

| Grafikkarte         | Time   | Ave-fps | Minimale fps | Min. Rahmen | Max. fps | Maximaler Frame |
|-----------------------|--------|---------|---------|-----------|---------|-----------|
| NVIDIA 8800 GTS       | 23,58  | 84,80   | 60,78   | 1957      | 130,83  | 1022      |
| NVIDIA 8500 gt        | 47,63  | 41,99   | 25,67   | 1986      | 72,57   | 991       |
| NVIDIA Quadro 290     | 67,16  | 29,78   | 18,19   | 1969      | 49,87   | 1017      |
| NVIDIA 8400 GS        | 59,01  | 33,89   | 21.22   | 1962      | 51,82   | 1021      |
| ATI 3400              | 53,79  | 37,18   | 22.97   | 618       | 59,77   | 1021      |
| ATI 3200              | 67,19  | 29,77   | 18,91   | 1963      | 45,74   | 980       |
| ATI 2400 pro          | 67,04  | 29,83   | 17,97   | 606       | 45,91   | 987       |
| Intel DX10 integriert | 386,94 | 5.17    | 1,74    | 1974      | 16,22   | 995       |

## <a name="warp-conformance"></a>Warp-Konformität

Warp übergibt alle standardmäßigen Windows Hardware Quality Labs (WHQL)-Konformitätstests zum Überprüfen von Direct3D-Hardware Geräten.

Warp wurde für eine Sammlung von Direct3D 10-und Direct3D 10,1-Anwendungen und-Benchmarks sowie für SDK-Beispiele aus DirectX, NVIDIA und AMD getestet.

Warp hat das [pix](https://msdn.microsoft.com/library/ee417062(v=VS.85).aspx) -Debugging und-Analysetool für Windows beim Testen verwendet. Microsoft verfügt über eine große Bibliothek von einzelnen Frame-Erfassungen von Anwendungen, die für den Vergleich von Hardware und Warp verwendet werden. Der Großteil der Images ist nahezu identisch zwischen Hardware und Warp. Wenn kleine Unterschiede manchmal auftreten, werden Sie in den von der Direct3D 10-Spezifikation definierten Toleranzen gefunden.