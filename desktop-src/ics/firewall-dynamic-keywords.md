---
title: Dynamische Firewallschlüsselwörter
description: Sie verwenden die APIs für dynamische Firewallschlüsselwörter, um dynamische Schlüsselwortadressen in Windows Defender Firewall zu verwalten.
keywords:
- Dynamische Firewallschlüsselwörter
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: e60526d8a7889af3173913774790bdd209121040
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681166"
---
# <a name="firewall-dynamic-keywords"></a>Dynamische Firewallschlüsselwörter

Sie verwenden die APIs für dynamische Schlüsselwörter der Firewall, um *dynamische Schlüsselwortadressen* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)zu verwalten. Eine dynamische Schlüsselwortadresse wird verwendet, um einen Satz von IP-Adressen zu erstellen, auf die eine oder mehrere Firewallregeln verweisen können. Dynamische Schlüsselwortadressen unterstützen sowohl IPv4 als auch IPv6.

> [!NOTE]
> Api-Referenzinhalte für die in diesem Thema eingeführten APIs finden Sie unter Referenz zu [dynamischen Firewallschlüsselwörtern.](firewall-dynamic-keywords-reference.md)

## <a name="operations-on-dynamic-keyword-addresses"></a>Vorgänge für dynamische Schlüsselwortadressen

Mit den APIs für dynamische Firewallschlüsselwörter können Sie die folgenden Vorgänge ausführen.

* Hinzufügen dynamischer Schlüsselwortadressen
* Löschen dynamischer Schlüsselwortadressen
* Aufzählen dynamischer Schlüsselwortadressen nach ID oder Typ
* Aktualisieren dynamischer Schlüsselwortadressen
* Abonnieren und Behandeln von Benachrichtigungen über Dynamische Schlüsselwortadressänderungen

Es gibt Codebeispiele für alle diese Vorgänge weiter unten in diesem Thema.

Nachdem Sie eine dynamische Schlüsselwortadresse hinzugefügt haben, wird sie bei Neustarts beibehalten. Sie müssen eine dynamische Schlüsselwortadresse löschen, sobald Sie mit dem -Objekt fertig sind.

Es gibt zwei Klassen dynamischer Schlüsselwortadressen, wie in den nächsten beiden Abschnitten beschrieben.

## <a name="autoresolve-dynamic-keyword-addresses"></a>Dynamische Schlüsselwortadressen automatisch auflösen

Der erste Typ ist *AutoResolve,* wobei das *Schlüsselwortfeld* einen auflösbaren Namen darstellt und die IP-Adressen bei der Erstellung nicht definiert werden.

Diese Objekte sollen ihre IP-Adressen automatisch auflösen. Das heißt, nicht über einen Administrator zum Zeitpunkt der Objekterstellung; auch nicht über das Betriebssystem selbst. Eine Komponente außerhalb des Firewalldiensts muss die IP-Adressauflösung für diese Objekte durchführen und sie entsprechend aktualisieren. Die Implementierung einer solchen Komponente liegt außerhalb des Bereichs dieses Inhalts.

Eine dynamische Schlüsselwortadresse wird als *AutoResolve* angegeben, indem das **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE-Flag** im -Objekt festgelegt wird, wenn die [**FWAddDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) aufgerufen wird. Das *Schlüsselwortfeld* sollte verwendet werden, um den aufgelösten Wert &mdash; darzustellen, d. h. einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder einen Hostnamen. Das  Adressfeld muss für diese Objekte anfänglich NULL sein. Bei diesen Objekten werden ihre IP-Adressen nicht über Startzyklen hinweg beibehalten, und Sie sollten ihre Adressen während des nächsten Startzyklus neu auswerten/erneut auffüllen.

> [!NOTE]
> AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).

## <a name="non-autoresolve-dynamic-keyword-addresses"></a>Dynamische Schlüsselwortadressen, die nicht automatisch aufgelöst werden

Der zweite Typ ist *nicht AutoResolve,* wobei das *Schlüsselwortfeld* eine beliebige Zeichenfolge ist und die Adressen zum Zeitpunkt der Erstellung definiert werden.

Diese Objekte werden verwendet, um einen Satz von IP-Adressen, Subnetzen oder Bereichen zu speichern. Das *Schlüsselwortfeld* wird hier zur Vereinfachung der Verwaltung verwendet und kann auf eine beliebige Zeichenfolge festgelegt werden. Das  Adressfeld muss bei der Erstellung ungleich NULL sein. Adressen für diese Objekte werden bei Neustarts beibehalten.

> [!NOTE]
> Nicht automatisch auflösende dynamische Schlüsselwortadressobjekte lösen Benachrichtigungen für [**FWAddDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)und auch [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)aus.

## <a name="more-about-dynamic-keyword-addresses"></a>Weitere Informationen zu dynamischen Schlüsselwortadressen 

Alle dynamischen Schlüsselwortadressen müssen über einen eindeutigen [**GUID-Bezeichner**](/windows/win32/api/guiddef/ns-guiddef-guid) verfügen, um sie darzustellen.

