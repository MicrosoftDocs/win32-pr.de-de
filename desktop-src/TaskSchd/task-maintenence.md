---
title: Automatische Wartung (Taskplaner)
description: Wartungsaktivität bezieht sich auf eine Anwendung oder einen Prozess, die bzw. der die Integrität und Leistung eines Windows unterstützt.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43fe72159ac5fd14c2dcc80126e572fa1475ed52ffd5710b74621cf00ad40a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139303"
---
# <a name="automatic-maintenance"></a>Automatische Wartung

Wartungsaktivität bezieht sich auf eine Anwendung oder einen Prozess, die bzw. der die Integrität und Leistung eines Windows unterstützt. Die Wartung umfasst die Windows Betriebssystem und Anwendungen auf dem neuesten Stand zu halten, die Sicherheit zu überprüfen und Überprüfungen auf Schadsoftware ausführen. Windows Bei der automatischen Verwaltung (WAM) handelt es sich um eine Reihe von Erweiterungen der Taskplaner-API, mit denen Sie Ihre Anwendungen mit dem Wartungszeitplan Windows verknüpfen können. Insbesondere ermöglicht WAM das Hinzufügen von Aktivitäten, die eine regelmäßige Planung erfordern, aber keine genauen Zeitanforderungen haben. Stattdessen verwendet WAM das Betriebssystem, um den geeigneten Zeitpunkt für die Aktivierung der Aufgabe im Laufe des Tages zu wählen. Das System wählt diese Zeiten basierend auf minimalen Auswirkungen auf den Benutzer, die PC-Leistung und die Energieeffizienz aus.

## <a name="how-scheduled-maintenance-works"></a>Funktionsweise der geplanten Wartung

Taskplaner Wartungsaufgaben sind deterministische Aufgaben, die ausgeführt werden, wenn sich der Computer im Leerlauf befindet und mit Netzstrom ausgenutzt wird. Eines der wichtigsten Ziele von Wartungsaufgaben besteht in der Minimierung der Auswirkungen auf den PC, indem die Wartung nur geplant wird, wenn der PC an die Stromversorgung des Wechselstroms angeschlossen ist und sich im Leerlauf befindet (d. h., wenn Sie den Computer nicht verwenden oder abgestuft haben). Die Idee der Wartung besteht heutzutage in der Arbeit des Computers mit der geringsten Unterbrechung für den Benutzer. Daher wurde die Wartungszeit im alten Stil **&mdash;** (dies wird im Abschnitt Automatische tägliche Wartung weiter unten in diesem Thema erläutert) verbessert, um diese Leerlaufzeiten zu nutzen. Die Wartungszeit kann zwar weiterhin genutzt werden, aber die Ausführung einer deterministischen Wartung ist für die Systemzustand besser.

Ihre Aufgabe wird möglicherweise nicht mehr unterstützt, wenn ein Computer nicht viel Zeit sowohl im Leerlauf als auch bei der Stromversorgung des Netzgeräts verbringt. Stellen Sie sicher, dass Ihr Szenario dem Benutzer auch dann einen Mehrwert bietet, wenn es verzögert wird. Wenn der Benutzer den Computer aktiv verwendet, wird die Wartung vom System auf einen späteren Zeitpunkt zurück verzögerungen. Das System setzt auch alle ausgeführten Wartungsaufgabe an, wenn der Benutzer zur Verwendung des PCs zurückkehrt.

Das System startet einen angehaltenen Wartungsaufwand während des nächsten Leerlaufzeitraums neu. Das System setzt jedoch keine als kritisch markierten Aufgaben an. Stattdessen lässt das System zu, dass eine kritische Aufgabe unabhängig von der Benutzeraktion abgeschlossen wird.

