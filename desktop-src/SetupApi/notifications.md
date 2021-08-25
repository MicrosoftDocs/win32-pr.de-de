---
description: Benachrichtigungen sind Werte, die eine Setupfunktion an eine Rückrufroutine sendet, um einen Zustand oder ein Ereignis anzugeben. Die beiden Parameter Param1 und Param2 werden mit der Benachrichtigung gesendet und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Benachrichtigungen (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f602e2062be01e3f521147d7a820d3afc1424f5421667716d3f8d4273f0dd866
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992660"
---
# <a name="notifications-setup-api"></a>Benachrichtigungen (Setup-API)

Benachrichtigungen sind Werte, die eine Setupfunktion an eine Rückrufroutine sendet, um einen Zustand oder ein Ereignis anzugeben. Die beiden Parameter *Param1* und *Param2* werden mit der Benachrichtigung gesendet und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind.

Die Rückrufroutine verarbeitet die Benachrichtigung und gibt eine ganze Zahl ohne Vorzeichen an die Setupfunktion zurück. Abhängig von der Setupfunktion können Sie diesen Wert verwenden, um einen Vorgang oder eine Benutzerauswahl anzugeben, oder Sie können ihn ignorieren.

Die Setupfunktionen senden mithilfe der folgenden Syntax Benachrichtigungen an Rückrufroutinen.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Der *Context-Parameter* ist ein void-Zeiger auf eine Kontextvariable oder -struktur, mit der die Rückrufroutine Informationen speichern kann, die zwischen nachfolgenden Aufrufen der Rückrufroutine beibehalten werden müssen.

Da die Rückrufroutine die Implementierung des Kontexts angibt und nie von den Setupfunktionen darauf verwiesen oder geändert wird, wird der Kontext nicht im Referenzmaterial für die folgenden Benachrichtigungsmeldungen dokumentiert.

Der *Notification-Parameter* gibt einen ganzzahligen Wert ohne Vorzeichen für ein Ereignis oder einen Zustand an, der bewirkt, dass die Setupfunktion die Rückrufroutine aufruft.

*Param1* und *Param2* sind optionale Parameter, die zusätzliche Informationen enthalten können, die für die Benachrichtigung relevant sind. Diese Parameter sind ganze Zahlen ohne Vorzeichen. Wenn *Param1* oder *Param2* Informationen zurückgeben, die keine ganze Zahl ohne Vorzeichen sind, wird sie in eine ganze Zahl ohne Vorzeichen umgeformt und muss in ihren ursprünglichen Datentyp umgeformt werden, bevor sie von der Rückrufroutine verwendet werden kann.

> [!Note]  
> Die folgenden Benachrichtigungen stellen jede Benachrichtigung dar, die von den Setupfunktionen verwendet wird. Einzelne Funktionen verwenden eine Teilmenge dieser Benachrichtigungen. Anders ausgedrückt: Nicht jede Benachrichtigung wird von jeder Funktion verwendet.

 

Die folgenden Benachrichtigungen werden von den Setupfunktionen verwendet.



| Benachrichtigung                                                                     | Beschreibung                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)                        | Während eines Dateikopiervorgangs ist ein Fehler aufgetreten.                                               |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)                    | Während eines Dateilöschvorgangs ist ein Fehler aufgetreten.                                           |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)                            | Ein Dateikopiervorgang wurde beendet.                                                              |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)                        | Ein Dateilöschvorgang wurde beendet.                                                          |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)                          | Der Commit für die Warteschlange wurde abgeschlossen.                                                            |
| [**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)            | Die Registrierung oder Aufhebung der Registrierung der Datei wurde abgeschlossen.                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)                        | Ein Datei-Umbenennungsvorgang wurde beendet.                                                            |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)                    | Eine Unterabfrage (kopieren, umbenennen oder löschen) wurde beendet.                                         |
| [**SPFILENOTIFY \_ FILEEXTRACTED**](spfilenotify-fileextracted.md)                | Die Datei wurde aus dem Schränk extrahiert.                                                 |
| [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md)                | Eine Datei wird im Schränk gefunden.                                                         |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md)                | Die Datei wurde verwendet, und der aktuelle Vorgang wurde verzögert, bis das System neu gestartet wurde. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)                  | Die Sprache des aktuellen Vorgangs stimmt nicht mit der Systemsprache überein.                     |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)                        | Neue Quellmedien sind erforderlich.                                                                 |
| [**SPFILENOTIFY \_ NEEDNEWCABINET**](spfilenotify-neednewcabinet.md)              | Die aktuelle Datei wird im nächsten Schränk fortgesetzt.                                            |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)                        | Ein Knoten in der Dateiwarteschlange wurde überprüft.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ EX**](spfilenotify-queuescan-ex.md)                 | Ein Knoten in der Dateiwarteschlange wurde überprüft.                                                    |
| [**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO**](spfilenotify-queuescan-signerinfo.md) | Ein Knoten in der Dateiwarteschlange wurde überprüft.                                                    |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)                    | Fehler beim Umbenennen einer Datei.                                             |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)                        | Ein Dateikopiervorgang wurde gestartet.                                                            |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)                    | Ein Dateilöschvorgang wurde gestartet.                                                          |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)                      | Die Warteschlange hat mit dem Commit begonnen.                                                              |
| [**SPFILENOTIFY \_ STARTREGISTRATION**](spfilenotify-startregistration.md)        | Die Registrierung oder Aufhebung der Registrierung der Datei wurde gestartet.                                   |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)                    | Ein Datei-Umbenennungsvorgang wurde gestartet.                                                          |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md)                | Eine Unterabfrage (kopieren, umbenennen oder löschen) wurde gestartet.                                       |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)                  | Eine Kopie der angegebenen Datei ist bereits auf dem Ziel vorhanden.                                    |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)                    | Eine neuere Version der angegebenen Datei ist auf dem Ziel vorhanden.                                   |



 

 

 



