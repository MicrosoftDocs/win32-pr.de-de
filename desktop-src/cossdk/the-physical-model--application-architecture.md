---
description: Nachdem die konzeptionellen und logischen Modelle fertiggestellt wurden, können Sie Entscheidungen über die physische Implementierung der Anwendung treffen.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Das physische Modell: Anwendungsarchitektur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127541"
---
# <a name="the-physical-model-application-architecture"></a>Das physische Modell: Anwendungsarchitektur

Nachdem die konzeptionellen und logischen Modelle fertiggestellt wurden, können Sie Entscheidungen über die physische Implementierung der Anwendung treffen. Um das physische Modell zu erstellen, müssen Sie wissen, wo sich die verschiedenen Dienste der Anwendung befinden sollten und wie Sie implementiert werden sollen. Zu bestimmen, wo sich verschiedene Dienste befinden, sollte vor der Implementierung der Dienste stehen.

Eine grundlegende Regel, die festlegt, wo sich verschiedene Dienste befinden, ist Folgendes: Platzieren Sie die Komponente, in der Sie verwendet wird. Wenn z. b. eine Komponente Informationen für den Basis Client anzeigt, muss Sie auf dem Computer des Benutzers angezeigt werden. Wenn eine Komponente Informationen vom Basis Client überprüft, sollte Sie sich auch auf dem Computer des Basis Clients befinden. Wenn eine Komponente Informationen in einer-Datenbank aktualisiert, sollte Sie sich auf dem Datenbankserver befinden.

Es gibt natürlich weitere Überlegungen, die Ausnahmen zu dieser Regel machen. Leistungs-und Sicherheitsprobleme können auch vorschreiben, wo sich eine Komponente befindet. Beachten Sie Folgendes:

-   Wird eine Komponente häufig geändert, sodass die Verteilung von Updates erschwert wird?
-   Wird die Komponente von anderen Anwendungen, z. b. einer allgemeinen Sicherheits Überprüfungs Komponente, verwendet?
-   Nimmt die Komponente lange Berechnungen vor oder führt Funktionen wie z. b. Drucken aus, die auf einen Server ausgelagert werden können?
-   Kann die Sicherheit einer Komponente durch die Platzierung auf einem Server verbessert werden?

Wenn Sie die Komponenten einer Anwendung ordnungsgemäß suchen, können Sie das Entwicklungsteam auch vor kostspieligen neuzustellungen isolieren, wenn sich das System oder der Speicherort der Daten ändert. Wenn Sie z. b. die Datenzugriffs Regeln in einer Datenschicht anstatt in gespeicherten Prozeduren platzieren, kann die Anwendung leichter von der Abhängigkeit von einem bestimmten DBMS isoliert werden. Nicht nur die Änderungen sind eingeschränkt, und die Tests werden getrennt, aber Datenquellen können geändert werden, und Daten können verteilt werden, ohne dass die Anwendung grundsätzlich geändert werden muss.

Zum Schluss sollte das Auffinden von Komponenten die Effizienz des Systems ausnutzen. Es ist Zeit und kostengünstig, Geschäftsobjekte an zentralen Orten im Netzwerk zu platzieren. -Objekte können von-Anwendungen gemeinsam genutzt werden. Komponententests können vor der Bereitstellung von Komponenten ausgeführt werden. Wartungskosten können auch verringert werden, da Regeländerungen nur an einem einzigen Punkt erfolgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das konzeptionelle Modell: Anwendungsanforderungen](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Das logische Modell: Anwendungs Definition und-Planung](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



