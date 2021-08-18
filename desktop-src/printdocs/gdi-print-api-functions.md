---
description: GDI-Druck-API-Funktionen
ms.assetid: cf3f4a61-8858-4c91-a778-d2a65998ef70
title: GDI-Druck-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcdb6119a56524d3e94c1c1e35f3f1a95bfb86d6e9a23343b07d4250bfc178eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971509"
---
# <a name="gdi-print-api-functions"></a>GDI-Druck-API-Funktionen

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortDoc**](/windows/desktop/api/Wingdi/nf-wingdi-abortdoc)<br/>                                     | Die [**AbortDoc-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-abortdoc) beendet den aktuellen Druckauftrag und löscht alles, was seit dem letzten Aufruf der [**StartDoc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) gezeichnet wurde.<br/>                                                                                                                                                                                                 |
| [*AbortProc*](/windows/desktop/api/Wingdi/nc-wingdi-abortproc)<br/>                                     | Die [**AbortProc-Funktion**](/windows/desktop/api/wingdi/nc-wingdi-abortproc) ist eine anwendungsdefinierte Rückruffunktion, die mit der [**SetAbortProc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc) verwendet wird. Er wird aufgerufen, wenn ein Druckauftrag während des Spoolings abgebrochen werden soll. Der **ABORTPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion. **AbortProc** ist ein Platzhalter für den anwendungsdefinierte Funktionsnamen.<br/> |
| [**DeviceCapabilities**](/windows/desktop/api/WinGdi/nf-wingdi-devicecapabilitiesa)<br/>                 | Die [**DeviceCapabilities-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-devicecapabilitiesa) ruft die Funktionen eines Druckertreibers ab.<br/>                                                                                                                                                                                                                                                       |
| [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)<br/>                                         | Die [**EndDoc-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-enddoc) beendet einen Druckauftrag.<br/>                                                                                                                                                                                                                                                                                                             |
| [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage)<br/>                                       | Die **EndPage-Funktion** benachrichtigt das Gerät, dass die Anwendung das Schreiben auf eine Seite abgeschlossen hat. Diese Funktion wird in der Regel verwendet, um den Gerätetreiber anweisen, zu einer neuen Seite zu wechseln.<br/>                                                                                                                                                                             |
| [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape)<br/>                                         | ermöglicht einer Anwendung den Zugriff auf die vom System definierten Gerätefunktionen, die nicht über GDI verfügbar sind.<br/>                                                                                                                                                                                                                                                         |
| [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)<br/>                                   | Die [**ExtEscape-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-extescape) ermöglicht einer Anwendung den Zugriff auf Gerätefunktionen, die nicht über GDI verfügbar sind.<br/>                                                                                                                                                                                                                                |
| [**IsWindowRedirectedForPrint**](iswindowredirectedforprint.md)<br/> | Die [**IsWindowRedirectedForPrint-Funktion**](iswindowredirectedforprint.md) bestimmt, ob das angegebene Fenster derzeit zum Drucken umgeleitet wird.<br/>                                                                                                                                                                                                         |
| [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)<br/>                               | Die [**PrintWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-printwindow) kopiert ein visuelles Fenster in den angegebenen Gerätekontext (DC), in der Regel einen Druckerdomänencontroller.<br/>                                                                                                                                                                                                                              |
| [**SetAbortProc**](/windows/desktop/api/Wingdi/nf-wingdi-setabortproc)<br/>                             | Die [**SetAbortProc-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-setabortproc) legt die anwendungsdefinierte Abbruchfunktion fest, mit der ein Druckauftrag während des Spoolings abgebrochen werden kann.<br/>                                                                                                                                                                                                               |
| [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)<br/>                                     | Die [**StartDoc-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-startdoca) startet einen Druckauftrag.<br/>                                                                                                                                                                                                                                                                                                       |
| [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage)<br/>                                   | Die [**StartPage-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-startpage) bereitet den Druckertreiber auf das Akzeptieren von Daten vor.<br/>                                                                                                                                                                                                                                                                             |



 

 

