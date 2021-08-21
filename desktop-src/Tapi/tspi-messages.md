---
description: Dieser Abschnitt enthält eine Liste der Nachrichten in der Telefoniedienstanbieterschnittstelle (TSPI).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: TSPI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27aadfd1c39babb8f848a0553ede8efab968a08b3219f85ea8eab988bb3064bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860498"
---
# <a name="tspi-messages"></a>TSPI-Nachrichten

Dieser Abschnitt enthält eine Liste der Nachrichten in der Telefoniedienstanbieterschnittstelle (TSPI). Diese Nachrichten werden verwendet, um TAPI über das Auftreten asynchroner Ereignisse zu benachrichtigen, die im Dienstanbieter auftreten. Der Dienstanbieter übergibt diese Ereignisse an TAPI, indem er eine [**LINEEVENT-**](/windows/win32/api/tspi/nc-tspi-lineevent) oder [**PHONEEVENT-Rückruffunktion**](/windows/desktop/api/tspi/nc-tspi-phoneevent) aufruft, je nachdem, ob der Dienstanbieter ein Ereignis über eine Zeile, einen Anruf oder ein Telefongerät meldet. Die **LINEEVENT-Prozedur** zum Melden von Ereignissen, die in einer Zeile oder einem Aufruf auftreten, wird dem Dienstanbieter zum Zeitpunkt des Öffnens der Zeile mit der [**TSPI \_ lineOpen-Funktion**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) bereitgestellt. Das **PHONEEVENT-Verfahren** zum Melden von Ereignissen, die auf einem Telefon auftreten, wird mit der [**TSPI \_ phoneOpen-Funktion**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) bereitgestellt.

Diese unaufgeforderten Ereignisse werden von TAPI in dem Sinne angefordert, dass sie keine direkte Antwort auf eine Anforderung sind. Diese Ereignisse stehen im Gegensatz zu denen, die den Abschluss von Anforderungen von TAPI melden. Solche Abschlussereignisse werden über die [**ASYNC \_ COMPLETION-Rückruffunktion**](/windows/win32/api/tspi/nc-tspi-async_completion) gemeldet.

Die Parameterprofile für die Prozeduren des ereignisbehinderten Ereignisses enthalten Parameter, die das relevante Objekt identifizieren, für das das Ereignis gemeldet wird (Telefon, Leitung oder Anruf). Die Identifizierung erfolgt in Form eines nicht transparenten Handles, dessen genaue Interpretation nicht von TSPI veröffentlicht wird. TAPI bestimmt intern die Beziehung zwischen diesen nicht transparenten Handles und den Datenstrukturen, die zum Darstellen der Geräte verwendet wurden.

Das Parameterprofil für prozedurende Ereignisse enthält auch einen Nachrichtenparameter, der den Typ der Nachricht identifiziert. Jeder Nachrichtentyp verfügt über eine entsprechende Definition, die die enthaltenen Handles sowie andere Parameter und ihre Bedeutung bestimmt. Es gibt eine sehr starke Entsprechung zwischen den Nachrichten, die auf der TSPI-Ebene angezeigt werden, und den Nachrichten, die auf tapi-Ebene angezeigt werden. Dies sind die allgemeinen Entsprechungsregeln:

-   Der Satz von Nachrichten ist nahezu identisch. Wenn Nachrichten übereinstimmen, werden der gleiche Nachrichtenname und -wert auf TSPI-Ebene verwendet.
-   Handles, die auf tspi-Ebene angezeigt werden, sind die nicht transparenten Typen, die durch die TSPI-Spezifikation definiert werden. Diese Typen (und ihre Interpretation) unterscheiden sich von denen auf TAPI-Ebene, obwohl sie sich auf die gleiche Geräteklasse beziehen. Wenn eine TAPI-Nachricht beispielsweise ein HLINE-Handle enthält, enthält die entsprechende TSPI-Nachricht in der Regel ein [**HTAPILINE-Handle.**](htapiline.md)
-   An den Rückruf werden keine *dwCallbackInstance-Daten* übergeben.
-   Die Parameter *dwParam1,* *dwParam2* und *dwParam3* sind in der Regel mit den entsprechenden Parametern für die TAPI-Nachricht identisch.
-   Zeilenorientierte und anruforientierte Nachrichten werden an eine andere Rückrufprozedur als telefonorientierte Nachrichten übergeben.

In diesem Abschnitt werden für jede Nachricht die folgenden Elemente aufgelistet:

-   Zweck der Nachricht
-   Die Rückrufprozedur, an die diese Nachricht übergeben wird.
-   Eine Beschreibung der Nachrichtenparameter
-   Optionale Kommentare zur Verwendung der Nachricht
-   Optionale Verweise auf andere Funktionen, Nachrichten und Datenstrukturen
-   Optionale Kommentare, die diese Meldung mit der TAPI-Schnittstelle vergleichen

Bestimmte Nachrichten werden verwendet, um TAPI über eine Änderung des Status eines Objekts zu benachrichtigen. Diese Meldungen stellen das nicht transparente TAPI-Objekthandle und einen Hinweis darauf bereit, welches Statuselement sich geändert hat. TAPI kann anschließend eine entsprechende "Get Status"-Funktion des Objekts aufrufen, um den vollständigen Status des Objekts abzurufen.

Wenn ein Ereignis auftritt, kann eine Nachricht an TAPI gesendet werden. Für einige Ereignistypen, z. B. Statusänderungen, gibt TAPI eine Reihe von Statusänderungen an, an denen es interessiert ist. Dem Dienstanbieter wird empfohlen, die Statusänderungsmeldungsereignisse, die er meldet, auf die in dieser Gruppe enthaltenen Ereignisse zu beschränken. Der Dienstanbieter muss diesen Grenzwert nicht einhalten. Anders ausgedrückt: Möglicherweise werden mehr Änderungen als unbedingt erforderlich berichtet. Es sollte jedoch aus Leistungsgründen versucht werden, den Grenzwert zu beobachten.

Die \_ LINE REPLY-Nachricht wird nicht auf TSPI-Ebene verwendet. Der Abschluss einer asynchronen Anforderung wird mithilfe des [**ASYNC \_ COMPLETION-Rückrufs**](/windows/win32/api/tspi/nc-tspi-async_completion) gemeldet.

Die PHONE \_ REPLY-Nachricht wird nicht auf TSPI-Ebene verwendet. Der Abschluss einer asynchronen Anforderung wird mithilfe des [**ASYNC \_ COMPLETION-Rückrufs**](/windows/win32/api/tspi/nc-tspi-async_completion) gemeldet.

Weitere Informationen finden Sie in den folgenden Themen:

-   [TSPI-Zeilengerätemeldungen](tspi-line-device-messages.md)
-   [TSPI Telefon Gerätemeldungen](tspi-phone-device-messages.md)

 

 
