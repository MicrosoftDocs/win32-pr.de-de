---
title: Informationen zu NDF
description: Das Netzwerkdiagnoseframework (Network Diagnostics Framework, NDF) reduziert die Beteiligung von Netzwerkadministratoren und Computerbenutzern, indem häufige Netzwerkprobleme behandelt werden, sobald diese auftreten.
ms.assetid: ac4ef38e-2818-4df4-b9f9-28326b974698
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2ce4890645e83c27e9c1cf594d7fbf4d81ce3d662a2b470ce652c71e7d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798902"
---
# <a name="about-ndf"></a>Informationen zu NDF

Das Netzwerkdiagnoseframework (Network Diagnostics Framework, NDF) reduziert die Beteiligung von Netzwerkadministratoren und Computerbenutzern, indem häufige Netzwerkprobleme behandelt werden, sobald diese auftreten. Durch die Verwendung der Diagnose- und Reparaturfunktionen von NDF benötigen Benutzer und Administratoren keine zusätzlichen Tools, um einige relativ häufige Probleme zu behandeln. NDF wird als Teil von Windows Vista, Windows Server 2008 und höher. Sie ist immer verfügbar, wenn ein System gestartet wird (aber nicht im Tresor ausgeführt werden kann).

## <a name="ndf-helper-classes"></a>NDF-Hilfsklassen

NDF enthält Hilfsklassen, die Netzwerkprobleme diagnostizieren, sobald sie auftreten. Jede dieser Hilfsklassen enthält die Logik, die für die Problembehandlung mindestens einer Komponente oder Anwendung erforderlich ist.

Einzelne NDF-Hilfsklassen führen die Hauptaufgaben der Diagnosesitzung aus. Jede Hilfsklasse ist eine Codeeinheit, die einen Integritätsaspekt der jeweiligen Netzwerkkomponente auswertet. Die Hilfsklasse versteht auch, welche möglichen Reparaturoptionen verfügbar sind, um die Integrität der Komponente wiederherzustellen, sowie die Kosten und risiken einer bestimmten Reparaturoption.

Jede Hilfsklasse wird in das gesamte Netzwerkdiagnoseframework eingedrungen. Wenn eine Netzwerkkomponente eines Drittanbieters eine NDF-Hilfsklasse enthält, können Probleme mit dieser Komponente von anderen Anwendungen mit NDF gelöst werden, ohne dass sie über spezifische Kenntnisse dieser Komponente verfügen müssen.

Die von Microsoft entwickelten Hilfsklassen stellen Softwareentwicklern die primäre Diagnose- und Reparaturfunktion zur Verfügung. Es gibt auch eine kleine Gruppe von APIs, mit denen Entwickler Netzwerkprobleme mithilfe von NDF diagnostizieren können. Weitere Informationen finden Sie unter NDF Functions and NDF Diagnostics Example [(NDF-Funktionen](ndf-functions.md) und [NDF-Diagnosebeispiel).](ndf-diagnostics-example.md)

## <a name="extensible-helper-classes"></a>Erweiterbare Hilfsklassen

In einigen Fällen können anwendungsentwickler spezifischere Diagnose- und Reparaturfunktionen zur Verfügung stellen.

Einige NDF-Hilfsklassen von Microsoft sind so konzipiert, dass sie erweitert werden können, um zusätzliche Diagnose- und Reparaturfunktionen zu bieten. Dies bedeutet, dass Entwickler Funktionen zur Verwendung von NDF-Diagnose- und Reparaturfunktionen zur Behandlung von Spezifischen Problemen mit ihrer Software oder Hardware verwenden können.

Beispielsweise stellt das Drahtlosteam von Microsoft eine erweiterbare Hilfsklasse zur Verfügung, mit der drahtlos arbeitende Drittanbieter spezifische Problembehandlungslogik für ihre spezifische Hardware und/oder Software hinzufügen können. Sie können dies tun, indem sie eine NDF-Hilfsklassenerweiterung entwickeln. Weitere Informationen finden Sie unter [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

Eine NDF-Hilfsklassenerweiterung erweitert definitionsgemäß die Funktionalität einer vorhandenen erweiterbaren Hilfsklasse. Wenn eine Hilfsklasse nicht erweiterbar ist, kann niemand eine Erweiterung für diese Hilfsklasse schreiben.

## <a name="benefits-of-helper-class-extensions"></a>Vorteile von Hilfsklassenerweiterungen

NDF bietet verschiedene Vorteile, um die Verwendung durch Netzwerkkomponentenentwickler zu fördern. Am Anfang der Liste steht, dass Kunden von Anbietersoftware einige ihrer eigenen Problembehandlungsressourcen frei geben und die Gesamtbetriebskosten reduzieren. Eine gut geschriebene Hilfsklassenerweiterung bietet auch die folgenden Vorteile:

-   Ermöglicht es einem Team zu bestimmen, wann seine Komponente nicht die Ursache eines Konnektivitätsproblems ist. Beispielsweise wird das Netzwerk häufig für Konnektivitätsprobleme verantwortlich gemacht, die nicht tatsächlich das Ergebnis eines Ausfalls einer Netzwerkkomponente sind. Durch das Schreiben einer Hilfsklassenerweiterung kann ein Team eine bestimmte Komponente leichter als Ursache für einen Konnektivitätsfehler ausschließen.
-   Ermöglicht es einem Team, ein Problem innerhalb der Komponente schnell zu diagnostizieren und zu debuggen. Zeit für Debuggen und Problembehandlung kann beseitigt werden, wenn eine Hilfsklasse geschrieben wird, um alle standardmäßigen Diagnoseschritte durchzuführen, die ohnehin erforderlich wären.
-   Es entfällt die Notwendigkeit, einmalige Tools zum Diagnostizieren von Problemen zu schreiben und zu unterstützen. Eine Hilfsklasse kann das zentrale Repository für die Diagnosefunktionen und Methoden zum Sammeln von Informationen einer Komponente sein.
-   Stellt komponentenspezifische Diagnosen für Anwendungen zur Verfügung, ohne dass sie über direkte Kenntnisse über die Komponente verfügen müssen.

 

 




