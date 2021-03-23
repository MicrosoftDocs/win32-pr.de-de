---
title: Direct3D 12-Programmieranleitung
description: Direct3D 12 bietet eine API und Plattform, mit deren Hilfe Apps die Grafik-und Berechnungsfunktionen von PCs nutzen können, die mit mindestens einem Direct3D 12-kompatiblen GPUs ausgestattet sind.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: bf6a52b91604d8a9432bf646097e3f31e44967d7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/06/2019
ms.locfileid: "104548732"
---
# <a name="direct3d-12-programming-guide"></a>Direct3D 12-Programmieranleitung

Direct3D 12 bietet eine API und Plattform, mit deren Hilfe Apps die Grafik-und Berechnungsfunktionen von PCs nutzen können, die mit mindestens einem Direct3D 12-kompatiblen GPUs ausgestattet sind.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Was ist Direct3D 12?](what-is-directx-12-.md) | DirectX 12 führt die nächste Version von Direct3D ein, die 3D-Grafik-API im Kern von DirectX. Diese Direct3D-Version ist schneller und effizienter als jede vorherige Version. Direct3D 12 ermöglicht umfangreichere Szenen, mehr Objekte, komplexere Effekte und eine vollständige Nutzung moderner GPU-Hardware.  |
| [Neuerungen in Direct3D 12](new-releases.md) | Beschreibt die wichtigste neue Dokumentation, die für die neueste SDK-Version verfügbar ist. |
| [Grundlegendes zu Direct3D 12](directx-12-getting-started.md) | Um 3D-Spiele und-Apps für Windows 10 und Windows 10 Mobile zu schreiben, müssen Sie sich mit den Grundlagen der Direct3D 12-Technologie und der Vorbereitung der Verwendung in ihren spielen und apps vertraut machen. |
| [Arbeits Übermittlung in Direct3D 12](command-queues-and-command-lists.md) | Um die CPU-Effizienz von Direct3D-apps zu verbessern, unterstützt Direct3D 12 nicht mehr einen unmittelbaren Kontext, der mit einem Gerät verknüpft ist. Stattdessen erfassen und übermitteln die apps *Befehlslisten*, die Zeichnungs-und Ressourcen Verwaltungs Aufrufe enthalten. Diese Befehlslisten können von mehreren Threads an eine oder mehrere Befehls Warteschlangen übermittelt werden, die die Ausführung der Befehle verwalten. Diese grundlegende Änderung erhöht die Effizienz mit einem einzelnen Thread, indem Apps die renderingarbeit vorab berechnen können, um Sie später wieder zu verwenden, und Sie nutzt mehr Kernsysteme, indem renderingarbeiten über mehrere Threads verteilt werden.  |
| [Ressourcenbindung in Direct3D 12](resource-binding.md) | Die Bindung ist der Prozess, bei dem Ressourcen Objekte mit den Shadern der Grafik Pipeline verknüpft werden.  |
| [Arbeitsspeicherverwaltung in Direct3D 12](memory-management.md) | Die Umstellung auf D3D12 umfasst die ordnungsgemäße Synchronisierung und Verwaltung der Speicher Residenz. Das Verwalten der Speicher Residenz bedeutet, dass noch mehr Synchronisierungen ausgeführt werden müssen. In diesem Abschnitt werden die Strategien für die Speicherverwaltung und die unter Zuordnung von Heaps und Puffern behandelt.  |
| [Systeme mit mehreren Adaptern](multi-engine.md) | Beschreibt die Unterstützung in Direct3D 12 für Systeme, die mehrere Adapter installiert haben, und umfasst Szenarien, in denen Ihre Anwendung explizit mehrere GPU-Adapter als Ziel verwendet, und Szenarios, in denen Treiber implizit mehrere GPU-Adapter im Auftrag der Anwendung verwenden. |
| [Multi-Engine-Synchronisierung](user-mode-heap-synchronization.md) | In diesem Thema wird die Synchronisierung des Zugriffs auf mehrere unabhängige Engines in den meisten modernen GPUs erläutert. |
| [Darstellung](rendering.md) | Dieser Abschnitt enthält Informationen zu den Renderingfunktionen, die für Direct3D 12 (und Direct3D 11,3) neu sind. |
| [Zähler, Abfragen und Leistungsmessung](performance-measurement.md) | In den folgenden Abschnitten werden die Features beschrieben, die bei Leistungstests und-Verbesserungen verwendet werden können, wie z. b. Abfragen, Leistungsindikatoren, zeitliche Steuerung |
| [Arbeiten mit Direct3D 11, Direct3D 10 und Direct2D](direct3d-12-interop.md) | In diesem Abschnitt werden Interop-Techniken mit früheren Versionen von Direct3D und Direct2D, der Direct3D 11on12-API und der Portierungs Richtlinien von Direct3D 11 bis Direct3D 12 behandelt. |
| [Funktionierende Beispiele](working-samples.md) | Funktionierende Beispiele sind zum Herunterladen verfügbar und zeigen die Verwendung einer Reihe von Features von Direct3D 12. |
| [D3D12-Code Exemplarische Vorgehensweisen](d3d12-code-walk-throughs.md) | Dieser Abschnitt enthält Code für Beispielszenarien. Viele der exemplarischen Vorgehensweisen enthalten Informationen dazu, welche Codierung einem einfachen Beispiel hinzugefügt werden muss, um zu vermeiden, dass der Grundkomponenten Code für jedes Szenario wiederholt wird. |
| [Debuggen und Diagnose mit Direct3D 12](understanding-the-d3d12-debug-layer.md) | Enthält Themen, in denen beschrieben wird, wie die Direct3D 12-debugschicht mit GPU-basierter Validierung (GBV) optimal verwendet werden kann und wie das Gerät entfernte erweiterte Daten (Dred) verwendet wird. |

## <a name="related-topics"></a>Verwandte Themen

* [Direct3D 12-Grafiken](direct3d-12-graphics.md)
* [Direct3D 12-Referenz](direct3d-12-reference.md)
* [Video-Tutorials zu DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
