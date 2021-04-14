---
title: Automatische Wartung (Taskplaner)
description: Bei der Wartungs Aktivität handelt es sich um eine Anwendung oder einen Prozess, mit der die Integrität und Leistung eines Windows-PCs gewährleistet wird.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2020
ms.locfileid: "104391165"
---
# <a name="automatic-maintenance"></a>Automatische Wartung

Bei der Wartungs Aktivität handelt es sich um eine Anwendung oder einen Prozess, mit der die Integrität und Leistung eines Windows-PCs gewährleistet wird. Die Wartung umfasst das aktuelle Aktualisieren des Windows-Betriebssystems (OS) und der Anwendungen, das Überprüfen der Sicherheit und das Ausführen von Überprüfungen auf Schadsoftware. Windows Automatic Management (WAM) ist ein Satz von Erweiterungen für die Taskplaner-API, mit der Sie Ihre Anwendungen mit dem Windows-Wartungs Zeitplan verknüpfen können. WAM ermöglicht Ihnen insbesondere das Hinzufügen von Aktivitäten, die eine reguläre Planung erfordern, aber nicht über genaue Zeitanforderungen verfügen. Stattdessen unterstützt WAM das Betriebssystem, um die geeignete Zeit zum Aktivieren des Tasks während des Tages auszuwählen. Das System wählt diese Zeiten basierend auf minimalen Auswirkungen auf den Benutzer, die PC-Leistung und die Energieeffizienz aus.

## <a name="how-scheduled-maintenance-works"></a>Funktionsweise der geplanten Wartung

Taskplaner Wartungs Tasks sind opportunistische Aufgaben, die ausgeführt werden, wenn sich der Computer im Leerlauf befindet und sich im Energiesparmodus befindet. Eines der Hauptziele von Wartungs Tasks besteht darin, die Auswirkungen auf den PC zu minimieren, indem die Wartung nur dann durch geplant wird, wenn der PC an der Stromversorgung angeschlossen ist und sich im Leerlauf befindet (d. h. Wenn Sie den Computer nicht verwenden oder davon versetzt wurden). Die Idee der Wartung besteht heute darin, dass der Computer mit den geringsten Unterbrechungen für den Benutzer funktioniert. Aus diesem Grund wurde die Wartungs Stunde im alten Stil (Weitere Informationen hierzu finden Sie im Abschnitt **&mdash; tägliche Aktivierungs für automatische Wartung** weiter unten in diesem Thema) verbessert, um diese Leerlauf Zeiträume zu nutzen. Während die Wartungs Stunde weiterhin genutzt werden kann, ist die Ausführung der opportunistischen Wartung besser für den Systemzustand.

Der Task ist möglicherweise hungrig, wenn ein Computer nicht viel Zeit für den Leerlauf und die Stromversorgung verbringt. Stellen Sie sicher, dass Ihr Szenario weiterhin einen Wert für den Benutzer bereitstellt, auch wenn es verzögert wird. Wenn der Benutzer den Computer aktiv verwendet, stellt das System die Wartung bis zu einem späteren Zeitpunkt wieder her. Das System hält auch alle ausgeführten Wartungs Tasks an, wenn der Benutzer den PC verwendet.

Vom System wird ein angehaltene Wartungs Task während des nächsten Leerlauf Zeitraums neu gestartet. Allerdings hält das System keine als kritisch markierte Aufgabe an. Stattdessen kann das System unabhängig von der Benutzeraktion eine wichtige Aufgabe ausführen.

Aufgrund der Art der Planung werden möglicherweise einige geplante Aufgaben nicht abgeschlossen: möglicherweise sind zu viele geplante Ereignisse in das Wartungsfenster für eine Stunde passen, oder der Computer war einfach nicht eingeschaltet. In solchen Fällen können Sie eine Aufgabe mit einer Frist definieren. Ein Stichtag ist als Wiederholungszeit Spanne definiert, in der das System die Aufgabe mindestens einmal erfolgreich ausführen muss.

Wenn ein Task einen Stichtag verpasst, versucht der Wartungsplaner weiterhin, die Aufgabe während des Wartungs Fensters auszuführen. Außerdem beschränkt sich der Scheduler nicht auf das reguläre Zeit Limit von 1 Stunde. Stattdessen verlängert der Planer die Dauer des Wartungs Fensters, um die verzögerte Aufgabe abzuschließen.

Nachdem das System die Aufgabe abgeschlossen hat (auch mit einem Fehlercode), wird der Versuch als erfolgreich betrachtet. Nach einem erfolgreichen Versuch wird der Planer auf den regulären Wartungs Zeitplan zurückgesetzt, und der Task wird während des nächsten Zeitraums versucht.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Tägliche Aktivierung der automatischen Wartung &mdash;

Unter Windows 7 wird ein Wartungs Task exklusiv während der *Wartungs Stunde* ausgeführt, bis zu 3 Uhr und über Gruppenrichtlinie konfiguriert. Der Computer wird aus dem Standbymodus reaktiviert, Wartungs Tasks ausführen und wieder in den Standbymodus wechseln. Diese tägliche Sitzung war auf eine maximale Dauer von 1 Stunde pro Versuch beschränkt. Dadurch kann das System die Wartung täglich, beginnend um 3 Uhr, durchführen. Beachten Sie, dass der Benutzer die Zeit, zu der die Wartung ausgelöst wird, erneut planen kann, indem Sie diese Einstellungen konfigurieren.

