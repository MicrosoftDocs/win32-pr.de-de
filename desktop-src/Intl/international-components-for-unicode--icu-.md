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
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="9bac8-103">Internationale Komponenten für Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="9bac8-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="9bac8-104">International Components for Unicode (ICU) ist ein ausgereifter, weit verbreiteter Satz von Open-Source-Globalisierungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="9bac8-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="9bac8-105">ICU nutzt das umfangreiche Common Locale Data Repository (CLDR) von Unicode als Datenbibliothek und bietet Globalisierungsunterstützung für Softwareanwendungen.</span><span class="sxs-lookup"><span data-stu-id="9bac8-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="9bac8-106">ICU ist weit verbreitet portabel und bietet Anwendungen auf allen Plattformen die gleichen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9bac8-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="9bac8-107">Highlights der Globalisierungs-API von ICU bereitgestellten Dienste</span><span class="sxs-lookup"><span data-stu-id="9bac8-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="9bac8-108">**Codepagekonvertierung:** Konvertieren von Textdaten in oder aus Unicode und nahezu jedem anderen Zeichensatz oder jeder Codierung.</span><span class="sxs-lookup"><span data-stu-id="9bac8-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="9bac8-109">Die Konvertierungstabellen von ICU basieren auf Zeichensatzdaten, die von IBM im Laufe vieler Jahrzehnten gesammelt wurden, und sind die vollständigsten, die überall verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9bac8-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="9bac8-110">**Sortierung:** Vergleichen Sie Zeichenfolgen gemäß den Konventionen und Standards einer bestimmten Sprache, Region oder eines bestimmten Landes.</span><span class="sxs-lookup"><span data-stu-id="9bac8-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="9bac8-111">Die Sortierung von ICU basiert auf dem Unicode-Sortierungsalgorithmus sowie auf den lokalen Vergleichsregeln der CLDR.</span><span class="sxs-lookup"><span data-stu-id="9bac8-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="9bac8-112">**Formatierung:** Formatieren Sie Zahlen, Datumsangaben, Zeiten und Währungsbeträge gemäß den Konventionen eines ausgewählten Locales.</span><span class="sxs-lookup"><span data-stu-id="9bac8-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="9bac8-113">Dies umfasst die Übersetzung von Monats- und Tagesnamen in die ausgewählte Sprache, die Auswahl geeigneter Abkürzungen, die korrekte Sortierung von Feldern usw. Diese Daten stammen auch aus dem Common Locale Data Repository.</span><span class="sxs-lookup"><span data-stu-id="9bac8-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="9bac8-114">**Zeitberechnungen:** Über den traditionellen gregorianischen Kalender hinaus werden mehrere Kalendertypen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9bac8-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="9bac8-115">Ein gründlicher Satz von Zeitzonenberechnungs-APIs wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9bac8-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="9bac8-116">**Unicode-Unterstützung:** ICU verfolgt den Unicode-Standard genau nach und bietet einfachen Zugriff auf alle vielen Unicode-Zeicheneigenschaften, Unicode-Normalisierung, Case Folding und andere grundlegende Vorgänge, wie im [Unicode-Standard angegeben.](https://www.unicode.org/)</span><span class="sxs-lookup"><span data-stu-id="9bac8-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="9bac8-117">**Regulärer Ausdruck:** Die regulären Ausdrücke von ICU unterstützen Unicode vollständig und bieten gleichzeitig eine sehr wettbewerbsvorteil Leistung.</span><span class="sxs-lookup"><span data-stu-id="9bac8-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="9bac8-118">**Bidi:** Unterstützung für die Verarbeitung von Text, der eine Mischung aus Daten von links nach rechts (Englisch) und von rechts nach links (Arabisch oder Hebräisch) enthält.</span><span class="sxs-lookup"><span data-stu-id="9bac8-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="9bac8-119">Weitere Informationen finden Sie auf der ICU-Website: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="9bac8-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="9bac8-120">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9bac8-120">Overview</span></span>

