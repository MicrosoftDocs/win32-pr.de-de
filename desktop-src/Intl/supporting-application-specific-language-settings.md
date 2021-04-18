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
# <a name="supporting-application-specific-language-settings"></a>Unterstützen von Application-Specific Spracheinstellungen

Die Anwendung kann eine andere Gruppe von Benutzeroberflächen Sprachen als die vom Ziel Betriebssystem unterstützten Sprachen unterstützen. In diesem Thema wird diese Art der Unterstützung mithilfe von Code Ausschnitten aus kompletten Beispielen erläutert.

## <a name="interpret-users-language-preference"></a>Spracheinstellung des Benutzers interpretieren

Die Anwendung muss zuerst festlegen, welche Benutzeroberflächen Sprache auf der Grundlage der Benutzereinstellung angezeigt werden soll. Der Code kann die Einstellungen aus einer Konfigurationsdatei oder aus Registrierungs Einstellungen lesen.

Im folgenden Beispiel werden zwei Funktionen definiert, die verwendet werden, um die Spracheinstellung des Benutzers zu interpretieren. Die erste Funktion veranschaulicht das Lesen einer durch Trennzeichen getrennten Liste von Sprachen aus einer Datei, die im Code als "langs.txt" dargestellt wird. Die im Beispiel unterstützten Trennzeichen sind ",", ";", "." und "". Die zweite Funktion konvertiert die aus der Datei gelesene Zeichenfolge in einen Wert mit mehreren Zeichen folgen. Dieser Vorgang ist erforderlich, da die MUI-Funktionen, die zum Festlegen von Sprachen verwendet werden, nur Werte für mehrere Zeichen folgen akzeptieren.


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



## <a name="set-the-application-language"></a>Festlegen der Anwendungs Sprache

Nachdem Sie die sprach Einstellungs Informationen gelesen haben, muss der Anwendungscode die abgerufene Einstellung verwenden, um die Anwendungs Sprache festzulegen. Unter Windows 7 und höher kann die Anwendung die Sprache auf Prozessebene festlegen, indem Sie die Funktion [**setprocesliniferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) aufruft.


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



Unter Windows Vista und höher wird die Anwendungs Sprache auf Thread Ebene festgelegt, indem die Funktion [**setthreadpreferreduilanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) aufgerufen wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Einstellungen für die Anwendungs Sprache](setting-application-language-preferences.md)
</dt> <dt>

[Beispiel für MUI: Application-Specific Einstellungen (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[Beispiel für MUI: Application-Specific Einstellungen (Pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



