---
description: Sie können Objekt Statistiken überwachen, während eine Anwendung ausgeführt wird. Auf diese Weise können Sie die Eigenschaften des Objekt Pools optimieren, um das Gleichgewicht der Leistung und Ressourcen zu erzielen, die Sie nutzen möchten.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Objekt Statistik überwachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342199"
---
# <a name="monitoring-object-statistics"></a>Objekt Statistik überwachen

Sie können Objekt Statistiken überwachen, während eine Anwendung ausgeführt wird. Auf diese Weise können Sie die Eigenschaften des Objekt Pools optimieren, um das Gleichgewicht der Leistung und Ressourcen zu erzielen, die Sie nutzen möchten.

Sie können den Status für alle Objekte überwachen, die für die Unterstützung von Objekt Statistiken und Ereignis Berichterstattung konfiguriert sind. Die Aktivierung von Objekt Statistiken hat einen sehr geringen Leistungs Aufwand zur Folge.

**So aktivieren Sie Objekt Statistiken**

1.  Klicken Sie im Detailbereich des Verwaltungs Programms Komponenten Dienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die Registerkarte **Aktivierung** .

3.  Aktivieren Sie zum Aktivieren von Objekt Statistiken für die Komponente unter **Aktivierungs Kontext** das Kontrollkästchen **Komponente unterstützt Ereignisse und Statistiken** .

**So überwachen Sie den Objektstatus**

1.  Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste den Ordner für die Anwendung, die die Komponenten enthält, die Sie überwachen möchten.

2.  Klicken Sie mit der rechten Maustaste auf den Ordner **Komponenten** , zeigen Sie auf **anzeigen**, und klicken Sie dann auf **Status Ansicht**. Im Detailbereich wird nun die Statusansicht für alle Komponenten in der Anwendung angezeigt. In der folgenden Tabelle werden die sechs Spalten in der Statusansicht beschrieben.

    

    | Column                        | BESCHREIBUNG                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifiziert eine bestimmte Komponente.<br/>                                                                                                                                                                                |
    | **Objekte**<br/>        | Zeigt die Anzahl der Objekte an, die zurzeit von Client verweisen aufbewahrt werden.<br/>                                                                                                                                       |
    | **Aktiviert**<br/>      | Zeigt die Anzahl der Objekte an, die derzeit aktiviert sind. <br/>                                                                                                                                                      |
    | **Pool**<br/>         | Zeigt die Gesamtanzahl der Objekte, die vom Pool erstellt wurden, einschließlich verwenener Objekte und deaktivierter Objekte.<br/>                                                                                      |
    | **Im-Befehl**<br/>        | Identifiziert Objekte im-Befehl.<br/>                                                                                                                                                                                     |
    | **Aufruf Zeit (MS)**<br/> | Zeigt die durchschnittliche Aufruf Dauer (in Millisekunden) der in den letzten 20 Sekunden (bis zu 20 aufrufen) erfolgten Methodenaufrufe an. Die Aufruf Zeit wird beim Objekt gemessen und umfasst nicht die Zeit, die zum Durchlaufen des Netzwerks verwendet wird.<br/> |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren einer Komponente, die in einem Pool zusammengefasst werden soll](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




