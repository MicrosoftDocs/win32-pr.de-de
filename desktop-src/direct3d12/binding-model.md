---
title: Unterschiede im Bindungs Modell von Direct3D 11
description: Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, Sie von anderen Verwaltungsaufgaben zu trennen. Dadurch sind einige Anforderungen an die APP erforderlich, um bestimmte potenzielle Gefahren zu verwalten.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104724"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Unterschiede im Bindungs Modell von Direct3D 11

Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, Sie von anderen Verwaltungsaufgaben zu trennen. Dadurch sind einige Anforderungen an die APP erforderlich, um bestimmte potenzielle Gefahren zu verwalten.

Der Hauptvorteil des D3D12-Bindungs Modells besteht darin, dass apps häufig Textur Bindungen ändern können, ohne dass die CPU-Leistung beeinträchtigt wird. Andere Vorteile sind, dass Shader auf eine sehr große Anzahl von Ressourcen zugreifen können, dass Shader nicht im Voraus wissen müssen, wie viele Ressourcen gebunden werden, und dass ein einheitliches Ressourcen Bindungs Modell unabhängig von der Hardware oder dem App-Inhalts Fluss verwendet werden kann.

Um die Leistung zu verbessern, erfordert das Bindungs Modell nicht, dass das System nachverfolgt, welche Bindungen die GPU von der APP angefordert hat, und es gibt eine saubere Integration zwischen Bindungen und Multithread-Befehlslisten.

In den folgenden Abschnitten werden einige der Änderungen am Ressourcen Bindungs Modell seit D3D11 aufgelistet.

-   [Verwaltung der Speicher Residenz durch Bindung getrennt](#memory-residency-management-separated-from-binding)
-   [Verwaltung der Objekt Lebensdauer getrennt von Bindung](#object-lifetime-management-separated-from-binding)
-   [Treiber Ressourcen-Statusüberwachung getrennt von Bindung](#driver-resource-state-tracking-separated-from-binding)
-   [CPU-GPU-zugeordnete Speicher Synchronisierung getrennt von Bindung](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Verwandte Themen](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Verwaltung der Speicher Residenz durch Bindung getrennt

Anwendungen können explizit steuern, welche Oberflächen verfügbar sein müssen, damit die GPU direkt verwendet werden muss (als "residente" bezeichnet). Im Gegensatz dazu können Sie andere Zustände auf Ressourcen anwenden, z. b. explizites Anfügen von Dateien oder das Betriebssystem für bestimmte Anwendungs Klassen, die einen minimalen Speicherbedarf erfordern. Der wichtigste Punkt hierbei ist, dass die Verwaltung des Residenten der Anwendung vollständig von der Verwaltung des Zugriffs auf Ressourcen für Shader entkoppelt ist.

Durch die Entkopplung der Residenz Verwaltung von dem Mechanismus zum Gewähren von Shadern auf Ressourcen werden die System-/Hardwarekosten für das Rendering reduziert, da das Betriebssystem den Zustand der lokalen Bindung nicht ständig überprüfen muss, um zu wissen, was der residente Außerdem müssen Shader nicht mehr wissen, auf welche exakten Oberflächen Sie möglicherweise verweisen müssen, solange der gesamte Satz von Ressourcen, auf die möglicherweise zugegriffen werden kann, bereits im Voraus verfügbar gemacht wurde.

## <a name="object-lifetime-management-separated-from-binding"></a>Verwaltung der Objekt Lebensdauer getrennt von Bindung

Im Gegensatz zu vorherigen APIs verfolgt das System keine Bindungen von Ressourcen mehr an die Pipeline. Dies wurde verwendet, um dem System zu ermöglichen, von der Anwendung freigegebene Ressourcen beizubehalten, da noch immer eine ausstehende GPU-Arbeit referenziert ist.

Vor dem Freigeben von Ressourcen, wie z. b. einer Textur, müssen Anwendungen nun sicherstellen, dass die GPU den Verweis abgeschlossen hat. Dies bedeutet, dass eine Anwendung, die eine Ressource sicher freigeben kann, die Ausführung der Befehlsliste, die auf die Ressource verweist, abgeschlossen haben muss.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Treiber Ressourcen-Statusüberwachung getrennt von Bindung

Das System überprüft Ressourcen Bindungen nicht mehr, um zu verstehen, wann Ressourcen Übergänge aufgetreten sind, die zusätzliche Treiber-oder GPU-Arbeiten erfordern. Ein gängiges Beispiel für viele GPUs und Treiber ist zu wissen, wenn eine Oberfläche von der Verwendung als renderzielansicht (RTV) zu Shader Ressourcenansicht (SRV) übergeht. Anwendungen selbst müssen jetzt ermitteln, wann Ressourcen Übergänge, die das System möglicherweise benötigt, über dedizierte APIs erfolgen.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>CPU-GPU-zugeordnete Speicher Synchronisierung getrennt von Bindung

Das System überprüft Ressourcen Bindungen nicht mehr, um zu verstehen, ob das Rendering verzögert werden muss, da es von einer Ressource abhängt, die für den CPU-Zugriff zugeordnet wurde, aber noch nicht zugeordnet wurde. Anwendungen sind jetzt in der Verantwortung, CPU-und GPU-Speicherzugriffe zu synchronisieren. Um dies zu unterstützen, stellt das System Mechanismen bereit, mit denen die Anwendung den Ruhezustand eines CPU-Threads anfordern kann, bis die Arbeit abgeschlossen ist. Der Abruf kann auch durchgeführt werden, kann jedoch weniger effizient sein.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> </dl>

 

 




