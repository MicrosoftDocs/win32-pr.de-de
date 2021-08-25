---
title: Informationen zu Strsafe.h
description: Eine schlechte Pufferbehandlung ist in vielen Sicherheitsproblemen mit Pufferüberläufen zu sehen.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- Zeichenfolgenfunktionen (string-Funktionen)
- Strsafe.h
- Strsafe-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5d50a6921e2775c64fd4db53393332c667aba975ffa366fb2eb49881b6beaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720590"
---
# <a name="about-strsafeh"></a>Informationen zu Strsafe.h

Eine schlechte Pufferbehandlung ist in vielen Sicherheitsproblemen mit Pufferüberläufen zu sehen. Die in Strsafe.h definierten Funktionen bieten zusätzliche Verarbeitung für die richtige Pufferbehandlung in Ihrem Code. Aus diesem Grund sollen sie ihre integrierten C/C++-Entsprechungen sowie bestimmte Windows ersetzen. Strsafe.h ist im Windows SDK ab Windows XP mit Service Pack 2 (SP2) verfügbar.

Die Strsafe-Funktionen bieten u. a. folgende Vorteile:

-   Die Größe des Zielpuffers wird der Funktion immer bereitgestellt, um sicherzustellen, dass die Funktion nicht über das Ende des Puffers schreibt.

-   Puffer werden garantiert mit NULL beendet, auch wenn der Vorgang das beabsichtigte Ergebnis abschneiden kann.

-   Alle Funktionen geben einen **HRESULT-Wert** zurück, mit nur einem möglichen Erfolgscode (**S \_ OK**).

-   Jede Funktion ist in einer entsprechenden Zeichenanzahl ("cch") oder Byteanzahl ("cb")-Version verfügbar.

-   Die meisten Funktionen verfügen über eine erweiterte Version ("Ex"), die für erweiterte Funktionen verfügbar ist.

Weitere Informationen hierzu finden Sie in den nachfolgenden Abschnitten.

-   [Funktionen für die Zeichenanzahl](#character-count-functions)
-   [Byteanzahlfunktionen](#byte-count-functions)
-   [Verwenden von Strsafe.h](#using-strsafeh)
-   [Zugehörige Themen](#related-topics)

## <a name="character-count-functions"></a>Funktionen für die Zeichenanzahl

Die folgenden Funktionen verwenden eine Zeichenanzahl anstelle einer Byteanzahl.



| Funktion                                                                                                                                                                                                                      | Ersetzt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Byteanzahlfunktionen

Die folgenden Funktionen verwenden eine Byteanzahl anstelle einer Zeichenanzahl.



| Funktion                                                                                                                                                                                                                  | Ersetzt                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**StrCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**StringCbCatn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **StrNCat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**StrCpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**StringCbCopyn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Verwenden von Strsafe.h

-   Um die Strsafe-Funktionen inline zu verwenden, schließen Sie die Headerdatei wie hier gezeigt ein, und folgen Sie dabei den **\# include-Anweisungen** für alle anderen Headerdateien.

    `#include <strsafe.h>`

-   Um die Funktionen in Bibliotheksform zu verwenden, schließen Sie die folgende Anweisung ein, bevor Sie Strsafe.h hinzufügen. Es wird jedoch empfohlen, die Inlinefunktionen zu verwenden.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : Die folgenden Funktionen müssen als Inlinefunktionen verwendet werden: [**StringCbGets,**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa) [**StringCbGetsEx,**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa) [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)und [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa).

     

-   Wenn Sie Strsafe.h in Ihre Datei einreihen, sind die älteren Funktionen, die durch die Strsafe.h-Funktionen ersetzt werden, veraltet. Versuche, diese älteren Funktionen zu verwenden, führen zu einem Compilerfehler, der Sie anfing, die neueren Funktionen zu verwenden. Wenn Sie dieses Verhalten außer Kraft setzen möchten, schließen Sie die folgende Anweisung ein, bevor Sie Strsafe.h enthalten.

    `#define STRSAFE_NO_DEPRECATE`

-   Um nur Zeichenzählungsfunktionen zu ermöglichen, schließen Sie die folgende Anweisung ein, bevor Sie Strsafe.h enthalten.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Um nur Byteanzahlfunktionen zu erlauben, schließen Sie die folgende -Anweisung ein, bevor Sie Strsafe.h enthalten.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Sie können **STRSAFE \_ NO CB \_ FUNCTIONS \_ oder** **STRSAFE NO \_ \_ CCH \_ FUNCTIONS** definieren, aber nicht beide.

     

-   Einige Strsafe-Funktionen verfügen über lokal orientierte Versionen. Standardmäßig deklariert der Header diese Funktionen nicht. Um diese Deklarationen zu aktivieren, schließen Sie die folgende Makro-Anweisung ein, bevor Sie Strsafe.h enthalten.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   Die maximal unterstützte Zeichenfolgenlänge beträgt 2.147.483.647 Zeichen **(STRSAFE \_ MAX \_ CCH),** entweder ANSI oder Unicode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strsafe-Funktionen](string-overviews.md)
</dt> </dl>

 

 