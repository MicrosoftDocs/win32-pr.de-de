---
description: 'Der zweite Schritt in einem COM+-Anwendungsentwurfsprozess besteht im Aufbrechen des konzeptionellen Modells in die logischen Ebenen der Drei-Ebenen-Architektur: die Präsentationsebene oder Benutzerdienste. die mittlere Ebene oder Geschäftsdienste; und die Datenebene oder Datendienste. Wenn Sie mit der Architektur mit drei Ebenen nicht vertraut sind, finden Sie weitere Informationen unter Verwenden eines Three-Tier Architekturmodells.'
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: 'Logisches Modell: Anwendungsdefinition und -planung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19a493ebdacebac27edd291e747b5c42612f5fffd3ac7ea489f99b41de272b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120330"
---
# <a name="the-logical-model-application-definition-and-planning"></a>Logisches Modell: Anwendungsdefinition und -planung

Der zweite Schritt in einem COM+-Anwendungsentwurfsprozess besteht im Aufbrechen des konzeptionellen Modells in die logischen Ebenen der Drei-Ebenen-Architektur: die Präsentationsebene *oder* Benutzerdienste. die *mittlere Ebene* oder Geschäftsdienste; und die *Datenebene oder* Datendienste. Wenn Sie mit der Architektur mit drei Ebenen nicht vertraut sind, finden Sie weitere Informationen unter [Verwenden eines Three-Tier-Architekturmodells.](using-a-three-tier-architecture-model.md)

Beginnen Sie diesen Prozess, indem Sie das konzeptionelle Modell nach Nomen und Verben durchdrungen. Die Nomen können häufig in Geschäftsobjekte (Klassen) übersetzt werden, und die ihnen zugeordneten Verben können in Aktionen (Methoden der Klassen) übersetzt werden. Obwohl es schwierig sein kann, alle Nomen als Geschäftsobjekte zu definieren, werden Auslassungs- oder Fehlerfehler deutlich, wenn Sie das logische Modell abschließen.

Die meisten Geschäftsobjekte werden auf der Ebene der Geschäftsdienste gespeichert, und die restlichen Objekte werden zwischen Benutzeroberflächenobjekten auf der Ebene der Benutzerdienste und Datenobjekten in der Datendienstebene aufgeteilt. Beachten Sie beim Erstellen eines logischen Modells mit der Architektur mit drei Ebenen Folgendes:

-   Einige der Nomen im konzeptionellen Entwurf stellen keine tatsächlichen physischen Daten dar, können aber eine Aktion auf dem System oder die Rolle eines Geschäftsobjekts im System darstellen. Ein Geschäftsobjekt kann auch ein Dienst sein, der eine Art Von Systemsteuerung ausführt, z. B. eine Anmelde-ID aus Sicherheitsgründen.
-   Vermeiden Sie die Erstellung ungenauer Geschäftsobjekte, indem Sie im konzeptionellen Modell zwischen den [Zeilen lesen.](the-conceptual-model--application-requirements.md) Solche Geschäftsobjekte sind möglicherweise nicht korrekt, und Sie sollten sie sorgfältig berücksichtigen, bevor Sie sie in das logische Modell einplanen. Wenn sie korrekt erscheinen, fügen Sie sie explizit dem konzeptionellen Modell hinzu.
-   Vermeiden Sie das Erstellen von Geschäftsobjekten, die die gleichen Informationen oder Funktionen ausdrücken. Die Duplizierung kann in Bezug auf Anwendungsgeschwindigkeit und -leistung kostspielig sein.
-   Bestimmen Sie Objektabhängigkeiten. Einige Nomen im konzeptionellen Modell können einfach Attribute anderer Geschäftsobjekte sein. Entscheiden Sie, ob das Attribut unabhängig voneinander vorhanden sein kann. Wenn ja, sollte es sein eigenes Geschäftsobjekt werden. Wenn dies nicht der Dert ist, sollte es mit dem entsprechenden Geschäftsobjekt kombiniert werden.
-   Vermeiden Sie das Erstellen von Geschäftsobjekten, die versuchen, zu viel zu tun. Das Überladen von Geschäftsobjekten kann zu einer späteren Trennung von Code führen und zu Wartungsbebrechen führen. Unterschiedliche Objekte im konzeptionellen Modell sollten nicht kombiniert werden. sie sollten separate Geschäftsobjekte bleiben. Sie können alle Ähnlichkeiten behandeln, indem Sie Code verwenden, um ihre gemeinsamen Funktionen an ein Geschäftsobjekt zu delegieren.
-   Entfernen Sie alle Geschäftsobjekte, die in keinen Verwendungsszenarien verwendet werden. Wenn die Objekte für zukünftiges Wachstum vorgesehen sind, sollten Sie sie implementieren, nachdem die erste Anwendung abgeschlossen ist.

An diesem Punkt können Sie in Bezug auf die Computer und den Code denken. Bestimmen Sie in diesen Geschäftsdiensten die Anzeige- und Eingabefunktionen, die Sie als Benutzerdienste bereitstellen müssen. Definieren Sie, welche Tabellen und gespeicherten Prozeduren als Datendienste bereitgestellt werden müssen. Definieren Sie zum Abschließen des logischen Modells die Schnittstellen für jeden Dienst, und fügen Sie Definitionen der einzelnen Datenfelds und deren Validierungsregeln ein. Schließen Sie auch alle Funktionen, ihre Syntax und ihre Parameter ein.

Die Dienst- oder Objektdefinition sollte keinen Aspekt der physischen Implementierung enthalten. Die Absicht besteht in der Bereitstellung einer eindeutigen Richtlinie für die logischen Komponenten-Generatoren, um anderen Programmierern zu ermöglichen, Teile der Anwendung zu programmieren, die die Komponente möglicherweise verwenden, bevor sie tatsächlich abgeschlossen wird. Im Entwurf des logischen Modells sollten Sie jeden Bildschirm, jede Funktion und jedes Objekt dokumentieren. Fahren Sie erst mit dem physischen Modell oder der Implementierung fort, wenn Sie diese Kriterien erfüllen. Wenn Sie fortfahren, während das konzeptionelle Modell und das logische Modell nicht in Übereinstimmung sind, haben Sie später im Entwicklungszyklus schwerwiegende Probleme.

Die inkrementelle Entwicklung einer COM+-Anwendung ist üblich. Dies umfasst das Erstellen einer Teilmenge der endgültigen bekannten Komponenten und deren Tests über jede Ebene der Anwendung: Client-, Geschäfts- und Datenebenen bis hin zur Datenspeicherung. Dieses Funktionierende Modell bietet Einblicke in zusätzliche Anforderungen des Kunden und Überlegungen zur Implementierung. Dieses Funktionierende Modell wird häufig auf einem einzelnen Computer getestet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzeptionelles Modell: Anwendungsanforderungen](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Das physische Modell: Anwendungsarchitektur](the-physical-model--application-architecture.md)
</dt> <dt>

[Verwenden eines Three-Tier Architekturmodells](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



