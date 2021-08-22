---
description: Msiinfo.exe ist ein Befehlszeilenprogramm, das Datenbankfunktionen und Installerfunktionen verwendet, um den Zusammenfassungsinformationsdatenstrom einer Datenbank zu bearbeiten oder anzuzeigen.
ms.assetid: 3f60146e-12bf-4755-bbca-93bb1c300fb7
title: Msiinfo.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57487406533b060d9343d4afbdf7e5254c32e15149bb3385f81cc7dc3923fc71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628098"
---
# <a name="msiinfoexe"></a>Msiinfo.exe

Msiinfo.exe ist ein Befehlszeilenprogramm, das [Datenbankfunktionen](database-functions.md) und [Installerfunktionen](installer-functions.md) verwendet, um den [Zusammenfassungsinformationsdatenstrom](summary-information-stream.md) einer Datenbank zu bearbeiten oder anzuzeigen.

## <a name="syntax"></a>Syntax

**MsiInfo** *{database} \[ \[ /B \] /D \] {option}{data}*

-   Die Datenbank kann keine schreibgeschützte Datenbank sein.
-   Wenn keine Daten auf eine Option folgen, wird die entsprechende Eigenschaft entfernt.
-   In der Befehlszeile können maximal 20 Optionen angegeben werden. Die gleichen Eigenschaften können mehrmals angegeben werden.
-   Wenn die Daten ein Leerzeichen enthalten, schließen Sie die Daten in Anführungszeichen ein. Beispiel: /T "MY TITLE".

## <a name="command-line-options"></a>Befehlszeilenoptionen

Msiinfo.exe verwendet die folgenden Befehlszeilenoptionen, bei der die Groß-/Kleinschreibung nicht beachtet wird. Anstelle eines Bindestrichs kann auch ein Schrägstrichtrennzeichen verwendet werden. Weitere Informationen finden Sie unter [Stream-Eigenschaftensatz für Zusammenfassungsinformationen.](summary-information-stream-property-set.md)



| Option | Beschreibung                                                                                                                                                                                                                                                                                                                                                      | Eigenschafts-ID        | PID |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|-----|
| *keine* | Wenn keine Optionen angegeben sind, zeigt das Hilfsprogramm die aktuellen Werte der Eigenschaften zusammenfassungsinformationen an.                                                                                                                                                                                                                                                      |                    |     |
| -b     | Zeigt Informationen zu jeder Zeichenfolge im Zeichenfolgenpool an. Die Option -b ist nur gültig, wenn auch -d verwendet wird und -b vor der Option -d steht.                                                                                                                                                                                                                 |                    |     |
| -d     | Zeigt Informationen zum Zeichenfolgenpool an. Überprüft den Zeichenfolgenpool und stellt Informationen zur Codepage der Datenbank bereit. Beachten Sie, dass sich die Codepage der Datenbank von der Codepage des Datenstroms "Zusammenfassungsinformationen" (PID \_ CODEPAGE) unterscheidet. Diese Option überprüft auch jede Zeichenfolge auf Zeichen, die in der Codepage der Datenbank ungültig sind. |                    |     |
| -i     | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | PID \_ DICTIONARY    | 0   |
| -c     | Legt die [**Codepage-Zusammenfassungseigenschaft fest.**](codepage-summary.md)                                                                                                                                                                                                                                                                                                  | PID \_ CODEPAGE      | 1   |
| -t     | Legt die [**Titelzusammenfassungseigenschaft fest.**](title-summary.md)                                                                                                                                                                                                                                                                                                        | PID \_ TITLE         | 2   |
| -j     | Legt die [**Subject Summary-Eigenschaft**](subject-summary.md)fest.                                                                                                                                                                                                                                                                                                    | ID PID \_ SUBJECT    | 3   |
| -a     | Legt die [**Author Summary-Eigenschaft fest.**](author-summary.md)                                                                                                                                                                                                                                                                                                      | PID \_ AUTHOR        | 4   |
| -k     | Legt die [**Schlüsselwortzusammenfassungseigenschaft fest.**](keywords-summary.md)                                                                                                                                                                                                                                                                                                  | \_PID-SCHLÜSSELWÖRTER      | 5   |
| -o     | Legt die [**Comments Summary-Eigenschaft**](comments-summary.md)fest.                                                                                                                                                                                                                                                                                                  | \_PID-KOMMENTARE      | 6   |
| -p     | Legt die [**Vorlagenzusammenfassungseigenschaft fest.**](template-summary.md)                                                                                                                                                                                                                                                                                                  | \_PID-VORLAGE      | 7   |
| -l     | Legt die [**Last Saved By Summary-Eigenschaft**](last-saved-by-summary.md)fest.                                                                                                                                                                                                                                                                                        | PID \_ LASTAUTHOR    | 8   |
| -v     | Legt die [**Revision Number Summary-Eigenschaft fest.**](revision-number-summary.md)                                                                                                                                                                                                                                                                                    | PID \_ REVNUMBER     | 9   |
| -E     | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | PID \_ EDITTIME      | 10  |
| -S     | Legt die [**Last Printed Summary-Eigenschaft**](last-printed-summary.md)fest. Um Jahr, Monat, Tag, Stunde, Minute und Sekunde anzugeben, verwenden Sie das Format "yyyy/mm/dd hh:mm:ss". Beispiel: "1997/06/20 03:25:59".                                                                                                                                                     | PID \_ LASTPRINTED   | 11  |
| -r     | Legt die [**Create Time/Date Summary-Eigenschaft**](create-time-date-summary.md)fest. Um Jahr, Monat, Tag, Stunde, Minute und Sekunde anzugeben, verwenden Sie das Format "yyyy/mm/dd hh:mm:ss". Beispiel: "1997/06/20 03:25:59".                                                                                                                                             | PID \_ CREATE \_ PIC   | 12  |
| -q     | Legt die [**Last Saved Time/Date Summary-Eigenschaft**](last-saved-time-date-summary.md)fest. Um Jahr, Monat, Tag, Stunde, Minute und Sekunde anzugeben, verwenden Sie das Format "yyyy/mm/dd hh:mm:ss". Beispiel: "1997/06/20 03:25:59".                                                                                                                                     | PID \_ LASTSAVE \_ PNR | 13  |
| -g     | Legt die [**Page Count Summary-Eigenschaft**](page-count-summary.md)fest.                                                                                                                                                                                                                                                                                              | PID \_ PAGECOUNT     | 14  |
| -w     | Legt die [**Word Count Summary-Eigenschaft fest.**](word-count-summary.md)                                                                                                                                                                                                                                                                                              | PID \_ WORDCOUNT     | 15  |
| -H     | Legt die [**Zeichenanzahl-Zusammenfassungseigenschaft fest.**](character-count-summary.md)                                                                                                                                                                                                                                                                                    | PID \_ CHARCOUNT     | 16  |
|        | Nicht zutreffend Reserviert.                                                                                                                                                                                                                                                                                                                                        | \_PID-MINIATURANSICHT     | 17  |
| -n     | Legt die [**Eigenschaft Creating Application Summary fest.**](creating-application-summary.md)                                                                                                                                                                                                                                                                          | PID \_ APPNAME       | 18  |
| -U     | Legt die [**Sicherheitszusammenfassungseigenschaft**](security-summary.md)fest.                                                                                                                                                                                                                                                                                                  | \_PID-SICHERHEIT      | 19  |



 

Dieses Tool ist nur in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Installationsentwicklungstools](windows-installer-development-tools.md)
</dt> <dt>

[Veröffentlichte Versionen, Tools und Redistributables](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



