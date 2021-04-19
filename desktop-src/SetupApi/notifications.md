---
description: Benachrichtigungen sind Werte, die von einer Setup Funktion an eine Rückruf Routine gesendet werden, um einen Status oder ein Ereignis anzugeben. Zwei Parameter, param1 und param2, werden mit der Benachrichtigung gesendet und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind.
ms.assetid: 93434558-ae83-4ea2-9324-659e5873a8c3
title: Benachrichtigungen (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096d4261a99e0a837a90aa5c965a3b676843945d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353618"
---
# <a name="notifications-setup-api"></a>Benachrichtigungen (Setup-API)

Benachrichtigungen sind Werte, die von einer Setup Funktion an eine Rückruf Routine gesendet werden, um einen Status oder ein Ereignis anzugeben. Zwei Parameter, *param1* und *Param2*, werden mit der Benachrichtigung gesendet und enthalten zusätzliche Informationen, die für die Benachrichtigung relevant sind.

Die Rückruf Routine verarbeitet die Benachrichtigung und gibt eine Ganzzahl ohne Vorzeichen an die Setup-Funktion zurück. Abhängig von der Setup Funktion können Sie diesen Wert verwenden, um einen Vorgang oder eine Benutzer Auswahl anzugeben, oder Sie können ihn ignorieren.

Die Setup Funktionen senden mithilfe der folgenden Syntax Benachrichtigungen an Rückruf Routinen.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //notification code
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

Der *Kontext* Parameter ist ein void-Zeiger auf eine Kontext Variable oder-Struktur, die von der Rückruf Routine zum Speichern von Informationen verwendet werden kann, die zwischen nachfolgenden Aufrufen der Rückruf Routine bestehen müssen.

Da die Rückruf Routine die Implementierung des Kontexts angibt und nie von den Setup Funktionen referenziert oder geändert wird, ist der Kontext im Verweis Material der folgenden Benachrichtigungs Meldungen nicht dokumentiert.

Der *Benachrichtigungs* Parameter gibt einen ganzzahligen Wert ohne Vorzeichen für ein Ereignis oder einen Status an, der bewirkt, dass die Setup Funktion die Rückruf Routine aufruft.

*Param1* und *Param2* sind optionale Parameter, die zusätzliche für die Benachrichtigung relevante Informationen enthalten können. Diese Parameter sind ganze Zahlen ohne Vorzeichen. Wenn *param1* oder *Param2* Informationen zurückgibt, bei denen es sich nicht um eine Ganzzahl ohne Vorzeichen handelt, wird Sie in eine ganze Zahl ohne Vorzeichen umgewandelt und muss in ihren ursprünglichen Datentyp konvertiert werden, bevor Sie von der Rückruf Routine verwendet werden kann.

> [!Note]  
> Die folgenden Benachrichtigungen stellen jede Benachrichtigung dar, die von den Setup Funktionen verwendet wird. Einzelne Funktionen verwenden eine Teilmenge dieser Benachrichtigungen. Anders ausgedrückt: nicht jede Benachrichtigung wird von jeder Funktion verwendet.

 

Die folgenden Benachrichtigungen werden von den Setup Funktionen verwendet.



| Benachrichtigung                                                                     | Beschreibung                                                                                   |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**spfilenotify \_ copyError**](spfilenotify-copyerror.md)                        | Fehler während eines Datei Kopiervorgangs.                                               |
| [**deleteerror für spfilenotify \_**](spfilenotify-deleteerror.md)                    | Fehler beim Löschen der Datei.                                           |
| [**spfilenotify- \_ endkopie**](spfilenotify-endcopy.md)                            | Ein Datei Kopiervorgang wurde beendet.                                                              |
| [**spfilenotify- \_ enddelete**](spfilenotify-enddelete.md)                        | Ein Datei Löschvorgang wurde beendet.                                                          |
| [**spfilenotify- \_ endwarteschlange**](spfilenotify-endqueue.md)                          | Der Commit der Warteschlange ist abgeschlossen.                                                            |
| [**spfilenotify- \_ endregistrierung**](spfilenotify-endregistration.md)            | Die Registrierung oder Aufhebung der Registrierung der Datei wurde beendet.                                  |
| [**spfilenotify \_ endrename**](spfilenotify-endrename.md)                        | Ein Vorgang zum Umbenennen der Datei wurde beendet.                                                            |
| [**spfilenotifident \_ endsubqueue**](spfilenotify-endsubqueue.md)                    | Eine unter Warteschlange (kopieren, umbenennen oder löschen) wurde beendet.                                         |
| [**spfilenotifizieren von \_ fileextrahierung**](spfilenotify-fileextracted.md)                | Die Datei wurde aus der CAB-Datei extrahiert.                                                 |
| [**spfilenotify \_ filinput Cabinet**](spfilenotify-fileincabinet.md)                | In der CAB-Datei ist eine Datei aufgetreten.                                                         |
| [**\_spfilenotififileopverzögert**](spfilenotify-fileopdelayed.md)                | Die Datei wurde verwendet, und der aktuelle Vorgang wurde verzögert, bis das System neu gestartet wird. |
| [**spfilenotify nicht übereinstimmende \_**](spfilenotify-langmismatch.md)                  | Die Sprache des aktuellen Vorgangs entspricht nicht der Systemsprache.                     |
| [**spfilenotify \_ needmedia**](spfilenotify-needmedia.md)                        | Es ist ein neues Quell Medium erforderlich.                                                                 |
| [**spfilenotify \_ neednewcabinet**](spfilenotify-neednewcabinet.md)              | Die aktuelle Datei wird in der nächsten CAB-Datei fortgesetzt.                                            |
| [**spfilenotify \_ queuescan**](spfilenotify-queuescan.md)                        | Ein Knoten in der Datei Warteschlange wurde gescannt.                                                    |
| [**spfilenotify \_ queuescan \_ Ex**](spfilenotify-queuescan-ex.md)                 | Ein Knoten in der Datei Warteschlange wurde gescannt.                                                    |
| [**spfilenotify Queue \_ \_ Info Info**](spfilenotify-queuescan-signerinfo.md) | Ein Knoten in der Datei Warteschlange wurde gescannt.                                                    |
| [**spfilenotify \_ renameerror**](spfilenotify-renameerror.md)                    | Fehler während eines Datei Umbenennungs Vorgangs.                                             |
| [**spfilenotify \_ StartCopy**](spfilenotify-startcopy.md)                        | Ein Datei Kopiervorgang wurde gestartet.                                                            |
| [**spfilenotify \_ startdelete**](spfilenotify-startdelete.md)                    | Ein Datei Löschvorgang wurde gestartet.                                                          |
| [**spfilenotify \_ startqueue**](spfilenotify-startqueue.md)                      | Der Commit der Warteschlange wurde gestartet.                                                              |
| [**spfilenotify \_ startregistration**](spfilenotify-startregistration.md)        | Die Registrierung oder Aufhebung der Registrierung der Datei wurde gestartet.                                   |
| [**spfilenotify \_ startrename**](spfilenotify-startrename.md)                    | Ein Vorgang zum Umbenennen von Dateien wurde gestartet.                                                          |
| [**spfilenotify \_ startsubqueue**](spfilenotify-startsubqueue.md)                | Eine unter Warteschlange (kopieren, umbenennen oder löschen) wurde gestartet.                                       |
| [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md)                  | Eine Kopie der angegebenen Datei ist bereits auf dem Ziel vorhanden.                                    |
| [**spfilenotify \_ targetneuere**](spfilenotify-targetnewer.md)                    | Eine neuere Version der angegebenen Datei ist auf dem Ziel vorhanden.                                   |



 

 

 



