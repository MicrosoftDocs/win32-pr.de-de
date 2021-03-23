---
title: Arbeits Übermittlung in Direct3D 12
description: Um die CPU-Effizienz von Direct3D-apps zu verbessern, unterstützt Direct3D 12 nicht mehr einen unmittelbaren Kontext, der mit einem Gerät verknüpft ist.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104640"
---
# <a name="work-submission-in-direct3d-12"></a>Arbeits Übermittlung in Direct3D 12

Um die CPU-Effizienz von Direct3D-apps zu verbessern, unterstützt Direct3D nicht mehr den einem Gerät zugeordneten unmittelbaren Kontext. Stattdessen werden von Ihrer Anwendung *Befehlslisten* aufgezeichnet und übermittelt, die Zeichnungs-und Ressourcen Verwaltungs Aufrufe enthalten. Sie können diese Befehlslisten aus mehreren Threads an eine oder mehrere Befehls Warteschlangen übermitteln, die die Ausführung der Befehle verwalten. Diese grundlegende Änderung steigert die Single Thread Effizienz, indem es Ihrer Anwendung ermöglicht wird, Renderingvorgänge für eine spätere Wiederverwendung vorzuberechnen, und Sie nutzt mehr Kernsysteme, indem renderingarbeiten über mehrere Threads verteilt werden.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [Entwurfs Philosophie von Befehls Warteschlangen und Befehlslisten](design-philosophy-of-command-queues-and-command-lists.md) | Die Ziele der Aktivierung der Wiederverwendung von renderingarbeiten und der Multithread-Skalierung erforderten grundlegende Änderungen an der Art und Weise, wie Direct3D apps renderingarbeit an die GPU |
| [Erstellen und Aufzeichnen von Befehlslisten und Paketen](recording-command-lists-and-bundles.md) | In diesem Thema wird das Aufzeichnen von Befehlslisten und Paketen in Direct3D 12-apps beschrieben. Mit Befehlslisten und-Paketen können Sie sowohl Zeichnungs-als auch Zustands ändernde Aufrufe für die spätere Ausführung auf der GPU (Graphics Processing Unit) aufzeichnen. |
| [Ausführen und Synchronisieren von Befehlslisten](executing-and-synchronizing-command-lists.md) | In Microsoft Direct3D 12 ist der unmittelbare Modus vorheriger Versionen nicht mehr vorhanden. Stattdessen erstellen apps Befehlslisten und Pakete und zeichnen dann Sätze von GPU-Befehlen auf. Befehls Warteschlangen werden verwendet, um auszuführende Befehlslisten zu übermitteln. Dieses Modell ermöglicht Entwicklern eine bessere Kontrolle über die effiziente Nutzung von GPU und CPU. |
| [Verwalten des Grafik Pipeline Status in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | In diesem Thema wird beschrieben, wie der Status der Grafik Pipeline in Direct3D 12 festgelegt wird. |
| [Verwenden von Ressourcen Barrieren zum Synchronisieren von Ressourcen Zuständen in Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Um die CPU-Gesamtauslastung zu reduzieren und das Multithreading und die Vorverarbeitung von Treibern zu ermöglichen, verschiebt Direct3D 12 die Verantwortung für die Ressourcen übergreifende Zustands Verwaltung vom Grafiktreiber zur Anwendung. |
| [Pipelines und Shader mit Direct3D 12](pipelines-and-shaders-with-directx-12.md) | Die programmierbare Pipeline Direct3D 12 erhöht die Renderingleistung im Vergleich zu den Schnittstellen Schnittstellen für die Grafik Programmierung. |
| [Schattierung variabler Rate (VRS)](vrs.md) | Das Schattieren von Variablenraten &mdash; oder grobe Pixel Schattierung &mdash; ist ein Mechanismus, mit dem Sie Renderingleistung/-Leistung zu raten zuweisen können, die in Ihrem gerenderten Bild variieren. |
| [Rendering-Durchlauf](direct3d-12-render-passes.md) | Die Funktion "renderingüberläufen" hilft Ihrem Renderer, die GPU-Effizienz zu verbessern, indem der Speicher Datenverkehr auf den/aus dem Dies geschieht, indem es Ihrer Anwendung ermöglicht wird, Anforderungen an die Reihenfolge von Ressourcen Rendering und Daten Abhängigkeiten besser zu identifizieren. |

## <a name="related-topics"></a>Verwandte Themen

* [Direct3D 12-Programmieranleitung](directx-12-programming-guide.md)
