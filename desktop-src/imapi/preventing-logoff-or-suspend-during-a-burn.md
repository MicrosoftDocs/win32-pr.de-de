---
title: Verhindern der Abmeldung oder aussetzen während eines Burn-Vorgangs
description: Wenn in einer Anwendung keine angemessenen Vorsichtsmaßnahmen getroffen werden, kann sich ein Benutzer während eines Verbrennungs Vorgangs abmelden. Dies führt zu einer Unterbrechung des Brennvorgangs, was zu Datenverlusten führen und die Diskette möglicherweise unbrauchbar machen kann.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472876"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Verhindern der Abmeldung oder aussetzen während eines Burn-Vorgangs

Wenn in einer Anwendung keine angemessenen Vorsichtsmaßnahmen getroffen werden, kann sich ein Benutzer während eines Verbrennungs Vorgangs abmelden. Dies führt zu einer Unterbrechung des Brennvorgangs, was zu Datenverlusten führen und die Diskette möglicherweise unbrauchbar machen kann.

Um dieses Problem zu vermeiden, sollte die Anwendung die " [**WM \_ queryendsession**](/windows/desktop/Shutdown/wm-queryendsession) "-Nachricht verarbeiten, die vor der Abmeldung zugestellt wird. Wenn die Anwendung diese Nachricht beim Ausführen eines Verbrennungs Vorgangs empfängt, geben Sie **false** zurück, um die Abmelde Prozedur abzubrechen. Wenn die Anwendung es dem Benutzer ermöglicht, sich zu entscheiden, ob die Anmeldung fortgesetzt werden soll, sollte eine Warnung angezeigt werden, die besagt, dass der Benutzerdaten verliert.

Durch Strom Übergänge während des Brennvorgangs können auch potenzielle Probleme beim Erfolg einer Verbrennungs Aktivität entstehen. Um diese Komplikationen während des Verbrennungs Vorgangs zu verhindern, muss eine Anwendung wissen, wann die Strom Übergänge stattfinden. Dies wird durch ermöglicht, dass die Anwendung die WM- [**\_ powerbroadcast**](/windows/desktop/Power/wm-powerbroadcast) -Nachricht verarbeiten kann. Anwendungen, die für Windows XP oder Windows Server 2003 entwickelt wurden, können als Reaktion auf [**PBT \_ apmquerysuspend**](/windows/desktop/Power/pbt-apmquerysuspend) **Broadcast- \_ Abfrage \_ ablehnen** zurückgeben und verhindern, dass während des Brennvorgangs angehalten wird.

Aufgrund von Änderungen im Energie Verwaltungsmodell für Windows Vista und Windows Server 2008 wird das [**PBT \_ apmquerysuspend**](/windows/desktop/Power/pbt-apmquerysuspend) -Ereignis nicht mehr an Anwendungen übermittelt. Stattdessen wird das [**PBT \_ apmsuspend**](/windows/desktop/Power/pbt-apmsuspend) -Ereignis zugestellt, das zwei Sekunden für eine Anwendung zur Vorbereitung des Übergangs bereitstellt.

Aufgrund dieser Änderungen wird empfohlen, dass Anwendungen die [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) -Funktion aufrufen, um zu verhindern, dass ein Timeout für das System im Leerlauf ist, was normalerweise zu einem Übergang zum aussetzen führt. Beachten Sie, dass das Aufrufen dieser Funktion mit den entsprechenden Flags nur das System im Leerlauf und keinen laufenden Anhaltevorgang verhindert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von IMAPI](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 