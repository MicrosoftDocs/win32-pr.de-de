---
description: Objektpooling ist ein automatischer, von COM+ bereitgestellter Dienst, mit dem Sie eine Komponente so konfigurieren können, dass Instanzen von sich selbst in einem Pool aktiv bleiben und von jedem Client verwendet werden können, der die Komponente anfordert.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: COM+-Objektpoolingkonzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 836dd6f29c2f0bd120843a1a93763d46cb51224966f255251f7e3bfb4c7fa66a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129142"
---
# <a name="com-object-pooling-concepts"></a>COM+-Objektpoolingkonzepte

Objektpooling ist ein automatischer, von COM+ bereitgestellter Dienst, mit dem Sie eine Komponente so konfigurieren können, dass Instanzen von sich selbst in einem Pool aktiv bleiben und von jedem Client verwendet werden können, der die Komponente anfordert. Sie können den Pool, der für eine bestimmte Komponente verwaltet wird, administrativ konfigurieren und überwachen, indem Sie Merkmale wie pool size und creation request time-out values angeben. Wenn die Anwendung ausgeführt wird, verwaltet COM+ den Pool für Sie und verarbeitet die Details der Objektaktivierung und -wiederverwendung gemäß den von Ihnen angegebenen Kriterien.

Sie können erhebliche Leistungs- und Skalierungsvorteile erzielen, indem Sie Objekte auf diese Weise wiederverwenden, insbesondere, wenn sie geschrieben werden, um die Wiederverwendung in vollem Umfang zu nutzen. Mit dem Objektpooling profitieren Sie von den folgenden Vorteilen:

-   Sie können die Objektnutzungszeit für jeden Client beschleunigen und zeitaufwändige Initialisierung und Ressourcenerfassung aus der tatsächlichen Arbeit herausholen, die das Objekt für Clients ausführt.
-   Sie können die Kosten für den Erwerb teurer Ressourcen auf alle Clients verteilen.
-   Sie können Objekte vorab zuordnen, wenn die Anwendung gestartet wird, bevor Clientanforderungen eingeht.
-   Sie können die Ressourcennutzung mit der Verwaltung von Verwaltungspools steuern, indem Sie z. B. eine geeignete maximale Poolebene festlegen. Sie können nur so viele Datenbankverbindungen geöffnet lassen, wie Sie über eine Lizenz verfügen.
-   Sie können Pooling administrativ konfigurieren, um die verfügbaren Hardwareressourcen optimal zu nutzen. Sie können die Poolkonfiguration problemlos anpassen, wenn sich die verfügbaren Hardwareressourcen ändern.
-   Sie können die Reaktivierungszeit für Objekte beschleunigen, die die [Just-In-Time-Aktivierung (JIT)](com--just-in-time-activation.md)verwenden, während Sie bewusst steuern, wie Ressourcen clients zugewiesen werden.

## <a name="writing-poolable-objects"></a>Schreiben von poolfähigen Objekten

Poolfähige Objekte müssen bestimmte Anforderungen erfüllen, damit eine einzelne Objektinstanz von mehreren Clients verwendet werden kann. Sie können z. B. weder den Clientzustand noch threadaffin sein. Transaktionsobjekte haben auch besondere Anforderungen, da verwaltete Ressourcen, die von einem pooled-Objekt gehalten werden, manuell in einer Transaktion eingetragen werden müssen.

Poolobjekte können [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) implementieren, um zu steuern, wie sie wiederverwendet werden. Dadurch können sie die Initialisierung durchführen, wenn sie in einem bestimmten Kontext aktiviert sind, um alle Clientstatus bei deaktivierung zu bereinigen und anzugeben, wann sie sich in einem nicht wiederverwendbaren Zustand befinden.

Häufig ist es hilfreich, poolfähige Objekte auf etwas generische Weise zu schreiben, damit sie mit einer Konstruktorzeichenfolge administrativ angepasst werden können. Beispielsweise kann ein Objekt so geschrieben werden, dass es eine generische ODBC-Verbindung enthält, wobei ein bestimmter DSN in einer Konstruktorzeichenfolge administrativ angegeben ist.

Die Themen in diesem Abschnitt, die in der folgenden Tabelle beschrieben werden, enthalten Informationen zur Funktionsweise von Objektpooling in COM+ sowie Informationen zum Schreiben, Konfigurieren und Implementieren von poolfähigen Objekten.



| Thema                                                                                                 | Beschreibung                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Funktionsweise von Objektpooling](how-object-pooling-works.md)<br/>                                   | Stellt grundlegende Konzepte vor.<br/>                                                                      |
| [Verbessern der Leistung mit Objektpooling](improving-performance-with-object-pooling.md)<br/> | Stellt spezifische Details zur effektivsten Verwendung des Objektpoolings bereit.<br/>                 |
| [Anforderungen für poolfähige Objekte](requirements-for-poolable-objects.md)<br/>                 | Enthält Details zum Schreiben eines Objekts, das in einem Pool zusammengefasst werden soll.<br/>                              |
| [Pooling von Transaktionsobjekten](pooling-transactional-objects.md)<br/>                         | Stellt Details zu den speziellen Anforderungen bereit, die für poolfähige Transaktionsobjekte gelten.<br/> |
| [Steuern der Lebensdauer und des Zustands von Objekten](controlling-object-lifetime-and-state.md)<br/>         | Beschreibt, wie Poolobjekte implementiert werden können, um zu steuern, wie sie wiederverwendet werden.<br/>               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Objektpoolingtasks](com--object-pooling-tasks.md)
</dt> </dl>

 

 




