---
description: Spitzen Zähler
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Spitzen Zähler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127093"
---
# <a name="peak-meters"></a>Spitzen Zähler

Zur Unterstützung von Windows-Anwendungen, in denen Spitzen Zähler angezeigt werden, enthält die [endpointvolume-API](endpointvolume-api.md) eine [**iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) -Schnittstelle. Diese Schnittstelle stellt einen Spitzen Zähler auf einem [audioendpunktgerät](audio-endpoint-devices.md)dar. Bei einem renderinggerät stellt der Wert, der von der Spitzen Messung abgerufen wird, den maximalen Stichproben Wert dar, der im Ausgabestream des Geräts während des vorangegangenen Messungs Zeitraums gefunden wurde. Bei einem Erfassungsgerät stellt der Wert, der von der Spitzen Messung abgerufen wurde, den maximalen Stichproben Wert dar, der im Eingabestream vom Gerät gefunden wurde.

Bei den Spitzenwert Werten, die von den Methoden in der [**iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) -Schnittstelle abgerufen werden, handelt es sich um Gleit Komma Zahlen im normalisierten Bereich von 0,0 bis 1,0. Wenn z. b. ein PCM mit 16-Bit-Stichproben und der Höchstwert für einen bestimmten Messungs Zeitraum – 8914 ist, dann ist der absolute Wert, der von der Spitzen Messung aufgezeichnet wird, 8914, und der normalisierte Spitzenwert, der von der **iaudiometerinformation** -Schnittstelle gemeldet wird, ist 8914/32768 = 0,272.

Wenn das audioendpunktgerät die Spitzen Meter in Hardware implementiert, verwendet die [**iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) -Schnittstelle die Hardware Spitzen Meter. Andernfalls implementiert die-Schnittstelle die Spitzen Meter in Software.

Wenn ein Gerät über einen Hardware Spitzen Zähler verfügt, ist die Spitzen Messgröße sowohl im gemeinsam genutzten als auch im exklusiven Modus aktiv. Wenn auf einem Gerät keine Hardware Spitzen gemessen werden, ist die Spitzen Verbrauchseinheit im Modus freigegeben, aber nicht im exklusiven Modus aktiv. Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus, wobei der Software-Spitzen Zähler umgangen wird (der stets einen Spitzenwert von 0,0 meldet).

Das folgende C++-Codebeispiel ist eine Windows-Anwendung, die eine Spitzen Meter für das standardmäßige renderinggerät anzeigt:


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



Im vorangehenden Codebeispiel ruft die [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion die [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um eine Instanz der [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle zu erstellen, und ruft die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode auf, um die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des standardrenderinggeräts abzurufen. **WinMain** Ruft die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode auf, um die [**iaudiometerinformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) -Schnittstelle des Geräts zu erhalten, und öffnet ein Dialogfeld, in dem eine Spitzen Meter für das Gerät angezeigt wird. Weitere Informationen zu **WinMain** und **cokreateinstance** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu " **immdeviceenumerator** " und " **immdevice**" finden Sie unter Auflisten von [Audiogeräten](enumerating-audio-devices.md).

Im vorangehenden Codebeispiel zeigt die DlgProc-Funktion den Spitzen Zähler im Dialogfeld an. Bei der Verarbeitung der WM- \_ InitDialog-Nachricht ruft DlgProc die [**SETTIMER**](/windows/win32/api/winuser/nf-winuser-settimer) -Funktion auf, um einen Timer einzurichten, der \_ in regelmäßigen Abständen WM-Zeit Geber Nachrichten generiert. Wenn DlgProc eine WM-Zeit Geber \_ Nachricht empfängt, ruft er [**iaudiometerinformation:: getPeer Value**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) auf, um das neueste Lese-/ausgabelesevorgang für den Datenstrom abzurufen. DlgProc ruft dann die drawpeer Meter-Funktion auf, um die aktualisierte Spitzen Meter im Dialogfeld zu zeichnen. Weitere Informationen zu den **tittimer** -und WM-und WM-Zeit Geber \_ \_ Meldungen finden Sie in der Windows SDK-Dokumentation.

Sie können das vorangehende Codebeispiel leicht ändern, um eine Spitzen Meter für das Standard Erfassungsgerät anzuzeigen. Ändern Sie in der [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) -Funktion den Wert des ersten Parameters im-Befehl von " [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) " von "-" in "ecapture".

Das folgende Codebeispiel ist das Ressourcen Skript, das die Steuerelemente definiert, die im vorangehenden Codebeispiel angezeigt werden:


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



Das folgende Codebeispiel zeigt die Ressourcen Header Datei, die die Steuerelement Bezeichner definiert, die in den vorangehenden Codebeispielen angezeigt werden:


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

 

 
