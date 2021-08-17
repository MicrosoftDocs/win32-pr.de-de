---
title: Übersicht über Deskriptorheaps
description: Deskriptor-Heaps enthalten viele Objekttypen, die nicht Teil eines Pipelinezustandsobjekts (Pipeline State Object, PSO) sind, z. B. Shader-Ressourcenansichten (SRVs), ungeordnete Zugriffsansichten (Unordered Access Views, UAVs), Konstantenpufferansichten (Constant Buffer Views, CBVs) und Sampler.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d0017f10a6027fc7ce48618a9d28bd4e92262d83d0f3aa81cc0bc8d02b7edc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124335"
---
# <a name="descriptor-heaps-overview"></a>Übersicht über Deskriptorheaps

Deskriptor-Heaps enthalten viele Objekttypen, die nicht Teil eines Pipelinezustandsobjekts (Pipeline State Object, PSO) sind, z. B. Shader-Ressourcenansichten (SRVs), ungeordnete Zugriffsansichten (Unordered Access Views, UAVs), Konstantenpufferansichten (Constant Buffer Views, CBVs) und Sampler.

-   [Zweck von Deskriptor-Heaps](#the-purpose-of-descriptor-heaps)
-   [Synchronisierung](#synchronization)
-   [Binding](#binding)
-   [Wechseln von Heaps](#switching-heaps)
-   [Bundles](#bundles)
-   [Verwaltung](#management)
-   [Zugehörige Themen](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>Zweck von Deskriptor-Heaps

Der Hauptzweck eines Deskriptorheaps ist es, den Großteil der Speicherzuweisung zu umfassen, die zum Speichern der Deskriptorspezifikationen von Objekttypen erforderlich ist, auf die Shader so groß wie möglich in einem Renderingfenster verweisen (idealerweise ein gesamter Renderingrahmen oder mehr). Wenn eine Anwendung wechselt, welche Texturen die Pipeline schnell über die API sieht, muss im Deskriptor-Heap Speicherplatz zur Verfügung stehen, um Deskriptortabellen für jeden benötigten Zustandssatz direkt zu definieren. Die Anwendung kann Definitionen wiederverwenden, wenn die Ressourcen z. B. erneut in einem anderen Objekt verwendet werden, oder den Heapbereich einfach sequenziell zuweisen, wenn verschiedene Objekttypen umgeschaltet werden.

Deskriptor-Heaps ermöglichen es auch einzelnen Softwarekomponenten, Deskriptorspeicher getrennt voneinander zu verwalten.

Alle Heaps sind für die CPU sichtbar. Die Anwendung kann auch anfordern, über welche CPU-Zugriffseigenschaften ein Deskriptor heap verfügen soll (sofern verfügbar) – kombiniert schreiben, zurückschreiben und so weiter. Apps können mit den gewünschten Eigenschaften so viele Deskriptor-Heaps wie gewünscht erstellen. Apps haben immer die Möglichkeit, Deskriptor-Heaps zu erstellen, die ausschließlich für Stagingzwecke bestimmt sind, deren Größe nicht ungeniert ist, und das Kopieren in Deskriptorhaps, die bei Bedarf zum Rendern verwendet werden.

Es gibt einige Einschränkungen, was in demselben Deskriptorhap verwendet werden kann. CBV-, UAV- und SRV-Einträge können sich im gleichen Deskriptor-Heap enthalten. Samplers-Einträge können jedoch keinen Heap mit CBV-, UAV- oder SRV-Einträgen gemeinsam haben. In der Regel gibt es zwei Sätze von Deskriptorhaps, einen für die allgemeinen Ressourcen und den zweiten für Sampler.

Die Verwendung von Deskriptor-Heaps durch Direct3D 12 spiegelt die Leistung der meisten GPU-Hardware wieder, d.&a; deskriptor muss entweder nur in Deskriptor heaps live sein, oder einfach, dass weniger Adressierungsbits erforderlich sind, wenn diese Heaps verwendet werden. Direct3D 12 erfordert die Verwendung von Deskriptorhaps. Es gibt keine Option, Deskriptoren an beliebiger Stelle im Arbeitsspeicher abspeichern zu können.

Deskriptor-Heaps können nur sofort von der CPU bearbeitet werden. Es gibt keine Option zum Bearbeiten eines Deskriptorhaps durch die GPU.

## <a name="synchronization"></a>Synchronisierung

Deskriptor-Heapinhalte können vor, während und nach aufzeichnungsaufzeichnenden Befehlslisten geändert werden, die darauf verweisen. Deskriptoren können jedoch nicht geändert werden, während eine zur Ausführung übermittelte Befehlsliste auf diesen Speicherort verweisen könnte, da dies eine Racebedingung aufrufen könnte.

## <a name="binding"></a>Bindung

Es kann immer nur ein kombinierter CBV-/SRV-/UAV-Heap und ein Sampler-Heap gebunden werden. Diese Heaps werden sowohl von grafik- als auch von compute-Pipelines gemeinsam genutzt (in ihren PSOs beschrieben).

## <a name="switching-heaps"></a>Wechseln von Heaps

Es ist akzeptabel, dass eine Anwendung Heaps innerhalb derselben Befehlsliste oder in verschiedenen Befehlslisten mithilfe der [**APIs SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) und [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) umschaltet. Auf einigen Hardwarekomponenten kann dies ein kostspieliger Vorgang sein, bei dem eine GPU nicht mehr alle Arbeiten leeren muss, die vom derzeit gebundenen Deskriptorheap abhängig sind. Wenn Deskriptor-Heaps geändert werden müssen, sollten Anwendungen daher versuchen, dies zu tun, wenn die GPU-Workload relativ gering ist, und möglicherweise Änderungen am Anfang einer Befehlsliste einschränken.

## <a name="bundles"></a>Bundles

Bei Paketen kann nur ein Aufruf der [**SetDescriptorHeaps-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) ausgeführt werden, und die Deskriptorheaps müssen genau mit denen der Befehlsliste übereinstimmen, die das Paket aufruft. Wenn das Paket keine Deskriptortabellen ändert, müssen die Deskriptorhaps nicht festgelegt werden.

Eine Liste der API-Aufrufe, die nicht mit Paketen verwendet werden können, finden Sie unter Erstellen und Aufzeichnen von [Befehlslisten und Paketen.](recording-command-lists-and-bundles.md)

## <a name="management"></a>Verwaltung

Um alle Objekte in einer Szene zu rendern, sind viele Deskriptoren erforderlich, und es gibt verschiedene Verwaltungsstrategien, die befolgt werden können.

Die grundlegendste Strategie wäre, einen neuen Bereich des Deskriptorhaps mit allen Anforderungen für den nächsten Zeichnen-Aufruf zu füllen. Kurz vor dem Ausstellen des Draw-Aufrufs in der Befehlsliste würde also ein Deskriptortabellenzeiger auf den Anfang der neu aufgefüllten Tabelle festgelegt werden. Der Nachteil ist, dass nicht notiert werden muss, wo sich ein bestimmter Deskriptor im Heap befindet.

Der Nachteil dieser Strategie ist, dass es viele Wiederholungen von Deskriptoren im Deskriptorhap geben kann, insbesondere wenn eine sehr ähnliche Szene gerendert wird und dieser Deskriptor-Heapbereich schnell auf genutzt wird. Separate Deskriptor-Heaps für diejenigen, die auf der GPU gerendert werden, und für diejenigen, die von der CPU aufgezeichnet werden, sind wahrscheinlich erforderlich, um Konflikte zu vermeiden. Alternativ kann ein Unterzuordnungssystem verwendet werden.

Darüber hinaus könnte das grundlegende System weiter optimiert werden, indem überlappende Deskriptortabellen von einem Zeichnen-Aufruf zum nächsten sorgfältig verwendet werden, sodass nur die neuen erforderlichen Deskriptoren hinzugefügt werden.

Eine effizientere Als die grundlegende Strategie wäre, Deskriptor-Heaps mit Deskriptoren zu füllen, die für die Objekte (oder Materialien) erforderlich sind, die bekannter weise Teil der Szene sind. Die Idee hierbei ist, dass die Deskriptortabelle nur zur Zeichnen-Zeit festgelegt werden muss, da der Deskriptorhap im Voraus aufgefüllt wird.

Eine Variante der Vorfüllstrategie besteht in der Behandlung des Deskriptorhaps als ein großes Array, das alle erforderlichen Deskriptoren an festen bekannten Speicherorten enthält. Anschließend muss der Draw-Aufruf nur einen Satz von Konstanten empfangen, bei denen es sich um die Indizes im Array handelt, in dem die Deskriptoren verwendet werden müssen.

Eine weitere Optimierung besteht in der Sicherstellung, dass Stammkonstatoren und Stammdeskriptoren diejenigen enthalten, die sich am häufigsten ändern, anstatt Konstanten im Deskriptor-Heap zu platzieren. Für die meisten Hardware ist dies eine effiziente Möglichkeit, Konstanten zu behandeln.

In der Praxis kann eine Grafik-Engine in verschiedenen Situationen eine andere Strategie verwenden und Elemente jeder Strategie kombinieren, um die jeweiligen Zeichnungsanforderungen zu erfüllen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




