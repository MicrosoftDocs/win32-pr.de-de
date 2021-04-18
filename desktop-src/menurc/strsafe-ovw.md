---
title: Informationen zu "strausafe. h"
description: Eine schlechte Puffer Behandlung ist in vielen Sicherheitsproblemen enthalten, die Pufferüberläufe einschließen.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- Zeichenfolgenfunktionen (string-Funktionen)
- "\"Strausafe. h\""
- Strauchsichere Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9b993ccff6d085f3b1eb14c1920c4c633661df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338462"
---
# <a name="about-strsafeh"></a>Informationen zu "strausafe. h"

Eine schlechte Puffer Behandlung ist in vielen Sicherheitsproblemen enthalten, die Pufferüberläufe einschließen. Die in "strausafe. h" definierten Funktionen bieten zusätzliche Verarbeitungsschritte für die ordnungsgemäße Puffer Behandlung in Ihrem Code. Aus diesem Grund sind Sie für die Ersetzung ihrer integrierten C/C++-Entsprechungen sowie bestimmter Windows-Implementierungen vorgesehen. "Strausafe. h" ist im Windows SDK ab Windows XP mit Service Pack 2 (SP2) verfügbar.

Zu den Vorteilen der strauchsicheren Funktionen gehören:

-   Die Größe des Ziel Puffers wird immer der-Funktion bereitgestellt, um sicherzustellen, dass die Funktion nicht über das Ende des Puffers hinaus schreibt.

-   Puffer werden garantiert NULL-terminiert, auch wenn der Vorgang das beabsichtigte Ergebnis abschneidet.

-   Alle Funktionen geben einen **HRESULT** -Wert zurück, wobei nur ein möglicher Erfolgs Code (**S \_ OK**) verwendet wird.

-   Jede Funktion ist in einer entsprechenden Zeichen Anzahl ("CCH") oder Byte Anzahl ("CB")-Version verfügbar.

-   Die meisten Funktionen verfügen über eine erweiterte ("ex") Version, die für erweiterte Funktionen verfügbar ist.

Weitere Informationen hierzu finden Sie in den nachfolgenden Abschnitten.

-   [Zeichen Anzahl Funktionen](#character-count-functions)
-   [Byte Anzahl-Funktionen](#byte-count-functions)
-   [Verwenden von "strausafe. h"](#using-strsafeh)
-   [Zugehörige Themen](#related-topics)

## <a name="character-count-functions"></a>Zeichen Anzahl Funktionen

In den folgenden Funktionen wird anstelle einer Byte Anzahl eine Zeichen Anzahl verwendet.



| Funktion                                                                                                                                                                                                                      | Arbeits                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **stringcch.**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> " <dt>[strecat", "wcscat", " \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrancat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> " </dl>                                                                             |
| <dl> <dt>[**Stringcchovn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **stringcchcatcher**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> " <dt>[strinncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> " <dt> [ ](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **stringcchcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[cpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrincpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**Stringcchcopyn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **stringcchcopynetx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>["straupie", "wcsncpy", " \_ tcsncpy"](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**Stringcchgets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **stringcchgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[Get, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **stringcchprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, WS-printf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**Stringcchvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **stringcchvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vtauprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**Wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**Stringcchlength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[Straume, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Byte Anzahl-Funktionen

Die folgenden Funktionen verwenden eine Byte Anzahl anstelle einer Zeichen Anzahl.



| Funktion                                                                                                                                                                                                                  | Arbeits                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**Stringcbcat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **stringcb| Ex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> " <dt>[strecat", "wcscat", " \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrancat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> " </dl>                                                                            |
| <dl> <dt>[**Stringcb-n**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **stringcbcr-x**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> " <dt>[strinncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> " <dt> [ ](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**Stringcbcopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **stringcbcopyex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[cpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrincpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**Stringcbcopyn**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **stringcbcopynetx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>["straupie", "wcsncpy", " \_ tcsncpy"](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **Stringcbget stringcbgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[Get, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**Stringcbprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **stringcbprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, WS-printf, \_ stprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**Stringcbvprintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **stringcbvprintfex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vtauprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**Wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[**wvnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**Stringcblength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[Straume, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Verwenden von "strausafe. h"

-   Wenn Sie die "stresafe"-Funktionen Inline verwenden möchten, schließen Sie die Header Datei wie hier gezeigt ein, indem Sie die **\# include** -Anweisungen für alle anderen Header Dateien befolgen

    `#include <strsafe.h>`

-   Um die Funktionen in der Bibliothek zu verwenden, schließen Sie die folgende Anweisung ein, bevor Sie "tresafe. h" einschließen. Es wird jedoch empfohlen, die Inline Funktionen zu verwenden.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : Die folgenden Funktionen müssen als Inline Funktionen verwendet werden: " [**stringcbgets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)", " [**stringcbgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)", " [**stringcchgets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)" und " [**stringcchgetsex**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)".

     

-   Wenn Sie "strausafe. h" in die Datei einschließen, werden die älteren Funktionen, die durch die Funktionen "strausafe. h" ersetzt werden, als veraltet markiert. Versuche, diese älteren Funktionen zu verwenden, führen zu einem Compilerfehler, der Sie darüber informiert, dass die neueren Funktionen verwendet werden. Wenn Sie dieses Verhalten außer Kraft setzen möchten, schließen Sie die folgende Anweisung ein, bevor Sie "tresafe. h" einschließen.

    `#define STRSAFE_NO_DEPRECATE`

-   Um nur Zeichen Anzahl Funktionen zuzulassen, schließen Sie die folgende Anweisung ein, bevor Sie "tresafe. h" einschließen.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Fügen Sie die folgende Anweisung ein, bevor Sie "tresafe. h" einschließen, um nur Byte Anzahl Funktionen zuzulassen.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Sie können nicht beide-und-keine- **\_ \_ CCH- \_ Funktionen**, sondern nicht **beides definieren. \_ \_ \_**

     

-   Einige strauchsichere Funktionen verfügen über Gebiets Schema abhängige Versionen. Standardmäßig deklariert der-Header diese Funktionen nicht. Um diese Deklarationen zu aktivieren, schließen Sie die folgende Makro Anweisung ein, bevor Sie "strausafe. h" einschließen

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   Die maximal unterstützte Zeichen folgen Länge beträgt 2.147.483.647 (stringentes maximales **\_ \_ CCH**), entweder ANSI oder Unicode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strauchsichere Funktionen](string-overviews.md)
</dt> </dl>

 

 