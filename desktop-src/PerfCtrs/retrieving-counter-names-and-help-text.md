---
description: Die Leistungsdaten enthalten Indexwerte, mit denen Sie die Namen und den Hilfetext für die einzelnen registrierten Objekte und Leistungsindikator suchen.
ms.assetid: 9ddd1672-61cf-41c2-bec0-0d2b775bf970
title: Abrufen von Namen von Zählern und Hilfe Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5b49f852e6af22dc2ec31d341ee6176913f98e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349857"
---
# <a name="retrieving-counter-names-and-help-text"></a><span data-ttu-id="87501-103">Abrufen von Namen von Zählern und Hilfe Text</span><span class="sxs-lookup"><span data-stu-id="87501-103">Retrieving Counter Names and Help Text</span></span>

<span data-ttu-id="87501-104">Die Leistungsdaten enthalten Indexwerte, mit denen Sie die Namen und den Hilfetext für die einzelnen registrierten Objekte und Leistungsindikator suchen.</span><span class="sxs-lookup"><span data-stu-id="87501-104">The performance data contains index values that you use to locate the names and help text for each registered object and counter.</span></span> <span data-ttu-id="87501-105">Die Member **objectnametitleindex** und **objecthelptitleindex** der [**perf- \_ \_ Objekttyp**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) Struktur enthalten die Indexwerte für den Objektnamen bzw. den Hilfetext, und die Elemente **counternametitleindex** und **counterhelptitleindex** der Leistungsindikator [**\_ \_ Definitions**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) Struktur enthalten die Indexwerte für den Indikator Namen bzw. den Hilfetext.</span><span class="sxs-lookup"><span data-stu-id="87501-105">The **ObjectNameTitleIndex** and **ObjectHelpTitleIndex** members of the [**PERF\_OBJECT\_TYPE**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) structure contain the index values to the object name and help text, respectively, and the **CounterNameTitleIndex** and **CounterHelpTitleIndex** members of the [**PERF\_COUNTER\_DEFINITION**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) structure contain the index values to the counter name and help text, respectively.</span></span>

