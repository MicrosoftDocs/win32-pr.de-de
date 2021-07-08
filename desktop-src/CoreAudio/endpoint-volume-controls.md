---
description: Steuerelemente für Endpunktvolumen
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Steuerelemente für Endpunktvolumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481885"
---
# <a name="endpoint-volume-controls"></a>Steuerelemente für Endpunktvolumen

Mit den [**Schnittstellen ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) können Clients die Lautstärkeebenen von Audiositzungen [steuern,](audio-sessions.md)bei denen es sich um Sammlungen von Audiostreams im freigegebenen Modus handelt. Diese Schnittstellen funktionieren nicht mit Audiostreams im exklusiven Modus.

Anwendungen, die Streams im exklusiven Modus verwalten, können die Volumeebenen dieser Streams über die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) steuern. Diese Schnittstelle steuert die Lautstärke des [Audioendpunktgeräts.](audio-endpoint-devices.md) Sie verwendet die Hardware-Volumesteuerung für das Endpunktgerät, wenn die Audiohardware ein solches Steuerelement implementiert. Andernfalls implementiert **die IAudioEndpointVolume-Schnittstelle** die Volumesteuerung in der Software.

Wenn ein Gerät über ein Hardwarevolume-Steuerelement verfügt, wirken sich Änderungen, die über die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) am Steuerelement vorgenommen werden, sowohl im gemeinsam genutzten als auch im exklusiven Modus auf die Volumeebene aus. Wenn auf einem Gerät kein Hardwarevolumen und stummgeschaltete Steuerelemente verfügbar sind, wirken sich Änderungen am Softwarevolumen und stummgeschalteten Steuerelementen über diese Schnittstelle auf die Volumeebene im gemeinsam genutzten Modus aus, jedoch nicht im exklusiven Modus. Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus und umgehen dabei die Softwaresteuerelemente.

Im Allgemeinen sollten Anwendungen vermeiden, die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) zu verwenden, um die Volumeebenen von Streams im freigegebenen Modus zu steuern. Stattdessen sollten Anwendungen zu diesem Zweck die [**Schnittstelle ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)oder [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) verwenden.

Wenn eine Anwendung ein Volumesteuerprogramm anzeigt, das die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) verwendet, um die Lautstärke eines Audioendpunktgeräts zu steuern, sollte dieses Volumesteuerprogramm das vom Systemvolumesteuerungsprogramm Sndvol angezeigte Steuerelement des Endpunktvolumes spiegeln. Wie bereits erläutert, wird das Steuerelement für das Endpunktvolume auf der linken Seite des Fensters Sndvol im Gruppenfeld Mit der Bezeichnung **Gerät angezeigt.** Wenn der Benutzer das Endpunktvolume eines Geräts über die Volumesteuerung in Sndvol ändert, sollte die entsprechende Steuerung des Endpunktvolumes in der Anwendung zusammen mit dem Steuerelement in Sndvol übertragen werden. Wenn der Benutzer die Volumeebene über das Endpunktvolume-Steuerelement im Anwendungsfenster ändert, sollte die entsprechende Volumesteuerung in Sndvol zusammen mit der Volumesteuerung der Anwendung bewegt werden.

Um sicherzustellen, dass das Endpunktvolume-Steuerelement in einem Anwendungsfenster das Endpunktvolume-Steuerelement in Sndvol spiegelt, muss die Anwendung eine [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) implementieren und diese Schnittstelle für den Empfang von Benachrichtigungen registrieren. Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Endpunktvolumeebene in Sndvol ändert, einen Benachrichtigungsaufruf über die [**IAudioEndpointVolumeCallback::OnNotify-Methode.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) Während dieses Aufrufs kann die **OnNotify-Methode** das Endpunktvolume-Steuerelement im Anwendungsfenster aktualisieren, damit es mit der in Sndvol angezeigten Steuerelementeinstellung übereinstimmen kann. Ebenso empfängt Sndvol jedes Mal, wenn der Benutzer die Endpunktvolumeebene über die Volumesteuerung im Anwendungsfenster ändert, eine Benachrichtigung und aktualisiert sofort das Endpunktvolume-Steuerelement, um die neue Volumeebene anzuzeigen.

Das folgende Codebeispiel ist eine Headerdatei, die eine mögliche Implementierung der [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) zeigt:


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



Die CAudioEndpointVolumeCallback-Klasse im vorherigen Codebeispiel ist eine Implementierung der [**IAudioEndpointVolumeCallback-Schnittstelle.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) Da **IAudioEndpointVolumeCallback** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown-Methoden** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der Klassendefinition wird jedes Mal aufgerufen, wenn eine der folgenden Methoden die Endpunktvolumenebene ändert:

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

Die Implementierung der [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) im vorherigen Codebeispiel sendet Nachrichten an das Volumesteuersystem im Anwendungsfenster, um die angezeigte Volumeebene zu aktualisieren.

