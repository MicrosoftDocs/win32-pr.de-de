---
description: Wenn eine Opertion Erfolg zurückgibt, wurde die Funktion erfolgreich zu einem Punkt fortgeführt, der durch die API für eine Funktion durch Funktions Basis definiert wird.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: Die Bedeutung des Erfolgs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d183695e9dce9df88dea5fe9464f16163130cd0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360698"
---
# <a name="the-meaning-of-success"></a>Die Bedeutung des Erfolgs

## <a name="tapi-2x"></a>TAPI 2. x

Wenn ein Vorgang einen Erfolgsindikator zurückgibt (entweder synchron bei Funktions Rückgabe für synchrone Vorgänge oder asynchron durch eine [**Zeilen \_ Antwort**](./line-reply.md) oder eine [**Telefon \_ Antwort**](./phone-reply.md) Nachricht für asynchrone Vorgänge), wird angenommen, dass der folgende Wert zutrifft:

-   Die Funktion wurde erfolgreich zu einem Punkt fortgeführt, der von der API auf Funktionsweise definiert wird. Nachdem dieser Punkt erreicht wurde, ist entweder der Vorgang vollständig abgeschlossen, oder er befindet sich in einem Zustand, in dem die Anwendung von unabhängigen Zustands Meldungen über den nachfolgenden Fortschritt informiert wird.

    So sollte z. b. die Implementierung von [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) eines Dienstanbieters Success No zurückgeben, als wenn der Anruf in den Status der fort setzungs Aufrufe wechselt. Im Idealfall sollte der Anbieter so bald wie möglich einen Erfolg angeben, z. b. wenn der-Befehl in den Status des Dial-Tone-Aufrufes wechselt (falls zutreffend). Sobald der Erfolg an die Anwendung zurückgegeben wurde, \_ wird die Anwendung durch Zeilen-CallState-Meldungen über den Fortschritt des Aufrufes informiert. Dienstanbieter, die die Rückgabe der **linemakecall** -Erfolgs Anzeige verzögern, z. b. bis nach Abschluss des Einwähl Vorgangs, müssen beachten, dass dieser Anbieter dadurch benachteiligt wird, da die Nutzbarkeit auf Anwendungsebene stark eingeschränkt sein kann. Beispielsweise ist es nicht möglich, dass ein Benutzer die in Bearbeitung befindliche Anforderung zum Einrichten des Aufrufens abbrechen kann, bis die Wahl abgeschlossen ist und alle Ziffern an den Switch gesendet wurden.

-   Funktionen, die Informationen zurückgeben (z. b. [**linegetcallinfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)), geben nur dann Erfolg zurück, wenn die angeforderten Informationen für die Anwendung verfügbar sind. Funktionen, die Handles (für Zeilen oder Aufrufe) zurückgeben, können den Erfolg nur zurückgeben, wenn das Handle gültig ist. Vor der Erfolgs Angabe der Funktion, die die Erstellung verursacht hat, sollten keine Nachrichten zu dieser Zeile gesendet oder aufgerufen werden. Der Dienstanbieter ist für das unterdrücken solcher Nachrichten verantwortlich.
-   Funktionen, die bestimmte permanente Bedingungen ermöglichen (z. b. [**linemonitordigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)), geben nur dann Erfolg zurück, wenn die Bedingung aktiviert ist, nicht, wenn die Bedingung erneut entfernt wird (z. b. nicht, wenn die gesamte Ziffern Überwachung abgeschlossen ist).
-   Anruf Steuerungsfunktionen (z. b. [**linehold**](/windows/win32/api/tapi/nf-tapi-linehold) oder [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), aber nicht [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall)) geben einen Erfolg zurück, wenn der Vorgang abgeschlossen ist. Einige Telefon Netzwerke bieten keine Bestätigung (positiv oder negativ) zum Abschluss bestimmter Anforderungen von Dienstanbietern. In solchen Fällen muss der Dienstanbieter entscheiden, wann die Anforderung erfolgreich oder fehlerhaft war. Daher kann ein Erfolg darauf hindeuten, dass der Dienstanbieter Aktionen zum erfüllen der Anforderung initiiert hat, aber nicht unbedingt etwas anderes. Der Anbieter erhält z. b. möglicherweise keine positive Bestätigung für seine Anforderung vom Switch, obwohl bereits eine Erfolgsmeldung an die Anwendung gesendet wurde.

