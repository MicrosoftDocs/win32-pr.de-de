---
description: Sie können Objektstatistiken überwachen, während eine Anwendung ausgeführt wird. Dadurch können Sie die Eigenschaften des Objektpools optimieren, um ein ausgewogenes Verhältnis zwischen Leistung und Ressourcen zu erzielen.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Überwachen von Objektstatistiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e58946953ef1688dcb44223522cc58ccd1195f07ec0173a0b75413fe441195f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070460"
---
# <a name="monitoring-object-statistics"></a>Überwachen von Objektstatistiken

Sie können Objektstatistiken überwachen, während eine Anwendung ausgeführt wird. Dadurch können Sie die Eigenschaften des Objektpools optimieren, um ein ausgewogenes Verhältnis zwischen Leistung und Ressourcen zu erzielen.

Sie können den Status für alle Objekte überwachen, die zur Unterstützung von Objektstatistiken und Ereignisberichten konfiguriert sind. Das Aktivieren von Objektstatistiken verursacht einen sehr geringen Leistungsaufwand.

**So aktivieren Sie Objektstatistiken**

1.  Klicken Sie im Detailbereich des Verwaltungstool Komponentendienste mit der rechten Maustaste auf die Komponente, die Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften.**

2.  Klicken Sie im Dialogfeld Komponenteneigenschaften auf die **Registerkarte Aktivierung.**

3.  Aktivieren Sie zum Aktivieren von Objektstatistiken für die Komponente unter **Aktivierungskontext** das Kontrollkästchen **Komponente unterstützt** Ereignisse und Statistiken.

**So überwachen Sie den Objektstatus**

1.  Öffnen Sie in der Konsolenstruktur des Verwaltungstool Komponentendienste den Ordner für die Anwendung, die die komponenten enthält, die Sie überwachen möchten.

2.  Klicken Sie mit der rechten Maustaste auf den Ordner **Komponenten,** zeigen Sie **auf Anzeigen,** und klicken Sie dann auf **Statusansicht**. Im Detailbereich wird nun die Statusansicht für alle Komponenten in der Anwendung angezeigt. In der folgenden Tabelle werden die sechs Spalten in der Statusansicht beschrieben.

    

    | Column                        | BESCHREIBUNG                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **ProgID**<br/>         | Identifiziert eine bestimmte Komponente.<br/>                                                                                                                                                                                |
    | **Objekte**<br/>        | Zeigt die Anzahl der Objekte an, die derzeit von Clientverweisen gehalten werden.<br/>                                                                                                                                       |
    | **Aktiviert**<br/>      | Zeigt die Anzahl der objekte an, die derzeit aktiviert sind. <br/>                                                                                                                                                      |
    | **Gebündelt**<br/>         | Zeigt die Gesamtanzahl der vom Pool erstellten Objekte an, einschließlich der objekte, die verwendet werden, und der deaktivierten Objekte.<br/>                                                                                      |
    | **In Call**<br/>        | Identifiziert Objekte im Aufruf.<br/>                                                                                                                                                                                     |
    | **Aufrufzeit (ms)**<br/> | Zeigt die durchschnittliche Aufrufdauer (in Millisekunden) von Methodenaufrufen an, die in den letzten 20 Sekunden (bis zu 20 Aufrufe) durchgeführt wurden. Die Aufrufzeit wird am -Objekt gemessen und enthält nicht die Zeit, die zum Durchlaufen des Netzwerks verwendet wird.<br/> |

    

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren einer Zu poolenden Komponente](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




