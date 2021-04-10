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
# <a name="international-components-for-unicode-icu"></a><span data-ttu-id="73f75-103">Internationale Komponenten für Unicode (ICU)</span><span class="sxs-lookup"><span data-stu-id="73f75-103">International Components for Unicode (ICU)</span></span>

<span data-ttu-id="73f75-104">Internationale Komponenten für Unicode (ICU) ist ein ausgereifter, häufig verwendeter Satz von Open Source-Globalisierungs-APIs.</span><span class="sxs-lookup"><span data-stu-id="73f75-104">International Components for Unicode (ICU) is a mature, widely used set of open-source globalization APIs.</span></span> <span data-ttu-id="73f75-105">ICU nutzt das riesige Common Locale Data Repository (CLDR) von Unicode als Datenbibliothek und bietet Globalisierungs Unterstützung für Softwareanwendungen.</span><span class="sxs-lookup"><span data-stu-id="73f75-105">ICU utilizes Unicode's vast Common Locale Data Repository (CLDR) as its data library, providing globalization support for software applications.</span></span> <span data-ttu-id="73f75-106">ICU ist umfassend portierbar und bietet Anwendungen die gleichen Ergebnisse auf allen Plattformen.</span><span class="sxs-lookup"><span data-stu-id="73f75-106">ICU is widely portable and gives applications the same results across on all platforms.</span></span>

## <a name="highlights-of-the-globalization-api-services-provided-by-icu"></a><span data-ttu-id="73f75-107">Highlights der von ICU bereitgestellten Globalisierungs-API-Dienste</span><span class="sxs-lookup"><span data-stu-id="73f75-107">Highlights of the Globalization API services provided by ICU</span></span>

