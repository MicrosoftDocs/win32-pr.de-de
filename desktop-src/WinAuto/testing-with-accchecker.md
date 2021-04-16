---
title: Testen mit accchecker
description: Beschreibt den typischen Test Workflow, der accchecker integriert.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- Testen mit accchecker
- Accchecker, Testen des Workflows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515524"
---
# <a name="testing-with-accchecker"></a>Testen mit accchecker

Im folgenden Szenario werden die Schritte beschrieben, die Sie normalerweise beim Testen mit der-Zugriffsmethode ausführen.

> [!Note]  
> Wenn accchecker-Überprüfungs Routinen ausgeführt werden, kann die Benutzerinteraktion mit dem Host Computer einige Routinen stören. Es wird empfohlen, keine weitere Benutzerinteraktion auszuführen, bis die Zugriffs Überprüfung den Benutzer darüber benachrichtigt, dass alle Aufgaben vollständig sind.

 

1.  Ausführen von accchecker-Verifizierungen für eine bestimmte Zielanwendung oder ein bestimmtes Steuerelement Weitere Informationen finden Sie auf der [Registerkarte Überprüfungen](the-accchecker-graphical-user-interface.md).
    > [!Note]  
    > Die Zugriffs Prüfung untersucht nicht alle UI-Permutationen in einer Anwendung. Elemente, die in Steuerelementen wie Fenstern, Bereichen, Registerkarten und Menüs ausgeblendet sind, müssen manuell verfügbar gemacht werden.

     

2.  Überprüfen Sie das Fehlerprotokoll der Zugriffs Überprüfung, und bewerten oder selelieren Sie die Ergebnisse. Beheben Sie triviale Probleme, und protokollieren Sie gegebenenfalls schwerwiegende Fehler.
3.  Generieren Sie eine Unterdrückungs Datei für Fehler und Fehler, die bis zum Testen der Regression ignoriert werden können.
4.  Führen Sie accchecker-Überprüfungen mit der Unterdrückungs Datei und den anfänglichen Fehlerbehebungen erneut aus. Dies bietet eine Momentaufnahme der Probleme in der aktuellen Implementierung von Microsoft Active Accessibility und legt eine Baseline für Regressionstests fest.
5.  Integrieren Sie die accchecker-APIs und die Unterdrückungs Datei in ein automatisiertes Test Framework, um Regressionstests für Fehler zu überprüfen, die bei der anfänglichen Zugriffs Überprüfung protokolliert wurden
    > [!Note]  
    > Da Fehler behoben werden, sollte die Unterdrückungs Datei bei Bedarf geändert werden.

     

6.  Vergewissern Sie sich, dass in der Anwendung oder im Steuerelement keine Regressionen oder neuen Barrierefreiheits Fehler eingeführt wurden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




