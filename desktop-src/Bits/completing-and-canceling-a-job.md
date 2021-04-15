---
title: Abschließen und Abbrechen eines Auftrags
description: Um einen Übertragungs Auftrag abzuschließen, wenden Sie die Methode "ibackgroundcopyjob Complete" an.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- Übertragen von Auftrags Bits, Abbrechen
- Abbrechen von Auftrags Bits
- Übertragen von Auftrags Bits, abschließen
- Abschließen von Auftrags Bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470980"
---
# <a name="completing-and-canceling-a-job"></a>Abschließen und Abbrechen eines Auftrags

Um einen Übertragungs Auftrag abzuschließen, können Sie die [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode abrufen. Für Download Aufträge können Sie die **Complete** -Methode aufzurufen, bevor alle Dateien im Auftrag übertragen wurden (vor dem Status des Auftrags lautet der Status der BG- \_ Auftrags \_ \_ Übertragung). Nur die Dateien, die von Bits vor dem Aufruf der **Complete** -Methode erfolgreich an den Client übertragen wurden, sind für den Benutzer verfügbar.

Bei Uploadaufträgen wird die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode nur aufgerufen, wenn der Status des Auftrags "BG \_ Job \_ State \_ transferi" lautet. Um zu ermitteln, wann der Status des Auftrags "BG \_ Job \_ State \_ transferi" lautet, rufen Sie die Zustands Eigenschaft des Auftrags ab, oder registrieren Sie sich, um [die](polling-for-the-status-of-the-job.md) \_ \_ \_ [Ereignis Benachrichtigung](registering-a-com-callback.md)"BG notify notify Job

Um einen Übertragungs Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode auf. Die **Cancel** -Methode entfernt den Auftrag aus der Übertragungs Warteschlange und entfernt die temporären Dateien vom Client. In der Regel wird diese Methode aufgerufen, wenn Sie einen Fehler, der dem Auftrag zugeordnet ist, nicht beheben können.

Die [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode bricht einen Upload ab, wenn der Upload nicht beendet ist. Wenn der Upload fertiggestellt ist und der Auftrag vom Typ "BG \_ Job \_ Type \_ Upload Reply" ist, wird die Antwort von \_ der Methode abgebrochen.

Wenn Sie die [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) -Methode oder die [**ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) -Methode nicht innerhalb von 90 Tagen aufrufen (Standardwert für [jobinactivitytimeout](group-policies.md) Gruppenrichtlinie), bricht der Dienst den Auftrag ab. Wenn der Dienst den Auftrag abbricht, sind die heruntergeladenen Dateien und die Antwortdatei für den Client nicht verfügbar. die Auftrags Abbruch wirkt sich nicht auf Dateien aus, die erfolgreich hochgeladen wurden. Sie sollten immer die **Complete** -oder **Cancel** -Methode aufrufen und sich nicht auf die jobinactivitytimeout-Richtlinie verlassen, um die Aufträge zu bereinigen. Die in der Warteschlange verbleibenden Aufträge können verhindern, dass Benutzer andere Aufträge erstellen, wenn das Richtlinien Limit von maxjobsperuser oder maxjobspermachine erreicht wird.

 

 




