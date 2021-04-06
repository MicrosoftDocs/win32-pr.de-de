---
title: Informationen zu NDF
description: Das Netzwerk Diagnose Framework (ndf) reduziert die Einbindung von Netzwerkadministratoren und Computerbenutzern, indem häufige Netzwerkprobleme behandelt werden.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b638298fe321d314815c74fced49d3dfb623022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709791"
---
# <a name="about-ndf"></a>Informationen zu NDF

Das Netzwerk Diagnose Framework (ndf) reduziert die Einbindung von Netzwerkadministratoren und Computerbenutzern, indem häufige Netzwerkprobleme behandelt werden. Durch die Verwendung der Diagnose-und Reparaturfunktionen von NDF benötigen Benutzer und Administratoren keine zusätzlichen Tools, um einige relativ häufige Probleme zu behandeln. NDF wird als Teil von Windows Vista, Windows Server 2008 und höher ausgeliefert. Sie ist immer verfügbar, wenn ein System gestartet wird (aber nicht im abgesicherten Modus ausgeführt werden kann).

## <a name="ndf-helper-classes"></a>NDF-Hilfsklassen

NDF umfasst Hilfsklassen, mit denen Netzwerkprobleme beim Auftreten diagnostiziert werden. Jede dieser Hilfsklassen enthält die erforderliche Logik zur Behandlung von Problemen mit mindestens einer Komponente oder Anwendung.

Einzelne NDF-Hilfsklassen führen die primären Aufgaben der Diagnose Sitzung aus. Jede Hilfsklasse ist eine Einheit von Code, die entwickelt wurde, um einen Integritäts Aspekt der jeweiligen Netzwerkkomponente auszuwerten. Die Hilfsklasse versteht auch, welche möglichen Reparatur Optionen zum Wiederherstellen der Integrität der Komponente verfügbar sind, sowie die Kosten und Risiken einer bestimmten Reparaturoption.

Jede Hilfsklasse wird in das gesamte Netzwerk Diagnose-Framework eingebunden. Wenn eine Netzwerkkomponente eines Drittanbieters eine NDF-Hilfsklasse enthält, können Probleme mit dieser Komponente durch andere Anwendungen gelöst werden, die NDF verwenden, ohne dass Sie über bestimmte Kenntnisse dieser Komponente verfügen müssen.

Die von Microsoft entwickelten Hilfsklassen stellen Softwareentwicklern die primäre Diagnose-und Reparatur Funktionalität zur Verfügung. Es gibt auch einen kleinen Satz von APIs, mit denen Entwickler Netzwerkprobleme mithilfe von NDF diagnostizieren können. Weitere Informationen finden Sie unter [NDF-Funktionen](ndf-functions.md) und Beispiel für die [NDF-Diagnose](ndf-diagnostics-example.md).

## <a name="extensible-helper-classes"></a>Erweiterbare Hilfsklassen

In einigen Fällen können Anwendungsentwickler spezifischere Diagnose-und Reparaturfunktionen bereitstellen.

Einige der NDF-Hilfsklassen von Microsoft sind darauf ausgelegt, erweitert zu werden, um zusätzliche Diagnose-und Reparaturfunktionen bereitzustellen. Dies bedeutet, dass Entwickler Funktionen für die Verwendung von NDF-Diagnose-und Reparaturfunktionen zum Beheben von Problemen mit Ihrer Software oder Hardware verwenden können.

Beispielsweise stellt das drahtlose Team bei Microsoft eine erweiterbare Hilfsklasse bereit, die es Drittanbietern ermöglicht, eine spezifische Problem Behandlungs Logik für Ihre bestimmte Hardware und/oder Software hinzuzufügen. Hierzu können Sie eine NDF-Hilfsklassen Erweiterung entwickeln. Weitere Informationen finden Sie unter [802,11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

Eine NDF-Hilfsklassen Erweiterung erweitert definitionsgemäß die Funktionalität einer vorhandenen Extensible Helper-Klasse. Wenn eine Hilfsklasse nicht erweiterbar ist, kann niemand eine Erweiterung für diese Hilfsklasse schreiben.

## <a name="benefits-of-helper-class-extensions"></a>Vorteile von Hilfsklassen Erweiterungen

NDF bietet verschiedene Vorteile, um die Verwendung durch Entwickler von Netzwerkkomponenten zu unterstützen. Ganz oben in der Liste ist, dass Kunden der Hersteller Software einige ihrer Ressourcen zur Problembehandlung freigeben und die Gesamtbetriebskosten senken. Eine gut geschriebene Hilfsklassen Erweiterung bietet außerdem die folgenden Vorteile:

-   Ermöglicht einem Team, zu bestimmen, wann die Komponente nicht die Ursache eines Konnektivitätsproblems ist. Beispielsweise wird das Netzwerk häufig für Konnektivitätsprobleme verantwortlich sein, die nicht tatsächlich das Ergebnis eines Fehlers bei der Netzwerkkomponente sind. Durch das Schreiben einer Hilfsklassen Erweiterung kann ein Team eine bestimmte Komponente einfacher als Ursache für einen Verbindungsfehler ausschließen.
-   Ermöglicht einem Team, ein Problem innerhalb der Komponente schnell zu diagnostizieren und zu debuggen. Die Zeit, die für das Debuggen und die Problembehandlung aufgewendet wurde, kann eliminiert werden, wenn eine Hilfsklasse geschrieben wurde, um alle erforderlichen Standard Diagnose Schritte auszuführen.
-   Entfällt das Schreiben und unterstützen von einmaligen Tools, um Probleme zu diagnostizieren. Eine Hilfsklasse kann das zentrale Repository für die Diagnosefunktionen einer Komponente und für das Sammeln von Informationen sein.
-   Macht die Komponenten spezifische Diagnose für Anwendungen verfügbar, ohne dass Sie über direkte Kenntnisse über die Komponente verfügen müssen.

 

 




