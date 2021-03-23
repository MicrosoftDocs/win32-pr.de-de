---
title: Übersicht über deskriptorheaps
description: Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipeline Zustands Objekts (PSO) sind, wie z. b. Shader-Ressourcen Sichten (Srvs), ungeordnete Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers.
ms.assetid: 14561E77-44E0-4A58-8456-F40D59ECA175
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8bf720ebb71d016457fa4383a8d33aa62e2eee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103404"
---
# <a name="descriptor-heaps-overview"></a>Übersicht über deskriptorheaps

Deskriptorheaps enthalten viele Objekttypen, die nicht Teil eines Pipeline Zustands Objekts (PSO) sind, wie z. b. Shader-Ressourcen Sichten (Srvs), ungeordnete Zugriffs Sichten (UAVs), Konstante Puffer Ansichten (cbvs) und Samplers.

-   [Zweck der deskriptorheaps](#the-purpose-of-descriptor-heaps)
-   [Synchronisierung](#synchronization)
-   [Binding](#binding)
-   [Wechseln von Heaps](#switching-heaps)
-   [Bundles](#bundles)
-   [Verwaltung](#management)
-   [Verwandte Themen](#related-topics)

## <a name="the-purpose-of-descriptor-heaps"></a>Zweck der deskriptorheaps

Der primäre Zweck eines deskriptorheaps besteht darin, den größten Teil der Arbeitsspeicher Belegung zu umfassen, der zum Speichern der deskriptorspezifikationen von Objekttypen erforderlich ist, auf die sich Shader für einen großen Teil des Renderings als möglich (idealerweise ein ganzer Renderingbereich) beziehen. Wenn eine Anwendung wechselt, welche Texturen die Pipeline schnell von der API sieht, muss im deskriptorheap Speicherplatz vorhanden sein, um deskriptortabellen für jeden benötigten Status dynamisch zu definieren. Die Anwendung kann die Definitionen wieder verwenden, wenn die Ressourcen in einem anderen Objekt wieder verwendet werden, oder Sie können den Heap Bereich nur sequenziell zuweisen, wenn verschiedene Objekttypen gewechselt werden.

Deskriptorheaps erlauben auch einzelnen Softwarekomponenten, den deskriptorspeicher getrennt voneinander zu verwalten.

Alle Heaps sind für die CPU sichtbar. Die Anwendung kann auch anfordern, welche CPU-Zugriffs Eigenschaften ein deskriptorheap aufweisen soll (sofern vorhanden) – zusammen schreiben, Zurückschreiben usw. Apps können beliebig viele deskriptorheaps mit den gewünschten Eigenschaften erstellen. Apps haben immer die Möglichkeit, deskriptorheaps zu erstellen, die ausschließlich für stagingzwecke verwendet werden, deren Größe nicht eingeschränkt ist, sowie zum Kopieren in deskriptorheaps, die bei Bedarf für das Rendering verwendet werden.

Es gibt einige Einschränkungen in Bezug auf das, was sich im gleichen deskriptorheap befinden kann. CBV-, UAV-und SRV-Einträge können sich im gleichen deskriptorheap befinden. Allerdings können sampleneinträge keinen Heap mit CBV-, UAV-oder SRV-Einträgen freigeben. In der Regel gibt es zwei Sätze von deskriptorheaps, eine für die gemeinsamen Ressourcen und die zweite für Samplers.

Die Verwendung von deskriptorheaps durch Direct3D 12 spiegelt die meisten GPU-Hardware wider, d. h., dass Deskriptoren nur in deskriptorheaps verwendet werden müssen oder dass weniger Adressierungs Bits erforderlich sind, wenn diese Heaps verwendet werden. Direct3D 12 erfordert die Verwendung von deskriptorheaps, es gibt keine Möglichkeit, Deskriptoren an einer beliebigen Stelle im Arbeitsspeicher zu platzieren.

Deskriptorheaps können nur direkt von der CPU bearbeitet werden, es gibt keine Option zum Bearbeiten eines deskriptorheap durch die GPU.

## <a name="synchronization"></a>Synchronization

Der Inhalt des deskriptorheaps kann vor, während und nach dem Aufzeichnen von Befehlslisten, die auf ihn verweisen, geändert werden. Allerdings können Deskriptoren nicht geändert werden, während eine Befehlsliste, die zur Ausführung übermittelt wird, auf diesen Speicherort verweist, da dadurch eine Racebedingung aufgerufen werden kann.

## <a name="binding"></a>Bindung

Höchstens ein kombinierter CBV-/SRV-/UU--Heap und ein Sampler-Heap können gleichzeitig gebunden werden. Diese Heaps werden sowohl für die Grafik-als auch für die Compute-Pipelines gemeinsam genutzt (in ihren PSOs beschrieben).

## <a name="switching-heaps"></a>Wechseln von Heaps

Es ist zulässig, dass eine Anwendung Heaps in derselben Befehlsliste oder in verschiedenen Einstellungen mithilfe der [**setdescriptorheaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) -und [**Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) -APIs wechselt. Bei manchen Hardware kann dies ein kostspieliger Vorgang sein, der einen GPU-Stall erfordert, um alle Arbeiten zu leeren, die vom zurzeit gebundenen deskriptorheap abhängen. Wenn deskriptorheaps geändert werden müssen, sollten Sie daher versuchen, dies zu tun, wenn die GPU-Arbeitsauslastung relativ gering ist, was möglicherweise die Änderungen am Anfang einer Befehlsliste einschränkt.

## <a name="bundles"></a>Bundles

Bei Paketen kann nur ein Aufruf der [**setdescriptorheaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) -Methode erfolgen, und die festgelegten deskriptorheaps müssen genau denen der Befehlsliste entsprechen, die das Paket aufruft. Wenn das Paket keine deskriptortabellen ändert, müssen die deskriptorheaps nicht festgelegt werden.

Eine Liste der API-Aufrufe, die nicht mit Paketen verwendet werden können, finden Sie unter [Erstellen und Aufzeichnen von Befehlslisten und Paketen](recording-command-lists-and-bundles.md).

## <a name="management"></a>Verwaltung

Um alle Objekte in einer Szene zu erzeugen, werden viele Deskriptoren benötigt, und es gibt verschiedene Verwaltungsstrategien, die befolgt werden können.

Die grundlegendste Strategie besteht darin, einen neuen Bereich des deskriptorheap mit allen Anforderungen für den nächsten zeichnen-Befehl auszufüllen. Bevor Sie also den Draw-Befehl in der Befehlsliste ausgeben, wird ein deskriptortabellenzeiger auf den Anfang der neu aufgefüllten Tabelle festgelegt. Der Vorteil besteht darin, dass es nicht erforderlich ist, den Speicherort eines bestimmten Deskriptors im Heap aufzuzeichnen.

Der Nachteil dieser Strategie besteht darin, dass es möglicherweise viele Wiederholungen von Deskriptoren im deskriptorheap gibt, insbesondere wenn eine sehr ähnliche Szene gerendert wird und der deskriptorheap-Speicherplatz schnell aufgebraucht wird. Für diejenigen, die auf der GPU gerendert werden, und für diejenigen, die von der CPU aufgezeichnet werden, wäre es wahrscheinlich notwendig, Konflikte zu vermeiden. Alternativ kann ein unter Zuordnungs System verwendet werden.

Außerdem könnte das grundlegende System durch die sorgfältige Verwendung von überschneidenden deskriptortabellen von einem zeichnen-Befehl zum nächsten optimiert werden, sodass nur die neuen erforderlichen Deskriptoren hinzugefügt werden.

Eine effizientere Strategie als die Basis ist, deskriptorheaps mit Deskriptoren vorab auszufüllen, die für die Objekte (oder Materialien) erforderlich sind, die bekanntermaßen Teil der Szene sind. Die Idee besteht darin, dass es nur notwendig ist, die Deskriptortabelle zur zeichnungszeit festzulegen, da der deskriptorheap vorab aufgefüllt wird.

Eine Variation der vorab abfüllenden Strategie besteht darin, den deskriptorheap als ein riesiges Array zu behandeln, das alle erforderlichen Deskriptoren in den bekannten Speicherorten enthält. Dann benötigt der Draw-Befehl nur einen Satz von Konstanten, die die Indizes in das Array von sind, in dem die Deskriptoren verwendet werden müssen.

Eine weitere Optimierung besteht darin, sicherzustellen, dass Stamm Konstanten und Stamm Deskriptoren solche enthalten, die am häufigsten geändert werden, anstatt Konstanten im deskriptorheap zu platzieren. Für die meisten Hardware ist dies eine effiziente Methode zur Handhabung von Konstanten.

In der Praxis kann eine Grafik-Engine in unterschiedlichen Situationen eine andere Strategie verwenden und die Elemente jeder Strategie so kombinieren, dass Sie den jeweiligen Zeichnungs Anforderungen entsprechen.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Deskriptorheaps](descriptor-heaps.md)
</dt> </dl>

 

 




