---
description: Wenn eine Funktion SUCCESS zurückgibt, wurde die Funktion erfolgreich bis zu einem Punkt ausgeführt, der von der API auf Funktionsbasis definiert wird.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: Die Bedeutung von SUCCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae38aa834b3c60107c0245be2c792703a9c038c6e9b96f982e720bf417af58f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126120"
---
# <a name="the-meaning-of-success"></a>Die Bedeutung von SUCCESS

## <a name="tapi-2x"></a>TAPI 2.x

Wenn ein Vorgang eine SUCCESS-Angabe zurückgibt (entweder synchron bei Funktionsrückgabe für synchrone Vorgänge oder asynchron über eine [**LINE \_ REPLY-**](./line-reply.md) oder [**PHONE \_ REPLY-Nachricht**](./phone-reply.md) für asynchrone Vorgänge), wird Folgendes als true angenommen:

-   Die Funktion wurde erfolgreich zu einem Punkt weiterentwickelt, der von der API auf Funktionsbasis definiert wird. Nachdem dieser Punkt erreicht wurde, ist entweder der Vorgang vollständig abgeschlossen, oder er befindet sich in einem Zustand, in dem unabhängige Zustandsmeldungen die Anwendung über den nachfolgenden Fortschritt informieren.

    Beispielsweise sollte die Implementierung von [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) eines Dienstanbieters SUCCESS nicht später zurückgeben, wenn der Aufruf in den zustandsaufgehende Aufruf wechselt. Im Idealfall sollte der Anbieter success so bald wie möglich angeben, z. B. wenn der Anruf in den Anrufzustand des Wähltons wechselt (falls zutreffend). Sobald SUCCESS an die Anwendung zurückgegeben wurde, informieren LINE \_ CALLSTATE-Meldungen die Anwendung über den Fortschritt des Aufrufs. Dienstanbieter, die die Angabe **lineMakeCall** SUCCESS verzögern, z. B. bis zum Abschluss der Wählverbindung, müssen beachten, dass dieser Anbieter dadurch einen Nachteil hat, da die Nutzbarkeit auf Anwendungsebene stark eingeschränkt sein kann. Beispielsweise wäre es für einen Benutzer nicht möglich, die derzeit ausgeführte Anrufeinrichtungsanforderung abzubrechen, bis das Wählen abgeschlossen ist und alle Ziffern an den Schalter gesendet wurden.

-   Funktionen, die Informationen zurückgeben (z. B. [**lineGetCallInfo),**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)geben SUCCESS nur zurück, wenn die angeforderten Informationen für die Anwendung verfügbar sind. Funktionen, die Handles zurückgeben (an Zeilen oder Aufrufe), können SUCCESS nur zurückgeben, nachdem das Handle gültig ist. Es sollten keine Nachrichten über diese Zeile oder den Aufruf gesendet werden, bevor die SUCCESS-Angabe der Funktion angezeigt wird, die ihre Erstellung verursacht hat. Der Dienstanbieter ist für das Unterdrücken solcher Nachrichten verantwortlich.
-   Funktionen, die bestimmte permanente Bedingungen aktivieren (z. [**B. lineMonitorDigits),**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)geben SUCCESS erst zurück, nachdem die Bedingung aktiviert wurde, nicht, wenn die Bedingung erneut entfernt wird (z. B. nicht, wenn die Überwachung aller Ziffern abgeschlossen ist).
-   Aufrufsteuerungsfunktionen (z. B. [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) oder [**lineSetupTransfer,**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer)aber nicht [**lineMakeCall)**](/windows/win32/api/tapi/nf-tapi-linemakecall)geben SUCCESS zurück, wenn der Vorgang abgeschlossen ist. Einige Telefonnetzwerke stellen keine Bestätigung (positiv oder negativ) über den Abschluss bestimmter Anforderungen von Dienstanbietern bereit. In solchen Situationen muss der Dienstanbieter entscheiden, ob die Anforderung erfolgreich war oder nicht. Daher kann SUCCESS darauf hindeuten, dass der Dienstanbieter Aktionen initiiert hat, um die Anforderung zu erfüllen, aber nicht notwendigerweise mehr. Beispielsweise erhält der Anbieter möglicherweise keine positive Bestätigung für seine Anforderung vom Switch, obwohl er bereits eine Erfolgsmeldung an die Anwendung gesendet hat.