<span data-ttu-id="87501-106">Um die Namen oder den Hilfetext abzurufen, rufen Sie die [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="87501-106">To retrieve the names or help text, call the [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function.</span></span> <span data-ttu-id="87501-107">Legen Sie den *HKEY* -Parameter auf einen der folgenden vordefinierten Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="87501-107">Set the *hKey* parameter to one of the following predefined keys.</span></span> <span data-ttu-id="87501-108">Normalerweise verwenden Sie den Schlüssel **HKEY \_ Performance \_ nlstext** , damit Sie die sprach Kennung des Benutzers nicht ermitteln müssen.</span><span class="sxs-lookup"><span data-stu-id="87501-108">Typically, you would use the **HKEY\_PERFORMANCE\_NLSTEXT** key, so you do not have to determine the user's language identifier.</span></span>



| <span data-ttu-id="87501-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="87501-109">Key</span></span>                            | <span data-ttu-id="87501-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87501-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87501-111">**HKEY- \_ Leistungs \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="87501-111">**HKEY\_PERFORMANCE\_DATA**</span></span>    | <span data-ttu-id="87501-112">Abfrage Zeichenfolgen basierend auf dem Sprach-ID-Wert, den Sie im *lpvaluename* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="87501-112">Query strings based on the language identifier value that you specify in the *lpValueName* parameter.</span></span> <span data-ttu-id="87501-113">Legen Sie den *lpvaluename* -Parameter entweder auf "Counter &lt; LangID &gt; " oder "Help &lt; LangID" fest, &gt; um die Namen bzw. den Hilfetext abzurufen, wobei " &lt; LangID &gt; " für die Systemsprachen-ID steht, die als 0 (null) mit **drei Ziffern** formatiert ist.</span><span class="sxs-lookup"><span data-stu-id="87501-113">Set *lpValueName* parameter to either "Counter &lt;langid&gt;" or "Help &lt;langid&gt;" to retrieve the names or help text, respectively, where "&lt;langid&gt;" is the system language identifier formatted as **zero-padded 3-digit hex number**.</span></span> <span data-ttu-id="87501-114">Der sprach Bezeichner ist optional.</span><span class="sxs-lookup"><span data-stu-id="87501-114">The language identifier is optional.</span></span> <span data-ttu-id="87501-115">Wenn Sie keinen sprach Bezeichner angeben, gibt die Funktion englische Zeichen folgen zurück.</span><span class="sxs-lookup"><span data-stu-id="87501-115">If you do not specify a language identifier, the function returns English strings.</span></span> <span data-ttu-id="87501-116">Überprüfen Sie den `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` Registrierungsschlüssel auf die Liste der Sprachen, die auf Ihrem System verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="87501-116">Check the `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` registry key for the list of languages available on your system.</span></span><br/><span data-ttu-id="87501-117">Wenn Sie Text in den meisten Sprachen abrufen möchten, geben Sie nur die primäre Sprach-ID an.</span><span class="sxs-lookup"><span data-stu-id="87501-117">To retrieve text in most languages, specify the primary language identifier only.</span></span> <span data-ttu-id="87501-118">Wenn Sie z. b. englische Zeichen folgen abrufen möchten, geben Sie den sprach Bezeichner als 009, nicht als 1033 für Englisch-US an.</span><span class="sxs-lookup"><span data-stu-id="87501-118">For example, to retrieve English strings, specify the language identifier as 009, not 1033 for English-US.</span></span><br/><span data-ttu-id="87501-119">Geben Sie zum Abrufen von Chinesisch-und Portugiesisch-Text sowohl die primären als auch die unter Sprachen-IDs an.</span><span class="sxs-lookup"><span data-stu-id="87501-119">To retrieve Chinese and Portuguese text, specify both the primary and sublanguage identifiers.</span></span><br/><span data-ttu-id="87501-120">**Windows Server 2003 und Windows XP:** Geben Sie nur die primäre Sprachen-ID für Portugiesisch an.</span><span class="sxs-lookup"><span data-stu-id="87501-120">**Windows Server 2003 and Windows XP:** Specify only the primary language identifier for Portuguese.</span></span><br/><span data-ttu-id="87501-121">**Windows 10**: "Help &lt; LangID &gt; " Text mit benutzerdefiniertem sprach Bezeichner gibt immer Zeichen folgen in englischer Sprache zurück, obwohl der lokalisierte Wert weiterhin mithilfe des zuvor erwähnten Schlüssels aus der Registrierung abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="87501-121">**Windows 10**: "Help &lt;langid&gt;" text with custom language identifier always returns strings in English, although localized value can still be retrieved from the registry using the aforementioned key.</span></span><br/><br/> |
| <span data-ttu-id="87501-122">**HKEY- \_ Leistung \_ nlstext**</span><span class="sxs-lookup"><span data-stu-id="87501-122">**HKEY\_PERFORMANCE\_NLSTEXT**</span></span> | <span data-ttu-id="87501-123">Abfrage Zeichenfolgen basierend auf der Standardbenutzer Oberflächen Sprache des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="87501-123">Query strings based on the default UI language of the current user.</span></span> <span data-ttu-id="87501-124">Legen Sie den *lpvaluename* -Parameter entweder auf "Counter" oder "Help" fest, um die Namen bzw. den Hilfetext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87501-124">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="87501-125">**HKEY- \_ Leistungs \_ Text**</span><span class="sxs-lookup"><span data-stu-id="87501-125">**HKEY\_PERFORMANCE\_TEXT**</span></span>    | <span data-ttu-id="87501-126">Abfragen von englischen Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="87501-126">Query English strings.</span></span> <span data-ttu-id="87501-127">Legen Sie den *lpvaluename* -Parameter entweder auf "Counter" oder "Help" fest, um die Namen bzw. den Hilfetext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87501-127">Set the *lpValueName* parameter to either "Counter" or "Help" to retrieve the names or help text, respectively.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





<span data-ttu-id="87501-128">Die-Funktion gibt die Daten als Liste von Zeichen folgen zurück.</span><span class="sxs-lookup"><span data-stu-id="87501-128">The function returns the data as a list of strings.</span></span> <span data-ttu-id="87501-129">Jede Zeichenfolge wird mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="87501-129">Each string is null-terminated.</span></span> <span data-ttu-id="87501-130">Auf die letzte Zeichenfolge folgt ein zusätzliches null-Terminator.</span><span class="sxs-lookup"><span data-stu-id="87501-130">The last string is followed by an additional null terminator.</span></span> <span data-ttu-id="87501-131">Die Zeichen folgen werden als Paare aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="87501-131">The strings are listed in pairs.</span></span> <span data-ttu-id="87501-132">Die erste Zeichenfolge jedes Paars ist der Index, und die zweite Zeichenfolge ist der Text, der dem Index zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87501-132">The first string of each pair is the index, and the second string is the text associated with the index.</span></span> <span data-ttu-id="87501-133">Die Indikator Daten verwenden nur gerade nummerierte Indizes, während die Hilfe Daten ungerade nummerierte Indizes verwenden.</span><span class="sxs-lookup"><span data-stu-id="87501-133">The counter data uses only even-numbered indexes, while the help data uses odd-numbered indexes.</span></span> <span data-ttu-id="87501-134">Die Paare werden in einer zunehmenden Index Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87501-134">The pairs are returned in increasing index order.</span></span>

<span data-ttu-id="87501-135">In den folgenden Listen finden Sie Beispiele für Counter-und Help-Daten.</span><span class="sxs-lookup"><span data-stu-id="87501-135">The following lists show examples of counter and help data.</span></span> <span data-ttu-id="87501-136">Wenn Sie den Indexwert eines bestimmten Zählers um eins erhöhen, erhalten Sie den Index für den Hilfetext des Zählers.</span><span class="sxs-lookup"><span data-stu-id="87501-136">Incrementing a given counter's index value by one gives you the index to the counter's help text.</span></span> <span data-ttu-id="87501-137">Beispielsweise ist 7 der Hilfe Index, der dem Indikator Index 6 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="87501-137">For example, 7 is the help index associated with counter index 6.</span></span>

<span data-ttu-id="87501-138">Gegen Datenpaare.</span><span class="sxs-lookup"><span data-stu-id="87501-138">Counter data pairs.</span></span>

<dl> <span data-ttu-id="87501-139">2 System 4 Arbeitsspeicher 6% Prozessorzeit</span><span class="sxs-lookup"><span data-stu-id="87501-139">2 System 4 Memory 6 % Processor Time</span></span>
</dl>

<span data-ttu-id="87501-140">Hilfe Datenpaare.</span><span class="sxs-lookup"><span data-stu-id="87501-140">Help data pairs.</span></span>

<dl> <span data-ttu-id="87501-141">3 der System Objekttyp enthält die Leistungsindikatoren... 5 der Arbeitsspeicher Objekttyp enthält die Leistungsindikatoren... 7 Prozessorzeit wird als Prozentsatz des...</span><span class="sxs-lookup"><span data-stu-id="87501-141">3 The System object type includes those counters that ... 5 The Memory object type includes those counters that ... 7 Processor Time is expressed as a percentage of the ...</span></span>
</dl>

<span data-ttu-id="87501-142">Beachten Sie, dass das erste Zeichen folgen Paar in den Daten des Zählers keinen Namen für den Namen identifiziert und ignoriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="87501-142">Note that the first pair of strings in the counter data do not identify a counter name and can be ignored.</span></span> <span data-ttu-id="87501-143">Die Indexnummer des ersten Paars ist 1, und die Zeichenfolge ist eine numerische Zeichenfolge, die den maximalen Indexwert für System Zähler darstellt.</span><span class="sxs-lookup"><span data-stu-id="87501-143">The index number of the first pair is 1 and the string is a numeric string that represents the maximum index value for system counters.</span></span>

<span data-ttu-id="87501-144">Informationen dazu, wie ein Anbieter den Namen und den Hilfetext lädt, finden [Sie unter Hinzufügen von Counter-Namen und Beschreibungen zur Registrierung](adding-counter-names-and-descriptions-to-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="87501-144">For information on how a provider loads the name and help text, see [Adding Counter Names and Descriptions to the Registry](adding-counter-names-and-descriptions-to-the-registry.md).</span></span>

<span data-ttu-id="87501-145">Der Text enthält keine Informationen, die angeben, ob der Text einen Leistungs-oder Leistungs Objektwert identifiziert.</span><span class="sxs-lookup"><span data-stu-id="87501-145">There is no information in the text that indicates if the text identifies a counter or performance object.</span></span> <span data-ttu-id="87501-146">Die einzige Möglichkeit, dieses oder die Beziehung zwischen Indikatoren und Objekten zu ermitteln, besteht darin, die Leistungsdaten selbst abzufragen.</span><span class="sxs-lookup"><span data-stu-id="87501-146">The only way to determine this, or the relationship between counters and objects, is to query the performance data itself.</span></span> <span data-ttu-id="87501-147">Wenn Sie z. b. eine Liste von Objekten und deren Indikatoren auf einer Benutzeroberfläche anzeigen möchten, müssen Sie die Leistungsdaten abrufen und dann die Indexwerte verwenden, um die Textdaten für die Zeichen folgen zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="87501-147">For example, if you want to display a list of objects and their counters in a user interface, you must retrieve the performance data, and then use the index values to parse the text data for the strings.</span></span> <span data-ttu-id="87501-148">Ein Beispiel hierfür finden Sie unter Anzeigen von [Objekt-, Instanz-und Counter-Namen](displaying-object-instance-and-counter-names.md).</span><span class="sxs-lookup"><span data-stu-id="87501-148">For an example that does this, see [Displaying Object, Instance, and Counter Names](displaying-object-instance-and-counter-names.md).</span></span>

<span data-ttu-id="87501-149">Im folgenden Beispiel wird gezeigt, wie **HKEY \_ Performance \_ nlstext** zum Abrufen des Zählers und des Hilfetexts und zum Erstellen einer Tabelle für nachfolgenden Zugriff verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="87501-149">The following example shows how to use **HKEY\_PERFORMANCE\_NLSTEXT** to retrieve the counter and help text and build a table for subsequent access.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.


    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_NLSTEXT key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_NLSTEXT, pwszSource, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array


    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{    UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```



<span data-ttu-id="87501-150">Im folgenden Beispiel wird gezeigt, wie **HKEY- \_ Leistungs \_ Daten** verwendet werden, um den gegen Text abzurufen.</span><span class="sxs-lookup"><span data-stu-id="87501-150">The following example shows how to use **HKEY\_PERFORMANCE\_DATA** to retrieve the counter text.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <strsafe.h>

#pragma comment(lib, "advapi32.lib")

LPWSTR GetText(LPWSTR pwszSource);
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets);
DWORD GetNumberOfTextEntries(LPWSTR pwszSource);
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets);
LANGID GetLanguageId();

void wmain(void)
{
    LPWSTR pCounterTextHead = NULL; // Head of the MULTI_SZ buffer that contains the Counter text.
    LPWSTR pHelpTextHead = NULL;    // Head of the MULTI_SZ buffer that contains the Help text.
    LPDWORD pTextOffsets = NULL;    // Array of DWORDS that contain the offsets to the text in
                                    // pCounterTextHead and pHelpTextHead. The text index
                                    // values mirror the array index.
    DWORD dwNumberOfOffsets = 0;    // Number of elements in the pTextOffsets array.

    pCounterTextHead = GetText(L"Counter");
    if (NULL == pCounterTextHead)
    {
        wprintf(L"GetText(L\"Counter\") failed.\n");
        goto cleanup;
    }

    pHelpTextHead = GetText(L"Help");
    if (NULL == pHelpTextHead)
    {
        wprintf(L"GetText(L\"Help\") failed.\n");
        goto cleanup;
    }

    if (BuildTextTable(pCounterTextHead, pHelpTextHead, &pTextOffsets, &dwNumberOfOffsets))
    {
        PrintCounterAndHelpText(pCounterTextHead, pHelpTextHead, pTextOffsets, dwNumberOfOffsets);
    }
    else
    {
        wprintf(L"BuildTextTable failed.\n");
    }

cleanup:

    if (pCounterTextHead)
        free(pCounterTextHead);

    if (pHelpTextHead)
        free(pHelpTextHead);

    if (pTextOffsets)
        free(pTextOffsets);

    // You do not need to call RegCloseKey if you are only
    // retrieving names and help text.
}


// Get the text based on the source value. This function uses the
// HKEY_PERFORMANCE_DATA key to get the strings.
LPWSTR GetText(LPWSTR pwszSource)
{
    LPWSTR pBuffer = NULL;
    DWORD dwBufferSize = 0;
    LONG status = ERROR_SUCCESS;
    LANGID langid = 0;
    WCHAR wszSourceAndLangId[15];   // Identifies the source of the text; either
                                    // "Counter <langid>" or "Help <langid>"


    // Create the lpValueName string for the registry query.
    langid = GetLanguageId();
    if (0 == langid)
    {
        wprintf(L"GetLanguageId failed to get the default language identifier.\n");
        goto cleanup;
    }

    StringCchPrintf(wszSourceAndLangId, 15, L"%s %03x", pwszSource, langid);

    // Query the size of the text data so you can allocate the buffer.
    status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, NULL, &dwBufferSize);
    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed getting required buffer size. Error is 0x%x.\n", status);
        goto cleanup;
    }

    // Allocate the text buffer and query the text.
    pBuffer = (LPWSTR)malloc(dwBufferSize);
    if (pBuffer)
    {
        status = RegQueryValueEx(HKEY_PERFORMANCE_DATA, wszSourceAndLangId, NULL, NULL, (LPBYTE)pBuffer, &dwBufferSize);
        if (ERROR_SUCCESS != status)
        {
            wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
            free(pBuffer);
            pBuffer = NULL;
            goto cleanup;
        }
    }
    else
    {
        wprintf(L"malloc failed to allocate memory.\n");
    }

cleanup:

    return pBuffer;
}


// Retrieve the default language identifier of the current user. For most languages,
// you use the primary language identifier only to retrieve the text. In Windows XP and
// Windows Server 2003, you use the complete language identifier to retrieve Chinese
// text. In Windows Vista, you use the complete language identifier to retrieve Portuguese
// text.
LANGID GetLanguageId()
{
    LANGID langid = 0;  // Complete language identifier.
    WORD primary = 0;   // Primary language identifier.
    OSVERSIONINFO osvi;

    ZeroMemory(&osvi, sizeof(OSVERSIONINFO));
    osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFO);

    if (GetVersionEx(&osvi))
    {
        langid = GetUserDefaultUILanguage();
        primary = PRIMARYLANGID(langid);

        if ( (LANG_PORTUGUESE == primary && osvi.dwBuildNumber > 5) || // Windows Vista and later
             (LANG_CHINESE == primary && (osvi.dwMajorVersion == 5 && osvi.dwMinorVersion >= 1)) ) // XP and Windows Server 2003
        {
            ; //Use the complete language identifier.
        }
        else
        {
            langid = primary;
        }
    }
    else
    {
        wprintf(L"GetVersionEx failed with 0x%x.\n", GetLastError());
    }

    return langid;
}


// Build a table of offsets into the counter and help text buffers. Use the index
// values from the performance data queries to access the offsets.
BOOL BuildTextTable(LPWSTR pCounterHead, LPWSTR pHelpHead, LPDWORD* pOffsetsHead, LPDWORD pNumberOfOffsets)
{
    BOOL fSuccess = FALSE;
    LPWSTR pwszCounterText = NULL;  // Used to cycle through the Counter text
    LPWSTR pwszHelpText = NULL;     // Used to cycle through the Help text
    LPDWORD pOffsets = NULL;
    DWORD dwCounterIndex = 0;       // Index value of the Counter text
    DWORD dwHelpIndex = 0;          // Index value of the Help text
    DWORD dwSize = 0;               // Size of the block of memory that holds the offset array

    pwszCounterText = pCounterHead;
    pwszHelpText = pHelpHead;

    *pNumberOfOffsets = GetNumberOfTextEntries(L"Last Help");
    if (0 == *pNumberOfOffsets)
    {
        wprintf(L"GetNumberOfTextEntries failed; returned 0 for number of entries.\n");
        goto cleanup;
    }

    dwSize = sizeof(DWORD) * (*pNumberOfOffsets + 1);  // Add one to make the array one-based

    pOffsets = (LPDWORD)malloc(dwSize);
    if (pOffsets)
    {
        ZeroMemory(pOffsets, dwSize);
        *pOffsetsHead = pOffsets;

        // Bypass first record (pair) of the counter data - contains upper bounds of system counter index.
        pwszCounterText += (wcslen(pwszCounterText)+1);
        pwszCounterText += (wcslen(pwszCounterText)+1);

        for (; *pwszCounterText; pwszCounterText += (wcslen(pwszCounterText)+1))
        {
            dwCounterIndex = _wtoi(pwszCounterText);
            dwHelpIndex = _wtoi(pwszHelpText);

            // Use the counter's index value as an indexer into the pOffsets array.
            // Store the offset to the counter text in the array element.
            pwszCounterText += (wcslen(pwszCounterText)+1);  //Skip past index value
            pOffsets[dwCounterIndex] = (DWORD)(pwszCounterText - pCounterHead);

            // Some help indexes for system counters do not have a matching counter, so loop
            // until you find the matching help index or the index is greater than the corresponding
            // counter index. For example, if the indexes were as follows, you would loop
            // until the help index was 11.
            //
            // Counter index       Help Index
            //   2                    3
            //   4                    5
            //   6                    7
            //                        9   (skip because there is no matching Counter index)
            //   10                   11
            while (*pwszHelpText && dwHelpIndex < dwCounterIndex)
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past index value
                pwszHelpText += (wcslen(pwszHelpText)+1);  // Skip past help text to the next index value
                dwHelpIndex = _wtoi(pwszHelpText);
            }

            // Use the Help index value as an indexer into the pOffsets array.
            // Store the offset to the help text in the array element.
            if (dwHelpIndex == (dwCounterIndex + 1))
            {
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past index value
                pOffsets[dwHelpIndex] = (DWORD)(pwszHelpText - pHelpHead);
                pwszHelpText += (wcslen(pwszHelpText)+1);  //Skip past help text to next index value
            }
        }

        fSuccess = TRUE;
    }

cleanup:

    return fSuccess;
}


// Retrieve the last help index used from the registry. Use this number
// to allocate an array of DWORDs. Note that index values are not contiguous.
DWORD GetNumberOfTextEntries(LPWSTR pwszSource)
{
    DWORD dwEntries = 0;
    LONG status = ERROR_SUCCESS;
    HKEY hkey = NULL;
    DWORD dwSize = sizeof(DWORD);
    LPWSTR pwszMessage = NULL;

    status = RegOpenKeyEx(HKEY_LOCAL_MACHINE,
        L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib",
        0,
        KEY_READ,
        &hkey);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegOpenKeyEx failed with 0x%x.\n", status);
        goto cleanup;
    }

    status = RegQueryValueEx(hkey, pwszSource, NULL, 0, (LPBYTE)&dwEntries, &dwSize);

    if (ERROR_SUCCESS != status)
    {
        wprintf(L"RegQueryValueEx failed with 0x%x.\n", status);
    }

cleanup:

    if (hkey)
        RegCloseKey(hkey);

    return dwEntries;
}


// Print the pairs of counter and help text.
void PrintCounterAndHelpText(LPWSTR pCounterTextHead, LPWSTR pHelpTextHead, LPDWORD pTextOffsets, DWORD dwNumberOfOffsets)
{   UNREFERENCED_PARAMETER(dwNumberOfOffsets);
    // Counter index values are even numbers that start at 2 so begin with
    // the second element of the array of offsets. Many array elements will
    // not contain offset values (index values are not contiguous).

    // There is typically a large number of counters, so this example prints
    // the first 10 counters and help text.
    //for (DWORD i = 2; i < (dwNumberOfOffsets+1); i++)

    for (DWORD i = 2; i < 22; i++)
    {
        if (pTextOffsets[i]) // If index offset is not zero
        {
            if (0 == (i % 2)) // Counter text index (even number)
                wprintf(L"%d %s\n", i, pCounterTextHead+pTextOffsets[i]);
            else
                wprintf(L"%d %s\n\n", i, pHelpTextHead+pTextOffsets[i]);
        }
    }
}
```
