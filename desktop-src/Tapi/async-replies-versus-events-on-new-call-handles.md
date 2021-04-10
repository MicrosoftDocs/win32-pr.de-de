---
description: TSPI umfasst eine Reihe von Vorgängen, mit denen die Lebensdauer eines Rückruf Handles gestartet wird.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Asynchrone Antworten und Ereignisse bei neuen aufrufshandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866603"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a>Asynchrone Antworten und Ereignisse bei neuen aufrufshandles

TSPI umfasst eine Reihe von Vorgängen, mit denen die Lebensdauer eines Rückruf Handles gestartet wird. Wenn der Dienstanbieter einen Erfolg für einen solchen Vorgang zurückgibt, muss er den nicht transparenten Handle des Typs " **hdrvcall"** ausfüllen, der für den neuen-Befehl verwendet wird, bevor er zurückgegeben wird. TAPI führt niemals Vorgänge für den-Befehl aus, bevor die entsprechende Abschluss Prozedur empfangen wurde. [*\_*](/windows/win32/api/tspi/nc-tspi-async_completion) Wenn der Dienstanbieter einen Fehler zurückgibt, wird das Handle automatisch ungültig (d. h. ohne [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)). In der Tat behandelt TAPI das Handle als "noch nicht gültig", bis der asynchrone Abschluss abgeschlossen ist.

Der Dienstanbieter muss das Handle auch als "noch nicht gültig" behandeln, bis der entsprechende [*Abschluss \_ proc*](/windows/win32/api/tspi/nc-tspi-async_completion) -Prozess empfangen wurde. Anders ausgedrückt: Es darf keine [*Zeilen \_ Ereignis*](/windows/win32/api/tspi/nc-tspi-lineevent) Funktionen für den neuen-Befehl ausgeben oder in die Anzahl von Aufrufen in Nachrichten oder Statusdaten Strukturen für die Zeile einschließen.

Die TAPI-Ebene entspricht auch diesen Lebenszyklus Einschränkungen. ein neues-Rückruf Handle wird erst zurückgegeben oder gültig, wenn die übereinstimmende [**Zeilen \_ Antwort**](./line-reply.md) Nachricht und keine Ereignisse für den neuen-Befehl an die Anwendung übermittelt werden, bis die Zeilen \_ Antwortnachricht angezeigt wird.

Die TSPI-Vorgänge, auf die das Prinzip "Start Lebensdauer" angewendet wird, lauten wie folgt:

-   [**TSPI \_ linecompletetransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [**TSPI ( \_ lineforward)**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [**TSPI- \_ linepickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [**TSPI \_ lineprepareaddumconference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [**TSPI \_ linesetupconference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [**TSPI \_ lineunpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
