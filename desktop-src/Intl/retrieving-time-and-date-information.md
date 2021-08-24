---
description: Dieses Thema enthält Anweisungen für die Verwendung der NLS-Funktionen in Ihren Anwendungen zum Abrufen von Uhrzeit- und Datumsinformationen sowie Dauerdaten. Wenn Ihre Anwendung Daten beibehalten muss, finden Sie weitere Informationen unter Verwenden von persistenten Gebietsschemadaten.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Abrufen von Uhrzeit- und Datumsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f461f12cb1c6324892a415142c159ba570759128e61dd02b53a7cceebccc57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040410"
---
# <a name="retrieving-time-and-date-information"></a>Abrufen von Uhrzeit- und Datumsinformationen

Dieses Thema enthält Anweisungen für die Verwendung der NLS-Funktionen in Ihren Anwendungen zum Abrufen von [Uhrzeit- und Datumsinformationen](time-and-date.md) sowie Dauerdaten. Wenn Ihre Anwendung Daten beibehalten muss, finden Sie weitere Informationen unter [Verwenden von persistenten Gebietsschemadaten.](using-persistent-locale-data.md)

**Windows Vista und höher:** Die in diesem Thema erläuterten Funktionen können Daten aus [benutzerdefinierten Gebietsschemas](custom-locales.md)abrufen. Insbesondere können sie verwendet werden, um Uhrzeit- und Datumsformate anzupassen. Beispielsweise ist es möglich, ein Zeitformat wie "hhHmm ess''" zu verwenden, was zu Zeitzeichenfolgen wie "12H34'12''" führt.

## <a name="retrieve-time-information"></a>Abrufen von Zeitinformationen

Ihre Anwendung kann Zeichenfolgen jederzeit in einem Format abrufen, das für das aktuelle Gebietsschema geeignet ist, indem die Funktionen [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) und [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) verwendet werden. Beide Funktionen überprüfen jeden Zeitwert in einer gültigen [**SYSTEMTIME-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) um zu ermitteln, ob sie sich innerhalb des entsprechenden Wertebereichs befindet, wobei die Datumsteile der Struktur ignoriert werden. Wenn einer der Zeitwerte außerhalb des richtigen Bereichs liegt, schlägt die Funktion mit dem Code ERROR \_ INVALID \_ PARAMETER fehl. Die Funktion gibt keine Fehler für eine ungültige Formatzeichenfolge zurück, sondern bildet einfach die bestmögliche Zeitzeichenfolge.

> [!Note]  
> Die NLS-Zeitfunktionen enthalten keine Millisekunden als Teil einer formatierten Zeitzeichenfolge.

 

Um das Zeitformat abzurufen, ohne eine tatsächliche Formatierung durchzuführen, kann die Anwendung die [**GetLocaleInfo-**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) verwenden und die [LOCALE \_ STIMEFORMAT-Konstante](locale-stime-constants.md) im Aufruf angeben.

**Verwenden von Zeitmarkern**

Beispiele für Zeitmarkierungen sind "AM" und "PM" für Englisch (USA) und "de". und "du". für Spanisch (Mexiko). Wenn TIME \_ NOTIMEMARKER im Aufruf von [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)angegeben ist, entfernt die Funktion die Trennzeichen vor und nach dem Zeitmarker. Wenn ein Zeitmarker vorhanden ist und das TIME \_ NOTIMEMARKER-Flag im Aufruf nicht festgelegt ist, lokalisiert die Funktion den Zeitmarker basierend auf dem angegebenen Gebietsschemabezeichner.

**Entfernen von Trennzeichen in den vorherigen Minuten und Sekunden**

Ihre Anwendung kann [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) mit TIME \_ NOMINUTESORSECONDS oder TIME SECONDSCONDS aufrufen, \_ die angegeben wurde, um die Trennzeichen vor den Elementen für Minuten und/oder Sekunden zu entfernen.

**Verwenden des 24-Stunden-Zeitformats**

Wenn Ihre Anwendung das 24-Stunden-Zeitformat unterstützt, kann sie [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) oder [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) mit TIME \_ FORCE24HOURFORMAT aufrufen. Sofern das TIME \_ NOTIMEMARKER-Flag nicht festgelegt ist, zeigt die Funktion einen beliebigen vorhandenen Zeitmarker an.

## <a name="retrieve-date-information"></a>Abrufen von Datumsinformationen

