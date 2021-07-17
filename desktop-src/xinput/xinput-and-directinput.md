---
title: XInput und DirectInput
description: XInput ist eine API, mit der Anwendungen Eingaben vom Xbox Controller für die Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373191"
---
# <a name="xinput-and-directinput"></a>XInput und DirectInput

XInput ist eine API, mit der Anwendungen Eingaben vom Xbox Controller für die Windows. In diesem Dokument werden die Unterschiede zwischen XInput- und [DirectInput-Implementierungen](/previous-versions/windows/desktop/ee416842(v=vs.85)) des Xbox-Controllers beschrieben und wie Sie XInput-Geräte und ältere DirectInput-Geräte gleichzeitig unterstützen können.

> [!Note]  
> Die Verwendung von [Legacy-DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) wird nicht empfohlen, und DirectInput ist für Windows Store verfügbar.

## <a name="the-new-standard-xinput"></a>Der neue Standard: XInput

XInput ist jetzt für die Spieleentwicklung verfügbar. Dies ist der neue Eingabestandard für xbox und Windows. Die APIs sind über das DirectX SDK verfügbar, und der Treiber ist über das Windows verfügbar.

Die Verwendung von XInput gegenüber [DirectInput hat mehrere Vorteile:](/previous-versions/windows/desktop/ee416842(v=vs.85))

-   XInput ist einfacher zu verwenden und erfordert weniger Setup als [DirectInput.](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   Bei der Xbox- Windows-Programmierung werden die gleichen Sätze von Kern-APIs verwendet, sodass die Programmierung die plattformübergreifende Übersetzung erheblich vereinfacht.
-   Es wird eine große installierte Basis von Xbox-Controllern geben.
-   XInput-Geräte (d. h. Xbox-Controller) verfügen nur über Vibrationsfunktionen, wenn XInput-APIs verwendet werden.
-   Zukünftige Controller, die für die Xbox-Konsole veröffentlicht werden (d. h. Rädchen), funktionieren auch auf Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Verwenden des Xbox-Controllers mit DirectInput

Der Xbox Controller wird ordnungsgemäß auf [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))aufzählt und kann mit den DirectInputAPIs verwendet werden. Einige von XInput bereitgestellte Funktionen fehlen jedoch in der DirectInput-Implementierung:

-   Die linken und rechten Triggerschaltflächen fungieren als einzelne Schaltfläche, nicht unabhängig voneinander.
-   Die Vibrationseffekte sind nicht verfügbar.
-   Abfragen für Headsetgeräte sind nicht verfügbar.

Die Kombination der linken und rechten Trigger in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ist standardmäßig. Spiele gehen immer davon aus, dass DirectInput-Geräteachsen zentriert sind, wenn keine Benutzerinteraktion mit dem Gerät besteht. Der Xbox-Controller wurde jedoch so entworfen, dass er den Mindestwert registriert, nicht den Mittelpunkt, wenn die Trigger nicht gehalten werden. Bei älteren Spielen wird daher eine Benutzerinteraktion angenommen.

Die Lösung war das Kombinieren der Trigger, das Festlegen eines Triggers auf eine positive und der andere auf eine negative Richtung, sodass keine Benutzerinteraktion darauf hindeuten [kann, dass DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) das "Steuerelement" in der Mitte befindet.

Um die Triggerwerte separat zu testen, müssen Sie XInput verwenden.

## <a name="xinput-and-directinput-side-by-side"></a>XInput und DirectInput nebeneinander

Durch die ausschließliche Unterstützung von XInput funktioniert Ihr Spiel nicht mit [älteren DirectInput-Geräten.](/previous-versions/windows/desktop/ee416842(v=vs.85)) XInput erkennt diese Geräte nicht.

Wenn Ihr Spiel ältere [DirectInput-Geräte](/previous-versions/windows/desktop/ee416842(v=vs.85)) unterstützen soll, können Sie DirectInput und XInput nebeneinander verwenden. Beim Aufzählen Ihrer DirectInput-Geräte werden alle DirectInput-Geräte ordnungsgemäß aufzählt. Alle XInput-Geräte werden sowohl als XInput- als auch als DirectInput-Geräte gezeigt, sollten aber nicht über DirectInput verarbeitet werden. Sie müssen ermitteln, welche Ihrer DirectInput-Geräte Legacygeräte und welche XInput-Geräte sind, und sie aus der Enumeration der DirectInput-Geräte entfernen.

Fügen Sie hierzu diesen Code in den DirectInput-Enumerationsrückruf ein:

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
        }
    }

LCleanup:
    VariantClear(&var);
    
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> Eine etwas verbesserte Version dieses Codes finden Sie im älteren [DirectInput-Beispiel FürSt.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)

## <a name="related-topics"></a>Zugehörige Themen

[Erste Schritte mit XInput](getting-started-with-xinput.md)

[Programmierverzeichnis](programming-reference.md)
