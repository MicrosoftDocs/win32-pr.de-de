---
description: Spitzenzähler
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Spitzenzähler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e04a15ddd2e5fd91cf60845f2a939715e7a4a992f36aea3b9129e69c30d05961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077504"
---
# <a name="peak-meters"></a>Spitzenzähler

Zur Unterstützung Windows Anwendungen, die Spitzenzähler anzeigen, enthält die [EndpointVolume-API](endpointvolume-api.md) eine [**IAudioMeterInformation-Schnittstelle.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) Diese Schnittstelle stellt eine Spitzenmessung auf einem [Audioendpunktgerät dar.](audio-endpoint-devices.md) Bei einem Renderinggerät stellt der von der Spitzenmessung abgerufene Wert den maximalen Stichprobenwert dar, der während des vorherigen Messzeitraums im Ausgabestream an das Gerät gefunden wurde. Bei einem Erfassungsgerät stellt der von der Spitzenmessung abgerufene Wert den maximalen Stichprobenwert dar, der im Eingabestream des Geräts gefunden wurde.

Die Spitzenmessungswerte, die von den Methoden in der [**IAudioMeterInformation-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) ermittelt werden, sind Gleitkommazahlen im normalisierten Bereich von 0,0 bis 1,0. Wenn ein PCM-Datenstrom beispielsweise 16-Bit-Stichproben enthält und der Spitzenwert für die Stichprobenentnahme während eines bestimmten Messzeitraums –8914 ist, ist der absolute Wert, der von der Spitzenmessung aufgezeichnet wird, 8914, und der von der **IAudioMeterInformation-Schnittstelle** gemeldete normalisierte Spitzenwert ist 8914/32768 = 0,272.

Wenn das Audioendpunktgerät die Spitzenmessung in der Hardware implementiert, verwendet die [**Schnittstelle IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) die Hardwarespitzenmessung. Andernfalls implementiert die Schnittstelle die Spitzenmessung in der Software.

Wenn ein Gerät über eine Hardwarespitzenmessung verfügt, ist die Spitzenmessung sowohl im gemeinsam genutzten als auch im exklusiven Modus aktiv. Wenn ein Gerät keine Hardwarespitzenmessung hat, ist die Spitzenmessung im modus shared aktiv, aber nicht im exklusiven Modus. Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus und umgehen dabei die Softwarespitzenmessung (die immer einen Spitzenwert von 0,0 meldet).

Das folgende C++-Codebeispiel ist eine Windows-Anwendung, die eine Spitzenmessung für das Standardrenderinggerät anzeigt:


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



Im vorherigen Codebeispiel ruft die [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine Instanz der [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) zu erstellen, und ruft die [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Standardrenderinggeräts zu erhalten. **WinMain** ruft die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) auf, um die [**IAudioMeterInformation-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) des Geräts zu erhalten, und öffnet ein Dialogfeld, in dem eine Spitzenmessung für das Gerät angezeigt wird. Weitere Informationen zu **WinMain** und **CoCreateInstance** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu **IMMDeviceEnumerator** und **IMMDevice finden** Sie unter [Aufzählen von Audiogeräten.](enumerating-audio-devices.md)

Im obigen Codebeispiel zeigt die DlgProc-Funktion die Spitzenmessung im Dialogfeld an. Während der Verarbeitung der WM \_ INITDIALOG-Nachricht ruft DlgProc die [**SetTimer-Funktion**](/windows/win32/api/winuser/nf-winuser-settimer) auf, um einen Timer zu einrichten, der in regelmäßigen Zeitintervallen WM \_ TIMER-Nachrichten generiert. Wenn DlgProc eine WM TIMER-Nachricht empfängt, ruft sie \_ [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) auf, um den letzten Messwert der Spitzenmessung für den Stream zu erhalten. DlgProc ruft dann die DrawPeakMeter-Funktion auf, um die aktualisierte Spitzenmessung im Dialogfeld zu zeichnen. Weitere Informationen zu **SetTimer und** den WM INITDIALOG- und WM TIMER-Meldungen finden Sie in der Windows \_ \_ SDK-Dokumentation.

Sie können das vorherige Codebeispiel problemlos ändern, um eine Spitzenmessung für das Standarderfassungsgerät anzuzeigen. Ändern Sie in der [**WinMain-Funktion**](/windows/win32/api/winbase/nf-winbase-winmain) den Wert des ersten Parameters im Aufruf von [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) von eRender in eCapture.

Das folgende Codebeispiel ist das Ressourcenskript, das die Steuerelemente definiert, die im vorherigen Codebeispiel angezeigt werden:


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



Das folgende Codebeispiel ist die Ressourcenheaderdatei, die die Steuerelementbezeichner definiert, die in den obigen Codebeispielen angezeigt werden:


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 
