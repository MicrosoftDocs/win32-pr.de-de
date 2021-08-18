---
description: Ihre Anwendung kann einen Computer, der sich im Energiesparmodus befindet, mithilfe eines geplanten Timers oder eines Geräteereignisses in den Arbeitszustand wiederherstellen.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Systemreaktivierungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f67ec53b474e303bada3a27bda1adea8170d5be2d6a84354fc17094ddec7da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143223"
---
# <a name="system-wake-up-events"></a>Systemreaktivierungsereignisse

Die folgenden Informationen gelten für Aktivierungen aus [dem Standbymodus (S3) und Ruhezustand (S4).](/windows-hardware/drivers/kernel/system-sleeping-states) Informationen zu Aktivierungen aus dem modernen Standbymodus (S0 Low Power Idle) finden Sie unter [Übergänge vom Leerlauf zum aktiven](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

Ihre Anwendung kann einen Computer, der sich im Energiesparmodus befindet, mithilfe eines geplanten Timers oder eines Geräteereignisses in den Arbeitszustand wiederherstellen. Dies wird als *Aktivierungsereignis* bezeichnet. Verwenden Sie ein [wartebares Timerobjekt,](/windows/desktop/Sync/waitable-timer-objects) um die Zeit anzugeben, zu der das System aktiviert werden soll. Verwenden Sie zum Erstellen des Objekts die [**CreateWaitableTimer-Funktion.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Verwenden Sie zum Festlegen des Timers die [**SetWaitableTimer-Funktion.**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) Der *pDueTime-Parameter* gibt an, wann der Timer signalisiert wird. Um anzugeben, dass das System aktiviert werden soll, wenn der Timer signalisiert wird, legen Sie den *fResume-Parameter* auf **TRUE** fest.

Wenn das System aufgrund eines Ereignisses (mit Ausnahme eines Netzschalters oder einer Benutzeraktivität) automatisch aktiviert wird, legt das System automatisch einen unbeaufsichtigten Leerlauftimer auf mindestens 2 Minuten fest. Dieser Timer gibt Anwendungen ausreichend Zeit, um die [**SetThreadExecutionState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufzurufen, um anzugeben, dass sie ausgelastet sind. Dadurch kann das System schnell wieder in den Standbyzustand versetzt werden, nachdem der Computer nicht mehr benötigt wird. Die folgenden Kriterien bestimmen, ob das System in den Standbyzustand zurückkehrt:

-   Wenn das System automatisch aktiviert wird (d. h., es ist keine Benutzeraktivität vorhanden), wird es heruntergefahren, sobald der unbeaufsichtigte Leerlauftimer abläuft, vorausgesetzt, dass keine Anwendungen [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) aufgerufen haben, um anzugeben, dass das System erforderlich ist.
-   Gerätebasierte Aktivierungen lösen den unbeaufsichtigten Leerlauftimer standardmäßig aus, es sei denn, der Gerätetreiber weist auf benutzerseitige Präsenz hin. Wenn der Treiber die Anwesenheit des Benutzers angibt, wird der Leerlauftimer des Systems verwendet.
-   Wenn das System automatisch aktiviert wird, der Benutzer jedoch neue Eingaben bereitstellt, während das Ereignis behandelt wird, kehrt das System basierend auf dem unbeaufsichtigten Leerlaufzeitgeber nicht automatisch in den Ruhezustand zurück. Stattdessen kehrt das System basierend auf dem Leerlauftimer des Systems in den Standbymodus zurück.
-   Wenn das System aufgrund von Benutzeraktivitäten reaktiviert wird, kehrt das System basierend auf dem unbeaufsichtigten Leerlaufzeitgeber nicht automatisch in den Standbymodus zurück. Stattdessen kehrt das System basierend auf dem Leerlauftimer des Systems in den Standbymodus zurück.

Wenn das System automatisch aktiviert wird, überträgt es das [PBT \_ APMRESUMEAUTOMATIC-Ereignis](pbt-apmresumeautomatic.md) an alle Anwendungen. Da der Benutzer nicht vorhanden ist, sollten die meisten Anwendungen nichts tun. Ereignisbehandlungsanwendungen, z. B. Faxserver, sollten ihre Ereignisse verarbeiten. Um zu bestimmen, ob sich das System in diesem Zustand befindet, rufen Sie die [**IsSystemResumeAutomatic-Funktion**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) auf. Wenn das System automatisch aktiviert wird, wird die Anzeige nicht automatisch aktiviert.

Wenn das System aufgrund von Benutzeraktivitäten aktiviert wird, überträgt das System zuerst das [ \_ PBT-Ereignis APMRESUMEAUTOMATIC,](pbt-apmresumeautomatic.md) gefolgt von einem [ \_ PBT-Ereignis APMRESUMESUSPEND.](pbt-apmresumesuspend.md) Darüber hinaus schalte das System die Anzeige ein. Ihre Anwendung sollte dateien erneut öffnen, die sie geschlossen hat, als das System in den Standbymodus versetzt wurde, und sich auf Benutzereingaben vorbereiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> <dt>

[Kriterien für den Systemmodus](system-sleep-criteria.md)
</dt> </dl>

 

 