<span data-ttu-id="9bac8-121">In Windows 10 Creators Update wurde ICU in Windows integriert, wodurch die C-APIs und Daten öffentlich zugänglich wurden.</span><span class="sxs-lookup"><span data-stu-id="9bac8-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bac8-122">Die ICU-Version in Windows macht nur die C-APIs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bac8-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="9bac8-123">Sie macht keine der C++-APIs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9bac8-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="9bac8-124">Leider ist es unmöglich, die C++-APIs jemals verfügbar zu machen, da keine stabile ABI in C++ verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="9bac8-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="9bac8-125">Die Dokumentation zu den ICU-C-APIs finden Sie hier auf der offiziellen ICU-Dokumentationsseite: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="9bac8-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="9bac8-126">Verlauf der Änderungen an der ICU-Bibliothek in Windows</span><span class="sxs-lookup"><span data-stu-id="9bac8-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="9bac8-127">Version 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="9bac8-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="9bac8-128">Die ICU-Bibliothek wurde dem Betriebssystem in Windows 10 Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9bac8-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="9bac8-129">Es wurde hinzugefügt als:</span><span class="sxs-lookup"><span data-stu-id="9bac8-129">It was added as:</span></span>
- <span data-ttu-id="9bac8-130">Zwei System-DLLs:</span><span class="sxs-lookup"><span data-stu-id="9bac8-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="9bac8-131">**icuuc.dll** (dies ist die "allgemeine" ICU-Bibliothek)</span><span class="sxs-lookup"><span data-stu-id="9bac8-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="9bac8-132">**icuin.dll** (dies ist die ICU-Bibliothek "i18n")</span><span class="sxs-lookup"><span data-stu-id="9bac8-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="9bac8-133">Zwei Headerdateien im Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="9bac8-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="9bac8-134">**icucommon.h**</span><span class="sxs-lookup"><span data-stu-id="9bac8-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="9bac8-135">**icui18n.h**</span><span class="sxs-lookup"><span data-stu-id="9bac8-135">**icui18n.h**</span></span>
- <span data-ttu-id="9bac8-136">Zwei Importbibliotheken im Windows 10 SDK:</span><span class="sxs-lookup"><span data-stu-id="9bac8-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="9bac8-137">**icuuc.lib**</span><span class="sxs-lookup"><span data-stu-id="9bac8-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="9bac8-138">**icuin.lib**</span><span class="sxs-lookup"><span data-stu-id="9bac8-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="9bac8-139">Version 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="9bac8-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="9bac8-140">Die kombinierte Headerdatei **icu.h** wurde hinzugefügt, die den Inhalt beider oben genannten Headerdateien (icucommon.h und icui18n.h) enthält und außerdem den Typ von in `UCHAR` `char16_t` ändert.</span><span class="sxs-lookup"><span data-stu-id="9bac8-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="9bac8-141">Version 1903 (Update mai 2019)</span><span class="sxs-lookup"><span data-stu-id="9bac8-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="9bac8-142">Eine neue kombinierte DLL, **icu.dll,** wurde hinzugefügt, die sowohl die Bibliotheken "common" als auch "i18n" enthält.</span><span class="sxs-lookup"><span data-stu-id="9bac8-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="9bac8-143">Außerdem wurde eine neue Importbibliothek zum Windows 10 SDK hinzugefügt: **icu.lib**.</span><span class="sxs-lookup"><span data-stu-id="9bac8-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="9bac8-144">In Zukunft werden den alten Headern (icucommon.h und icui18n.h) oder den alten Importbibliotheken (icuuc.lib und icuin.lib) keine neuen APIs hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9bac8-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="9bac8-145">Neue APIs werden nur dem kombinierten Header (icu.h) und der kombinierten Importbibliothek (icu.lib) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9bac8-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="9bac8-146">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="9bac8-146">Getting Started</span></span>

<span data-ttu-id="9bac8-147">Es gibt drei Hauptschritte: (Windows 10 Creators Update oder höher)</span><span class="sxs-lookup"><span data-stu-id="9bac8-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="9bac8-148">Ihre Anwendung muss auf Version 1703 Windows 10 Version 1703 (Creators Update) oder höher.</span><span class="sxs-lookup"><span data-stu-id="9bac8-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="9bac8-149">Fügen Sie in den Headern Hinzu:</span><span class="sxs-lookup"><span data-stu-id="9bac8-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="9bac8-150">In Windows 10 Version 1709 und höher sollten Sie stattdessen den kombinierten Header hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="9bac8-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="9bac8-151">Link zu den beiden Bibliotheken:</span><span class="sxs-lookup"><span data-stu-id="9bac8-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="9bac8-152">icuuc.lib</span><span class="sxs-lookup"><span data-stu-id="9bac8-152">icuuc.lib</span></span>
   -   <span data-ttu-id="9bac8-153">icuin.lib</span><span class="sxs-lookup"><span data-stu-id="9bac8-153">icuin.lib</span></span>

   <span data-ttu-id="9bac8-154">In Windows 10 Version 1903 und höher sollten Sie stattdessen die kombinierte Bibliothek verwenden:</span><span class="sxs-lookup"><span data-stu-id="9bac8-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="9bac8-155">icu.lib</span><span class="sxs-lookup"><span data-stu-id="9bac8-155">icu.lib</span></span>

