---
title: Direct3D 12-Programmieranleitung
description: Direct3D 12 bietet eine API und Plattform, mit der Apps die Grafik- und Computingfunktionen von PCs nutzen können, die mit mindestens einer Direct3D 12-kompatiblen GPUs ausgestattet sind.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: c7dfaf55b44da4a05616db7b7f64c262a3c5b6920ab2c0665e1196d70b539215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045488"
---
# <a name="direct3d-12-programming-guide"></a>Direct3D 12-Programmieranleitung

Direct3D 12 bietet eine API und Plattform, mit der Apps die Grafik- und Computingfunktionen von PCs nutzen können, die mit mindestens einer Direct3D 12-kompatiblen GPUs ausgestattet sind.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Was ist Direct3D 12?](what-is-directx-12-.md) | DirectX 12 führt die nächste Version von Direct3D ein, die 3D-Grafik-API, die das Herzstück von DirectX ist. Diese Version von Direct3D ist schneller und effizienter als jede vorherige Version. Direct3D 12 ermöglicht vielfältigere Szenen, mehr Objekte, komplexere Effekte und die vollständige Nutzung moderner GPU-Hardware.  |
| [Neuerungen in Direct3D 12](new-releases.md) | Beschreibt die wichtigste neue Dokumentation, die mit dem neuesten SDK-Release verfügbar ist. |
| [Grundlegendes zu Direct3D 12](directx-12-getting-started.md) | Um 3D-Spiele und -Apps für Windows 10 und Windows 10 Mobile zu schreiben, müssen Sie die Grundlagen der Direct3D 12-Technologie verstehen und sich darauf vorbereiten, sie in Ihren Spielen und Apps zu verwenden. |
| [Arbeitsübermittlung in Direct3D 12](command-queues-and-command-lists.md) | Um die CPU-Effizienz von Direct3D-Apps zu verbessern, unterstützt Direct3D 12 keinen unmittelbaren Kontext mehr, der einem Gerät zugeordnet ist. Stattdessen zeichnen Apps Befehlslisten auf und übermitteln diese, *die* Zeichnungs- und Ressourcenverwaltungsaufrufe enthalten. Diese Befehlslisten können von mehreren Threads an eine oder mehrere Befehlswarteschlangen übermittelt werden, die die Ausführung der Befehle verwalten. Diese grundlegende Änderung erhöht die Effizienz des Singlethreadings, da Apps das Rendern vorab berechnen können, um sie später wiederverarbeiten zu können, und nutzt Systeme mit mehreren Kernen, indem Renderingarbeit auf mehrere Threads verteilt wird.  |
| [Ressourcenbindung in Direct3D 12](resource-binding.md) | Bindung ist der Prozess, bei dem Ressourcenobjekte mit den Shadern der Grafikpipeline verlinkt werden.  |
| [Speicherverwaltung in Direct3D 12](memory-management.md) | Der Wechsel zu D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicherresidenz. Die Verwaltung der Speicherresidenz bedeutet, dass noch mehr Synchronisierung durchgeführt werden muss. In diesem Abschnitt werden Strategien für die Speicherverwaltung und die Unterzuordnung innerhalb von Heaps und Puffern behandelt.  |
| [Systeme mit mehreren Adaptern](multi-engine.md) | Beschreibt die Unterstützung in Direct3D 12 für Systeme, auf denen mehrere Adapter installiert sind, und beschreibt Szenarien, in denen Ihre Anwendung explizit mehrere GPU-Adapter als Ziel verwendet, sowie Szenarien, in denen Treiber implizit mehrere GPU-Adapter im Auftrag Ihrer Anwendung verwenden. |
| [Synchronisierung mit mehreren Modulen](user-mode-heap-synchronization.md) | In diesem Thema wird die Synchronisierung des Zugriffs auf die verschiedenen unabhängigen Engines in den meisten modernen GPUs erläutert. |
| [Rendering](rendering.md) | Dieser Abschnitt enthält Informationen zu Renderingfunktionen, die in Direct3D 12 (und Direct3D 11.3) neu sind. |
| [Leistungsindikatoren, Abfragen und Leistungsmessung](performance-measurement.md) | In den folgenden Abschnitten werden Features für die Verwendung bei Leistungstests und Verbesserungen beschrieben, z. B. Abfragen, Leistungsindikatoren, Zeitsteuerung und Prädication. |
| [Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md) | In diesem Abschnitt werden Interop-Techniken mit früheren Versionen von Direct3D und Direct2D, der Direct3D 11on12-API und Portierungsrichtlinien von Direct3D 11 auf Direct3D 12 behandelt. |
| [Arbeitsbeispiele](working-samples.md) | Arbeitsbeispiele stehen zum Download zur Verfügung, die die Verwendung einer Reihe von Features von Direct3D 12 zeigen. |
| [Exemplarische Vorgehensweisen für D3D12-Code](d3d12-code-walk-throughs.md) | Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Details dazu, welche Codierung zu einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der grundlegende Komponentencode für jedes Szenario wiederholt wird. |
| [Debuggen und Diagnose mit Direct3D 12](understanding-the-d3d12-debug-layer.md) | Enthält Themen, in denen beschrieben wird, wie Sie die Direct3D 12-Debugebene mit GPU-basierter Validierung (GBV) optimal nutzen und wie Sie device Removed Extended Data (DRED) verwenden. |

## <a name="related-topics"></a>Zugehörige Themen

* [Direct3D 12-Grafiken](direct3d-12-graphics.md)
* [Referenz für Direct3D 12](direct3d-12-reference.md)
* [Videotutorials für erweitertes Lernen mit DirectX](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