## <a name="tapi-3x"></a>TAPI 3. x

Wenn ein Vorgang einen Erfolgsindikator zurückgibt (entweder synchron bei Rückgabe der Funktion für synchrone Vorgänge oder asynchron mit einem Aufrufen der asynchronen [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückruf Prozedur für asynchrone Vorgänge), wird angenommen, dass die folgenden Punkte zutreffen:

-   Die Funktion wurde erfolgreich auf einen vom Dienstanbieter definierten Punkt fortgeführt. Der Dienstanbieter definiert den Punkt auf Funktionsweise Basis. Nachdem dieser Punkt erreicht wurde, ist entweder der Vorgang vollständig abgeschlossen, oder er befindet sich in einem Zustand, in dem die Anwendung durch nachfolgende unabhängige Zustands Meldungen über den Fortschritt informiert wird.
-   Funktionen, die Informationen zurückgeben (z. [**b. TSPI \_ linepark**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) oder [**TSPI \_ linedevspecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)), geben nur dann Erfolg zurück, wenn die angeforderten Informationen dem Aufrufer zur Verfügung stehen. Funktionen, die Handles zurückgeben (zum Öffnen von Zeilen, geöffneten Telefonen oder aufrufen), geben die Handles direkt für die Funktions Rückgabe zurück. Der Dienstanbieter und der Aufrufer müssen die Handles so lange als "noch nicht gültig" behandeln, bis die Erfolgsmeldung "letztlicher" vorliegt. Der Dienstanbieter ist für die Verhinderung von Rückruf Meldungen an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -oder [**phoneevent**](/windows/desktop/api/tspi/nc-tspi-phoneevent) -Prozedur über die geöffnete Zeile, das geöffnete Telefon oder den Anruf bis nach der Erfolgs Anzeige verantwortlich. Wenn das Endergebnis ein Fehler ist, wird jedes sofort zurückgegebene Handle ohne weitere Aktion ungültig.
-   Funktionen, die bestimmte permanente Bedingungen ermöglichen ( [**z. b. TSPI \_ linemonitordigits**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)), geben den Erfolg nur dann zurück, wenn die Bedingung aktiviert ist, nicht, wenn die Bedingung erneut entfernt wird (z. b. nicht, wenn die Ziffern Überwachung abgeschlossen ist).
-   Aufrufen von Steuerungsfunktionen (z. [**b. TSPI \_ linehold**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) und [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer), aber nicht [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)) geben Erfolg zurück, wenn der Vorgang abgeschlossen ist. In Telefonieumgebungen, die keine positive Bestätigung dieser Funktionen bieten, wird der Dienstanbieter gezwungen, eine bestmögliche Entscheidung hinsichtlich des Erfolgs oder Fehlers der Funktion zu treffen.
-   Die Implementierung von [**TSPI \_ linemakecall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) durch einen Dienstanbieter muss erfolgreich sein, wenn der Anruf in den Status der *fort* setzungs Aufrufe wechselt. Im Idealfall gibt der Anbieter den Erfolg so bald wie möglich an, z. b. wenn der-Befehl in den *dialtoneverfahren* -Ansichts Zustand wechselt (falls zutreffend). Wenn "Success" an die Anwendung zurückgegeben wird, wird der Aufrufer von [**Zeilen \_ Aufruf Zustands**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Meldungen über den Status des Aufrufes informiert. Dienstanbieter, die die Rückgabe der **TSPI- \_ linemakecall** -Erfolgs Anzeige verzögern, z. b. bis nach Abschluss des Wählens, schränken die Flexibilität auf Anwendungsebene erheblich ein. Eine Verzögerung bei der Rückgabe des Erfolgs in **TSPI \_ linemakecall** verhindert, dass ein Benutzer die Anforderung zum Einrichten des aufrufssetups abbricht, bis die Wahl abgeschlossen ist, und alle Ziffern werden an den Switch gesendet.

 

 