</dl>

<span data-ttu-id="9bac8-156">Anschließend können Sie die ICU-C-API aus diesen Bibliotheken aufrufen, die Sie wünschen.</span><span class="sxs-lookup"><span data-stu-id="9bac8-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="9bac8-157">(Es werden keine C++-APIs verfügbar gemacht.)</span><span class="sxs-lookup"><span data-stu-id="9bac8-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9bac8-158">Wenn Sie die älteren Importbibliotheken icuuc.lib und icuin.lib verwenden, stellen Sie sicher, dass sie vor den Schirmbibliotheken wie onecoreuap.lib oder WindowsApp.lib in der Einstellung Linker für zusätzliche Abhängigkeiten aufgeführt sind (siehe Abbildung unten).</span><span class="sxs-lookup"><span data-stu-id="9bac8-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="9bac8-159">Andernfalls wird der Linker mit "icu.lib" verlinkt, was dazu führt, dass versucht wird, icu.dll Laufzeit zu laden.</span><span class="sxs-lookup"><span data-stu-id="9bac8-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="9bac8-160">Diese DLL ist nur ab Version 1903 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9bac8-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="9bac8-161">Wenn also ein Benutzer das Windows 10 SDK auf einem Windows-Computer vor Version 1903 aktualisiert, kann die App nicht geladen und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9bac8-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="9bac8-162">Einen Verlauf der ICU-Bibliotheken in Windows finden Sie unter Verlauf der Änderungen an der [ICU-Bibliothek in Windows.](#history-of-changes-to-the-icu-library-in-windows)</span><span class="sxs-lookup"><span data-stu-id="9bac8-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![icu-Beispiel](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="9bac8-164">Dies ist die Konfiguration für "Alle Plattformen".</span><span class="sxs-lookup"><span data-stu-id="9bac8-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="9bac8-165">Damit Win32-Apps ICU verwenden können, müssen sie [zuerst CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9bac8-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span> <span data-ttu-id="9bac8-166">In Windows 10 Version 1903 und höher, in der die kombinierte ICU-Bibliothek (icu.dll/icu.lib) verfügbar ist, können Sie den CoInitializeEx-Aufruf weglassen, indem Sie die kombinierte Bibliothek verwenden.</span><span class="sxs-lookup"><span data-stu-id="9bac8-166">On Windows 10 version 1903 and above, where the combined ICU library (icu.dll/icu.lib) is available, you can omit the CoInitializeEx call by using the combined library.</span></span>
> - <span data-ttu-id="9bac8-167">Nicht alle von ICU-APIs zurückgegebenen Daten stimmen mit dem Windows-Betriebssystem ab, da diese Ausrichtung noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9bac8-167">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="9bac8-168">ICU-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="9bac8-168">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="9bac8-169">Beispielcodeausschnitt</span><span class="sxs-lookup"><span data-stu-id="9bac8-169">Example code snippet</span></span>

<span data-ttu-id="9bac8-170">Das folgende Beispiel veranschaulicht die Verwendung von ICU-APIs innerhalb einer C++-UWP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9bac8-170">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="9bac8-171">(Es ist nicht als vollständige eigenständige Anwendung gedacht, sondern nur ein Beispiel für den Aufruf einer ICU-Methode.)</span><span class="sxs-lookup"><span data-stu-id="9bac8-171">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="9bac8-172">Im folgenden kleinen Beispiel wird davon ausgegangen, dass es die **Methoden ErrorMessage** und **OutputMessage** gibt, die die Zeichenfolgen in irgendeiner Weise an den Benutzer ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="9bac8-172">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

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

 

 



