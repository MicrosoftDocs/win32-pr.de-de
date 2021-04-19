---
description: Die Anwendung kann einen Computer, der sich im Ruhezustand befindet, mithilfe eines geplanten Timers oder eines Geräte Ereignisses wieder in den Arbeitszustand versetzen.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: System Aktivierungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106363464"
---
# <a name="system-wake-up-events"></a>System Aktivierungs Ereignisse

Die folgenden Informationen gelten für Reaktivierungen aus dem Standbymodus [(S3) und Ruhezustand (S4)](/windows-hardware/drivers/kernel/system-sleeping-states). Informationen zu Reaktivierungen aus dem modernen Standby (S0-Low-Power-Leerlauf) finden Sie unter [Übergänge von Leerlauf zu aktiv](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

Die Anwendung kann einen Computer, der sich im Ruhezustand befindet, mithilfe eines geplanten Timers oder eines Geräte Ereignisses wieder in den Arbeitszustand versetzen. Dies wird als Reaktivierungs *Ereignis* bezeichnet. Verwenden Sie ein [wanutzbares timerobjekt](/windows/desktop/Sync/waitable-timer-objects) , um den Zeitpunkt anzugeben, an dem das System reaktivieren soll. Um das-Objekt zu erstellen, verwenden Sie die Funktion " [**kreatewaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) ". Verwenden Sie die [**setwaitabletimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) -Funktion, um den Timer festzulegen. Der *pduetime* -Parameter gibt an, wann der Timer signalisiert wird. Legen Sie den Parameter " *fresume* " auf " **true**" fest, um anzugeben, dass das System beim signalisieren des Timers aktiviert werden soll.

Wenn das System aufgrund eines Ereignisses (mit Ausnahme des Stromschalters oder der Benutzeraktivität) automatisch aktiviert wird, legt das System automatisch einen Timer für unbeaufsichtigte Leerlaufzeiten auf mindestens zwei Minuten fest. Dieser Timer gibt Anwendungen ausreichend Zeit zum Aufrufen der [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) -Funktion, um anzugeben, dass diese ausgelastet sind. Dieses Mal kann das System schnell wieder in den Standbymodus wechseln, wenn der Computer nicht mehr benötigt wird. Die folgenden Kriterien bestimmen, ob das System in den Ruhezustand zurückkehrt:

-   Wenn das System automatisch aktiviert wird (d. h. keine Benutzeraktivität vorhanden ist), wird es heruntergefahren, sobald der Timer für den unbeaufsichtigten Leerlauf abläuft, vorausgesetzt, dass keine Anwendungen [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufgerufen haben, um anzugeben, dass das System erforderlich ist.
-   Geräte basierte Reaktivierung löst standardmäßig den Timer für den unbeaufsichtigten Leerlauf aus, es sei denn, der Gerätetreiber weist auf eine Benutzer Wenn der Treiber anzeigt, dass ein Benutzer vorhanden ist, wird der Leerlaufzeit Geber des Systems verwendet.
-   Wenn das System automatisch aktiviert wird, der Benutzer jedoch neue Eingaben bereitstellt, während das Ereignis behandelt wird, wird das System nicht automatisch basierend auf dem Zeit Geber für unbeaufsichtigte Leerlaufzeiten wieder in den Standbymodus versetzt. Stattdessen kehrt das System basierend auf dem Leerlaufzeit Geber des Systems in den Standbymodus zurück.
-   Wenn das System aufgrund der Benutzeraktivität reaktiviert wird, wird das System nicht automatisch basierend auf dem unbeaufsichtigten Leerlaufzeit Geber wieder in den Standbymodus versetzt. Stattdessen kehrt das System basierend auf dem Leerlaufzeit Geber des Systems in den Standbymodus zurück.

Wenn das System automatisch aktiviert wird, überträgt es das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis an alle Anwendungen. Da der Benutzer nicht vorhanden ist, sollten die meisten Anwendungen nichts Unternehmen. Ereignis Behandlungs Anwendungen, wie z. b. Faxserver, sollten Ihre Ereignisse behandeln. Um zu ermitteln, ob sich das System in diesem Zustand befindet, nennen Sie die [**issystemresumeautomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) -Funktion. Wenn das System automatisch aktiviert wird, wird die Anzeige nicht automatisch aktiviert.

Wenn das System aufgrund der Benutzeraktivität aktiviert wird, überträgt das System zuerst das [PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md) -Ereignis, gefolgt von einem [PBT \_ apmresumesuspend](pbt-apmresumesuspend.md) -Ereignis. Außerdem schaltet das System die Anzeige ein. Die Anwendung sollte die Dateien erneut öffnen, die Sie geschlossen haben, als das System in den Standbymodus gewechselt und die Benutzereingaben vorbereitet

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> <dt>

[System Energiespar Kriterien](system-sleep-criteria.md)
</dt> </dl>

 

 
