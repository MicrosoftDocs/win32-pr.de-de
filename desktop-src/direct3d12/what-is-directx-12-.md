---
title: Was ist Direct3D 12
description: DirectX 12 führt die nächste Version von Direct3D ein. die 3D-Grafik-API im Kern von DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: b3ff1896372719b011b283e3ff1f5426db9e13d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104817"
---
# <a name="what-is-direct3d-12"></a>Was ist Direct3D 12?

Mit DirectX 12 wird die nächste Version von Direct3D &mdash; der 3D-Grafik-API im Kern von DirectX eingeführt. Direct3D 12 ist schneller und effizienter als jede vorherige Version. Direct3D 12 ermöglicht umfangreichere Szenen, mehr Objekte, komplexere Effekte und eine vollständige Nutzung moderner GPU-Hardware.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Wie können Direct3D 12 so viel schneller und effizienter sein?

Direct3D 12 ist insofern einzigartig, als es eine niedrigere Hardware Abstraktion als in früheren Versionen bietet, sodass Sie die Multi-Core-CPU-Skalierung ihres Titels (oder einer anderen Anwendung) erheblich verbessern können. In Direct3D 12 ist Ihr Titel für die eigene [Speicherverwaltung](memory-management.md)verantwortlich. Außerdem profitieren Ihre Titel und Anwendungen mithilfe von Direct3D 12 von einem reduzierten GPU-Overhead über Features wie [Befehls Warteschlangen und Listen](command-queues-and-command-lists.md), [deskriptortabellen](descriptor-tables.md)und präzise [Pipeline Zustands Objekte](managing-graphics-pipeline-state-in-direct3d-12.md).

Direct3D 12 und Direct3D 11,3 stellen eine Reihe neuer Features für die Renderingpipeline dar.

- [Konservative Rasterung](../direct3d11/conservative-rasterization.md) zum Aktivieren der zuverlässigen Treffer Erkennung.
- [Menge an Kacheln](../direct3d11/volume-tiled-resources.md) , um das Streamen von dreidimensionalen Ressourcen zu ermöglichen, die so behandelt werden, als wären Sie alles im Videospeicher.
- [Rasterizer-geordnete Sichten](../direct3d11/volume-tiled-resources.md) , um zuverlässiges Transparenz Rendering zu ermöglichen.
- Festlegen des Schablonen Verweises innerhalb eines Shaders, um besondere shadowingund andere Effekte zu ermöglichen.
- Verbesserte Textur Zuordnung und eingegebene UAV-Ladevorgänge (unsortierter Zugriffs Ansicht).

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Wie tief sollte ich in Direct3D 12 investieren?

Direct3D 12 bietet Grafik Entwicklern vier wichtige Vorteile (im Vergleich zu Direct3D 11).

- Erheblich reduzierter CPU-Aufwand.
- Erheblich Reduzierter Stromverbrauch.
- Bis zu (ungefähr) 20% Verbesserung der GPU-Effizienz.
- Plattformübergreifende Entwicklung für ein Windows 10-Gerät (PC, Tablet, Console, Mobile).

Direct3D 12 ist für die Verwendung durch erweiterte grafikprogrammierer konzipiert. Er erfordert bedeutende Grafiken und ein hohes Maß an Feinabstimmung. Direct3D 12 ist so konzipiert, dass Multithreading, sorgfältige CPU/GPU-Synchronisierung und der Übergang und die erneute Verwendung von Ressourcen von einem Zweck zu einem anderen vollständig genutzt werden. Dabei handelt es sich um Techniken, die eine beträchtliche Menge an Programmier Kenntnissen auf Speicher Ebene erfordern.

Ein weiterer Vorteil, den Direct3D 12 hat, ist der geringe API-Speicherbedarf. Es sind ungefähr 200 Funktionen vorhanden. und etwa ein Drittel der Arbeit ist alles ausgelastet. Dies bedeutet, dass Sie als Grafik Entwickler in der Lage sein sollten, sich über &mdash; den vollständigen API-Satz zu informieren und ihn zu beherrschen, &mdash; ohne zu viele API-Namen merken zu müssen.

Direct3D 11 ist neben Direct3D 12 weiterhin eine brauchbare Option. Viele der neuen Renderingfeatures von Direct3D 12 sind in [Direct3D 11,3](../direct3d11/direct3d-11-3-features.md)verfügbar. Direct3D 11,3 ist eine Grafik-Engine-API auf niedriger Ebene. und Direct3D 12 geht noch tiefer.

Es gibt mindestens zwei Möglichkeiten, wie das Entwicklungsteam einen Direct3D 12-Titel angehen kann.

### <a name="use-direct3d-12-exclusively"></a>Ausschließlich Direct3D 12 verwenden

Für ein Projekt, das alle Vorteile von Direct3D 12 vollständig nutzt, sollten Sie eine hochgradig angepasste Direct3D 12-Engine von Grund auf entwickeln.

Wenn Sie als Grafik Entwickler die Verwendung und Wiederverwendung von Ressourcen in ihren Titeln verstehen, die Sie nutzen können, indem Sie das Hochladen und kopieren minimieren, können Sie eine hochgradig effiziente Engine für diese Titel entwickeln und anpassen. Die Leistungsverbesserungen können sehr beträchtlich sein, und Sie können die CPU-Zeit verbessern, um die Anzahl der Draw-Aufrufe zu erhöhen, und so weitere Lustern zu Ihren Grafiken hinzufügen.

Der Aufwand für die Programmierung ist beträchtlich, und Sie sollten das Debuggen und Instrumentierungs Verfahren des Projekts von Anfang an in Erwägung gezogen. Threading-, Synchronisierungs-und andere Zeit Steuerungs Fehler können eine Herausforderung darstellen.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Verwenden Sie Direct3D 12 im Konzert mit Direct3D 11

Ein kürzerer Begriff besteht darin, bekannte Engpässe in Ihrem Direct3D 11-Titel zu beheben. Sie können diese mithilfe von [Direct3D 12-Interop-und/oder D3D11On12-](direct3d-12-interop.md) Techniken adressieren, die es ermöglichen, dass die beiden API-Versionen zusammenarbeiten. Dieser Ansatz minimiert die Änderungen, die für ein vorhandenes Direct3D 11-Grafik Modul erforderlich sind. Die Leistungssteigerungen werden jedoch auf die Erleichterung des Engpasses beschränkt, den der Direct3D 12-Code adressiert.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Videos zu Microsoft DirectX 12 (und Grafiken Education)

[Verbessertes Education für Grafik Entwickler](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). In diesen Videos werden Themen wie präsentationsmodi, Portieren auf DirectX 12, konservative rasterization, Grafiktools, Angle, Win2D und Ereignisse wie GDC, Build und mehr behandelt. Technical DirectX 12-Inhalt wird mit *DirectX 12* vorangestellt. Hier finden Sie Tipps und Tricks direkt aus dem Feature-Team von Direct3D 12. Wir möchten Sie dabei unterstützen, unsere neuesten Releases und Tools zu verwenden, damit Ihr Spiel das beste ist!

## <a name="conclusion"></a>Zusammenfassung

Bei Direct3D 12 geht es um das dramatische Grafik-Engine-Leistung. Die einfache Entwicklung, Konstrukte auf hoher Ebene und Compilerunterstützung wurden zurück skaliert, um dies zu ermöglichen. Die Treiberunterstützung und das einfache Debuggen bleiben bei Direct3D 11 unverändert.

Direct3D 12 ist ein neues Gebiet. Das Gebiet, das darauf wartet, dass der begierigen Experte es untersucht.
