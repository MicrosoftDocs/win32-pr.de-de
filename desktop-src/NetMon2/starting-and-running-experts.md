---
description: Wenn Sie im Fenster Experten der Netzwerkmonitor Benutzeroberfläche auf Experten ausführen klicken, werden die für die Erfassungsdatei ausgewählten Experten gestartet und die Run-Funktion angezeigt. Zu Beginn analysiert der Experte die Erfassungsdatei mithilfe mehrerer Expertenframefunktionen.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Starten und Ausführen von Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc85ba39c393ac253ca688a826bc77747c8d17bea29b089250a63f6f833066c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555320"
---
# <a name="starting-and-running-experts"></a>Starten und Ausführen von Experten

Wenn Sie im Fenster Experten der Netzwerkmonitor Benutzeroberfläche auf **Experten ausführen** klicken, werden die für die Erfassungsdatei ausgewählten Experten gestartet und die [**Run-Funktion**](run.md) aufruft. Zu Beginn analysiert der Experte die Erfassungsdatei mithilfe mehrerer Expertenframefunktionen.

Die [**ExpertIndicateStatus-Funktion**](expertindicatestatus.md) stellt Statusinformationen vom Experten bereit. Wenn Sie einen Experten mit Netzwerkmonitor ausführen, werden im Fenster Statusansicht des Experten regelmäßig aktualisierte Statusinformationen angezeigt (von 0 bis 100 Prozent).

![Ansichtsfenster für den Expertenstatus](images/exview.png)

Der Experte ist aktiv, bis die Daten ihren Durchlauf über die Erfassungsdatei abgeschlossen haben. Wenn der Durchlauf abgeschlossen ist, wird ein Ereignisanzeige Fenster angezeigt. Die Informationen in diesem Fenster hängen vom Typ des Experten ab, der die Daten analysiert hat. Die folgende Abbildung zeigt eine Ansicht des Eigenschaftsverteilungsexperten, in der die frame-Daten zusammengefasst sind, die der Experte analysiert hat.

![Expertenansicht für die Eigenschaftenverteilung](images/exview1.png)

In einem zweiten Bericht (nicht gezeigt) werden die Ergebnisse des TCP(Transmission Control Protocol) Retransmit-Experten zusammengefasst.

Sie haben außerdem folgende Möglichkeiten:

-   Erstellen Sie einen Eintrag für eine Ereignisreferenzseite (ERP), die den Benutzer über erkannte Bedingungen oder Probleme informiert (wie im Analysefenster dargestellt).
-   Erstellen Sie Einträge für vorgeschlagene Korrekturen oder erläuternde Daten, die zusätzliche Informationen bereitstellen (wie im Fenster Auflösung dargestellt).

Nachdem der Experte seine Aufgabe abgeschlossen hat, entfernt Netzwerkmonitor den Experten aus dem aktiven Arbeitsspeicher. Experten sollten die im Platform Software Development Kit (SDK) enthaltenen geschützten Arbeitsspeicherfunktionen verwenden. diese Funktionen bereinigen den Arbeitsspeicher, wenn die Experten während der Laufzeit ausfallen.

 

 



