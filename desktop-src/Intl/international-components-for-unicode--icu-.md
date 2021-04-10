---
description: Internationale Komponenten für Unicode (ICU) ist ein ausgereifter, häufig verwendeter Satz von Open Source-Globalisierungs-APIs.
ms.assetid: 4AEBE391-4121-44B2-B15B-0032645D7053
title: Internationale Komponenten für Unicode (ICU)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00a72885b37efebf8de0d5eb60a22fe01dfba4f
ms.sourcegitcommit: 176ef0a00690f849282cb48464c97f6526a82113
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/19/2021
ms.locfileid: "103961019"
---
# <a name="international-components-for-unicode-icu"></a>Internationale Komponenten für Unicode (ICU)

Internationale Komponenten für Unicode (ICU) ist ein ausgereifter, häufig verwendeter Satz von Open Source-Globalisierungs-APIs. ICU nutzt das riesige Common Locale Data Repository (CLDR) von Unicode als Datenbibliothek und bietet Globalisierungs Unterstützung für Softwareanwendungen. ICU ist umfassend portierbar und bietet Anwendungen die gleichen Ergebnisse auf allen Plattformen.

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a>Highlights der von ICU bereitgestellten Globalisierungs-API-Dienste

-   **Code Page Konvertierung**: Konvertieren von Textdaten in oder aus Unicode und fast allen anderen Zeichensätze oder Codierungen. Die Konvertierungstabellen von ICU basieren auf CharSet-Daten, die von IBM im Verlauf der jahrzehntelangen Jahrzehnten gesammelt werden, und sind die am meisten verfügbaren.
-   **Sortierung**: Vergleichen Sie Zeichen folgen gemäß den Konventionen und Standards einer bestimmten Sprache, Region oder eines bestimmten Landes. Die ICU-Sortierung basiert auf dem Unicode-Sortierungs Algorithmus sowie Gebiets Schema spezifischen Vergleichs Regeln von CLDR.
-   **Formatierung**: Formatieren von Zahlen, Datumsangaben, Uhrzeiten und Währungs Beträgen gemäß den Konventionen eines ausgewählten Gebiets Schemas. Dies umfasst das Übersetzen von Monats-und Tages Namen in die ausgewählte Sprache, das auswählen entsprechender Abkürzungen, das ordnungsgemäße Anordnen von Feldern usw. Diese Daten stammen auch aus dem Common Locale Data Repository.
-   **Zeit Berechnungen**: mehrere Kalender Typen werden über den herkömmlichen gregorianischen bereitgestellt. Es werden eine gründliche Reihe von APIs zur Zeit Zonen Berechnung bereitgestellt.
-   **Unicode-Unterstützung**: ICU verfolgt den Unicode-Standard genau und bietet einfachen Zugriff auf alle vielen Unicode-Zeichen Eigenschaften, Unicode-Normalisierung, Case-Faltung und andere grundlegende Vorgänge, wie im [Unicode-Standard](https://www.unicode.org/)angegeben.
-   **Regulärer Ausdruck**: die regulären Ausdrücke von ICU unterstützen Unicode vollständig und bieten gleichzeitig eine äußerst wettbewerbsfähige Leistung
-   **Bidi**: Unterstützung für die Behandlung von Text, der eine Mischung aus von links nach rechts (Englisch) und von rechts nach links (Arabisch oder Hebräisch) enthält.

Weitere Informationen finden Sie auf der ICU-Website: <http://site.icu-project.org/>

## <a name="overview"></a>Übersicht

In Windows 10 Creators Update war ICU in Windows integriert, sodass die C-APIs und Daten öffentlich zugänglich sind.

> [!IMPORTANT]
> Die ICU-Version in Windows macht nur die C-APIs verfügbar. Es macht keine der C++-APIs verfügbar. Leider ist es nicht möglich, die C++-APIs aufgrund fehlender stabiler ABI in C++ verfügbar zu machen.

Dokumentation zu den ICU-C-APIs finden Sie in der offiziellen ICU-Dokumentationsseite: <http://icu-project.org/apiref/icu4c/index.html#Module>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a>Verlauf der Änderungen an der ICU-Bibliothek in Windows

### <a name="version-1703-creators-update"></a>Version 1703 (Creators Update)
Die ICU-Bibliothek wurde zunächst dem Windows 10-Betriebssystem in dieser Version hinzugefügt.
Es wurde hinzugefügt als:
- Zwei System-DLLs:
    -   **icuuc.dll** (Dies ist die "allgemeine" ICU-Bibliothek)
    -   **icuin.dll** (Dies ist die ICU-Bibliothek "i18n")
- Zwei Header Dateien im Windows 10-SDK:
    -   **icucommon. h**
    -   **icui18n. h**
- Zwei Import-Liks im Windows 10-SDK:
    -   **icuuc. lib**
    -   **ICUin. lib**

### <a name="version-1709-fall-creators-update"></a>Version 1709 (Fall Creators Update)
Eine kombinierte Header Datei " **ICU. h**" wurde hinzugefügt, die den Inhalt der obigen Header Dateien ("icucommon. h" und "icui18n. h") enthält und außerdem den Typ von `UCHAR` in ändert `char16_t` .

### <a name="version-1903-may-2019-update"></a>Version 1903 (Mai 2019 Update)
Eine neue kombinierte dll, **icu.dll**, wurde hinzugefügt, die sowohl die "Common"-als auch die "i18n"-Bibliotheken enthält. Außerdem wurde eine neue Import Bibliothek zum Windows 10-SDK hinzugefügt: **ICU. lib**.

In Zukunft werden keine neuen APIs zu den alten Headern (icucommon. h und icui18n. h) oder zu den alten Import Bibliotheken (icuuc. lib und ICUin. lib) hinzugefügt. Neue APIs werden nur dem kombinierten Header (ICU. h) und dem kombinierten Import lib (ICU. lib) hinzugefügt.

## <a name="getting-started"></a>Erste Schritte

Es gibt drei Hauptschritte, die befolgt werden müssen: (Windows 10 Creators Update oder höher)

<dl>

1. Ihre Anwendung muss auf Windows 10, Version 1703 (Creators Update) oder höher ausgerichtet sein.

2. Fügen Sie die Header hinzu:

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   Unter Windows 10, Version 1709 und höher, sollten Sie stattdessen den kombinierten Header einschließen:

   ``` syntax
   #include <icu.h>
   ```
  
3. Verknüpfen Sie die beiden Bibliotheken:

   -   icuuc. lib
   -   ICUin. lib

   Unter Windows 10, Version 1903 und höher, sollten Sie stattdessen die kombinierte Bibliothek verwenden:

   -   ICU. lib

</dl>

Anschließend können Sie jede beliebige ICU-C-API aus den gewünschten Bibliotheken abrufen. (Es werden keine C++-APIs verfügbar gemacht.)

> [!IMPORTANT]
> Wenn Sie die Legacy-Import Bibliotheken icuuc. lib und ICUin. lib verwenden, stellen Sie sicher, dass Sie vor den Bildschirm Bibliotheken, wie z. b. onecoreuap. lib oder windowsapp. lib, in der linkereinstellung für zusätzliche Abhängigkeiten aufgeführt sind (siehe Abbildung unten). Andernfalls wird der Linker mit ICU. lib verknüpft, was dazu führt, dass icu.dll während der Laufzeit geladen werden. Diese dll ist nur ab Version 1903 vorhanden. Wenn ein Benutzer also das Windows 10 SDK auf einem Windows-Computer vor Version 1903 aktualisiert, kann die APP nicht geladen und ausgeführt werden. Einen Verlauf der ICU-Bibliotheken in Windows finden Sie unter [Verlauf der Änderungen an der ICU-Bibliothek in Windows](#history-of-changes-to-the-icu-library-in-windows).

![ICU-Beispiel](images/icu-example.png)

> [!Note]  
>
> - Dies ist die Konfiguration für "alle Plattformen".
> - Damit Win32-apps ICU verwenden können, müssen Sie zuerst [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen.
> - Nicht alle Daten, die von den ICU-APIs zurückgegeben werden, werden mit dem Windows-Betriebssystem übereinstimmen, da diese Ausrichtungs Arbeit noch nicht erfolgt 

## <a name="icu-example-app"></a>ICU-Beispiel-App

### <a name="example-code-snippet"></a>Beispielcode Ausschnitt

Im folgenden Beispiel wird die Verwendung von ICU-APIs in einer C++ UWP-Anwendung veranschaulicht. (Es ist nicht als vollständige eigenständige Anwendung gedacht, sondern nur ein Beispiel für den Aufruf einer ICU-Methode.)

Im folgenden kleinen Beispiel wird davon ausgegangen, dass die Methoden **ErrorMessage** und **outputmessage** vorhanden sind, die die Zeichen folgen auf irgendeine Weise an den Benutzer ausgeben.

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

 

 



