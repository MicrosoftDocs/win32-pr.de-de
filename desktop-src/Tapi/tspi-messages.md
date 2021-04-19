---
description: Dieser Abschnitt enthält eine Liste der Nachrichten in der Telefoniedienstanbieter-Schnittstelle (TSPI).
ms.assetid: 3d8bf980-81d6-49db-954f-af72458365dc
title: TSPI-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5772a1ccb0c07f03b2a17348ecf5e4834bb97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351051"
---
# <a name="tspi-messages"></a>TSPI-Nachrichten

Dieser Abschnitt enthält eine Liste der Nachrichten in der Telefoniedienstanbieter-Schnittstelle (TSPI). Diese Nachrichten werden verwendet, um TAPI über das Auftreten von asynchronen Ereignissen zu benachrichtigen, die innerhalb des Dienstanbieters spontan auftreten. Der Dienstanbieter übergibt diese Ereignisse an TAPI, indem er eine [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -oder [**phoneevent**](/windows/desktop/api/tspi/nc-tspi-phoneevent) -Rückruffunktion aufruft, abhängig davon, ob der Dienstanbieter ein Ereignis in einer Zeile, einem Aufruf oder einem Telefongerät meldet. Das **LineEvent** -Verfahren zum Melden von Ereignissen, die in einer Zeile oder einem Aufruf auftreten, wird dem Dienstanbieter zu dem Zeitpunkt bereitgestellt, zu dem die Zeile mit der [**TSPI-Funktion \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) geöffnet wird. Die **phoneevent** -Prozedur zum Melden von Ereignissen, die auf einem Telefon auftreten, wird mit der [**TSPI \_ phoneopen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen) -Funktion bereitgestellt.

Diese spontanen Ereignisse werden von TAPI in dem Sinne, dass Sie keine direkte Antwort auf eine Anforderung sind, nicht angefordert. Diese Ereignisse vergleichen mit denen, die den Abschluss von Anforderungen von TAPI melden. Solche Vervollständigungs Ereignisse werden über die asynchrone [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückruffunktion gemeldet.

Die Parameter Profile für die spontanen Ereignis Prozeduren enthalten Parameter, die das relevante Objekt identifizieren, für das das Ereignis gemeldet wird (Telefon, Zeile oder Anruf). Die Identifizierung erfolgt in Form eines nicht transparenten Handles, dessen exakte Interpretation nicht von TSPI veröffentlicht wird. TAPI bestimmt intern die Beziehung zwischen diesen nicht transparenten Handles und den Datenstrukturen, die für die Darstellung der Geräte verwendet wurden.

Das Parameter Profil für spontane Ereignis Prozeduren enthält auch einen Message-Parameter, der den Typ der Nachricht identifiziert. Jeder Nachrichtentyp verfügt über eine entsprechende Definition, die die enthaltenen Handles sowie andere Parameter und deren Bedeutungen bestimmt. Es gibt eine sehr starke Übereinstimmung zwischen den Nachrichten, die auf der TSPI-Ebene angezeigt werden, und denen, die auf der TAPI-Ebene vorkommen. Dies sind die allgemeinen Regeln der Entsprechung:

-   Der Satz von Nachrichten ist nahezu identisch. Wenn Nachrichten übereinstimmen, werden derselbe Nachrichten Name und-Wert auf der TSPI-Ebene verwendet.
-   Handles, die auf der TSPI-Ebene angezeigt werden, sind die durch die TSPI-Spezifikation definierten nicht transparenten Typen. Diese Typen (und ihre Interpretation) unterscheiden sich von denen auf der TAPI-Ebene, obwohl Sie auf dieselbe Geräteklasse verweisen. Wenn z. b. eine TAPI-Nachricht ein hline-Handle enthält, enthält die entsprechende TSPI-Nachricht normalerweise ein [**htapiline**](htapiline.md) -handle.
-   Es sind keine *dwcallbackinstance* -Daten an den Rückruf übermittelt.
-   Die Parameter *dwParam1*, *dwParam2* und *dwParam3* sind in der Regel mit den entsprechenden Parametern für die TAPI-Nachricht identisch.
-   Zeilen orientierte und Anruf orientierte Nachrichten werden an eine andere Rückruf Prozedur als Telefon orientierte Nachrichten übermittelt.

In diesem Abschnitt werden für jede Nachricht die folgenden Elemente aufgelistet:

-   Der Zweck der Nachricht.
-   Die Rückruf Prozedur, an die diese Nachricht übermittelt wird.
-   Eine Beschreibung der Nachrichten Parameter
-   Optionale Kommentare zur Verwendung der Nachricht
-   Optionale Verweise auf andere Funktionen, Meldungen und Datenstrukturen
-   Optionale Kommentare zum Vergleichen dieser Nachricht mit der TAPI-Schnittstelle

Bestimmte Nachrichten werden verwendet, um TAPI über eine Änderung des Status eines Objekts zu benachrichtigen. Diese Nachrichten stellen das nicht transparente Objekt Handle bereit und geben Aufschluss darüber, welches Status Element geändert wurde. TAPI kann anschließend eine entsprechende "Get Status"-Funktion des-Objekts abrufen, um den vollständigen Status des Objekts abzurufen.

Wenn ein Ereignis auftritt, kann eine Nachricht an TAPI gesendet werden oder nicht. Für einige Ereignis Typen, z. b. Statusänderungen, gibt TAPI eine Reihe von Statusänderungen an, die für Sie von Interesse sind. Der Dienstanbieter wird empfohlen, die Bericht erstatusmeldungs Ereignisse, die er meldet, auf die in dieser Gruppe enthaltenen Ereignisse zu beschränken. Der Dienstanbieter muss dieses Limit nicht einhalten. Anders ausgedrückt: Es werden möglicherweise mehr Änderungen als unbedingt erforderlich gemeldet. Es sollte jedoch versucht werden, das Limit aus Leistungsgründen zu beobachten.

Die Zeilen \_ Antwortnachricht wird nicht auf der TSPI-Ebene verwendet. Der Abschluss einer asynchronen Anforderung wird mithilfe des asynchronen [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückrufs gemeldet.

Die Telefon \_ Antwortnachricht wird nicht auf der TSPI-Ebene verwendet. Der Abschluss einer asynchronen Anforderung wird mithilfe des asynchronen [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückrufs gemeldet.

Weitere Informationen finden Sie in den folgenden Themen:

-   [TSPI-Geräte Nachrichten](tspi-line-device-messages.md)
-   [TSPI-Telefongeräte Meldungen](tspi-phone-device-messages.md)

 

 
