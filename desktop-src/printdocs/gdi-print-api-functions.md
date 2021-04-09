---
description: GDI-druckapi-Funktionen
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: GDI-druckapi-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125e5feef16a64433dadd11e830a09241877a453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864756"
---
# <a name="gdi-print-api-functions"></a>GDI-druckapi-Funktionen

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abortdoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | Die [**abortdoc**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) -Funktion hält den aktuellen Druckauftrag an und löscht alle Elemente, die seit dem letzten Aufrufen der [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) -Funktion gezeichnet wurden.<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | Die [**AbortProc**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) -Funktion ist eine Anwendungs definierte Rückruffunktion, die mit der [**SETABORTPROC**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) -Funktion verwendet wird. Sie wird aufgerufen, wenn ein Druckauftrag während des Spoolvorgangs abgebrochen werden soll. Der **AbortProc** -Typ definiert einen Zeiger auf diese Rückruffunktion. **AbortProc** ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.<br/> |
| [**Gerätefunktionen**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | Die Funktion [**devicecapabiliruft**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) die Funktionen eines Druckertreibers ab.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | Die [**EndDoc**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) -Funktion beendet einen Druckauftrag.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | Die **EndPage** -Funktion benachrichtigt das Gerät, dass die Anwendung das Schreiben auf eine Seite abgeschlossen hat. Diese Funktion wird normalerweise verwendet, um den Gerätetreiber anzuweisen, eine neue Seite zu verwenden.<br/>                                                                                                                                                                             |
| [**ESC**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | ermöglicht es einer Anwendung, auf die System definierten Gerätefunktionen zuzugreifen, die über GDI nicht verfügbar sind.<br/>                                                                                                                                                                                                                                                         |
| [**Extescape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | Die [**extescape**](/windows/desktop/api/wingdi/nf-wingdi-extescape) -Funktion ermöglicht einer Anwendung den Zugriff auf Gerätefunktionen, die über GDI nicht verfügbar sind.<br/>                                                                                                                                                                                                                                |
| [**Iswindowredirectedforprint**](iswindowredirectedforprint.md)<br/> | Die [**iswindowredirectedforprint**](iswindowredirectedforprint.md) -Funktion bestimmt, ob das angegebene Fenster zurzeit zum Drucken umgeleitet wird.<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | Die [**PrintWindow**](/windows/desktop/api/winuser/nf-winuser-printwindow) -Funktion kopiert ein visuelles Fenster in den angegebenen Gerätekontext (DC), in der Regel ein Drucker-DC.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | Die [**SETABORTPROC**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) -Funktion legt die Anwendungs definierte Abbruch Funktion fest, mit der ein Druckauftrag während des Spoolvorgangs abgebrochen werden kann.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | Die [**StartDoc**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) -Funktion startet einen Druckauftrag.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | Die [**Startpage**](/windows/desktop/api/wingdi/nf-wingdi-startpage) -Funktion bereitet den Druckertreiber auf die Annahme von Daten vor.<br/>                                                                                                                                                                                                                                                                             |



 

 

