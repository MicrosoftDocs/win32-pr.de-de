---
title: Testen mit AccChecker
description: Beschreibt den typischen Testworkflow, der AccChecker enthält.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- Testen mit AccChecker
- AccChecker, Testworkflow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addf725431a17a9b63376dfc3fc7ef8563a1737c9867b950f09eb123bf7daf18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795510"
---
# <a name="testing-with-accchecker"></a>Testen mit AccChecker

Im folgenden Szenario werden die Schritte beschrieben, die Sie normalerweise beim Testen mit AccChecker ausführen.

> [!Note]  
> Wenn AccChecker-Überprüfungsroutinen ausgeführt werden, kann die Benutzerinteraktion mit dem Hostcomputer einige Routinen beeinträchtigen. Es wird empfohlen, erst dann eine weitere Benutzerinteraktion durchzuführen, wenn AccChecker den Benutzer darüber informiert, dass alle Aufgaben abgeschlossen sind.

 

1.  Führen Sie AccChecker-Überprüfungen für eine bestimmte Zielanwendung oder ein bestimmtes Zielsteuerelement aus. Weitere Informationen finden Sie unter [Registerkarte "Überprüfungen".](the-accchecker-graphical-user-interface.md)
    > [!Note]  
    > AccChecker untersucht nicht alle Benutzeroberflächenpermutationen in einer Anwendung. Elemente, die in Steuerelementen wie Fenstern, Bereichen, Registerkarten und Menüs ausgeblendet sind, müssen manuell verfügbar gemacht werden.

     

2.  Untersuchen Sie das AccChecker-Fehlerprotokoll, und bewerten oder selektieren Sie die Ergebnisse. Beheben Sie triviale Probleme, und protokollieren Sie schwerwiegende Fehler nach Bedarf.
3.  Generieren Sie eine Unterdrückungsdatei für Fehler und Fehler, die bis zu Regressionstests ignoriert werden können.
4.  Führen Sie AccChecker-Überprüfungen mit der Unterdrückungsdatei und anfänglichen Fehlerbehebungen erneut aus. Dadurch wird eine Momentaufnahme der Probleme in der aktuellen Implementierung von Microsoft Active Accessibility erstellt und eine Baseline für Regressionstests erstellt.
5.  Integrieren Sie die AccChecker-APIs und die Unterdrückungsdatei in ein automatisiertes Testframework für Regressionstests bei Fehlern, die bei den anfänglichen AccChecker-Überprüfungen protokolliert wurden.
    > [!Note]  
    > Wenn Fehler behoben werden, sollte die Unterdrückungsdatei nach Bedarf geändert werden.

     

6.  Vergewissern Sie sich, dass keine Regressionen oder neue Barrierefreiheitsfehler in die Anwendung oder das Steuerelement eingeführt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




