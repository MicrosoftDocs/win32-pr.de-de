---
title: Abschließen und Abbrechen eines Auftrags
description: Um einen Übertragungsauftrag abzuschließen, rufen Sie die IBackgroundCopyJob Complete-Methode auf.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- BITS des Übertragungsauftrags, Abbrechen
- Abbrechen eines BITS-Auftrags
- Übertragen von Bits für den Übertragungsauftrag, Abschluss
- Abschließen eines BITS-Auftrags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 348ee7c4ad4b9a38350e6a1f25d8d05d206b299518cf25197b643dbcb15cb4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835055"
---
# <a name="completing-and-canceling-a-job"></a>Abschließen und Abbrechen eines Auftrags

Um einen Übertragungsauftrag abzuschließen, rufen Sie die [**IBackgroundCopyJob::Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) auf. Für Downloadaufträge können Sie die **Complete-Methode** aufrufen, bevor alle Dateien im Auftrag übertragen wurden (bevor der Status des Auftrags BG \_ JOB STATE \_ \_ TRANSFERD lautet). Nur die Dateien, die BITS erfolgreich an den Client übertragen hat, bevor Sie die **Complete-Methode** aufgerufen haben, sind für den Benutzer verfügbar.

Rufen Sie bei Uploadaufträgen nur dann die [**Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) auf, wenn der Status des Auftrags BG \_ JOB STATE \_ \_ TRANSFERD lautet. Um zu bestimmen, wann der Status des Auftrags BG \_ JOB \_ STATE TRANSFERD lautet, können Sie die \_ Zustandseigenschaft des Auftrags [abfragen](polling-for-the-status-of-the-job.md) oder registrieren, um die Ereignisbenachrichtigung BG NOTIFY JOB TRANSFERD zu \_ \_ \_ erhalten. [](registering-a-com-callback.md)

Um einen Übertragungsauftrag abzubrechen, rufen Sie die [**IBackgroundCopyJob::Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) auf. Die **Cancel-Methode** entfernt den Auftrag aus der Übertragungswarteschlange und die temporären Dateien vom Client. In der Regel rufen Sie diese Methode auf, wenn Sie einen Fehler im Zusammenhang mit dem Auftrag nicht beheben können.

Die [**Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) bricht einen Upload ab, wenn der Upload nicht abgeschlossen ist. Wenn der Upload abgeschlossen ist und der Auftrag vom Typ BG \_ JOB TYPE UPLOAD REPLY \_ \_ \_ ist, bricht die Methode die Antwort ab.

Wenn Sie die [**Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) oder die [**IBackgroundCopyJob::Cancel-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) nicht innerhalb von 90 Tagen aufrufen [(StandardauftragInactivityTimeout](group-policies.md) Gruppenrichtlinie), bricht der Dienst den Auftrag ab. Wenn der Dienst den Auftrag abbricht, sind die heruntergeladenen Dateien und die Antwortdatei für den Client nicht verfügbar. Der Auftragsabbruch wirkt sich nicht auf Dateien aus, die erfolgreich hochgeladen wurden. Sie sollten immer die **Complete-** oder **Cancel-Methode** aufrufen und sich nicht auf die JobInactivityTimeout-Richtlinie verlassen, um Ihre Aufträge zu bereinigen. Aufträge, die in der Warteschlange übrig bleiben, verhindern möglicherweise, dass Benutzer andere Aufträge erstellen, wenn das Richtlinienlimit für MaxJobsPerUser oder MaxJobsPerMachine erreicht ist.

 

 




