---
description: International Components for Unicode (ICU) ist ein ausgereifter, weit verbreiteter Satz von Open-Source-Globalisierungs-APIs.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Internationale Komponenten für Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560a2f344a3024685e17df0f434f8ffa040b5c8b
ms.sourcegitcommit: d5f16b9d3d5d2e2080ba7b6837eb37250fa67a30
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/02/2021
ms.locfileid: "111349989"
---
# <a name="international-components-for-unicode-icu"></a>Internationale Komponenten für Unicode (ICU)

International Components for Unicode (ICU) ist ein ausgereifter, weit verbreiteter Satz von Open-Source-Globalisierungs-APIs. ICU nutzt das umfangreiche Common Locale Data Repository (CLDR) von Unicode als Datenbibliothek und bietet Globalisierungsunterstützung für Softwareanwendungen. ICU ist weit verbreitet portabel und bietet Anwendungen auf allen Plattformen die gleichen Ergebnisse.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Highlights der Globalisierungs-API von ICU bereitgestellten Dienste

-   **Codepagekonvertierung:** Konvertieren von Textdaten in oder aus Unicode und nahezu jedem anderen Zeichensatz oder jeder Codierung. Die Konvertierungstabellen von ICU basieren auf Zeichensatzdaten, die von IBM im Laufe vieler Jahrzehnten gesammelt wurden, und sind die vollständigsten, die überall verfügbar sind.
-   **Sortierung:** Vergleichen Sie Zeichenfolgen gemäß den Konventionen und Standards einer bestimmten Sprache, Region oder eines bestimmten Landes. Die Sortierung von ICU basiert auf dem Unicode-Sortierungsalgorithmus sowie auf den lokalen Vergleichsregeln der CLDR.
-   **Formatierung:** Formatieren Sie Zahlen, Datumsangaben, Zeiten und Währungsbeträge gemäß den Konventionen eines ausgewählten Locales. Dies umfasst die Übersetzung von Monats- und Tagesnamen in die ausgewählte Sprache, die Auswahl geeigneter Abkürzungen, die korrekte Sortierung von Feldern usw. Diese Daten stammen auch aus dem Common Locale Data Repository.
-   **Zeitberechnungen:** Über den traditionellen gregorianischen Kalender hinaus werden mehrere Kalendertypen bereitgestellt. Ein gründlicher Satz von Zeitzonenberechnungs-APIs wird bereitgestellt.
-   **Unicode-Unterstützung:** ICU verfolgt den Unicode-Standard genau nach und bietet einfachen Zugriff auf alle vielen Unicode-Zeicheneigenschaften, Unicode-Normalisierung, Case Folding und andere grundlegende Vorgänge, wie im [Unicode-Standard angegeben.](https://www.unicode.org/)
-   **Regulärer Ausdruck:** Die regulären Ausdrücke von ICU unterstützen Unicode vollständig und bieten gleichzeitig eine sehr wettbewerbsvorteil Leistung.
-   **Bidi:** Unterstützung für die Verarbeitung von Text, der eine Mischung aus Daten von links nach rechts (Englisch) und von rechts nach links (Arabisch oder Hebräisch) enthält.

Weitere Informationen finden Sie auf der ICU-Website: <http://site.icu-project.org/>

## <a name="overview"></a>Übersicht

In Windows 10 Creators Update wurde ICU in Windows integriert, wodurch die C-APIs und Daten öffentlich zugänglich wurden.

> [!IMPORTANT]
> Die ICU-Version in Windows macht nur die C-APIs verfügbar. Sie macht keine der C++-APIs verfügbar. Leider ist es unmöglich, die C++-APIs jemals verfügbar zu machen, da keine stabile ABI in C++ verfügbar gemacht wird.

Die Dokumentation zu den ICU-C-APIs finden Sie hier auf der offiziellen ICU-Dokumentationsseite: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Verlauf der Änderungen an der ICU-Bibliothek in Windows

### <a name="version-1703-creators-update"></a>Version 1703 (Creators Update)
Die ICU-Bibliothek wurde dem Betriebssystem in Windows 10 Version hinzugefügt.
Es wurde hinzugefügt als:
- Zwei System-DLLs:
    -   **icuuc.dll** (dies ist die "allgemeine" ICU-Bibliothek)
    -   **icuin.dll** (dies ist die ICU-Bibliothek "i18n")
- Zwei Headerdateien im Windows 10 SDK:
    -   **icucommon.h**
    -   **icui18n.h**
- Zwei Importbibliotheken im Windows 10 SDK:
    -   **icuuc.lib**
    -   **icuin.lib**

### <a name="version-1709-fall-creators-update"></a>Version 1709 (Fall Creators Update)
Die kombinierte Headerdatei **icu.h** wurde hinzugefügt, die den Inhalt beider oben genannten Headerdateien (icucommon.h und icui18n.h) enthält und außerdem den Typ von in `UCHAR` `char16_t` ändert.

### <a name="version-1903-may-2019-update"></a>Version 1903 (Update mai 2019)
Eine neue kombinierte DLL, **icu.dll,** wurde hinzugefügt, die sowohl die Bibliotheken "common" als auch "i18n" enthält. Außerdem wurde eine neue Importbibliothek zum Windows 10 SDK hinzugefügt: **icu.lib**.

In Zukunft werden den alten Headern (icucommon.h und icui18n.h) oder den alten Importbibliotheken (icuuc.lib und icuin.lib) keine neuen APIs hinzugefügt. Neue APIs werden nur dem kombinierten Header (icu.h) und der kombinierten Importbibliothek (icu.lib) hinzugefügt.

## <a name="getting-started"></a>Erste Schritte

Es gibt drei Hauptschritte: (Windows 10 Creators Update oder höher)

<dl>

1. Ihre Anwendung muss auf Version 1703 Windows 10 Version 1703 (Creators Update) oder höher.

2. Fügen Sie in den Headern Hinzu:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   In Windows 10 Version 1709 und höher sollten Sie stattdessen den kombinierten Header hinzufügen:

   ``` syntax
   #include <icu.h>
   ```
  
3. Link zu den beiden Bibliotheken:

   -   icuuc.lib
   -   icuin.lib

   In Windows 10 Version 1903 und höher sollten Sie stattdessen die kombinierte Bibliothek verwenden:

   -   icu.lib

</dl>

Anschließend können Sie die ICU-C-API aus diesen Bibliotheken aufrufen, die Sie wünschen. (Es werden keine C++-APIs verfügbar gemacht.)

> [!IMPORTANT]
> Wenn Sie die älteren Importbibliotheken icuuc.lib und icuin.lib verwenden, stellen Sie sicher, dass sie vor den Schirmbibliotheken wie onecoreuap.lib oder WindowsApp.lib in der Einstellung Linker für zusätzliche Abhängigkeiten aufgeführt sind (siehe Abbildung unten). Andernfalls wird der Linker mit "icu.lib" verlinkt, was dazu führt, dass versucht wird, icu.dll Laufzeit zu laden. Diese DLL ist nur ab Version 1903 vorhanden. Wenn also ein Benutzer das Windows 10 SDK auf einem Windows-Computer vor Version 1903 aktualisiert, kann die App nicht geladen und ausgeführt werden. Einen Verlauf der ICU-Bibliotheken in Windows finden Sie unter Verlauf der Änderungen an der [ICU-Bibliothek in Windows.](#history-of-changes-to-the-icu-library-in-windows)

![icu-Beispiel](images/icu-example.png)

> [!Note]  
>
> - Dies ist die Konfiguration für "Alle Plattformen".
> - Damit Win32-Apps ICU verwenden können, müssen sie [zuerst CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen. In Windows 10 Version 1903 und höher, in der die kombinierte ICU-Bibliothek (icu.dll/icu.lib) verfügbar ist, können Sie den CoInitializeEx-Aufruf weglassen, indem Sie die kombinierte Bibliothek verwenden.
> - Nicht alle von ICU-APIs zurückgegebenen Daten stimmen mit dem Windows-Betriebssystem ab, da diese Ausrichtung noch ausgeführt wird. 

## <a name="icu-example-app"></a>ICU-Beispiel-App

### <a name="example-code-snippet"></a>Beispielcodeausschnitt

Das folgende Beispiel veranschaulicht die Verwendung von ICU-APIs innerhalb einer C++-UWP-Anwendung. (Es ist nicht als vollständige eigenständige Anwendung gedacht, sondern nur ein Beispiel für den Aufruf einer ICU-Methode.)

Im folgenden kleinen Beispiel wird davon ausgegangen, dass es die **Methoden ErrorMessage** und **OutputMessage** gibt, die die Zeichenfolgen in irgendeiner Weise an den Benutzer ausgegeben.

``` syntax
// On Windows 10 Creators Update, include the following two headers. With Windows 10 Fall Creators Update and later, you can just include the single header <icu.h>.
#include <icucommon.h>
#include <icui18n.h>

void FormatDateTimeICU()
{
    UErrorCode status = U_ZERO_ERROR;

    // Create a ICU date formatter, using only the 'short date' style format.
    UDateFormat* dateFormatter = udat_open(UDAT_NONE, UDAT_SHORT, nullptr, nullptr, -1, nullptr, 0, &status);

    if (U_FAILURE(status))
    {
        ErrorMessage(L"Failed to create date formatter.");
        return;
    }

    // Get the current date and time.
    UDate currentDateTime = ucal_getNow();

    int32_t stringSize = 0;
    
    // Determine how large the formatted string from ICU would be.
    stringSize = udat_format(dateFormatter, currentDateTime, nullptr, 0, nullptr, &status);

    if (status == U_BUFFER_OVERFLOW_ERROR)
    {
        status = U_ZERO_ERROR;
        // Allocate space for the formatted string.
        auto dateString = std::make_unique<UChar[]>(stringSize + 1);

        // Format the date time into the string.
        udat_format(dateFormatter, currentDateTime, dateString.get(), stringSize + 1, nullptr, &status);

        if (U_FAILURE(status))
        {
            ErrorMessage(L"Failed to format the date time.");
            return;
        }

        // Output the formatted date time.
        OutputMessage(dateString.get());
    }
    else
    {
        ErrorMessage(L"An error occured while trying to determine the size of the formatted date time.");
        return;
    }

    // We need to close the ICU date formatter.
    udat_close(dateFormatter);
}
```

 

 