Eine Anwendung kann Zeichenfolgen für jedes Datum in einem Format abrufen, das für das aktuelle Gebietsschema geeignet ist, indem die Funktionen [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) und [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) verwendet werden. Beide Funktionen überprüfen die Datumswerte Jahr, Monat, Tag und Wochentag in einer gültigen [**SYSTEMTIME-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) wobei die Zeitteile der Struktur ignoriert werden. Der Tagname, der abgekürzte Tagname, der Monatsname und der abgekürzte Monatsname werden basierend auf dem Gebietsschemabezeichner lokalisiert. Wenn der Wochentag falsch ist, verwendet die Funktion den richtigen Wert und gibt keinen Fehler zurück. Wenn einer der anderen Datumswerte außerhalb des richtigen Bereichs liegt, schlägt die Funktion mit dem Code ERROR \_ INVALID \_ PARAMETER fehl. Die Funktion gibt keine Fehler für eine ungültige Formatzeichenfolge zurück, sondern bildet einfach die bestmögliche Datumszeichenfolge.

Wenn die Anwendung das Datumsformat für einen bestimmten Kalender erfordert, sollte [**sie GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) oder [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)verwenden, wobei der entsprechende [**Kalenderbezeichner**](calendar-identifiers.md)übergeben wird. Um alle Datumsformate für einen bestimmten Kalender zurückzugeben, kann die Anwendung [**EnumCalendarInfoEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) [**EnumCalendarInfoExEx,**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex) [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)oder [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)verwenden.

**Angeben eines alternativen Kalenders**

Die Anwendung kann [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) oder [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) mit dem Flag DATE \_ USE ALT CALENDAR \_ \_ aufrufen, um das Standardformat für den angegebenen alternativen Kalender zu verwenden. Wenn kein Standardformat für den alternativen Kalender vorhanden ist, verwendet die Funktion die Benutzerüberschreibungen.

Um das Datumsformat für einen alternativen Kalender abzurufen, kann die Anwendung [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der [LOCALE \_ IOPTIONALCALENDAR-Konstante](locale-ioptionalcalendar.md) verwenden.

**Angeben des Datumstyps**

Wenn die Anwendung das kurze Datumsformat verwenden möchte, gibt sie DATE \_ SHORTDATE im Aufruf von [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) oder [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)an. Ein langes Datumsformat kann abgerufen werden, indem DATE \_ LONGDATE im Funktionsaufruf angegeben wird. Wenn kein Flag angegeben ist und *lpFormat* auf **NULL** festgelegt ist, verwendet die Funktion DATE \_ SHORTDATE als Standard.

Um das kurze und lange Datumsformat für den Standardgebietsschemakalender abzurufen, sollte die Anwendung die [**Funktion GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der [ \_ LOCALE-Konstante SSHORTDATE](locale-sshortdate.md) oder [LOCALE \_ SLONGDATE](locale-slongdate.md) verwenden.

**Angeben des Bilds für das Datumsformat**

Die Anwendung kann ein Datumsformatbild angeben, das [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) oder [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) verwendet, um die Datumszeichenfolge zu bilden. Wenn das Datumsformat für das angegebene Gebietsschema erforderlich ist, kann die Anwendung die Funktion aufrufen, wobei *lpFormat* auf **NULL** festgelegt ist. Wenn der Parameter nicht auf **NULL** festgelegt ist, verwendet die Funktion das Gebietsschema nur für Informationen, die nicht in der Formatbildzeichenfolge angegeben sind, z. B. die Namen von Tag und Monat für das Gebietsschema.

Die Anwendung kann jeden Text, der in exakter Form verbleiben soll, in einfache Anführungszeichen einschließen. Ein einfaches Anführungszeichen kann auch als Escapezeichen verwendet werden, damit die Markierung selbst in der Datumszeichenfolge angezeigt werden kann. Die Escapesequenz muss jedoch in zwei einfache Anführungszeichen eingeschlossen werden. Um beispielsweise das Datum als "Mai '93' anzuzeigen, lautet die Formatzeichenfolge: "MMMM ''''yy '.

## <a name="retrieve-duration-information"></a>Abrufen von Informationen zur Dauer

**Windows Vista und höher:** Die Funktionen [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) und [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) sind verfügbar, um Dauerformate für Gebietsschemas abzurufen, einschließlich benutzerdefinierter Gebietsschemas. Um das Standarddauerformat für ein Gebietsschema abzurufen, sollte die Anwendung die [**Funktion GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) oder [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) mit der [ \_ LOCALE SDURATION-Konstante](locale-sduration.md) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprachen](about-national-language-support.md)
</dt> <dt>

[Uhrzeit und Datum](time-and-date.md)
</dt> <dt>

[Verwenden von persistenten Gebietsschemadaten](using-persistent-locale-data.md)
</dt> </dl>

 

 
