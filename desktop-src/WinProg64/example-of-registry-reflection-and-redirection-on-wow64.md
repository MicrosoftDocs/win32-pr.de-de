---
title: Beispiel für die Registrierungsumleitung auf WOW64
description: Der folgende Beispielcode veranschaulicht die separaten Ansichten der Registrierung, die vom Registrierungs-Redirector auf 64-Bit-Windows bereitgestellt werden.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- Beispiele für die 64-Bit-Windows-Programmierung
- 64-Bit-Windows Programmierhandbuch Beispiele für 64-Bit-Windows-Programmierung
- 64-Bit-Windows Programmierhandbuch Beispiele für 64-Bit-Windows Programmierung, Registrierungsumleitung auf WOW64
- Beispiel für die 64-Bit-Windows-Programmierung für die Registrierungsumleitung
- 64-Bit-Windows-Programmierhandbuch 64-Bit-Windows Programmierung, Beispiele siehe 64-Bit-Windows Programmierhandbuchbeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83428edb31e53bdd1c70825c7fa5a4d799a36536fa9c17f9ce1c4587ab096048
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680229"
---
# <a name="example-of-registry-redirection-on-wow64"></a>Beispiel für die Registrierungsumleitung auf WOW64

Der folgende Beispielcode veranschaulicht die separaten Ansichten der Registrierung, die vom Registrierungs-Redirector auf 64-Bit-Windows bereitgestellt werden. Außerdem wird veranschaulicht, wie die Werte von Schlüsseln festgelegt werden, je nachdem, ob ein Schlüssel freigegeben oder umgeleitet wird. Weitere Informationen finden Sie unter [Von WOW64 betroffene Registrierungsschlüssel.](shared-registry-keys.md)

Kompilieren Sie den folgenden Code separat für 32-Bit- und 64-Bit-Windows. Führen Sie jede resultierende ausführbare Datei auf 64-Bit-Windows aus, und vergleichen Sie die Ausgabe. Die Beispielausgabe für beide Versionen ist unterhalb des Quellcodes aufgeführt.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



Wenn die 64-Bit-Version des Beispiels ausgeführt wird, erzeugt sie die folgende Ausgabe. Die Werte der Standardansicht und der alternativen Ansichten von **HKCR \\ Hello** sind identisch, da dieser Schlüssel gemeinsam verwendet wird. Die Werte der anderen Schlüssel unterscheiden sich, da sie umgeleitet werden.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Wenn dieses Beispiel unter diesen Betriebssystemen ausgeführt wird, haben die Standardansichten und alternativen Ansichten des LocalServer32-Schlüssels den gleichen Wert. Dies liegt daran, dass der LocalServer32-Schlüssel umgeleitet und *reflektiert* wird, wodurch sein Wert zwischen den 64-Bit- und 32-Bit-Ansichten der Registrierung synchronisiert wird, sobald das Handle für den Schlüssel geschlossen wird. Die Registrierungsreflektion wurde ab Windows 7 entfernt. Weitere Informationen finden Sie unter [Registrierungsreflektion.](registry-reflection.md)

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

Wenn die 32-Bit-Version des Beispiels ausgeführt wird, erzeugt sie die folgende Ausgabe. Bei einer 32-Bit-Anwendung ist die 64-Bit-Ansicht der Registrierung die alternative Ansicht, sodass die Werte umgekehrt werden, mit Ausnahme von HKCR \\ Hello, bei dem es sich um einen gemeinsam verwendeten Schlüssel handelt.

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

Um die Auswirkungen der Ausführung dieses Beispiels mit regedit zu untersuchen, überprüfen Sie die Werte der folgenden Schlüssel. Beachten Sie, dass Anwendungen die Verwendung von Wow6432Node in hart codierten Registrierungspfaden vermeiden sollten.

**HKLM \\ SOFTWARE \\ Hallo Welt**  
**HKLM \\ SOFTWARE \\ Wow6432Node \\ Hallo Welt**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**  
**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InprocServer32**  
**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-0000-ABCD0000000} \\ LocalServer32**  
**HKCR \\ Wow6432Node \\ Hello**  


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsumleitung](registry-redirector.md)
</dt> <dt>

[Registrierungsreflektion](registry-reflection.md)
</dt> </dl>

 

 




