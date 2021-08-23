---
title: Verhindern des Abmeldens oder Anhaltens während eines Brandes
description: Wenn innerhalb einer Anwendung keine geeigneten Vorsichtsmaßnahmen getroffen werden, kann sich ein Benutzer während eines Burn-Vorgangs abmelden. Dies führt zu einer Unterbrechung des Burn-Prozesses, was zu datenverlusten führen und die Datenträger möglicherweise unbrauchbar machen kann.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3dd6980db72854ff65d657cc58730335febcb1dbc8c4a467eedead88f5eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977130"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Verhindern des Abmeldens oder Anhaltens während eines Brandes

Wenn innerhalb einer Anwendung keine geeigneten Vorsichtsmaßnahmen getroffen werden, kann sich ein Benutzer während eines Burn-Vorgangs abmelden. Dies führt zu einer Unterbrechung des Burn-Prozesses, was zu datenverlusten führen und die Datenträger möglicherweise unbrauchbar machen kann.

Um dieses Problem zu vermeiden, sollte die Anwendung die [**WM \_ QUERYENDSESSION-Nachricht**](/windows/desktop/Shutdown/wm-queryendsession) verarbeiten, die vor der Abmeldung zugestellt wird. Wenn die Anwendung diese Meldung beim Ausführen eines Burn-Vorgangs empfängt, geben Sie **FALSE** zurück, um die Abmeldung abzubrechen. Wenn die Anwendung es dem Benutzer ermöglicht, zu entscheiden, ob die Abmeldung fortgesetzt werden soll, sollte eine Warnung ausgegeben werden, die darauf hinweist, dass der Benutzer Daten verliert.

Stromübergänge während des Verbrandungsprozesses können auch zu potenziellen Problemen beim Erfolg einer Brandaktivität beitragen. Um diese Schwierigkeiten während des Brandprozesses zu verhindern, muss eine Anwendung wissen, wann Stromübergänge stattfinden. Dies wird erreicht, indem die Anwendung die Verarbeitung der [**WM \_ POWERBROADCAST-Nachricht**](/windows/desktop/Power/wm-powerbroadcast) ermöglicht. Anwendungen, die für Windows XP oder Windows Server 2003 entwickelt wurden, können **BROADCAST \_ QUERY \_ DENY** als Reaktion auf [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend)zurückgeben, wodurch das Anhalten während des Burnvorgangs verhindert wird.

Aufgrund von Änderungen am Energieverwaltungsmodell für Windows Vista und Windows Server 2008 wird das [**\_ PBT-Ereignis APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) nicht mehr an Anwendungen übermittelt. Stattdessen wird das [**\_ PBT-APMSUSPEND-Ereignis**](/windows/desktop/Power/pbt-apmsuspend) übermittelt, das zwei Sekunden für eine Anwendung bereitstellt, um sich auf den Übergang vorzubereiten.

Aufgrund dieser Änderungen wird empfohlen, dass Anwendungen die [**SetThreadExecutionState-Funktion**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) aufrufen, um ein Leerlauftime out des Systems zu verhindern, was normalerweise zum Übergang zu Suspend führt. Es ist wichtig zu beachten, dass das Aufrufen dieser Funktion mit den entsprechenden festgelegten Flags nur den Leerlauf des Systems verhindert, nicht einen in Bearbeitung befindlichen Suspend.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 