Aufgrund der Art der Planung werden einige geplante Aufgaben möglicherweise nicht abgeschlossen: Möglicherweise gibt es zu viele geplante Ereignisse, die in das einstündige Wartungsfenster passen, oder der Computer wurde einfach nicht eingeschaltet. In solchen Fällen können Sie eine Aufgabe mit einem Stichtag definieren. Ein Stichtag ist als periodischen Zeitraum definiert, in dem das System die Aufgabe mindestens einmal erfolgreich ausführen muss.

Wenn ein Task einen Stichtag verpasst, versucht der Wartungsplaner weiterhin, den Task während des Wartungsfensters auszuführen. Darüber hinaus schränkt sich der Planer nicht auf das reguläre Zeitlimit von 1 Stunde ein. Stattdessen verlängert der Planer die Dauer des Wartungsfensters, um den verzögerten Task auszuführen.

Sobald das System die Aufgabe abgeschlossen hat (auch mit einem Fehlercode), wird der Versuch als erfolgreich betrachtet. Nach einem erfolgreichen Versuch wird der Planer auf den regulären Wartungszeitplan zurückgesetzt und versucht, den Task während des nächsten Zeitraums auszuführen.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Automatische tägliche &mdash; Wartung reaktivierung

Am Windows 7 wird ein Wartungsaufgabe ausschließlich während der Wartungszeit *ausgeführt.* Der Standardwert ist 3:00 Uhr und kann über Gruppenrichtlinie. Der Computer würde aus dem Standbymodus reaktiv werden, Wartungsaufgaben ausführen und wieder in den Standbymodus wechseln. Diese tägliche Sitzung war auf eine maximale Dauer von 1 Stunde pro Versuch beschränkt. Auf diese Weise kann das System täglich wartungen, standardmäßig ab 3:00 Uhr. Beachten Sie, dass der Benutzer die Zeit, zu der die Wartung ausgelöst wird, durch Konfigurieren dieser Einstellungen neu planen kann.

Mit der Einführung von Laptops und dem starken Fokus auf der Akkulebensdauer sind Computer in den meisten Fällen nicht mehr so konfiguriert, dass S3 reaktiviert werden kann, und in der Regel schnellstmöglich doze-to-S4 (Ruhezustand), um Akku zu sparen. Als Reaktion auf diese Änderungen führt Taskplaner (> Win7) Wartungsaufgaben aus, wann immer sie fällig sind, und der Computer befindet sich im Leerlauf und mit Netzstrom.

Diese Einstellung kann in der Systemsteuerung.

Öffnen **Systemsteuerung**  >  **System and Security Sicherheit und Wartung**  >    >  **Automatische Wartung**.

Je nach Konfiguration Ihrer Computer und Aufgaben tritt das tägliche Aktivierungsverhalten aufgrund dieser neuen Konfiguration möglicherweise heute möglicherweise nicht wie erwartet auf. Sie können zunächst ermitteln, ob Ihr Computer S3- oder CS-fähig (Verbundener Standbymodus) ist.
Dies kann durch Öffnen einer Power Shell-Eingabeaufforderung mit erhöhten Rechten und Ausführen des folgenden Befehls erfolgen.

```console
powercfg /a
```