Mit der Einführung von Laptops und dem Schwerpunkt der Akku Lebensdauer werden Computer nicht mehr so konfiguriert, dass die S3-Aktivierung in den meisten Fällen zulässig ist, und im allgemeinen Doze-to-S4 (Ruhezustand) so bald wie möglich, um Akku zu sparen. Als Reaktion auf diese Änderungen führt Taskplaner (> Win7) Wartungs Tasks aus, sobald sie fällig sind, und der Computer befindet sich im Leerlauf und in der Stromversorgung.

Diese Einstellung kann in der Systemsteuerung konfiguriert werden.

Öffnen Sie System **Steuerung**  >  **System und Sicherheit**  >  **und Wartung**  >  **Automatische Wartung**.

Je nachdem, wie Ihre Computer und ihre Tasks konfiguriert sind, kann das tägliche Aktivierungs Verhalten aufgrund der neuen Konfiguration nicht wie erwartet ausgeführt werden. Sie können zuerst feststellen, ob Ihr Computer S3-fähig ist, oder CS (verbundener Standbymodus).
Öffnen Sie hierzu eine PowerShell-Eingabeaufforderung mit erhöhten Rechten, und führen Sie den folgenden Befehl aus.

```console
powercfg /a
```

Wartungs Stunden, wenn der Computer ordnungsgemäß konfiguriert ist, funktioniert weiterhin, aber wenn dies nicht der Fall ist,
  - Überprüfen Sie die BIOS-Einstellungen auf Wake-Einstellungen. 
  - Überprüfen Sie, ob Aktivierungszeit Geber zulassen in den Energieoptionen aktiviert ist.
    Wechseln Sie zu **Systemsteuerung**  >  **Hardware und Sound**  >  **Energieoptionen**  >  **Bearbeitungs Plan Einstellungen**  >  **ändern erweiterte Energie Einstellungen** , > klicken Sie auf standbyaktivierungs-  >  **Timer zulassen**.
  - Überprüfen Sie, ob der geplante Task mit folgendem konfiguriert ist.
      * Maintenancesettings: der Task sollte mit dem Zeitraum und Stichtag konfiguriert werden.
      * Aktiviert: der Task muss aktiviert werden.
      * Waketor: der Task sollte zum Aktivieren des Computers zugelassen werden.
  - Zum Planen der Aktivierung von CS sollte der Computer auf der Grundlage von AOAC-fähig sein.
  - Zum Planen von Reaktivierung in S3-Computern
      * Überprüfen Sie, ob der Computer bei der Stromversorgung in S3 gewechselt ist.
      * Das System muss Wake-in Gruppenrichtlinie für die Wartung **aktiviert** haben.
 
Der verbundene Standbymodus ist der Systemstatus, der von einem mit einem AOAC kompatiblen System eingegeben werden kann.

Weitere Informationen finden Sie unter Unterschiede zwischen modernem Standby und S3 im Thema [modern Standby vs S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definieren eines automatischen Wartungs Tasks

Sie können beliebige Taskplaner Tasks in einen Wartungs Task konvertieren. Zu diesem Zweck müssen Sie sicherstellen, dass die Anwendung angehalten werden kann. Anschließend müssen Sie die Aufgabendefinition mit den neuen [**maintenancesettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) -und [**allowstartondemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) -Elementen erweitern.

Die Hauptaufgabe beim Erstellen eines Wartungs Tasks besteht darin sicherzustellen, dass das System den Task aussetzen und neu starten kann. Das System hält einen Wartungs Task wahrscheinlich mehrmals an; Daher müssen Sie sicherstellen, dass Ihre Anwendung in der Lage ist, ihren eigenen Zustand zu speichern, und dann zu einem beliebigen Zeitpunkt fortsetzen. Dadurch wird sichergestellt, dass das System nicht denselben Teil der Aufgabe wiederholt ausführt.

Nachdem Sie sichergestellt haben, dass die Anwendung angehalten und ordnungsgemäß fortgesetzt werden kann, können Sie die Elemente **maintenancesettings** und **allowstartondemand** verwenden, um den Zeitplan zu definieren. **Maintenancesettings** wird gemäß Zeitraum, Frist und Exklusivität definiert.

-   Der **Zeitraum** ist obligatorisch und definiert, wie oft die Aufgabe auftreten soll. Dies wird in der Regel in Form eines Multiday-Durchlaufs definiert, z. b. "einmal alle 5 Tage". Ein Zeitraum muss mindestens einen Tag betragen. Dies bedeutet, dass Sie nicht planen können, dass eine Aufgabe mehrmals täglich erfolgt.
-   Der **Stichtag** ist optional und legt fest, wie lange das Scheduler die Aufgabe nicht ausführen kann, bevor der Benutzer benachrichtigt oder eine Notfallwartung durchgeführt wird. Der Stichtag muss länger als der Zeitraum sein. Dies bedeutet, dass das System die Möglichkeit haben muss, die Aufgabe mindestens einmal zu versuchen, bevor der Benutzer benachrichtigt wird.
-   Außerdem kann ein Wartungs Task optional als *exklusiv* definiert werden. Eine exklusive Aufgabe wird separat von anderen Wartungs Tasks ausgeführt. In der Regel ist eine exklusive Aufgabe eine große Menge an Ressourcen, z. b. eine große Menge an CPU-Zeit oder ein exklusiver Zugriff auf eine Datenbank. Das System schließt alle nicht exklusiven Wartungs Tasks ab, bevor eine exklusive Aufgabe gestartet wird. Daher sollten Sie eine Aufgabe nur dann als exklusiv deklarieren, wenn dies erforderlich ist.

Im Gegensatz dazu gibt **allowstartondemand** lediglich an, dass das System oder der Benutzer die Aufgabe jederzeit starten kann. Dies ermöglicht es dem System, die Aufgabe während der regulären Wartung zu starten. Andernfalls müssten Sie einen eindeutigen-Auslösers für den Task festlegen.
