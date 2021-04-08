---
description: Solange das System feststellt, dass Benutzer-oder Anwendungs Aktivitäten vorhanden sind, wird es nicht in den Standbymodus versetzt.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: System Energiespar Kriterien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90950b980ec1e0fa06171d7a57d76b410534f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756565"
---
# <a name="system-sleep-criteria"></a>System Energiespar Kriterien

Solange das System feststellt, dass Benutzer-oder Anwendungs Aktivitäten vorhanden sind, wird es nicht in den Standbymodus versetzt. Das System kann bestimmte Aktivitäten, z. b. Benutzereingaben oder Netzwerkkommunikation, erkennen. Es gibt jedoch andere Aktivitäten, die vom System nicht erkannt werden können. Beispielsweise erfordert eine Präsentations Anwendung, dass der Bildschirm angezeigt wird. Es kann jedoch vorkommen, dass die Anwendung während der Präsentation im Leerlauf ist, was dazu führt, dass das System die Anzeige deaktiviert.

Verwenden Sie die Funktion [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) , um das System zu benachrichtigen, dass Ihre Anwendung ausgelastet ist. Diese Funktion verhindert, dass das System in den Standbymodus wechselt, oder schaltet die Anzeige aus, während die Anwendung ausgeführt wird.

Präsentations-und Multimediaanwendungen müssen die Funktion [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) mit der **\_ Anzeige \_ erforderlich** aufrufen, damit das System weiß, dass das Anzeigegerät nicht in den Standbymodus versetzt werden soll. Ereignis Behandlungs Anwendungen, wie z. b. Tools zum Verwalten eingehender Faxe, müssen **SetThreadExecutionState** mit **es- \_ System \_ erforderlich** aufrufen, das-Ereignis behandeln und dann das-Flag löschen, damit das System in den Standbymodus zurückkehren kann. Beachten Sie, dass die meisten Produktivitätsanwendungen nicht **SetThreadExecutionState** verwenden müssen, da das System in der Regel die Aktivität nach Benutzereingaben bestimmen kann.

Um die Zeit seit der letzten Benutzereingabe beizubehalten, verwendet das System einen Anzeige Leerlauf-Timer und einen Leerlauf Zeitgeber für das System. Das System vergleicht die Leerlaufzeit Geber mit den Werten, die im Energie Sparplan konfiguriert sind. Wenn der Zeit Geber Wert für die Anzeige im Leerlauf größer als der Anzeige Timeout Wert ist und keine Threads die Anzeige durch Aufrufen von [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) mit **der \_ Anzeige \_ erforderlich** angefordert haben, schaltet das System die Anzeige aus. Ebenso gilt, wenn der Timer für den System Leerlauf größer als der Timeout Wert des Systems ist und keine Anwendungen das System durch Aufrufen von **SetThreadExecutionState** mit dem **\_ System \_ erforderlich** angefordert haben, dass das System in den Standbymodus wechselt.

Das System verwaltet die Anzahl der Anwendungen, die [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)aufgerufen haben. Das System verfolgt jeden Thread nach, der **SetThreadExecutionState** aufruft und den Counter entsprechend anpasst. Wenn dieser Wert 0 (null) erreicht und keine Benutzereingaben vorhanden sind, wechselt das System in den Standbymodus.

Wenn die Stromversorgung gering ist, kann eine Anwendung einen Benutzereingriff anfordern oder anfordern, dass das System sich selbst anhält. Sie können den Systembetrieb mithilfe der [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) -Funktion aussetzen.

Wenn das System automatisch aktiviert wird ([PBT \_ apmresumeautomatic](pbt-apmresumeautomatic.md)), ist keiner der Timer relevant. Weitere Informationen finden Sie unter [System Aktivierungs Ereignisse](system-wake-up-events.md).

## <a name="entering-sleep"></a>Im Standbymodus

Wenn das System in den Standbymodus wechselt, wird automatisch der Status des gesamten Systems und aller Anwendungen beibehalten. Daher müssen die meisten Anwendungen keine besonderen Maßnahmen ergreifen. Anwendungen, die vor dem System Übergang bestimmte Aktionen ausführen müssen, können für Strom Ereignisse registriert werden.

Wenn das System ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis sendet, verfügt jede Anwendung über zwei Sekunden, um erforderliche Aktionen auszuführen, bevor das System den Übergang in den Standbymodus startet. Anwendungen müssen einschränken, welche Aktion Sie als Reaktion auf dieses Ereignis durchführen, um sicherzustellen, dass alle Vorgänge in der vorgesehenen Zeit ausgeführt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> <dt>

[System Aktivierungs Ereignisse](system-wake-up-events.md)
</dt> </dl>

 

 



