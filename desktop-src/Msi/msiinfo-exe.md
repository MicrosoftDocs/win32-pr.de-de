---
description: Msiinfo.exe ist ein Befehlszeilenprogramm, das Datenbankfunktionen und installerfunktionen verwendet, um den Zusammenfassungs Informationsdaten Strom einer Datenbank zu bearbeiten oder anzuzeigen.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98291c26678efa8b17b42c08bb34c0d1df16c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867915"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe ist ein Befehlszeilenprogramm, das [Datenbankfunktionen](database-functions.md) und [installerfunktionen](installer-functions.md) verwendet, um den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) einer Datenbank zu bearbeiten oder anzuzeigen.

## <a name="syntax"></a>Syntax

**Msiinfo** *{Database} \[ \[ /B \] /D \] {Option} {Data}*

-   Bei der Datenbank kann es sich nicht um eine schreibgeschützte Datenbank handeln.
-   Wenn keine Daten auf eine Option folgen, wird die entsprechende Eigenschaft entfernt.
-   In der Befehlszeile können maximal 20 Optionen angegeben werden. Die gleichen Eigenschaften können mehrmals angegeben werden.
-   Wenn die Daten ein Leerzeichen enthalten, schließen Sie die Daten mit Anführungszeichen ein. Beispielsweise/T "My Title".

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msiinfo.exe verwendet die folgenden Befehlszeilenoptionen für die Groß-und Kleinschreibung. Ein Schrägstrich kann auch anstelle eines Bindestrichs verwendet werden. Weitere Informationen finden Sie unter [Zusammenfassungs Informationsdaten Strom-Eigenschaften Satz](summary-information-stream-property-set.md).



| Option | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                      | Eigenschafts-ID        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *keine* | Wenn keine Optionen angegeben sind, zeigt das Hilfsprogramm die aktuellen Werte der Eigenschaften der Zusammenfassungs Informationen an.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Zeigt Informationen zu jeder Zeichenfolge im Zeichen folgen Pool an. Die Option-b ist nur gültig, wenn-d ebenfalls verwendet wird und-b vor der Option-d stehen muss.                                                                                                                                                                                                                 |                    |     |
| -d     | Zeigt Informationen zum Zeichen folgen Pool an. Überprüft den Zeichen folgen Pool und stellt Informationen über die Codepage der Datenbank bereit. Beachten Sie, dass sich die Codepage der Datenbank von der Codepage des Zusammenfassungs Informationsdaten Stroms (PID- \_ Codepage) unterscheidet. Diese Option überprüft auch jede Zeichenfolge auf Zeichen, die auf der Codepage der Datenbank ungültig sind. |                    |     |
| -i     | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | PID- \_ Wörterbuch    | 0   |
| -c     | Legt die [**Codepage-Zusammenfassungs Eigenschaft**](codepage-summary.md)fest.                                                                                                                                                                                                                                                                                                  | PID- \_ Codepage      | 1   |
| -t     | Legt die [**Eigenschaft für die Titel Zusammenfassung**](title-summary.md)fest.                                                                                                                                                                                                                                                                                                        | PID- \_ Titel         | 2   |
| -j     | Legt die [**betreffübersichts Eigenschaft**](subject-summary.md)fest.                                                                                                                                                                                                                                                                                                    | ID-PID- \_ Betreff    | 3   |
| -a     | Legt die [**Zusammenfassungs Eigenschaft des Autors**](author-summary.md)fest.                                                                                                                                                                                                                                                                                                      | PID- \_ Autor        | 4   |
| -k     | Legt die [**Schlüsselwort Zusammenfassungs Eigenschaft**](keywords-summary.md)fest.                                                                                                                                                                                                                                                                                                  | PID- \_ Schlüsselwörter      | 5   |
| -o     | Legt die [**Eigenschaft für die Kommentar Zusammenfassung**](comments-summary.md)fest.                                                                                                                                                                                                                                                                                                  | PID- \_ Kommentare      | 6   |
| -p     | Legt die [**Vorlagen Zusammenfassungs Eigenschaft**](template-summary.md)fest.                                                                                                                                                                                                                                                                                                  | PID- \_ Vorlage      | 7   |
| -l     | Legt die [**letzte gespeicherte by Summary-Eigenschaft**](last-saved-by-summary.md)fest.                                                                                                                                                                                                                                                                                        | PID \_ lastauthor    | 8   |
| -v     | Legt die [**Zusammenfassungs Eigenschaft der Revisionsnummer**](revision-number-summary.md)fest.                                                                                                                                                                                                                                                                                    | PID- \_ revnumber     | 9   |
| -E     | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | PID- \_ EditTime      | 10  |
| -S     | Legt die [**zuletzt gedruckte Zusammenfassungs Eigenschaft**](last-printed-summary.md)fest. Zum Angeben von Jahr, Monat, Tag, Stunde, Minute und Sekunde verwenden Sie das Format "yyyy/mm/dd hh: mm: SS". Beispiel: "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ lastprint   | 11  |
| -r     | Legt die [**Eigenschaft Create time/date Summary**](create-time-date-summary.md)fest. Zum Angeben von Jahr, Monat, Tag, Stunde, Minute und Sekunde verwenden Sie das Format "yyyy/mm/dd hh: mm: SS". Beispiel: "1997/06/20 03:25:59".                                                                                                                                             | PID \_ Erstellen von \_ DTM   | 12  |
| -q     | Legt die [**zuletzt gespeicherte Zeit-/datezusammenfassungs-Eigenschaft**](last-saved-time-date-summary.md)fest. Zum Angeben von Jahr, Monat, Tag, Stunde, Minute und Sekunde verwenden Sie das Format "yyyy/mm/dd hh: mm: SS". Beispiel: "1997/06/20 03:25:59".                                                                                                                                     | PID \_ lastsave \_ DTM | 13  |
| -g     | Legt die [**Zusammenfassungs Eigenschaft der Seitenanzahl**](page-count-summary.md)fest.                                                                                                                                                                                                                                                                                              | PID- \_ PageCount     | 14  |
| -w     | Legt die [**Zusammenfassungs Eigenschaft der Wort Zählung**](word-count-summary.md)fest.                                                                                                                                                                                                                                                                                              | PID- \_ WordCount     | 15  |
| -h     | Legt die [**Zusammenfassungs Eigenschaft für die Zeichen Anzahl**](character-count-summary.md)fest.                                                                                                                                                                                                                                                                                    | PID- \_ Anzahl     | 16  |
|        | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | PID- \_ Miniaturansicht     | 17  |
| -n     | Legt die [**Zusammenfassungs Eigenschaft**](creating-application-summary.md)für die Erstellung von Anwendungen fest.                                                                                                                                                                                                                                                                          | PID- \_ appname       | 18  |
| -U     | Legt die [**Sicherheits Zusammenfassungs Eigenschaft**](security-summary.md)fest.                                                                                                                                                                                                                                                                                                  | PID- \_ Sicherheit      | 19  |



 

Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Tools für Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und verteilbare Dateien](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