Eine Anwendung ruft die [**IAudioEndpointVolume::RegisterControlChangeNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) für den Empfang von Benachrichtigungen zu registrieren. Wenn die Anwendung keine Benachrichtigungen mehr benötigt, ruft sie die [**IAudioEndpointVolume::UnregisterControlChangeNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) auf, um die Registrierung zu löschen.

Das folgende Codebeispiel ist eine Windows-Anwendung, die die [**Methoden RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) und [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) aufruft, um die CAudioEndpointVolumeCallback-Klasse im vorherigen Codebeispiel zu registrieren und deren Registrierung zu aufheben:


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (g_pEndptVol != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



Im vorherigen Codebeispiel ruft die [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine Instanz der [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) zu erstellen, und ruft die [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Standardrenderinggeräts zu erhalten. **WinMain** ruft die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) auf, um die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) des Geräts zu erhalten, und [**ruft RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die Anwendung zum Empfangen von Benachrichtigungen über Änderungen des Endpunktvolumes zu registrieren. Als Nächstes **öffnet WinMain** ein Dialogfeld, in dem ein Endpunkt-Volumesteuerfeld für das Gerät angezeigt wird. Im Dialogfeld wird auch ein Kontrollkästchen angezeigt, das angibt, ob das Gerät stummgeschaltet ist. Das Kontrollkästchen Steuerelement für Endpunktvolume und Stummschaltung im Dialogfeld spiegelt die Einstellungen des Endpunktvolume-Steuerelements und des Kontrollkästchens Stummschalten wieder, das von Sndvol angezeigt wird. Weitere Informationen zu **WinMain** und **CoCreateInstance** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu **IMMDeviceEnumerator** und **IMMDevice finden** Sie unter [Aufzählen von Audiogeräten.](enumerating-audio-devices.md)

Die Dialogfeldprozedur DlgProc im vorherigen Codebeispiel verarbeitet die Änderungen, die der Benutzer am Volume vorn vorgenommen hat, und stummschalten die Einstellungen über die Steuerelemente im Dialogfeld. Wenn DlgProc [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) oder [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)aufruft, empfängt Sndvol eine Benachrichtigung über die Änderung und aktualisiert das entsprechende Steuerelement in seinem Fenster, um das neue Volume oder die Stummschaltungseinstellung widerzuanzeigen. Wenn der Benutzer anstelle des Dialogfelds das Volume aktualisiert und die Einstellungen über die Steuerelemente im Sndvol-Fenster stummschaltt, aktualisiert die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der CAudioEndpointVolumeCallback-Klasse die Steuerelemente im Dialogfeld, um die neuen Einstellungen anzuzeigen.

Wenn der Benutzer das Volume über die Steuerelemente im Dialogfeld ändert, sendet die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der CAudioEndpointVolumeCallback-Klasse keine Meldungen zum Aktualisieren der Steuerelemente im Dialogfeld. Dies wäre redundant. **OnNotify** aktualisiert die Steuerelemente im Dialogfeld nur, wenn die Volumeänderung aus Sndvol oder einer anderen Anwendung stammt. Der zweite Parameter in den [**Methodenaufrufen SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) und [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) in der DlgProc-Funktion ist ein Zeiger auf eine Ereigniskontext-GUID, die beide Methoden an **OnNotify** übergeben. **OnNotify überprüft** den Wert der Ereigniskontext-GUID, um zu bestimmen, ob das Dialogfeld die Quelle der Volumeänderung ist. Weitere Informationen zu Ereigniskontext-GUIDs finden Sie unter **IAudioEndpointVolumeCallback::OnNotify**.

Wenn der Benutzer das Dialogfeld beendet, löscht der [**UnregisterControlChangeNotify-Aufruf**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) im vorherigen Codebeispiel die Registrierung der CAudioEndpointVolumeCallback-Klasse, bevor das Programm beendet wird.

Sie können das vorherige Codebeispiel problemlos ändern, um Lautstärke- und Stummschaltelemente für das Standarderfassungsgerät anzuzeigen. Ändern Sie in der [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) den Wert des ersten Parameters im Aufruf der [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) von eRender in eCapture.

Das folgende Codebeispiel ist das Ressourcenskript, das das Volume und stummgeschaltete Steuerelemente definiert, die im vorherigen Codebeispiel angezeigt werden:


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



Das folgende Codebeispiel ist die Ressourcenheaderdatei, die die Steuerelementbezeichner definiert, die in den obigen Codebeispielen angezeigt werden:


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Die obigen Codebeispiele bilden eine einfache Anwendung zum Steuern und Überwachen des Endpunktvolumens des Standardrenderinggeräts. Eine nützlichere Anwendung kann den Benutzer darüber hinaus benachrichtigen, wenn sich der Status des Geräts ändert. Beispielsweise kann das Gerät deaktiviert, nicht angeschlossen oder entfernt werden. Weitere Informationen zum Überwachen dieser Ereignistypen finden Sie unter [Geräteereignisse.](device-events.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 
