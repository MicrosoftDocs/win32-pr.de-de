---
description: Die Anwendung kann eine andere Gruppe von Benutzeroberflächen Sprachen als die vom Ziel Betriebssystem unterstützten Sprachen unterstützen. In diesem Thema wird diese Art der Unterstützung mithilfe von Code Ausschnitten aus kompletten Beispielen erläutert.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: Unterstützen von Application-Specific Spracheinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6bddfe94586751d3b0f4757c670c006317e49b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352632"
---
# <a name="supporting-application-specific-language-settings"></a><span data-ttu-id="4b91b-104">Unterstützen von Application-Specific Spracheinstellungen</span><span class="sxs-lookup"><span data-stu-id="4b91b-104">Supporting Application-Specific Language Settings</span></span>

<span data-ttu-id="4b91b-105">Die Anwendung kann eine andere Gruppe von Benutzeroberflächen Sprachen als die vom Ziel Betriebssystem unterstützten Sprachen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4b91b-105">Your application can support a different set of user interface languages from those supported by the target operating system.</span></span> <span data-ttu-id="4b91b-106">In diesem Thema wird diese Art der Unterstützung mithilfe von Code Ausschnitten aus kompletten Beispielen erläutert.</span><span class="sxs-lookup"><span data-stu-id="4b91b-106">This topic discusses this type of support, using snippets from complete samples.</span></span>

## <a name="interpret-users-language-preference"></a><span data-ttu-id="4b91b-107">Spracheinstellung des Benutzers interpretieren</span><span class="sxs-lookup"><span data-stu-id="4b91b-107">Interpret User's Language Preference</span></span>

<span data-ttu-id="4b91b-108">Die Anwendung muss zuerst festlegen, welche Benutzeroberflächen Sprache auf der Grundlage der Benutzereinstellung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b91b-108">Your application must first determine which user interface language to display, based on user preference.</span></span> <span data-ttu-id="4b91b-109">Der Code kann die Einstellungen aus einer Konfigurationsdatei oder aus Registrierungs Einstellungen lesen.</span><span class="sxs-lookup"><span data-stu-id="4b91b-109">The code can read the settings from a configuration file or from registry settings.</span></span>

<span data-ttu-id="4b91b-110">Im folgenden Beispiel werden zwei Funktionen definiert, die verwendet werden, um die Spracheinstellung des Benutzers zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="4b91b-110">The following example defines two functions used to interpret the user's language preference.</span></span> <span data-ttu-id="4b91b-111">Die erste Funktion veranschaulicht das Lesen einer durch Trennzeichen getrennten Liste von Sprachen aus einer Datei, die im Code als "langs.txt" dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4b91b-111">The first function illustrates the reading of a delimited list of languages from a file, represented in the code as "langs.txt".</span></span> <span data-ttu-id="4b91b-112">Die im Beispiel unterstützten Trennzeichen sind ",", ";", "." und "".</span><span class="sxs-lookup"><span data-stu-id="4b91b-112">The delimiters supported in the sample are ",",";";"." and " ".</span></span> <span data-ttu-id="4b91b-113">Die zweite Funktion konvertiert die aus der Datei gelesene Zeichenfolge in einen Wert mit mehreren Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="4b91b-113">The second function converts the string read from the file to a multi-string value.</span></span> <span data-ttu-id="4b91b-114">Dieser Vorgang ist erforderlich, da die MUI-Funktionen, die zum Festlegen von Sprachen verwendet werden, nur Werte für mehrere Zeichen folgen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4b91b-114">This operation is necessary because the MUI functions used to set languages only accept multi-string values.</span></span>


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a><span data-ttu-id="4b91b-115">Festlegen der Anwendungs Sprache</span><span class="sxs-lookup"><span data-stu-id="4b91b-115">Set the Application Language</span></span>

<span data-ttu-id="4b91b-116">Nachdem Sie die sprach Einstellungs Informationen gelesen haben, muss der Anwendungscode die abgerufene Einstellung verwenden, um die Anwendungs Sprache festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4b91b-116">After reading the language preference information, the application code must use the retrieved setting to set the application language.</span></span> <span data-ttu-id="4b91b-117">Unter Windows 7 und höher kann die Anwendung die Sprache auf Prozessebene festlegen, indem Sie die Funktion [**setprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) aufruft.</span><span class="sxs-lookup"><span data-stu-id="4b91b-117">On Windows 7 and later, the application can set the language at the process level by calling the [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



<span data-ttu-id="4b91b-118">Unter Windows Vista und höher wird die Anwendungs Sprache auf Thread Ebene festgelegt, indem die Funktion [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4b91b-118">On Windows Vista and later, the application language is set at the thread level by calling the [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) function.</span></span>


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a><span data-ttu-id="4b91b-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b91b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b91b-120">Festlegen der Einstellungen für die Anwendungs Sprache</span><span class="sxs-lookup"><span data-stu-id="4b91b-120">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> <dt>

[<span data-ttu-id="4b91b-121">Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="4b91b-121">MUI: Application-Specific Settings Sample (Windows Vista)</span></span>](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[<span data-ttu-id="4b91b-122">Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="4b91b-122">MUI: Application-Specific Settings Sample (Pre-Windows Vista)</span></span>](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



