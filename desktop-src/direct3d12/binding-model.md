---
title: Unterschiede im Bindungsmodell von Direct3D 11
description: Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, sie von anderen Verwaltungsaufgaben zu trennen. Dies stellt einige Anforderungen an die App, um bestimmte potenzielle Risiken zu bewältigen.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a625bd1b79766990658feba9bf18ddf7f46c3788ca20aea1de0b4ab80ae0a71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632521"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Unterschiede im Bindungsmodell von Direct3D 11

Eine der wichtigsten Entwurfsentscheidungen hinter der DirectX12-Bindung besteht darin, sie von anderen Verwaltungsaufgaben zu trennen. Dies stellt einige Anforderungen an die App, um bestimmte potenzielle Risiken zu bewältigen.

Der Hauptvorteil des D3D12-Bindungsmodells besteht darin, dass Es Apps ermöglicht, Texturbindungen häufig ohne hohe CPU-Leistungskosten zu ändern. Weitere Vorteile sind, dass Shader Zugriff auf eine sehr große Anzahl von Ressourcen haben, Shader nicht im Voraus wissen müssen, wie viele Ressourcen gebunden werden, und dass ein einheitliches Ressourcenbindungsmodell unabhängig vom Hardware- oder App-Inhaltsfluss verwendet werden kann.

Um die Leistung zu verbessern, erfordert das Bindungsmodell nicht, dass das System nachverfolgt, welche Bindungen eine App von der GPU angefordert hat, und es gibt eine saubere Integration zwischen Bindungs- und Multithreadbefehlslisten.

In den folgenden Abschnitten werden einige änderungen am Ressourcenbindungsmodell seit D3D11 aufgeführt.

-   [Speicherresidenzverwaltung getrennt von Bindung](#memory-residency-management-separated-from-binding)
-   [Objektlebensdauerverwaltung getrennt von Bindung](#object-lifetime-management-separated-from-binding)
-   [Nachverfolgung des Treiberressourcenstatus getrennt von der Bindung](#driver-resource-state-tracking-separated-from-binding)
-   [CPU GPU Mapped Memory Synchronization Separated From Binding](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Zugehörige Themen](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Speicherresidenzverwaltung getrennt von Bindung

Anwendungen haben explizite Kontrolle darüber, welche Oberflächen für die direkte Verwendung durch die GPU verfügbar sein müssen (als "resident" bezeichnet). Im Gegensatz dazu können sie andere Zustände auf Ressourcen anwenden, z. B. sie explizit nicht als "resident" festlegen oder das Betriebssystem für bestimmte Klassen von Anwendungen auswählen lassen, die einen minimalen Speicherbedarf erfordern. Der wichtige Punkt hier ist, dass die Verwaltung des Gebietsansässigen durch die Anwendung vollständig von der Art und Weise entkoppelt ist, wie sie Shadern Zugriff auf Ressourcen gewährt.

Die Entkopplung der Residencyverwaltung vom Mechanismus für den Zugriff von Shadern auf Ressourcen reduziert die System-/Hardwarekosten für das Rendering, da das Betriebssystem nicht ständig den lokalen Bindungszustand überprüfen muss, um zu wissen, was als "resident" gelten soll. Darüber hinaus müssen Shader nicht mehr wissen, auf welche genauen Oberflächen sie verweisen müssen, solange der gesamte Satz von möglicherweise zugänglichen Ressourcen im Voraus als "resident" festgelegt wurde.

## <a name="object-lifetime-management-separated-from-binding"></a>Objektlebensdauerverwaltung getrennt von Bindung

Im Gegensatz zu vorherigen APIs verfolgt das System keine Bindungen von Ressourcen an die Pipeline mehr nach. Dies wird verwendet, um dem System das Beibehalten von Ressourcen zu ermöglichen, die von der Anwendung freigegeben wurden, da weiterhin von ausstehenden GPU-Arbeiten auf sie verwiesen wird.

Vor dem Freigeben einer Ressource, z. B. einer Textur, müssen Anwendungen jetzt sicherstellen, dass die GPU den Verweis darauf abgeschlossen hat. Das bedeutet, bevor eine Anwendung eine Ressource sicher freigeben kann, muss die GPU die Ausführung der Befehlsliste abgeschlossen haben, die auf die Ressource verweist.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Nachverfolgung des Treiberressourcenstatus getrennt von der Bindung

Das System überprüft ressourcenbindungen nicht mehr, um zu verstehen, wann Ressourcenübergänge aufgetreten sind, die zusätzliche Treiber- oder GPU-Arbeit erfordern. Ein gängiges Beispiel für viele GPUs und Treiber ist das Wissen, wann eine Oberfläche von der Verwendung als Renderzielansicht (RTV) zu Shader Ressourcenansicht (SRV) wechselt. Anwendungen selbst müssen jetzt über dedizierte APIs ermitteln, wann Ressourcenübergänge stattfinden, die für das System ggf. wichtig sind.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>CPU GPU Mapped Memory Synchronization Separated From Binding

Das System überprüft ressourcenbindungen nicht mehr, um zu verstehen, ob das Rendering verzögert werden muss, da es von einer Ressource abhängt, die für den CPU-Zugriff zugeordnet, aber noch nicht zugeordnet wurde. Anwendungen sind jetzt dafür verantwortlich, CPU- und GPU-Arbeitsspeicherzugriffe zu synchronisieren. Um dies zu unterstützen, stellt das System Mechanismen bereit, mit denen die Anwendung den Ruhemodus eines CPU-Threads anfordern kann, bis die Arbeit abgeschlossen ist. Der Abruf kann auch durchgeführt werden, kann aber weniger effizient sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenbindung](resource-binding.md)
</dt> </dl>

 

 




