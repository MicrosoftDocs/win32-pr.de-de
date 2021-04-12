---
title: Beispiel für Registrierungs Umleitung auf WOW64
description: Der folgende Beispielcode veranschaulicht die separaten Ansichten der Registrierung, die vom registrierungsredirector auf 64-Bit-Fenstern bereitgestellt werden.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- Beispiele 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch Beispiele 64-Bit Windows-Programmierung
- 64-Bit-Windows-Programmier Leit Faden Beispiele 64-Bit Windows-Programmierung, Registrierungs Umleitung auf WOW64
- Beispiel für die Registrierungs Umleitung 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Beispiele finden Sie unter Beispiele für den Windows-Programmier Leit Faden von 64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff37b077137e9802e6716319623fe8e372941500
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "104391159"
---
# <a name="example-of-registry-redirection-on-wow64"></a><span data-ttu-id="f52b6-108">Beispiel für Registrierungs Umleitung auf WOW64</span><span class="sxs-lookup"><span data-stu-id="f52b6-108">Example of Registry Redirection on WOW64</span></span>

<span data-ttu-id="f52b6-109">Der folgende Beispielcode veranschaulicht die separaten Ansichten der Registrierung, die vom registrierungsredirector auf 64-Bit-Fenstern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f52b6-109">The following example code demonstrates the separate views of the registry provided by the registry redirector on 64-bit Windows.</span></span> <span data-ttu-id="f52b6-110">Außerdem wird veranschaulicht, wie die Werte der Schlüssel festgelegt werden, abhängig davon, ob ein Schlüssel freigegeben oder umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f52b6-110">It also demonstrates how the values of keys are set depending on whether a key is shared or redirected.</span></span> <span data-ttu-id="f52b6-111">Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="f52b6-111">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>

<span data-ttu-id="f52b6-112">Kompilieren Sie den folgenden Code separat für 32-Bit-und 64-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="f52b6-112">Compile the following code separately for both 32-bit and 64-bit Windows.</span></span> <span data-ttu-id="f52b6-113">Führen Sie jede resultierende ausführbare Datei auf 64-Bit-Windows aus, und vergleichen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f52b6-113">Run each resulting executable file on 64-bit Windows and compare the output.</span></span> <span data-ttu-id="f52b6-114">Die Beispielausgabe für beide Versionen ist unterhalb des Quellcodes aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f52b6-114">Sample output for both versions is listed below the source code.</span></span>


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



<span data-ttu-id="f52b6-115">Wenn die 64-Bit-Version des Beispiels ausgeführt wird, wird die folgende Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f52b6-115">When the 64-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="f52b6-116">Die Werte sowohl der Standard-als auch der alternativen Ansicht von **HKCR \\ Hello** sind identisch, da dieser Schlüssel gemeinsam verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f52b6-116">The values of both the default and alternate views of **HKCR\\Hello** are the same because this key is shared.</span></span> <span data-ttu-id="f52b6-117">Die Werte der anderen Schlüssel unterscheiden sich, da Sie umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f52b6-117">The values of the other keys differ because they are redirected.</span></span>

<span data-ttu-id="f52b6-118">**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Wenn dieses Beispiel unter diesen Betriebssystemen ausgeführt wird, haben die standardmäßigen und alternativen Sichten des LocalServer32-Schlüssels denselben Wert.</span><span class="sxs-lookup"><span data-stu-id="f52b6-118">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** When this example is run on these operating systems, the default and alternate views of the LocalServer32 key have the same value.</span></span> <span data-ttu-id="f52b6-119">Dies liegt daran, dass die LocalServer32-Taste umgeleitet und *reflektiert* wird, wodurch der Wert zwischen den 64-Bit-und 32-Bit-Sichten der Registrierung synchronisiert wird, sobald das Handle für den Schlüssel geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="f52b6-119">This is because the LocalServer32 key is redirected and *reflected*, which causes its value to be synchronized between the 64-bit and 32-bit views of the registry as soon as the handle to the key is closed.</span></span> <span data-ttu-id="f52b6-120">Die Registrierungs Reflektion wurde ab Windows 7 entfernt.</span><span class="sxs-lookup"><span data-stu-id="f52b6-120">Registry reflection was removed starting with Windows 7.</span></span> <span data-ttu-id="f52b6-121">Weitere Informationen finden Sie unter [Registry Reflection](registry-reflection.md).</span><span class="sxs-lookup"><span data-stu-id="f52b6-121">For more information, see [Registry Reflection](registry-reflection.md).</span></span>

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

<span data-ttu-id="f52b6-122">Wenn die 32-Bit-Version des Beispiels ausgeführt wird, wird die folgende Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f52b6-122">When the 32-bit version of the example is run, it produces the following output.</span></span> <span data-ttu-id="f52b6-123">Bei einer 32-Bit-Anwendung ist die 64-Bit-Ansicht der Registrierung die Alternative Ansicht, sodass die Werte umgekehrt werden, mit Ausnahme von HKCR \\ Hello, einem gemeinsam verwendeten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="f52b6-123">For a 32-bit application, the 64-bit view of the registry is the alternate view so the values are reversed, except for HKCR\\Hello, which is a shared key.</span></span>

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

<span data-ttu-id="f52b6-124">Überprüfen Sie die Werte der folgenden Schlüssel, um die Auswirkung der Ausführung dieses Beispiels mit regedit zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f52b6-124">To examine the effect of running this example with regedit, inspect the values of the following keys.</span></span> <span data-ttu-id="f52b6-125">Beachten Sie, dass Anwendungen die Verwendung von Wow6432Node in hart codierten Registrierungs Pfaden vermeiden sollten.</span><span class="sxs-lookup"><span data-stu-id="f52b6-125">Note that applications should avoid using Wow6432Node in hard-coded registry paths.</span></span>

<span data-ttu-id="f52b6-126">**HKLM- \\ Software \\ Hallo Welt**</span><span class="sxs-lookup"><span data-stu-id="f52b6-126">**HKLM\\SOFTWARE\\Hello World**</span></span>  
<span data-ttu-id="f52b6-127">**HKLM \\ Software \\ Wow6432Node \\ Hallo Welt**</span><span class="sxs-lookup"><span data-stu-id="f52b6-127">**HKLM\\SOFTWARE\\Wow6432Node\\Hello World**</span></span>  
<span data-ttu-id="f52b6-128">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="f52b6-128">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="f52b6-129">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InProcServer32**</span><span class="sxs-lookup"><span data-stu-id="f52b6-129">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="f52b6-130">**HKCR \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="f52b6-130">**HKCR\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="f52b6-131">**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000}**</span><span class="sxs-lookup"><span data-stu-id="f52b6-131">**HKCR\\Hello HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}**</span></span>  
<span data-ttu-id="f52b6-132">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ InProcServer32**</span><span class="sxs-lookup"><span data-stu-id="f52b6-132">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32**</span></span>  
<span data-ttu-id="f52b6-133">**HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD00000000} \\ LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="f52b6-133">**HKCR\\Wow6432Node\\CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32**</span></span>  
<span data-ttu-id="f52b6-134">**HKCR \\ Wow6432Node \\ Hello**</span><span class="sxs-lookup"><span data-stu-id="f52b6-134">**HKCR\\Wow6432Node\\Hello**</span></span>  


## <a name="related-topics"></a><span data-ttu-id="f52b6-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f52b6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f52b6-136">Registrierungs Redirector</span><span class="sxs-lookup"><span data-stu-id="f52b6-136">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="f52b6-137">Registrierungs Reflektion</span><span class="sxs-lookup"><span data-stu-id="f52b6-137">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

 