Die [**FwpmDynamicKeywordSubscribe0-API**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) übermittelt Benachrichtigungen an einen Client, wenn sich dynamische Schlüsselwortadressen ändern. Es wird keine Nutzlast an den Client übermittelt, die genau beschreibt, was sich auf dem System geändert hat. Wenn Sie wissen müssen, welche Objekte sich geändert haben, sollten Sie den aktuellen Zustand von Objekten im System mithilfe der [**APIs FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) oder [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) abfragen. Sie können die verschiedenen Flags verwenden, um Benachrichtigungen nur für eine Teilmenge von -Objekten anzufordern. Wenn Sie keine Flags verwenden, werden Änderungsbenachrichtigungen für alle Objekte übermittelt.

Eine Firewallregel kann dynamische Schlüsselwortadressen verwenden, anstatt IP-Adressen explizit für die Remoteadressenbedingung zu definieren. Eine Firewallregel kann sowohl dynamische Schlüsselwortadressen als auch statisch definierte Remoteadressbereiche verwenden. Ein einzelnes dynamisches Schlüsselwortadressobjekt kann über mehrere Firewallregeln hinweg wiederverwendet werden. Wenn eine Firewallregel über keine konfigurierten Remoteadressen verfügt (d. h. nur mit AutoResolve-Objekten konfiguriert, die noch nicht aufgelöst wurden), wird die Regel nicht erzwungen. Wenn eine Regel mehrere dynamische Schlüsselwortadressen verwendet, wird die Regel außerdem für alle Adressen erzwungen, die derzeit aufgelöst werden, auch wenn es andere Objekte gibt, die noch nicht aufgelöst wurden. Wenn eine dynamische Schlüsselwortadresse aktualisiert wird, werden auch die Remoteadressen aller zugeordneten Regelobjekte aktualisiert.

Das Betriebssystem selbst erzwingt keine Abhängigkeiten zwischen einer Regel und einer dynamischen Schlüsselwortadresse. Dies bedeutet, dass beide Objekte zuerst erstellt werden können, &mdash; sodass die Regel auf dynamische Schlüsselwortadressen-IDs verweisen kann, die noch nicht vorhanden sind (in diesem Fall wird die Regel nicht erzwungen). Darüber hinaus können Sie eine dynamische Schlüsselwortadresse auch dann löschen, wenn sie von einer Firewallregel verwendet wird. In diesem Thema wird beschrieben, wie ein Administrator Regeln für die Verwendung der dynamischen Schlüsselwortadresse konfigurieren kann.

## <a name="code-examples"></a>Codebeispiele

Um jedes dieser Codebeispiele auszuprobieren, starten Sie zuerst Visual Studio und erstellen ein neues Projekt basierend auf der **Projektvorlage Konsolen-App.** Sie können einfach den Inhalt von `main.cpp` durch die Codeauflistung ersetzen.

In den meisten Codebeispielen werden die [Windows-Implementierungsbibliotheken (WINDOWS Implementation Libraries, WILL)](https://github.com/Microsoft/wil)verwendet. Eine bequeme Möglichkeit zum Installieren vonWILL besteht darin, zu Visual Studio zu wechseln, auf **Projekt** \> **NuGet-Pakete verwalten...** Durchsuchen zu \> klicken, **Microsoft.Windows.ImplementationLibrary** in das Suchfeld einzugeben, das Element in den Suchergebnissen auszuwählen und dann auf **Installieren** zu klicken, um das Paket für dieses Projekt zu installieren.

> [!NOTE]
> Zeigertypen für die freien NetFw-Funktionen werden über `NetFw.h` veröffentlicht, aber es wird keine statische Linkbibliothek veröffentlicht. Verwenden [](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)Sie das / [GetProcAddress-Muster](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) LoadLibraryExW zum Aufrufen dieser Funktionen, wie in diesen Codebeispielen gezeigt.

### <a name="add-a-dynamic-keyword-address"></a>Hinzufügen einer dynamischen Schlüsselwortadresse

In diesem Beispiel wird die Verwendung der [**FWAddDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) veranschaulicht.

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a>Löschen einer dynamischen Schlüsselwortadresse

In diesem Beispiel wird die Verwendung der [**FWDeleteDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) veranschaulicht.

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a>Aufzählen und Freigeben dynamischer Schlüsselwortadressen nach ID

In diesem Beispiel wird gezeigt, wie die Funktionen [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) und [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) verwendet werden.

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a>Aufzählen und Freigeben dynamischer Schlüsselwortadressen nach Typ

In diesem Beispiel wird gezeigt, wie die Funktionen [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) und [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) verwendet werden.

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a>Aktualisieren dynamischer Schlüsselwortadressen

In diesem Beispiel wird die Verwendung der [**FWUpdateDynamicKeywordAddress0-Funktion**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) veranschaulicht.

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a>Abonnieren und Behandeln von Benachrichtigungen über Dynamische Schlüsselwortadressänderungen

In diesem Beispiel wird gezeigt, wie die Funktionen [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) und [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) sowie der [**FWPM_DYNAMIC_KEYWORD_CALLBACK0-Rückruf**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) verwendet werden.

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a>Zugehörige Themen

* [Referenz zu dynamischen Firewallschlüsselwörtern](firewall-dynamic-keywords-reference.md)
