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
# <a name="xinput-and-directinput"></a><span data-ttu-id="90252-103">XInput und DirectInput</span><span class="sxs-lookup"><span data-stu-id="90252-103">XInput and DirectInput</span></span>

<span data-ttu-id="90252-104">XInput ist eine API, mit der Anwendungen Eingaben vom Xbox Controller für die Windows.</span><span class="sxs-lookup"><span data-stu-id="90252-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="90252-105">In diesem Dokument werden die Unterschiede zwischen XInput- und [DirectInput-Implementierungen](/previous-versions/windows/desktop/ee416842(v=vs.85)) des Xbox-Controllers beschrieben und wie Sie XInput-Geräte und ältere DirectInput-Geräte gleichzeitig unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="90252-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="90252-106">Die Verwendung von [Legacy-DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) wird nicht empfohlen, und DirectInput ist für Windows Store verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90252-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="90252-107">Der neue Standard: XInput</span><span class="sxs-lookup"><span data-stu-id="90252-107">The New Standard: XInput</span></span>

<span data-ttu-id="90252-108">XInput ist jetzt für die Spieleentwicklung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90252-108">XInput is now available for game development.</span></span> <span data-ttu-id="90252-109">Dies ist der neue Eingabestandard für xbox und Windows.</span><span class="sxs-lookup"><span data-stu-id="90252-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="90252-110">Die APIs sind über das DirectX SDK verfügbar, und der Treiber ist über das Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90252-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="90252-111">Die Verwendung von XInput gegenüber [DirectInput hat mehrere Vorteile:](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90252-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="90252-112">XInput ist einfacher zu verwenden und erfordert weniger Setup als [DirectInput.](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90252-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="90252-113">Bei der Xbox- Windows-Programmierung werden die gleichen Sätze von Kern-APIs verwendet, sodass die Programmierung die plattformübergreifende Übersetzung erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="90252-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="90252-114">Es wird eine große installierte Basis von Xbox-Controllern geben.</span><span class="sxs-lookup"><span data-stu-id="90252-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="90252-115">XInput-Geräte (d. h. Xbox-Controller) verfügen nur über Vibrationsfunktionen, wenn XInput-APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90252-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="90252-116">Zukünftige Controller, die für die Xbox-Konsole veröffentlicht werden (d. h. Rädchen), funktionieren auch auf Windows</span><span class="sxs-lookup"><span data-stu-id="90252-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="90252-117">Verwenden des Xbox-Controllers mit DirectInput</span><span class="sxs-lookup"><span data-stu-id="90252-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="90252-118">Der Xbox Controller wird ordnungsgemäß auf [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))aufzählt und kann mit den DirectInputAPIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90252-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="90252-119">Einige von XInput bereitgestellte Funktionen fehlen jedoch in der DirectInput-Implementierung:</span><span class="sxs-lookup"><span data-stu-id="90252-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="90252-120">Die linken und rechten Triggerschaltflächen fungieren als einzelne Schaltfläche, nicht unabhängig voneinander.</span><span class="sxs-lookup"><span data-stu-id="90252-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="90252-121">Die Vibrationseffekte sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90252-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="90252-122">Abfragen für Headsetgeräte sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="90252-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="90252-123">Die Kombination der linken und rechten Trigger in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ist standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="90252-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="90252-124">Spiele gehen immer davon aus, dass DirectInput-Geräteachsen zentriert sind, wenn keine Benutzerinteraktion mit dem Gerät besteht.</span><span class="sxs-lookup"><span data-stu-id="90252-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="90252-125">Der Xbox-Controller wurde jedoch so entworfen, dass er den Mindestwert registriert, nicht den Mittelpunkt, wenn die Trigger nicht gehalten werden.</span><span class="sxs-lookup"><span data-stu-id="90252-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="90252-126">Bei älteren Spielen wird daher eine Benutzerinteraktion angenommen.</span><span class="sxs-lookup"><span data-stu-id="90252-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="90252-127">Die Lösung war das Kombinieren der Trigger, das Festlegen eines Triggers auf eine positive und der andere auf eine negative Richtung, sodass keine Benutzerinteraktion darauf hindeuten [kann, dass DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) das "Steuerelement" in der Mitte befindet.</span><span class="sxs-lookup"><span data-stu-id="90252-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="90252-128">Um die Triggerwerte separat zu testen, müssen Sie XInput verwenden.</span><span class="sxs-lookup"><span data-stu-id="90252-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="90252-129">XInput und DirectInput nebeneinander</span><span class="sxs-lookup"><span data-stu-id="90252-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="90252-130">Durch die ausschließliche Unterstützung von XInput funktioniert Ihr Spiel nicht mit [älteren DirectInput-Geräten.](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90252-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="90252-131">XInput erkennt diese Geräte nicht.</span><span class="sxs-lookup"><span data-stu-id="90252-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="90252-132">Wenn Ihr Spiel ältere [DirectInput-Geräte](/previous-versions/windows/desktop/ee416842(v=vs.85)) unterstützen soll, können Sie DirectInput und XInput nebeneinander verwenden.</span><span class="sxs-lookup"><span data-stu-id="90252-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="90252-133">Beim Aufzählen Ihrer DirectInput-Geräte werden alle DirectInput-Geräte ordnungsgemäß aufzählt.</span><span class="sxs-lookup"><span data-stu-id="90252-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="90252-134">Alle XInput-Geräte werden sowohl als XInput- als auch als DirectInput-Geräte gezeigt, sollten aber nicht über DirectInput verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="90252-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="90252-135">Sie müssen ermitteln, welche Ihrer DirectInput-Geräte Legacygeräte und welche XInput-Geräte sind, und sie aus der Enumeration der DirectInput-Geräte entfernen.</span><span class="sxs-lookup"><span data-stu-id="90252-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="90252-136">Fügen Sie hierzu diesen Code in den DirectInput-Enumerationsrückruf ein:</span><span class="sxs-lookup"><span data-stu-id="90252-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

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

> <span data-ttu-id="90252-137">Eine etwas verbesserte Version dieses Codes finden Sie im älteren [DirectInput-Beispiel FürSt.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)</span><span class="sxs-lookup"><span data-stu-id="90252-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90252-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90252-138">Related topics</span></span>

[<span data-ttu-id="90252-139">Erste Schritte mit XInput</span><span class="sxs-lookup"><span data-stu-id="90252-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="90252-140">Programmierverzeichnis</span><span class="sxs-lookup"><span data-stu-id="90252-140">Programming Reference</span></span>](programming-reference.md)