Wartungszeit, wenn der Computer ordnungsgemäß konfiguriert ist, funktioniert weiterhin, aber wenn nicht,
  - Überprüfen Sie Ihre BIOS-Einstellungen auf Aktivierungseinstellungen. 
  - Überprüfen Sie, ob Aktivierungszeitr zulassen in der Energieoptionen.
    Wechseln Sie **Systemsteuerung** hardware and sound Energieoptionen Edit Plan Einstellungen Change advanced power settings (Erweiterte Energieeinstellungen ändern> klicken Sie auf  >    >    >    >   **Sleep** Allow Wake Timer (Aktivierungs-Timer für  >  **Ruhezustand zulassen).**
  - Überprüfen Sie, ob ihr geplanter Task wie folgt konfiguriert ist.
      * MaintenanceSettings: Task muss mit Zeitraum, Stichtag konfiguriert werden.
      * Aktiviert: Task muss aktiviert sein.
      * WakeToRun: Task sollte berechtigt sein, den Computer zu reaktiven.
  - Für die Planung von Aktivierungen von CS sollte der Computer AOAC-fähig sein.
  - Für die Planung von Aktivierungen auf S3-Computern:
      * Überprüfen Sie, ob der Computer in S3 unter Ac Power (Netzstrom) gelaufen ist.
      * Für das System sollte **wake enabled** in Gruppenrichtlinie for Maintenance (Aktivierung aktiviert) sein.
 
Verbundener Standbymodus ist der Systemstatus, den ein AOAC-kompatibles System eingeben kann.

Weitere Informationen zu den Unterschieden zwischen modernen Standbyservern und S3 finden Sie im Thema [Moderner Standbymodus im Vergleich zu S3.](/windows-hardware/design/device-experiences/modern-standby-vs-s3)

## <a name="defining-an-automatic-maintenance-task"></a>Definieren einer Automatische Wartung Aufgabe

Sie können jeden Taskplaner in einen Wartungsaufgabe konvertieren. Dazu müssen Sie bestätigen, dass Ihre Anwendung angehalten werden kann. Anschließend müssen Sie die Aufgabendefinition mit den neuen [**Elementen MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) und [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) erweitern.

Das Hauptanliegen beim Erstellen einer Wartungsaufgabe besteht darin, sicherzustellen, dass das System den Task an- und neu starten kann. Das System wird eine Wartungsaufgabe wahrscheinlich mehrmals aussetzen. Daher müssen Sie sicherstellen, dass Ihre Anwendung ihren eigenen Zustand speichern und dann zu einem beliebigen Zeitpunkt fortsetzen kann. Dadurch wird sichergestellt, dass das System den gleichen Teil der Aufgabe nicht wiederholt ausführen kann.

Nachdem Sie sichergestellt haben, dass Ihre Anwendung angehalten und ordnungsgemäß fortgesetzt werden kann, können Sie den Zeitplan mithilfe der **Elemente MaintenanceSettings** und **AllowStartOnDemand** definieren. **MaintenanceSettings** wird nach Zeitraum, Stichtag und Intervall definiert.

-   Der **Zeitraum** ist obligatorisch und definiert, wie oft die Aufgabe auftreten soll. In der Regel wird dies im Rahmen eines mehrtägigen Zyklus definiert, z. B. "einmal alle 5 Tage". Ein Zeitraum muss mindestens einen Tag sein. Das bedeutet, dass Sie nicht planen können, dass eine Aufgabe mehrmals pro Tag auftritt.
-   Der **Stichtag** ist optional und definiert, wie lange der Planer die Aufgabe nicht abschließen kann, bevor er den Benutzer benachrichtigt oder eine Notfallwartung durchführen kann. Die Frist muss länger als der Zeitraum sein. Dies bedeutet, dass das System die Möglichkeit haben muss, die Aufgabe mindestens einmal zu versuchen, bevor der Benutzer benachrichtigt wird.
-   Darüber hinaus kann ein Wartungsaufgabe optional als exklusive definiert *werden.* Eine exklusive Aufgabe wird getrennt von anderen Wartungsaufgaben ausgeführt. In der Regel ist eine exklusive Aufgabe eine Aufgabe, die eine große Menge an Ressourcen verwendet, z. B. viel CPU-Zeit oder exklusiven Zugriff auf eine Datenbank. Das System schließt alle nicht exklusiven Wartungsaufgaben ab, bevor eine exklusive Aufgabe gestartet wird. Daher sollten Sie eine Aufgabe nur bei Bedarf als exklusiv deklarieren.

Im Gegensatz dazu **gibt AllowStartOnDemand** lediglich an, dass das System oder der Benutzer die Aufgabe jederzeit starten kann. Dadurch kann das System die Aufgabe während der regelmäßigen Wartung starten. Andernfalls müssten Sie einen eindeutigen Trigger für die Aufgabe festlegen.
