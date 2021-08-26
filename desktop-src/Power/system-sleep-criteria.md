---
description: Solange das System feststellt, dass Benutzer- oder Anwendungsaktivitäten vorhanden sind, wird es nicht in den Standbymodus versetzt.
ms.assetid: 83c9394a-1813-405a-802a-0623e5de50d3
title: Kriterien für den Systemmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b93b0eb1a55d156a9d75b51ef826c85eabd28b29789cf50bb7f0fd7b5fee90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032820"
---
# <a name="system-sleep-criteria"></a>Kriterien für den Systemmodus

Solange das System feststellt, dass Benutzer- oder Anwendungsaktivitäten vorhanden sind, wird es nicht in den Standbymodus versetzt. Das System kann bestimmte Aktivitäten erkennen, z. B. Benutzereingaben oder Netzwerkkommunikation. Es gibt jedoch andere Aktivitäten, die das System nicht erkennen kann. Beispielsweise erfordert eine Präsentationsanwendung den Bildschirm für die Anzeige. Es kann jedoch vorkommen, dass sich die Anwendung während der Präsentation im Leerlauf befindet, was dazu führt, dass das System die Anzeige deaktiviert.

Verwenden Sie die [**SetThreadExecutionState-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) um das System zu benachrichtigen, dass Ihre Anwendung ausgelastet ist. Diese Funktion verhindert, dass das System in den Standbymodus versetzt oder die Anzeige deaktiviert wird, während die Anwendung ausgeführt wird.

Präsentations- und Multimediaanwendungen müssen die [**SetThreadExecutionState-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) mit **ES DISPLAY \_ \_ REQUIRED** aufrufen, damit das System weiß, dass das Anzeigegerät nicht in den Energiesparmodus versetzt werden soll. Ereignisbehandlungsanwendungen, z. B. Tools zum Verwalten eingehender Faxe, müssen **SetThreadExecutionState** mit **ES SYSTEM \_ \_ REQUIRED** aufrufen, das Ereignis behandeln und dann das Flag löschen, damit das System wieder in den Standbymodus versetzt werden kann. Beachten Sie, dass die meisten Produktivitätsanwendungen **SetThreadExecutionState** nicht verwenden müssen, da das System die Aktivität normalerweise anhand von Benutzereingaben bestimmen kann.

Um die Zeit seit der letzten Benutzereingabe beizubehalten, verwendet das System einen Leerlauftimer für die Anzeige und einen Leerlauftimer des Systems. Das System vergleicht die Leerlauftimer mit den im Energiesparplan konfigurierten Werten. Wenn der Wert des Leerlauftimers für die Anzeige größer als der Time out-Wert für die Anzeige ist und keine Threads die Anzeige durch Aufrufen von [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) mit **ES DISPLAY \_ \_ REQUIRED** angefordert haben, schaltet das System die Anzeige aus. Wenn der Leerlauftimer des Systems größer als der Time out-Wert des Systems ist und keine Anwendungen das System durch Aufrufen von **SetThreadExecutionState** mit **ES SYSTEM \_ \_ REQUIRED** angefordert haben, wechselt das System in den Standbymodus.

Das System verwaltet die Anzahl der Anwendungen, die [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)aufgerufen haben. Das System verfolgt jeden Thread, der **SetThreadExecutionState** aufruft, und passt den Indikator entsprechend an. Wenn dieser Leistungsindikator 0 (null) erreicht und keine Benutzereingabe erfolgt ist, wechselt das System in den Standbymodus.

Wenn die Stromversorgung niedrig ist, kann eine Anwendung einen Benutzereingriff anfordern oder anfordern, dass sich das System selbst aussetzt. Sie können den Systemvorgang mithilfe der [**SetSuspendState-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) anhalten.

Wenn das System automatisch reaktiviert wird[(PBT \_ APMRESUMEAUTOMATIC),](pbt-apmresumeautomatic.md)ist keiner der Timer relevant. Weitere Informationen finden Sie unter [Systemreaktivierungsereignisse.](system-wake-up-events.md)

## <a name="entering-sleep"></a>Eintritt in den Standbymodus

Wenn das System in den Standbymodus wechselt, behält es automatisch den Zustand des gesamten Systems und aller Anwendungen bei. Daher müssen die meisten Anwendungen keine besonderen Maßnahmen ergreifen. Anwendungen, die bestimmte Aktionen ausführen müssen, bevor der Systemübergang erfolgt, können sich für Energieereignisse registrieren.

Wenn das System ein [PBT-APMSUSPEND-Ereignis \_ ](pbt-apmsuspend.md) sendet, hat jede Anwendung zwei Sekunden Zeit, alle erforderlichen Aktionen auszuführen, bevor das System den Übergang in den Standbymodus startet. Anwendungen müssen einschränken, welche Maßnahmen sie als Reaktion auf dieses Ereignis ausführen, um sicherzustellen, dass sie alle Vorgänge in der zugewiesenen Zeit abschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> <dt>

[Systemreaktivierungsereignisse](system-wake-up-events.md)
</dt> </dl>

 

 