-   <span data-ttu-id="73f75-108">**Code Page Konvertierung**: Konvertieren von Textdaten in oder aus Unicode und fast allen anderen Zeichensätze oder Codierungen.</span><span class="sxs-lookup"><span data-stu-id="73f75-108">**Code Page Conversion**: Convert text data to or from Unicode and nearly any other character set or encoding.</span></span> <span data-ttu-id="73f75-109">Die Konvertierungstabellen von ICU basieren auf CharSet-Daten, die von IBM im Verlauf der jahrzehntelangen Jahrzehnten gesammelt werden, und sind die am meisten verfügbaren.</span><span class="sxs-lookup"><span data-stu-id="73f75-109">ICU's conversion tables are based on charset data collected by IBM over the course of many decades, and is the most complete available anywhere.</span></span>
-   <span data-ttu-id="73f75-110">**Sortierung**: Vergleichen Sie Zeichen folgen gemäß den Konventionen und Standards einer bestimmten Sprache, Region oder eines bestimmten Landes.</span><span class="sxs-lookup"><span data-stu-id="73f75-110">**Collation**: Compare strings according to the conventions and standards of a particular language, region or country.</span></span> <span data-ttu-id="73f75-111">Die ICU-Sortierung basiert auf dem Unicode-Sortierungs Algorithmus sowie Gebiets Schema spezifischen Vergleichs Regeln von CLDR.</span><span class="sxs-lookup"><span data-stu-id="73f75-111">ICU's collation is based on the Unicode Collation Algorithm plus locale-specific comparison rules from CLDR.</span></span>
-   <span data-ttu-id="73f75-112">**Formatierung**: Formatieren von Zahlen, Datumsangaben, Uhrzeiten und Währungs Beträgen gemäß den Konventionen eines ausgewählten Gebiets Schemas.</span><span class="sxs-lookup"><span data-stu-id="73f75-112">**Formatting**: Format numbers, dates, times and currency amounts according the conventions of a chosen locale.</span></span> <span data-ttu-id="73f75-113">Dies umfasst das Übersetzen von Monats-und Tages Namen in die ausgewählte Sprache, das auswählen entsprechender Abkürzungen, das ordnungsgemäße Anordnen von Feldern usw. Diese Daten stammen auch aus dem Common Locale Data Repository.</span><span class="sxs-lookup"><span data-stu-id="73f75-113">This includes translating month and day names into the selected language, choosing appropriate abbreviations, ordering fields correctly, etc. This data also comes from the Common Locale Data Repository.</span></span>
-   <span data-ttu-id="73f75-114">**Zeit Berechnungen**: mehrere Kalender Typen werden über den herkömmlichen gregorianischen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="73f75-114">**Time Calculations**: Multiple types of calendars are provided beyond the traditional Gregorian.</span></span> <span data-ttu-id="73f75-115">Es werden eine gründliche Reihe von APIs zur Zeit Zonen Berechnung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="73f75-115">A thorough set of time zone calculation APIs are provided.</span></span>
-   <span data-ttu-id="73f75-116">**Unicode-Unterstützung**: ICU verfolgt den Unicode-Standard genau und bietet einfachen Zugriff auf alle vielen Unicode-Zeichen Eigenschaften, Unicode-Normalisierung, Case-Faltung und andere grundlegende Vorgänge, wie im [Unicode-Standard](https://www.unicode.org/)angegeben.</span><span class="sxs-lookup"><span data-stu-id="73f75-116">**Unicode Support**: ICU closely tracks the Unicode standard, providing easy access to all of the many Unicode character properties, Unicode Normalization, Case Folding, and other fundamental operations as specified by the [Unicode Standard](https://www.unicode.org/).</span></span>
-   <span data-ttu-id="73f75-117">**Regulärer Ausdruck**: die regulären Ausdrücke von ICU unterstützen Unicode vollständig und bieten gleichzeitig eine äußerst wettbewerbsfähige Leistung</span><span class="sxs-lookup"><span data-stu-id="73f75-117">**Regular Expression**: ICU's regular expressions fully support Unicode while providing very competitive performance.</span></span>
-   <span data-ttu-id="73f75-118">**Bidi**: Unterstützung für die Behandlung von Text, der eine Mischung aus von links nach rechts (Englisch) und von rechts nach links (Arabisch oder Hebräisch) enthält.</span><span class="sxs-lookup"><span data-stu-id="73f75-118">**Bidi**: Support for handling text containing a mixture of left to right (English) and right to left (Arabic or Hebrew) data.</span></span>

<span data-ttu-id="73f75-119">Weitere Informationen finden Sie auf der ICU-Website: <http://site.icu-project.org/></span><span class="sxs-lookup"><span data-stu-id="73f75-119">For more information, you can visit the ICU website: <http://site.icu-project.org/></span></span>

## <a name="overview"></a><span data-ttu-id="73f75-120">Übersicht</span><span class="sxs-lookup"><span data-stu-id="73f75-120">Overview</span></span>

<span data-ttu-id="73f75-121">In Windows 10 Creators Update war ICU in Windows integriert, sodass die C-APIs und Daten öffentlich zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="73f75-121">In Windows 10 Creators Update, ICU was integrated into Windows, making the C APIs and data publicly accessible.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73f75-122">Die ICU-Version in Windows macht nur die C-APIs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73f75-122">The version of ICU in Windows only exposes the C APIs.</span></span> <span data-ttu-id="73f75-123">Es macht keine der C++-APIs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73f75-123">It does not expose any of the C++ APIs.</span></span> <span data-ttu-id="73f75-124">Leider ist es nicht möglich, die C++-APIs aufgrund fehlender stabiler ABI in C++ verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="73f75-124">Unfortunately, it is impossible to ever expose the C++ APIs due to the lack of a stable ABI in C++.</span></span>

<span data-ttu-id="73f75-125">Dokumentation zu den ICU-C-APIs finden Sie in der offiziellen ICU-Dokumentationsseite: <http://icu-project.org/apiref/icu4c/index.html#Module></span><span class="sxs-lookup"><span data-stu-id="73f75-125">For documentation on the ICU C APIs, please refer to the official ICU documentation page here: <http://icu-project.org/apiref/icu4c/index.html#Module></span></span>

## <a name="history-of-changes-to-the-icu-library-in-windows"></a><span data-ttu-id="73f75-126">Verlauf der Änderungen an der ICU-Bibliothek in Windows</span><span class="sxs-lookup"><span data-stu-id="73f75-126">History of changes to the ICU library in Windows</span></span>

### <a name="version-1703-creators-update"></a><span data-ttu-id="73f75-127">Version 1703 (Creators Update)</span><span class="sxs-lookup"><span data-stu-id="73f75-127">Version 1703 (Creators Update)</span></span>
<span data-ttu-id="73f75-128">Die ICU-Bibliothek wurde zunächst dem Windows 10-Betriebssystem in dieser Version hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73f75-128">The ICU library was first added to the Windows 10 OS in this version.</span></span>
<span data-ttu-id="73f75-129">Es wurde hinzugefügt als:</span><span class="sxs-lookup"><span data-stu-id="73f75-129">It was added as:</span></span>
- <span data-ttu-id="73f75-130">Zwei System-DLLs:</span><span class="sxs-lookup"><span data-stu-id="73f75-130">Two system DLLs:</span></span>
    -   <span data-ttu-id="73f75-131">**icuuc.dll** (Dies ist die "allgemeine" ICU-Bibliothek)</span><span class="sxs-lookup"><span data-stu-id="73f75-131">**icuuc.dll** (this is the ICU "common" library)</span></span>
    -   <span data-ttu-id="73f75-132">**icuin.dll** (Dies ist die ICU-Bibliothek "i18n")</span><span class="sxs-lookup"><span data-stu-id="73f75-132">**icuin.dll** (this is the ICU "i18n" library)</span></span>
- <span data-ttu-id="73f75-133">Zwei Header Dateien im Windows 10-SDK:</span><span class="sxs-lookup"><span data-stu-id="73f75-133">Two header files in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="73f75-134">**icucommon. h**</span><span class="sxs-lookup"><span data-stu-id="73f75-134">**icucommon.h**</span></span>
    -   <span data-ttu-id="73f75-135">**icui18n. h**</span><span class="sxs-lookup"><span data-stu-id="73f75-135">**icui18n.h**</span></span>
- <span data-ttu-id="73f75-136">Zwei Import-Liks im Windows 10-SDK:</span><span class="sxs-lookup"><span data-stu-id="73f75-136">Two import libs in the Windows 10 SDK:</span></span>
    -   <span data-ttu-id="73f75-137">**icuuc. lib**</span><span class="sxs-lookup"><span data-stu-id="73f75-137">**icuuc.lib**</span></span>
    -   <span data-ttu-id="73f75-138">**ICUin. lib**</span><span class="sxs-lookup"><span data-stu-id="73f75-138">**icuin.lib**</span></span>

### <a name="version-1709-fall-creators-update"></a><span data-ttu-id="73f75-139">Version 1709 (Fall Creators Update)</span><span class="sxs-lookup"><span data-stu-id="73f75-139">Version 1709 (Fall Creators Update)</span></span>
<span data-ttu-id="73f75-140">Eine kombinierte Header Datei " **ICU. h**" wurde hinzugefügt, die den Inhalt der obigen Header Dateien ("icucommon. h" und "icui18n. h") enthält und außerdem den Typ von `UCHAR` in ändert `char16_t` .</span><span class="sxs-lookup"><span data-stu-id="73f75-140">A combined header file, **icu.h**, was added, which contains the contents of both header files above (icucommon.h and icui18n.h), and also changes the type of `UCHAR` to `char16_t`.</span></span>

### <a name="version-1903-may-2019-update"></a><span data-ttu-id="73f75-141">Version 1903 (Mai 2019 Update)</span><span class="sxs-lookup"><span data-stu-id="73f75-141">Version 1903 (May 2019 Update)</span></span>
<span data-ttu-id="73f75-142">Eine neue kombinierte dll, **icu.dll**, wurde hinzugefügt, die sowohl die "Common"-als auch die "i18n"-Bibliotheken enthält.</span><span class="sxs-lookup"><span data-stu-id="73f75-142">A new combined DLL, **icu.dll**, was added, which contains both the "common" and "i18n" libraries.</span></span> <span data-ttu-id="73f75-143">Außerdem wurde eine neue Import Bibliothek zum Windows 10-SDK hinzugefügt: **ICU. lib**.</span><span class="sxs-lookup"><span data-stu-id="73f75-143">Also, a new import library was added to the Windows 10 SDK: **icu.lib**.</span></span>

<span data-ttu-id="73f75-144">In Zukunft werden keine neuen APIs zu den alten Headern (icucommon. h und icui18n. h) oder zu den alten Import Bibliotheken (icuuc. lib und ICUin. lib) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73f75-144">Going forward, no new APIs will be added to the old headers (icucommon.h and icui18n.h) or to the old import libs (icuuc.lib and icuin.lib).</span></span> <span data-ttu-id="73f75-145">Neue APIs werden nur dem kombinierten Header (ICU. h) und dem kombinierten Import lib (ICU. lib) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73f75-145">New APIs will only be added to the combined header (icu.h) and the combined import lib (icu.lib).</span></span>

## <a name="getting-started"></a><span data-ttu-id="73f75-146">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="73f75-146">Getting Started</span></span>

<span data-ttu-id="73f75-147">Es gibt drei Hauptschritte, die befolgt werden müssen: (Windows 10 Creators Update oder höher)</span><span class="sxs-lookup"><span data-stu-id="73f75-147">There are three main steps to follow: (Windows 10 Creators Update or higher)</span></span>

<dl>

1. <span data-ttu-id="73f75-148">Ihre Anwendung muss auf Windows 10, Version 1703 (Creators Update) oder höher ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="73f75-148">Your application needs to target Windows 10 Version 1703 (Creators Update) or higher.</span></span>

2. <span data-ttu-id="73f75-149">Fügen Sie die Header hinzu:</span><span class="sxs-lookup"><span data-stu-id="73f75-149">Add in the headers:</span></span>

   ``` syntax
   #include <icucommon.h>
   #include <icui18n.h>
   ```

   <span data-ttu-id="73f75-150">Unter Windows 10, Version 1709 und höher, sollten Sie stattdessen den kombinierten Header einschließen:</span><span class="sxs-lookup"><span data-stu-id="73f75-150">On Windows 10 Version 1709 and above, you should include the combined header instead:</span></span>

   ``` syntax
   #include <icu.h>
   ```
  
3. <span data-ttu-id="73f75-151">Verknüpfen Sie die beiden Bibliotheken:</span><span class="sxs-lookup"><span data-stu-id="73f75-151">Link to the two libraries:</span></span>

   -   <span data-ttu-id="73f75-152">icuuc. lib</span><span class="sxs-lookup"><span data-stu-id="73f75-152">icuuc.lib</span></span>
   -   <span data-ttu-id="73f75-153">ICUin. lib</span><span class="sxs-lookup"><span data-stu-id="73f75-153">icuin.lib</span></span>

   <span data-ttu-id="73f75-154">Unter Windows 10, Version 1903 und höher, sollten Sie stattdessen die kombinierte Bibliothek verwenden:</span><span class="sxs-lookup"><span data-stu-id="73f75-154">On Windows 10 Version 1903 and above, you should use the combined library instead:</span></span>

   -   <span data-ttu-id="73f75-155">ICU. lib</span><span class="sxs-lookup"><span data-stu-id="73f75-155">icu.lib</span></span>

</dl>

<span data-ttu-id="73f75-156">Anschließend können Sie jede beliebige ICU-C-API aus den gewünschten Bibliotheken abrufen.</span><span class="sxs-lookup"><span data-stu-id="73f75-156">Then, you can call whatever ICU C API from these libraries you want.</span></span> <span data-ttu-id="73f75-157">(Es werden keine C++-APIs verfügbar gemacht.)</span><span class="sxs-lookup"><span data-stu-id="73f75-157">(No C++ APIs are exposed.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73f75-158">Wenn Sie die Legacy-Import Bibliotheken icuuc. lib und ICUin. lib verwenden, stellen Sie sicher, dass Sie vor den Bildschirm Bibliotheken, wie z. b. onecoreuap. lib oder windowsapp. lib, in der linkereinstellung für zusätzliche Abhängigkeiten aufgeführt sind (siehe Abbildung unten).</span><span class="sxs-lookup"><span data-stu-id="73f75-158">If you are using the legacy import libraries, icuuc.lib and icuin.lib, ensure they're listed before the umbrella libraries, like onecoreuap.lib or WindowsApp.lib, in the Additional Dependencies Linker setting (see the image below).</span></span> <span data-ttu-id="73f75-159">Andernfalls wird der Linker mit ICU. lib verknüpft, was dazu führt, dass icu.dll während der Laufzeit geladen werden.</span><span class="sxs-lookup"><span data-stu-id="73f75-159">Otherwise, the linker will link to icu.lib, which will result in an attempt to load icu.dll during run time.</span></span> <span data-ttu-id="73f75-160">Diese dll ist nur ab Version 1903 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="73f75-160">That DLL is present only starting with version 1903.</span></span> <span data-ttu-id="73f75-161">Wenn ein Benutzer also das Windows 10 SDK auf einem Windows-Computer vor Version 1903 aktualisiert, kann die APP nicht geladen und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="73f75-161">So, if a user upgrades the Windows 10 SDK on a pre-version 1903 Windows machine, the app will fail to load and run.</span></span> <span data-ttu-id="73f75-162">Einen Verlauf der ICU-Bibliotheken in Windows finden Sie unter [Verlauf der Änderungen an der ICU-Bibliothek in Windows](#history-of-changes-to-the-icu-library-in-windows).</span><span class="sxs-lookup"><span data-stu-id="73f75-162">For a history of the ICU libraries in Windows, see [History of changes to the ICU library in Windows](#history-of-changes-to-the-icu-library-in-windows).</span></span>

![ICU-Beispiel](images/icu-example.png)

> [!Note]  
>
> - <span data-ttu-id="73f75-164">Dies ist die Konfiguration für "alle Plattformen".</span><span class="sxs-lookup"><span data-stu-id="73f75-164">This is the configuration for “All Platforms”.</span></span>
> - <span data-ttu-id="73f75-165">Damit Win32-apps ICU verwenden können, müssen Sie zuerst [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="73f75-165">For Win32 apps to use ICU, they need to call [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) first.</span></span>
> - <span data-ttu-id="73f75-166">Nicht alle Daten, die von den ICU-APIs zurückgegeben werden, werden mit dem Windows-Betriebssystem übereinstimmen, da diese Ausrichtungs Arbeit noch nicht erfolgt</span><span class="sxs-lookup"><span data-stu-id="73f75-166">Not all data returned by ICU APIs will align with the Windows OS, as this alignment work is still in progress.</span></span> 

## <a name="icu-example-app"></a><span data-ttu-id="73f75-167">ICU-Beispiel-App</span><span class="sxs-lookup"><span data-stu-id="73f75-167">ICU Example App</span></span>

### <a name="example-code-snippet"></a><span data-ttu-id="73f75-168">Beispielcode Ausschnitt</span><span class="sxs-lookup"><span data-stu-id="73f75-168">Example code snippet</span></span>

<span data-ttu-id="73f75-169">Im folgenden Beispiel wird die Verwendung von ICU-APIs in einer C++ UWP-Anwendung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="73f75-169">The following is an example illustrating the use of ICU APIs from within a C++ UWP application.</span></span> <span data-ttu-id="73f75-170">(Es ist nicht als vollständige eigenständige Anwendung gedacht, sondern nur ein Beispiel für den Aufruf einer ICU-Methode.)</span><span class="sxs-lookup"><span data-stu-id="73f75-170">(It is not intended to be a full stand-alone application, rather it is just an example of calling an ICU method.)</span></span>

<span data-ttu-id="73f75-171">Im folgenden kleinen Beispiel wird davon ausgegangen, dass die Methoden **ErrorMessage** und **outputmessage** vorhanden sind, die die Zeichen folgen auf irgendeine Weise an den Benutzer ausgeben.</span><span class="sxs-lookup"><span data-stu-id="73f75-171">The following small example assumes that there are methods **ErrorMessage** and **OutputMessage** that output the strings to the user in some manner.</span></span>

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

 

 



