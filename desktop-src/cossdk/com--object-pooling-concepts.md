---
description: Object Pooling ist ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine Komponente so konfigurieren können, dass Instanzen von selbst in einem Pool aktiv gehalten werden und von jedem Client verwendet werden können, der die Komponente anfordert.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Konzepte für COM+-Objekt Pooling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393014"
---
# <a name="com-object-pooling-concepts"></a>Konzepte für COM+-Objekt Pooling

Object Pooling ist ein von com+ bereitgestellter automatischer Dienst, mit dem Sie eine Komponente so konfigurieren können, dass Instanzen von selbst in einem Pool aktiv gehalten werden und von jedem Client verwendet werden können, der die Komponente anfordert. Sie können den Pool, der für eine bestimmte Komponente verwaltet wird, administrativ konfigurieren und überwachen, indem Sie Merkmale wie z. b. Poolgröße und Timeout Werte für Erstellungs Anforderungen angeben. Wenn die Anwendung ausgeführt wird, verwaltet com+ den Pool für Sie und verarbeitet die Details der Objekt Aktivierung und-Wiederverwendung gemäß den von Ihnen angegebenen Kriterien.

Sie können sehr bedeutende Leistungs-und Skalierungs Vorteile erzielen, indem Sie Objekte auf diese Weise wieder verwenden. Dies gilt insbesondere dann, wenn Sie geschrieben werden, um die Wiederverwendung zu nutzen. Mit dem Objekt Pooling profitieren Sie von folgenden Vorteilen:

-   Sie können die Objekt Verwendungs Zeit für jeden Client beschleunigen und zeitaufwändige Initialisierung und Ressourcen Erfassung von der eigentlichen Arbeit, die das Objekt für Clients durchführt, gestalten.
-   Sie können die Kosten für den Erwerb kostspieliger Ressourcen auf allen Clients freigeben.
-   Sie können Objekte vorab zuordnen, wenn die Anwendung gestartet wird, bevor Client Anforderungen eingehen.
-   Sie können die Ressourcenverwendung mit der Verwaltung administrativer Pools steuern, indem Sie beispielsweise eine geeignete maximale Poolebene festlegen, können Sie nur so viele Datenbankverbindungen öffnen, wie Sie über eine Lizenz für verfügen.
-   Sie können Pooling administrativ konfigurieren, um die verfügbaren Hardware Ressourcen optimal zu nutzen. Sie können die Pool Konfiguration problemlos als verfügbare Hardware Ressourcen ändern.
-   Sie können die Reaktivierungs Zeit für Objekte beschleunigen, die die [Just-in-time (JIT)-Aktivierung](com--just-in-time-activation.md)verwenden, während Sie absichtlich steuern, wie Ressourcen für Clients dediziert werden.

## <a name="writing-poolable-objects"></a>Schreiben von in einem Pool fähigen Objekten

In Poolable-Objekten müssen bestimmte Anforderungen erfüllt werden, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann. Beispielsweise können Sie den Client Zustand nicht speichern oder eine Thread Affinität aufweisen. Für Transaktions Objekte gelten auch bestimmte Anforderungen, da verwaltete Ressourcen, die von einem in einem Pool zusammengefassten Objekt aufbewahrt werden, manuell in eine Transaktion eingetragen werden müssen.

In einem Pool zusammengefasste Objekte können [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) implementieren, um die Wiederverwendung zu steuern. Dies ermöglicht es Ihnen, eine Initialisierung durchzuführen, wenn Sie in einem bestimmten Kontext aktiviert wird, um den Client Zustand bei der Deaktivierung zu bereinigen und um anzugeben, dass Sie sich in einem nicht wiederverwendbaren Zustand befinden.

Häufig ist es sinnvoll, in einer etwas generischen Weise beim-Objekte zu schreiben, sodass Sie mit einer Konstruktorzeichenfolge administrativ angepasst werden können. Beispielsweise kann ein Objekt so geschrieben werden, dass es eine generische ODBC-Verbindung enthält, wobei eine bestimmte DSN administrativ in einer Konstruktorzeichenfolge angegeben ist.

Die Themen in diesem Abschnitt, die in der folgenden Tabelle beschrieben werden, enthalten Informationen zur Funktionsweise von Objekt Pooling in com+ sowie Informationen zum Schreiben, konfigurieren und Implementieren von in einem Pool fähigen Objekten.



| Thema                                                                                                 | BESCHREIBUNG                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Funktionsweise des Objekt Pooling](how-object-pooling-works.md)<br/>                                   | Stellt grundlegende Konzepte dar.<br/>                                                                      |
| [Verbessern der Leistung durch Objekt Pooling](improving-performance-with-object-pooling.md)<br/> | Bietet spezifische Details zur optimalen Verwendung des Objekt Pools.<br/>                 |
| [Anforderungen für in einem Pool Bare Objekte](requirements-for-poolable-objects.md)<br/>                 | Bietet ausführliche Informationen zum Schreiben eines Objekts, das in einem Pool zusammengefasst werden soll.<br/>                              |
| [Pooling von transaktionalen Objekten](pooling-transactional-objects.md)<br/>                         | Enthält Details zu den speziellen Anforderungen, die für in einem Pool ausführbare Transaktions Objekte gelten.<br/> |
| [Steuern der Objekt Lebensdauer und des Zustands](controlling-object-lifetime-and-state.md)<br/>         | Beschreibt, wie in einem Pool zusammengefasste Objekte implementiert werden können, um die Wiederverwendung zu steuern.<br/>               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-objektpoolingaufgaben](com--object-pooling-tasks.md)
</dt> </dl>

 

 




