---
description: In diesem Thema werden die Kalenderbezeichner (Datentyp CALID) definiert, die zum Angeben verschiedener Kalender verwendet werden.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Kalenderbezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5f9f21aeff1143c4f981e3bfae20214f1b86e86307f7f32b103a19ef99b9803
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083030"
---
# <a name="calendar-identifiers"></a>Kalenderbezeichner

In diesem Thema werden die Kalenderbezeichner (Datentyp CALID) definiert, die zum Angeben verschiedener Kalender verwendet werden. Ihre Anwendungen können diese Bezeichner verwenden, wenn sie die folgenden NLS-Funktionen und Rückruffunktionen verwenden, die Parameter mit dem CALID-Datentyp aufweisen:

-   [**ConvertSystemTimeToCalDateTime**](convertsystemtimetocaldatetime.md)
-   [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   [**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))
-   [**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))
-   [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [**GetCalendarSupportedDateRange**](getcalendarsupporteddaterange.md)
-   [**IsCalendarLeapYear**](iscalendarleapyear.md)
-   [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

Die folgenden Werte sind definiert. Alle anderen Werte sind reserviert. Diese Werte können nicht miteinander kombiniert werden.



Kalenderbezeichner

Bedeutung

1

CAL \_ GREGORIAN

Gregorianisch (lokalisiert)

2

CAL \_ GREGORIAN \_ US

Gregorianisch (englische Zeichenfolgen immer)

3

CAL \_ JAPAN

Japanische Japanische Japanische Zeit

4

CAL \_ TAIWAN

Taiwan-Kalender

5

CAL \_ KOREA

Koreanische Tangunzeit

6

CAL \_ HIJRI

Hijri (Arabischer Mondlandefeiler)

7

CAL \_ THAI

Thailändisch

8

CAL \_ HEBRÄISCH

Hebräisch (Lunar)

9

CAL \_ GREGORIAN \_ ME \_ FRENCH

Gregorian Middle East French

10

CAL \_ \_ GREGORIANISCH ARABISCH

Gregorian Arabic

11

CAL \_ GREGORIAN \_ XLIT \_ ENGLISH

Gregorianisches transliteriertes Englisch

12

CAL \_ GREGORIAN \_ XLIT \_ FRENCH

Gregorianisches transliteriertes Französisch

23

CAL \_ UMALQURA

**Windows Vista und höher:** Um Al Qura-Kalender (arabischer Mondlandefzeichen)



 

> [!Note]  
> Die Lücke bei der Nummerierung zwischen den Bezeichnern CAL \_ GREGORIAN \_ XLIT \_ FRENCH und CAL \_ UMALQURA ist beabsichtigt. Der Bezeichner für CAL \_ UMALQURA ist 23, nicht 13.

 

Darüber hinaus ermöglichen [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) und [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) die Verwendung des Werts ENUM \_ ALL \_ CALENDARS, um eine Enumeration aller anwendbaren Kalender anzufordern.

Wert

Bedeutung

0xffffffff

AUFZÄHLEN \_ ALLER \_ KALENDER

Alle anwendbaren Kalender für das angegebene Gebietsschema



 

 

 