## <a name="tapi-3x"></a>TAPI 3.x

Wenn ein Vorgang eine SUCCESS-Angabe zurückgibt (entweder synchron bei Funktionsrückgabe für synchrone Vorgänge oder asynchron mit einem Aufruf der [**ASYNC \_ COMPLETION-Rückrufprozedur**](/windows/win32/api/tspi/nc-tspi-async_completion) für asynchrone Vorgänge), wird Folgendes als true angenommen:

-   Die Funktion wurde erfolgreich bis zu einem vom Dienstanbieter definierten Punkt ausgeführt. Der Dienstanbieter definiert den Punkt auf Funktionsbasis. Nach Erreichen dieses Punkts ist entweder der Vorgang vollständig abgeschlossen, oder er befindet sich in einem Zustand, in dem nachfolgende unabhängige Zustandsmeldungen die Anwendung über den Fortschritt informieren.
-   Funktionen, die Informationen zurückgeben (z. B. [**TSPI \_ linePark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) oder [**TSPI \_ lineDevSpecific),**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)geben SUCCESS nur zurück, wenn die angeforderten Informationen für den Aufrufer verfügbar sind. Funktionen, die Handles zurückgeben (für geöffnete Zeilen, geöffnete Smartphones oder Aufrufe), geben die Handles sofort bei der Funktionsrückgabe zurück. Sowohl der Dienstanbieter als auch der Aufrufer müssen die Handles bis zur letztlichen Erfolgsanzeige als "noch nicht gültig" behandeln. Der Dienstanbieter ist dafür verantwortlich, Rückrufmeldungen an das [**LINEEVENT-**](/windows/win32/api/tspi/nc-tspi-lineevent) oder [**PHONEEVENT-Verfahren**](/windows/desktop/api/tspi/nc-tspi-phoneevent) zu dieser geöffneten Zeile, dem geöffneten Telefon oder dem Anruf zu verhindern, bis nach der Erfolgsmeldung ein Anruf erfolgt. Wenn das letztliche Ergebnis ein Fehler ist, wird jedes sofort zurückgegebene Handle ohne weitere Aktion ungültig.
-   Funktionen, die bestimmte permanente Bedingungen aktivieren (z. [**B. TSPI \_ lineMonitorDigits),**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)geben SUCCESS erst zurück, nachdem die Bedingung aktiviert wurde, nicht, wenn die Bedingung erneut entfernt wird (z. B. nicht, wenn die Ziffernüberwachung abgeschlossen ist).
-   Aufrufsteuerfunktionen (z. [**B. TSPI \_ lineHold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) und [**TSPI \_ lineSetupTransfer,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)aber nicht [**TSPI \_ lineMakeCall)**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)geben SUCCESS zurück, wenn der Vorgang abgeschlossen ist. In Telefonieumgebungen, die keine positive Bestätigung dieser Funktionen bereitstellen, ist der Dienstanbieter gezwungen, eine bestmögliche Entscheidung über den Erfolg oder Fehler der Funktion zu treffen.
-   Die Implementierung von [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) durch einen Dienstanbieter muss SUCCESS nicht später zurückgeben, wenn der Aufruf in den *zustandsaufgehende* Aufruf wechselt. Im Idealfall gibt der Anbieter success so bald wie möglich an, z. B. wenn der Anruf in den *Dialtone-Anrufzustand* wechselt (falls zutreffend). Wenn SUCCESS an die Anwendung zurückgegeben wird, informieren [**LINE \_ CALLSTATE-Meldungen**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) den Aufrufer über den Status des Aufrufs. Dienstanbieter, die die Rückgabe der **\_ TSPI-ZeileMakeCall** SUCCESS-Angabe verzögern, z. B. bis nach Abschluss des Wählvorganges, beschränken die Flexibilität auf Anwendungsebene erheblich. Die Verzögerung bei der Rückgabe von SUCCESS in **TSPI \_ lineMakeCall** verhindert, dass ein Benutzer die ausgeführte Aufrufeinrichtungsanforderung abbricht, bis die Wählvorgang abgeschlossen ist und alle Ziffern an den Schalter gesendet werden.

 

 
