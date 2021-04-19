---
description: Wenn Sie im expertenfenster der Netzwerkmonitor-Benutzeroberfläche auf Experten ausführen klicken, werden die für die Erfassungs Datei ausgewählten Experten gestartet und die Run-Funktion aufgerufen. Wenn der Experte gestartet wird, analysiert er die Erfassungs Datei mithilfe mehrerer expertenframe-Funktionen.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Starten und Ausführen von Experten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366298"
---
# <a name="starting-and-running-experts"></a>Starten und Ausführen von Experten

Wenn Sie im expertenfenster der Netzwerkmonitor-Benutzeroberfläche auf **Experten ausführen** klicken, werden die für die Erfassungs Datei ausgewählten Experten gestartet und die [**Run**](run.md) -Funktion aufgerufen. Wenn der Experte gestartet wird, analysiert er die Erfassungs Datei mithilfe mehrerer expertenframe-Funktionen.

Die Funktion " [**expertindikatestatus**](expertindicatestatus.md) " stellt Statusinformationen vom Experten bereit. Wenn Sie einen Experten mit Netzwerkmonitor ausführen, zeigt das Fenster "expertenstatusansicht" regelmäßig aktualisierte Statusinformationen an (von 0 bis 100 Prozent).

![Fenster "expertenstatusansicht"](images/exview.png)

Der Experte ist aktiv, bis die Daten durch die Erfassungs Datei abgeschlossen sind. Wenn der Durchlauf abgeschlossen ist, wird ein Ereignisanzeige Fenster angezeigt. Die Informationen in diesem Fenster hängen von der Art des Experten ab, der die Daten analysiert hat. Die folgende Abbildung zeigt eine Expertenansicht für die Eigenschaften Verteilung, in der die vom Experten analysierten Frame Daten zusammengefasst werden.

![Expertenansicht für die Eigenschaften Verteilung](images/exview1.png)

Ein zweiter Bericht (nicht angezeigt) fasst die Ergebnisse der Übertragung des Transmission Control Protocol (TCP)-Neuübertragungs-Experten zusammen.

Sie können außerdem:

-   Erstellen Sie einen Eintrag für eine Ereignis Referenzseite (ERP), die dem Benutzer die erkannten Bedingungen oder Probleme (wie im Analysefenster angezeigt) rät.
-   Erstellen Sie Einträge für vorgeschlagene Korrekturen oder erläuternde Daten, die zusätzliche Informationen bereitstellen (wie im Fenster Auflösung angezeigt).

Nachdem der Experte seine Aufgabe abgeschlossen hat, Netzwerkmonitor den Experten aus dem aktiven Speicher entfernt. Experten sollten die geschützten Speicherfunktionen verwenden, die im Platform Software Development Kit (SDK) enthalten sind. Diese Funktionen bereinigen den Arbeitsspeicher, wenn die Experten während der Laufzeit fehlschlagen.

 

 



