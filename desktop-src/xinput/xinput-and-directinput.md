---
title: XInput und DirectInput
description: Xinput ist eine API, mit der Anwendungen Eingaben vom Xbox-Controller für Windows empfangen können.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/29/2020
ms.locfileid: "103730704"
---
# <a name="xinput-and-directinput"></a>XInput und DirectInput

Xinput ist eine API, mit der Anwendungen Eingaben vom Xbox-Controller für Windows empfangen können. In diesem Dokument werden die Unterschiede zwischen XInput-und [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) -Implementierungen des Xbox-Controllers beschrieben, und es wird erläutert, wie Sie xinput-Geräte und ältere DirectInput-Geräte gleichzeitig unterstützen können.

> [!Note]  
> Die Verwendung von Legacy- [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ist nicht empfehlenswert, und DirectInput ist für Windows Store-Apps nicht verfügbar.

## <a name="the-new-standard-xinput"></a>Der neue Standard: xinput

Xinput ist jetzt für die Spieleentwicklung verfügbar. Dies ist der neue Eingabe Standard für die Xbox und Windows. Die APIs sind über das DirectX SDK verfügbar, und der Treiber ist über Windows Update verfügbar.

Die Verwendung von xinput über [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))bietet mehrere Vorteile:

-   Xinput ist einfacher zu verwenden und erfordert weniger Setup als [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   Sowohl die Xbox-als auch die Windows-Programmierung verwenden die gleichen Sätze von Kern-APIs, sodass die Programmierung die plattformübergreifende Übersetzung vereinfachen kann.
-   Es gibt eine große installierte Basis von Xbox-Controllern.
-   Xinput-Geräte (d. h. die Xbox-Controller) verfügen nur bei Verwendung von xinput-APIs über eine Vibrations Funktionalität.
-   Zukünftige Controller, die für die Xbox-Konsole (d. h. Steuerungs Räder) freigegeben werden, funktionieren auch unter Windows.

### <a name="using-the-xbox-controller-with-directinput"></a>Verwenden des Xbox-Controllers mit DirectInput

Der Xbox-Controller ist in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))ordnungsgemäß aufgelistet und kann mit den directinputapis verwendet werden. In der DirectInput-Implementierung fehlen jedoch einige Funktionen, die von xinput bereitgestellt werden:

-   Die Schaltflächen Linker und rechter Auslösung fungieren als einzelne Schaltfläche, nicht unabhängig
-   Die Vibrationseffekte sind nicht verfügbar.
-   Das Abfragen von Headset-Geräten ist nicht verfügbar.

Die Kombination aus dem linken und rechten Trigger in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) ist Entwurfs bedingt. Spiele haben immer angenommen, dass DirectInput-Geräte Achsen zentriert werden, wenn keine Benutzerinteraktion mit dem Gerät vorhanden ist. Der Xbox-Controller wurde jedoch so konzipiert, dass der minimale Wert registriert wird, nicht Center, wenn die Trigger nicht gespeichert werden. Ältere Spiele nehmen daher eine Benutzerinteraktion an.

Die Lösung bestand darin, die Trigger zu kombinieren und einen Trigger auf eine positive Richtung und die andere auf eine negative Richtung festzulegen, sodass keine Benutzer [Interaktion darauf hinweist, dass](/previous-versions/windows/desktop/ee416842(v=vs.85)) das Steuerelement in der Mitte ist.

Um die auslöserwerte separat zu testen, müssen Sie xinput verwenden.

## <a name="xinput-and-directinput-side-by-side"></a>XInput und DirectInput nebeneinander

Wenn nur xinput unterstützt wird, funktioniert Ihr Spiel nicht mit älteren [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) -Geräten. Diese Geräte werden von xinput nicht erkannt.

Wenn Sie möchten, dass Ihr Spiel ältere [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) -Geräte unterstützt, können Sie DirectInput und xinput nebeneinander verwenden. Wenn Sie Ihre DirectInput-Geräte aufzählen, werden alle DirectInput-Geräte ordnungsgemäß aufgelistet. Alle xinput-Geräte werden als XInput-und DirectInput-Geräte angezeigt, Sie sollten jedoch nicht über DirectInput behandelt werden. Sie müssen bestimmen, welche ihrer DirectInput-Geräte Legacy Geräte sind und welche xinput-Geräte sind, und Sie aus der Enumeration von DirectInput-Geräten entfernen.

Fügen Sie zu diesem Zweck den folgenden Code in ihren DirectInput-enumerationsrückruf ein:

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
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
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
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
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a>Zugehörige Themen

[Einstieg in xinput](getting-started-with-xinput.md)

[Programmierverzeichnis](programming-reference.md)
