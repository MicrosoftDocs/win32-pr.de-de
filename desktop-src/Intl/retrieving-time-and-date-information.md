---
description: Dieses Thema enthält Anweisungen für die Verwendung der NLS-Funktionen in Ihren Anwendungen zum Abrufen von Zeit-und Datumsinformationen sowie Dauer Daten. Wenn Ihre Anwendung Daten beibehalten muss, finden Sie weitere Informationen unter Verwenden von permanenten Gebiets Schema Daten.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Abrufen von Zeit-und Datumsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2c2fa1d15de2c1ba5587a981373ff14b1c1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351414"
---
# <a name="retrieving-time-and-date-information"></a>Abrufen von Zeit-und Datumsinformationen

Dieses Thema enthält Anweisungen für die Verwendung der NLS-Funktionen in Ihren Anwendungen zum Abrufen von [Zeit-und Datums](time-and-date.md) Informationen sowie Dauer Daten. Wenn Ihre Anwendung Daten beibehalten muss, finden Sie weitere Informationen unter [Verwenden von permanenten](using-persistent-locale-data.md)Gebiets Schema Daten.

**Windows Vista und höher:** Die in diesem Thema behandelten Funktionen können Daten aus [benutzerdefinierten](custom-locales.md)Gebiets Schemas abrufen. Sie können insbesondere zum Anpassen von Zeit-und Datumsformaten verwendet werden. Beispielsweise ist es möglich, ein Zeitformat wie z. b. "hhhmm' SS ' '" zu haben, was Zeit Zeichenfolgen wie "12h34 ' 12 ' '" ergibt.

## <a name="retrieve-time-information"></a>Abrufen von Zeit Informationen

Die Anwendung kann Zeichen folgen für beliebige Zeit in einem Format erhalten, das für das aktuelle Gebiets Schema geeignet ist, indem die Funktionen [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) und [**gettimeformatex**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) verwendet werden. Beide-Funktionen überprüfen jeden der Uhrzeitwerte in einer gültigen [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, um zu bestimmen, ob Sie sich im entsprechenden Wertebereich befindet, wobei die Datums Teile der Struktur ignoriert werden. Wenn einer der Uhrzeitwerte außerhalb des richtigen Bereichs liegt, schlägt die Funktion mit dem \_ ungültigen Code Fehler \_ Parameter fehl. Die Funktion gibt keine Fehler für eine ungültige Format Zeichenfolge zurück, sondern bildet einfach die bestmögliche Zeit Zeichenfolge.

> [!Note]  
> Die NLS-Zeitfunktionen enthalten keine Millisekunden als Teil einer formatierten Zeit Zeichenfolge.

 

Um das Zeitformat zu erhalten, ohne eine tatsächliche Formatierung auszuführen, kann die Anwendung die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) -Funktion oder die [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) -Funktion verwenden. dabei wird die [locale \_ stimeformat](locale-stime-constants.md) -Konstante im Aufruf angegeben.

**Verwenden von Zeitmarkierungen**

Beispiele für Zeit Marker sind "am" und "PM" für Englisch (USA) und "de". und "Du" Spanisch (Mexiko). Wenn Time \_ notimemarker im Aufruf von [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**gettimeformatex**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)angegeben ist, entfernt die Funktion die Trennzeichen vor und nach dem Zeit Marker. Wenn ein Zeit Marker vorhanden ist und die Zeitangabe für das \_ Benachrichtigungs Kennzeichen im Aufruf nicht festgelegt ist, lokalisiert die Funktion den Zeit Marker auf der Grundlage des angegebenen Gebiets Schema Bezeichners.

**Trennzeichen vor Minuten und Sekunden entfernen**

Die Anwendung kann [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**gettimeformatex**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) mit Time \_ nominutesorseconds oder Time \_ noSeconds aufrufen, um die Trennzeichen vor den Minuten-und/oder Sekunden Elementen zu entfernen.

**Verwenden des 24-Stunden-Zeit Formats**

Wenn Ihre Anwendung das 24-Stunden-Zeitformat unterstützt, kann Sie [**getTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**gettimeformatex**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) mit Time \_ FORCE24HOURFORMAT aufrufen. \_Die Funktion zeigt einen beliebigen vorhandenen Zeit Marker an, es sei denn, das Kennzeichen für die Zeit wird festgelegt.

## <a name="retrieve-date-information"></a>Abrufen von Datumsinformationen

