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
# <a name="retrieving-counter-names-and-help-text"></a>Abrufen von Namen von Zählern und Hilfe Text

Die Leistungsdaten enthalten Indexwerte, mit denen Sie die Namen und den Hilfetext für die einzelnen registrierten Objekte und Leistungsindikator suchen. Die Member **objectnametitleindex** und **objecthelptitleindex** der [**perf- \_ \_ Objekttyp**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type) Struktur enthalten die Indexwerte für den Objektnamen bzw. den Hilfetext, und die Elemente **counternametitleindex** und **counterhelptitleindex** der Leistungsindikator [**\_ \_ Definitions**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition) Struktur enthalten die Indexwerte für den Indikator Namen bzw. den Hilfetext.

Um die Namen oder den Hilfetext abzurufen, rufen Sie die [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) -Funktion auf. Legen Sie den *HKEY* -Parameter auf einen der folgenden vordefinierten Schlüssel fest. Normalerweise verwenden Sie den Schlüssel **HKEY \_ Performance \_ nlstext** , damit Sie die sprach Kennung des Benutzers nicht ermitteln müssen.



| Schlüssel                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HKEY- \_ Leistungs \_ Daten**    | Abfrage Zeichenfolgen basierend auf dem Sprach-ID-Wert, den Sie im *lpvaluename* -Parameter angeben. Legen Sie den *lpvaluename* -Parameter entweder auf "Counter &lt; LangID &gt; " oder "Help &lt; LangID" fest, &gt; um die Namen bzw. den Hilfetext abzurufen, wobei " &lt; LangID &gt; " für die Systemsprachen-ID steht, die als 0 (null) mit **drei Ziffern** formatiert ist. Der sprach Bezeichner ist optional. Wenn Sie keinen sprach Bezeichner angeben, gibt die Funktion englische Zeichen folgen zurück. Überprüfen Sie den `HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Perflib` Registrierungsschlüssel auf die Liste der Sprachen, die auf Ihrem System verfügbar sind.<br/>Wenn Sie Text in den meisten Sprachen abrufen möchten, geben Sie nur die primäre Sprach-ID an. Wenn Sie z. b. englische Zeichen folgen abrufen möchten, geben Sie den sprach Bezeichner als 009, nicht als 1033 für Englisch-US an.<br/>Geben Sie zum Abrufen von Chinesisch-und Portugiesisch-Text sowohl die primären als auch die unter Sprachen-IDs an.<br/>**Windows Server 2003 und Windows XP:** Geben Sie nur die primäre Sprachen-ID für Portugiesisch an.<br/>**Windows 10**: "Help &lt; LangID &gt; " Text mit benutzerdefiniertem sprach Bezeichner gibt immer Zeichen folgen in englischer Sprache zurück, obwohl der lokalisierte Wert weiterhin mithilfe des zuvor erwähnten Schlüssels aus der Registrierung abgerufen werden kann.<br/><br/> |
| **HKEY- \_ Leistung \_ nlstext** | Abfrage Zeichenfolgen basierend auf der Standardbenutzer Oberflächen Sprache des aktuellen Benutzers. Legen Sie den *lpvaluename* -Parameter entweder auf "Counter" oder "Help" fest, um die Namen bzw. den Hilfetext abzurufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **HKEY- \_ Leistungs \_ Text**    | Abfragen von englischen Zeichen folgen. Legen Sie den *lpvaluename* -Parameter entweder auf "Counter" oder "Help" fest, um die Namen bzw. den Hilfetext abzurufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |





Die-Funktion gibt die Daten als Liste von Zeichen folgen zurück. Jede Zeichenfolge wird mit Null beendet. Auf die letzte Zeichenfolge folgt ein zusätzliches null-Terminator. Die Zeichen folgen werden als Paare aufgelistet. Die erste Zeichenfolge jedes Paars ist der Index, und die zweite Zeichenfolge ist der Text, der dem Index zugeordnet ist. Die Indikator Daten verwenden nur gerade nummerierte Indizes, während die Hilfe Daten ungerade nummerierte Indizes verwenden. Die Paare werden in einer zunehmenden Index Reihenfolge zurückgegeben.

In den folgenden Listen finden Sie Beispiele für Counter-und Help-Daten. Wenn Sie den Indexwert eines bestimmten Zählers um eins erhöhen, erhalten Sie den Index für den Hilfetext des Zählers. Beispielsweise ist 7 der Hilfe Index, der dem Indikator Index 6 zugeordnet ist.

Gegen Datenpaare.

<dl> 2 System 4 Arbeitsspeicher 6% Prozessorzeit
</dl>

Hilfe Datenpaare.

<dl> 3 der System Objekttyp enthält die Leistungsindikatoren... 5 der Arbeitsspeicher Objekttyp enthält die Leistungsindikatoren... 7 Prozessorzeit wird als Prozentsatz des...
</dl>

Beachten Sie, dass das erste Zeichen folgen Paar in den Daten des Zählers keinen Namen für den Namen identifiziert und ignoriert werden kann. Die Indexnummer des ersten Paars ist 1, und die Zeichenfolge ist eine numerische Zeichenfolge, die den maximalen Indexwert für System Zähler darstellt.

Informationen dazu, wie ein Anbieter den Namen und den Hilfetext lädt, finden [Sie unter Hinzufügen von Counter-Namen und Beschreibungen zur Registrierung](adding-counter-names-and-descriptions-to-the-registry.md).

Der Text enthält keine Informationen, die angeben, ob der Text einen Leistungs-oder Leistungs Objektwert identifiziert. Die einzige Möglichkeit, dieses oder die Beziehung zwischen Indikatoren und Objekten zu ermitteln, besteht darin, die Leistungsdaten selbst abzufragen. Wenn Sie z. b. eine Liste von Objekten und deren Indikatoren auf einer Benutzeroberfläche anzeigen möchten, müssen Sie die Leistungsdaten abrufen und dann die Indexwerte verwenden, um die Textdaten für die Zeichen folgen zu analysieren. Ein Beispiel hierfür finden Sie unter Anzeigen von [Objekt-, Instanz-und Counter-Namen](displaying-object-instance-and-counter-names.md).

Im folgenden Beispiel wird gezeigt, wie **HKEY \_ Performance \_ nlstext** zum Abrufen des Zählers und des Hilfetexts und zum Erstellen einer Tabelle für nachfolgenden Zugriff verwendet wird.


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



Im folgenden Beispiel wird gezeigt, wie **HKEY- \_ Leistungs \_ Daten** verwendet werden, um den gegen Text abzurufen.


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
