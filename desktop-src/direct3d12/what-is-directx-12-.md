---
title: Was ist Direct3D 12?
description: DirectX 12 führt die nächste Version von Direct3D ein. die 3D-Grafik-API, die das Herzstück von DirectX ist.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: 60ff57d8cf94ae7a47c6046ad49f7c7256a7edb6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2021
ms.locfileid: "115006795"
---
# <a name="what-is-direct3d-12"></a>Was ist Direct3D 12?

DirectX 12 führt die nächste Version von Direct3D ein, die &mdash; 3D-Grafik-API im Kern von DirectX. Direct3D 12 ist schneller und effizienter als jede vorherige Version. Direct3D 12 ermöglicht vielfältigere Szenen, mehr Objekte, komplexere Effekte und die vollständige Nutzung moderner GPU-Hardware.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Wie kann Direct3D 12 so viel schneller und effizienter sein?

Direct3D 12 ist einzigartig, da es eine niedrigere Hardwareabstraktion als frühere Versionen bietet, wodurch Sie die CPU-Skalierung mit mehreren Kernen Ihres Titels (oder einer anderen Anwendung) erheblich verbessern können. Bei Direct3D 12 ist Ihr Titel beispielsweise für die eigene [Speicherverwaltung verantwortlich.](memory-management.md) Darüber hinaus profitieren Ihre Titel und Anwendungen durch die Verwendung von Direct3D 12 durch Features wie Befehlswarteschlangen und Listen, [Deskriptortabellen](descriptor-tables.md)und präzise [Pipelinezustandsobjekte](command-queues-and-command-lists.md)vom reduzierten GPU-Mehraufwand. [](managing-graphics-pipeline-state-in-direct3d-12.md)

Direct3D 12 und Direct3D 11.3 führen eine Reihe neuer Features für die Renderingpipeline ein.

- [Konservative Rasterung,](../direct3d11/conservative-rasterization.md) um eine zuverlässige Treffererkennung zu ermöglichen.
- [Gekachelte Volumenressourcen,](../direct3d11/volume-tiled-resources.md) um zu ermöglichen, dass gestreamte dreidimensionale Ressourcen so behandelt werden, als ob sie sich alle im Videospeicher befingen.
- [Rasterizer-geordnete Ansichten, um](../direct3d11/rasterizer-order-views.md) zuverlässiges Transparenzrendering zu ermöglichen.
- Festlegen des Schablonenverweises in einem Shader, um spezielle Schatten und andere Effekte zu ermöglichen.
- Verbesserte Texturzuordnung und typierte UAV-Auslastungen (Unordered Access View, ungeordnete Zugriffsansicht).

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Wie tief sollte ich in Direct3D 12 investieren?

Direct3D 12 bietet Grafikentwicklern vier Hauptvorteile (im Vergleich zu Direct3D 11).

- Erheblich reduzierter CPU-Mehraufwand.
- Deutlich reduzierter Stromverbrauch.
- Bis zu (ca.) 20 % Verbesserung der GPU-Effizienz.
- Plattformübergreifende Entwicklung für ein Windows 10 Gerät (PC, Tablet, Konsole, mobil).

Direct3D 12 ist für fortgeschrittene Grafikprogrammierer konzipiert. Sie erfordert umfassende Grafikkenntnisse und ein hohes Maß an Feinabstimmung. Direct3D 12 ist so konzipiert, dass Multithreading, eine sorgfältige CPU/GPU-Synchronisierung sowie der Übergang und die Erneutnutzung von Ressourcen von einem Zweck zu einem anderen vollständig genutzt werden. Dies sind Techniken, die eine beträchtliche Menge an Programmierkenntnissen auf Arbeitsspeicherebene erfordern.

Ein weiterer Vorteil von Direct3D 12 ist der geringe API-Speicherbedarf. Es gibt etwa 200 Funktionen. und etwa ein Drittel dieser Personen sind für die arbeite Arbeit verantwortlich. Das bedeutet, dass Sie als Grafikentwickler in der Lage sein sollten, Dies zu informieren und den gesamten API-Satz zu meistern, ohne sich zu viele API-Namen merken &mdash; &mdash; zu müssen.

Direct3D 11 ist neben Direct3D 12 weiterhin eine sinnvolle Option. Viele der neuen Renderingfunktionen von Direct3D 12 sind in [Direct3D 11.3 verfügbar.](../direct3d11/direct3d-11-3-features.md) Direct3D 11.3 ist eine Low-Level-Grafik-Engine-API. und Direct3D 12 gehen noch tiefer.

Es gibt mindestens zwei Möglichkeiten, wie Ihr Entwicklungsteam sich einem Direct3D 12-Titel nähern kann.

### <a name="use-direct3d-12-exclusively"></a>Ausschließliches Verwenden von Direct3D 12

Für ein Projekt, das alle Vorteile von Direct3D 12 letztendlich nutzt, sollten Sie eine hochgradig angepasste Direct3D 12-Engine von Grund auf entwickeln.

Wenn Sie als Grafikentwickler die Verwendung und Erneutnutzung von Ressourcen in Ihren Titeln verstehen und dies nutzen können, indem Sie das Hochladen und Kopieren minimieren, können Sie eine äußerst effiziente Engine für diese Titel entwickeln und anpassen. Die Leistungsverbesserungen können sehr erheblich sein, was die CPU-Zeit zur Erhöhung der Anzahl von Zeichnen-Aufrufen und somit das Hinzufügen von zusätzlichem Aufwand für Ihre Grafiken frei macht.

Die Programmierinvestitionen sind erheblich, und Sie sollten das Debuggen und instrumentieren des Projekts von Anfang an in Betracht ziehen. Threading, Synchronisierung und andere Zeitsteuerungsfehler können eine Herausforderung darstellen.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Verwenden von Direct3D 12 in Zusammenarbeit mit Direct3D 11

Ein kürzerer Ansatz wäre, bekannte Engpässe in Ihrem Direct3D 11-Titel zu beheben. Sie können diese Mithilfe von [Direct3D 12-Interop- und/oder D3D11On12-Techniken](direct3d-12-interop.md) adressiert werden, mit denen die beiden API-Versionen zusammenarbeiten können. Dieser Ansatz minimiert die Änderungen, die an einer vorhandenen Direct3D 11-Grafik-Engine erforderlich sind. Die Leistungssteigerungen sind jedoch auf die Beseitigung des Engpasses beschränkt, den der Direct3D 12-Code beheben kann.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Videos zu Microsoft DirectX 12 (und Grafik education)

[Erweiterte Bildung für Grafikentwickler](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). Diese Videos behandeln Themen wie Präsentationsmodi, Portierung auf DirectX 12, konservative Rasterung, Grafiktools, Winkel, Win2D und Ereignisse wie GDC, Build und mehr. Technical DirectX 12 content is prefaced *with DirectX 12*. Hier erhalten Sie Tipps und Tricks direkt vom Direct3D 12-Featureteam. Wir möchten Ihnen helfen, unsere neuesten Releases und Tools zu verwenden, um Ihr Spiel so gut wie möglich zu machen!

## <a name="conclusion"></a>Zusammenfassung

Bei Direct3D 12 geht es um eine drastische Grafik-Engine-Leistung. Einfache Entwicklung, Konstrukte auf hoher Ebene und Compilerunterstützung wurden zurückskaliert, um dies zu ermöglichen. Treiberunterstützung und einfaches Debuggen bleiben gleich wie Direct3D 11.

Direct3D 12 ist ein neues Gebiet. Gebiet, das darauf wartet, dass der inquisitive Experte kommt und es untersucht.
