---
description: Windows Vista führt eine große Anzahl von Funktionen ein, die Gebiets Schema Namen anstelle von Gebiets Schema Bezeichnernamen verwenden.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Aufrufen der "locale Name"-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58c15d2d9fe7721eb162f8c7cf96084bd4afa2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751152"
---
# <a name="calling-the-locale-name-functions"></a>Aufrufen der "locale Name"-Funktionen

Windows Vista führt eine große Anzahl von Funktionen ein, die Gebiets Schema [Namen](locale-names.md) anstelle von Gebiets Schema [Bezeichnernamen](locale-identifiers.md)verwenden. Diese neuen Funktionen bieten eine gute unter [Stützung für zusätzliche](custom-locales.md)Gebiets Schemas, und einige von Ihnen bieten zusätzliche Funktionen, die in den älteren nls-Funktionen nicht verfügbar sind. Einige von Ihnen, wie z. b. die neuen Enumerationsfunktionen, stellen auch Entwurfs Verbesserungen dar.

> [!Note]  
> Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten die "locale Name"-Funktionen für die NLS-Funktionen verwenden, die Gebiets Schema Bezeichner verwenden.

 

In der folgenden Tabelle werden die Funktionen für den Gebiets Schema Namen zusammen mit den älteren Funktionen aufgelistet, die Sie ersetzen können.



| Funktionen mit Gebiets Schema Namen                                     | Funktionen mit Gebiets Schema Bezeichnerzeichen                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**Comparestringex**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [**Enumcalendarinfoexex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | [**Enumcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [ **enumcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) |
| [**Enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | [**Enumdateformats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [ **enumdateformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)     |
| [**Enumsystemlocalesex**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [**Enumsystemgebiets Schemas**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [**Enumtimeformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [**Enumtimeformats**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [**Findnlsstringex**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [**Findnlsstring**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [**Getcalendarinfoex**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [**Getcalendarinfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [**GetCurrency cyformatex**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [**Gethappcyformat**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [**Getdurationformatex**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [**Getdurationformat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [**Getlocaleingefo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [**Getnlsversion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [**Getnumformatex**](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [**Getnumformat**](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [**Getsystemdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [**Gettimeformatex**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [**Getuserdefaultlocalename**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [**Isvalidlocalename**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [**Isvalidlocale**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [**Lcmapstringex**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a>Beispiel

Ein Beispiel für die Verwendung mehrerer Funktionen, die auf Gebiets Schema Namen basieren, finden Sie im [Beispiel nls: Name-based APIs](nls--name-based-apis-sample.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Unterstützung für nationale Sprache](using-national-language-support.md)
</dt> </dl>

 

 
