---
description: 'Der zweite Schritt in einem com+-Anwendungs Entwurfsprozess besteht darin, das konzeptionelle Modell in die logischen Ebenen der dreistufigen Architektur zu unterbrechen: die Präsentationsebene oder die Benutzerdienste. die mittlere Ebene oder Unternehmens Dienste; und die Datenebene oder Datendienste. Wenn Sie mit der dreistufigen Architektur nicht vertraut sind, finden Sie unter Verwenden eines Three-Tier Architekturmodells Weitere Informationen.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'Das logische Modell: Anwendungs Definition und-Planung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb09b0d377fcd9bf5e2319868f4006b5dbfce75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127544"
---
# <a name="the-logical-model-application-definition-and-planning"></a>Das logische Modell: Anwendungs Definition und-Planung

Der zweite Schritt in einem com+-Anwendungs Entwurfsprozess besteht darin, das konzeptionelle Modell in die logischen Ebenen der dreistufigen Architektur zu unterbrechen: die *Präsentationsebene* oder die Benutzerdienste. die *mittlere Ebene* oder Unternehmens Dienste; und die *Datenebene* oder Datendienste. Wenn Sie mit der dreistufigen Architektur nicht vertraut sind, finden Sie unter [Verwenden eines Three-Tier Architekturmodells](using-a-three-tier-architecture-model.md)Weitere Informationen.

Beginnen Sie den Prozess, indem Sie das konzeptionelle Modell nach Substantiven und Verben betrachten. Die Nomen können häufig in Geschäftsobjekte (Klassen) übersetzt werden, und die zugeordneten Verben können in Aktionen übersetzt werden (Methoden der Klassen). Obwohl es schwierig sein kann, alle Nomen als Geschäftsobjekte zu definieren, werden Ausfälle oder Fehler durch den Zeitpunkt der Fertigstellung des logischen Modells offensichtlich.

Die meisten Geschäftsobjekte werden auf der Unternehmens Dienst Ebene erstellt, wobei die restlichen Objekte zwischen den Benutzeroberflächen Objekten in der Benutzer Dienst Ebene und den Datenobjekten auf der Ebene der Datendienste aufgeteilt werden. Beachten Sie beim Erstellen eines logischen Modells mit der dreistufigen Architektur Folgendes:

-   Einige der Nomen im konzeptionellen Entwurf stellen nicht die eigentlichen physischen Datenelemente dar, können aber eine Aktion im System oder in der Rolle eines Geschäftsobjekts im System darstellen. Ein Geschäftsobjekt kann auch ein Dienst sein, der eine bestimmte Art von Systemsteuerung ausführt, z. b. eine Anmelde-ID für die Sicherheit.
-   Vermeiden Sie es, vage Geschäftsobjekte zu erstellen, indem Sie im [konzeptionellen Modell](the-conceptual-model--application-requirements.md)"zwischen den Zeilen lesen". Diese Geschäftsobjekte sind möglicherweise nicht korrekt, und Sie sollten Sie sorgfältig in Erwägung ziehen, bevor Sie Sie in das logische Modell einschließen. Wenn Sie richtig angezeigt werden, fügen Sie Sie explizit dem konzeptionellen Modell hinzu.
-   Vermeiden Sie das Erstellen von Geschäftsobjekten, die dieselben Informationen oder Funktionen ausdrücken. Duplizierung kann in Bezug auf die Anwendungs Geschwindigkeit und-Leistung kostspielig sein.
-   Bestimmen von Objektabhängigkeiten. Einige Nomen im konzeptionellen Modell können einfach Attribute anderer Geschäftsobjekte sein. Entscheiden Sie, ob das Attribut unabhängig vorhanden sein kann. Wenn dies der Fall ist, sollte es ein eigenes Geschäftsobjekt werden. Wenn dies nicht der Fall ist, sollte Sie mit dem entsprechenden Geschäftsobjekt kombiniert werden.
-   Vermeiden Sie das Erstellen von Geschäftsobjekten, die zu viel versuchen. Das Überladen von Geschäftsobjekten kann bedeuten, dass mehr Zeit für die Trennung von Code aufgewendet wird und ein Wartungsaufwand entstehen kann. Unterschiedliche Objekte im konzeptionellen Modell sollten nicht kombiniert werden. Sie sollten separate Geschäftsobjekte verbleiben. Sie können alle Ähnlichkeiten behandeln, indem Sie Code verwenden, um die gemeinsamen Funktionen an ein Geschäftsobjekt zu delegieren.
-   Entfernen Sie alle Geschäftsobjekte, die in keinem Verwendungs Szenario verwendet werden. Wenn die Objekte für zukünftiges Wachstum vorgesehen sind, sollten Sie Sie nach Abschluss der ersten Anwendung implementieren.

An diesem Punkt können Sie mit der Betrachtung von Computern und Code beginnen. Bestimmen Sie aus diesen Unternehmens Diensten die Anzeige-und Eingabefunktionen, die Sie als Benutzerdienste bereitstellen müssen. Definieren Sie, welche Tabellen und gespeicherten Prozeduren als Datendienste bereitgestellt werden müssen. Um das logische Modell abzuschließen, definieren Sie die Schnittstellen für jeden Dienst, und schließen Sie die Definitionen der einzelnen Datenfelder und deren Validierungsregeln ein. Fügen Sie außerdem alle Funktionen, ihre Syntax und ihre Parameter ein.

Die Dienst-oder Objektdefinition sollte keinen Aspekt der physischen Implementierung enthalten. Ziel ist es, eine klare Richtlinie bereitzustellen, mit der die logischen Komponenten-Generatoren arbeiten und anderen Programmierern das Programmieren von Anwendungs Teilen ermöglichen können, die die Komponente verwenden können, bevor Sie tatsächlich abgeschlossen ist. Im logischen Modellentwurf sollten Sie jeden Bildschirm, jede Funktion und jedes Objekt dokumentieren. Fahren Sie erst mit dem physischen Modell oder der Implementierung fort, wenn Sie diese Kriterien erfüllen. Wenn Sie den Vorgang fortsetzen, während sich das konzeptionelle Modell und das logische Modell nicht in der Vereinbarung befinden, treten im Verlauf des Entwicklungs Zeitraums schwerwiegende Probleme auf.

Die inkrementelle Entwicklung einer COM+-Anwendung ist üblich. Dies umfasst das Erstellen einer Teilmenge der endgültigen, bekannten Komponenten und das Testen der einzelnen Anwendungsebenen: Client, Business und Daten Ebenen – bis zum Datenspeicher. Dieses Arbeitsmodell bietet Einblick in die zusätzlichen Anforderungen der Kunden-und Implementierungsaspekte. Dieses Arbeitsmodell wird häufig auf einem einzelnen Computer getestet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das konzeptionelle Modell: Anwendungsanforderungen](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Das physische Modell: Anwendungsarchitektur](the-physical-model--application-architecture.md)
</dt> <dt>

[Verwenden eines Three-Tier-Architekturmodells](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