Eine Anwendung kann Zeichen folgen für ein beliebiges Datum in einem Format abrufen, das für das aktuelle Gebiets Schema geeignet ist, indem die Funktionen [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) und [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) verwendet werden. Beide Funktionen überprüfen jeden der Datumswerte Year, month, Day und Day of week in einer gültigen [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) -Struktur, wobei die Zeit Teile der Struktur ignoriert werden. Der TagName, der abgekürzte Tagname, der Monats Name und der abgekürzte Monats Name werden basierend auf dem Gebiets Schema Bezeichner lokalisiert. Wenn der Wochentag nicht korrekt ist, verwendet die Funktion den korrekten Wert und gibt keinen Fehler zurück. Wenn einer der anderen Datumswerte außerhalb des richtigen Bereichs liegt, schlägt die Funktion mit dem \_ ungültigen Code Fehler \_ Parameter fehl. Die Funktion gibt keine Fehler für eine ungültige Format Zeichenfolge zurück, sondern bildet einfach die bestmögliche Datums Zeichenfolge.

Wenn die Anwendung das Datumsformat für einen bestimmten Kalender benötigt, sollte Sie [**getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) oder [**getcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)verwenden und dabei den entsprechenden [**Kalender Bezeichner**](calendar-identifiers.md)übergeben. Um alle Datumsformate für einen bestimmten Kalender zurückzugeben, kann die Anwendung [**enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**enumcalendarinfoexex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**enumdateformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [**enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)verwenden.

**Geben Sie einen alternativen Kalender an.**

Die Anwendung kann [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) oder [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) mit dem Flag "Date \_ \_ alt Calendar" aufrufen \_ , um das Standardformat für den angegebenen alternativen Kalender zu verwenden. Wenn kein Standardformat für den alternativen Kalender vorhanden ist, verwendet die Funktion die Benutzer Überschreibungen.

Um das Datumsformat für einen alternativen Kalender zu erhalten, kann die Anwendung [**getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**getlocaleingefoex**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit dem Gebiets Schema [ \_ ioptionalcalendar](locale-ioptionalcalendar.md) -Konstante verwenden.

**Date-Typ angeben**

Wenn für die Anwendung das kurze Datumsformat verwendet werden soll, wird das Datum " \_ SHORTDATE" beim Aufrufen von " [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) " oder " [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)" angegeben. Ein langes Datumsformat kann abgerufen werden, indem \_ das Date longDate im Funktions aufzurufen angegeben wird. Wenn keines der Flags angegeben wird und das *lpformat* auf **null** festgelegt ist, verwendet die Funktion das Datum " \_ SHORTDATE" als Standardwert.

Um das kurze und lange Datumsformat für den standardmäßigen Gebiets Schema Kalender zu erhalten, sollte die Anwendung die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) -Funktion oder die [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) -Funktion mit dem [Gebiets Schema \_ sshortdate](locale-sshortdate.md) oder der [locale \_ slongdate](locale-slongdate.md) -Konstante verwenden.

**Angeben des Datums Format Bilds**

Die Anwendung kann ein Datumsformat Bild angeben, das [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) oder [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) verwendet, um die Datums Zeichenfolge zu bilden. Wenn das Datumsformat für das angegebene Gebiets Schema erforderlich ist, kann die Anwendung die-Funktion mit dem auf **null** festgelegten *lpformat* abrufen. Wenn der-Parameter nicht auf **null** festgelegt ist, verwendet die Funktion das Gebiets Schema nur für Informationen, die nicht in der Format Bild Zeichenfolge angegeben sind, z. b. die Namen des Tags und Monats für das Gebiets Schema.

Die Anwendung kann Text einschließen, der in der exakten Form in einfachen Anführungszeichen verbleiben soll. Ein einzelnes Anführungszeichen kann auch als Escapezeichen verwendet werden, damit die Markierung selbst in der Datums Zeichenfolge angezeigt wird. Die Escapesequenz muss jedoch in zwei einfache Anführungszeichen eingeschlossen werden. Um beispielsweise das Datum als "Mai 93" anzuzeigen, lautet die Format Zeichenfolge "MMMM ' ' ' ' ' yy '".

## <a name="retrieve-duration-information"></a>Informationen zur Dauer abrufen

**Windows Vista und höher:** Die Funktionen " [**getdurationformat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) " und " [**getdurationformatex**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) " sind zum Abrufen von Dauer Formaten für Gebiets Schemas verfügbar, einschließlich benutzerdefinierter Gebiets Schemata. Um das Standardformat für die Dauer eines Gebiets Schemas zu erhalten, sollte die Anwendung die [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) -Funktion oder die [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) -Funktion mit der [ \_ sduration](locale-sduration.md) -Konstante für locale verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](about-national-language-support.md)
</dt> <dt>

[Uhrzeit und Datum](time-and-date.md)
</dt> <dt>

[Verwenden von persistenten Gebiets Schema Daten](using-persistent-locale-data.md)
</dt> </dl>

 

 
