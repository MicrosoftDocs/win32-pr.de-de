---
description: Ihre Anwendung kann einen anderen Satz von Benutzeroberflächensprachen unterstützen als die sprachen, die vom Zielbetriebssystem unterstützt werden. In diesem Thema wird diese Art von Unterstützung mithilfe von Codeausschnitten aus vollständigen Beispielen erläutert.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: Unterstützen von Application-Specific Language Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130060"
---
# <a name="supporting-application-specific-language-settings"></a>Unterstützen von Application-Specific Language Einstellungen

Ihre Anwendung kann einen anderen Satz von Benutzeroberflächensprachen unterstützen als die sprachen, die vom Zielbetriebssystem unterstützt werden. In diesem Thema wird diese Art von Unterstützung mithilfe von Codeausschnitten aus vollständigen Beispielen erläutert.

## <a name="interpret-users-language-preference"></a>Interpretieren der Spracheinstellung des Benutzers

Ihre Anwendung muss zunächst anhand der Benutzerpräferenz bestimmen, welche Sprache der Benutzeroberfläche angezeigt werden soll. Der Code kann die Einstellungen aus einer Konfigurationsdatei oder aus Registrierungseinstellungen lesen.

Im folgenden Beispiel werden zwei Funktionen definiert, die zum Interpretieren der Spracheinstellung des Benutzers verwendet werden. Die erste Funktion veranschaulicht das Lesen einer durch Trennzeichen getrennten Liste von Sprachen aus einer Datei, die im Code als "langs.txt" dargestellt wird. Die im Beispiel unterstützten Trennzeichen sind ",",";";"." und " ". Die zweite Funktion konvertiert die aus der Datei gelesene Zeichenfolge in einen Wert mit mehreren Zeichenfolgen. Dieser Vorgang ist erforderlich, da die ZUM Festlegen von Sprachen verwendeten FUNKTIONEN nur Werte mit mehreren Zeichenfolgen akzeptieren.


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



## <a name="set-the-application-language"></a>Festlegen der Anwendungssprache

Nach dem Lesen der Spracheinstellungsinformationen muss der Anwendungscode die abgerufene Einstellung verwenden, um die Anwendungssprache festzulegen. Ab Windows 7 kann die Anwendung die Sprache auf Prozessebene festlegen, indem sie die [**SetProcessPreferredUILanguages-Funktion aufruft.**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)


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



Auf Windows Vista und höher wird die Anwendungssprache auf Threadebene festgelegt, indem die [**SetThreadPreferredUILanguages-Funktion**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) aufgerufen wird.


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

[Festlegen von Einstellungen für die Anwendungssprache](setting-application-language-preferences.md)
</dt> <dt>

[WÄHREND: Application-Specific Einstellungen-Beispiel (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[WÄHREND: Application-Specific Einstellungen-Beispiel (Pre-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



