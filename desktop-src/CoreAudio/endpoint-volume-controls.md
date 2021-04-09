---
description: Steuerelemente für Endpunkt-
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Steuerelemente für Endpunkt-
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958428"
---
# <a name="endpoint-volume-controls"></a>Steuerelemente für Endpunkt-

Mit den Schnittstellen [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) können Clients die volumeebenen von [audiositzungen](audio-sessions.md)steuern, bei denen es sich um Sammlungen von Audiodatenströmen im freigegebenen Modus handelt. Diese Schnittstellen können nicht mit exklusiven Audiodatenströmen verwendet werden.

Anwendungen, die Streams im exklusiven Modus verwalten, können die volumeebenen dieser Streams über die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle steuern. Diese Schnittstelle steuert die Volumeebene des [audioendpunktgeräts](audio-endpoint-devices.md). Er verwendet das Hardware Volume-Steuerelement für das Endpunkt Gerät, wenn die Audiohardware ein solches Steuerelement implementiert. Andernfalls implementiert die **iaudioendpointvolume** -Schnittstelle das Volume-Steuerelement in Software.

Wenn ein Gerät über ein Hardware Volume-Steuerelement verfügt, wirken sich die Änderungen am Steuerelement über die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle auf die Volumeebene im gemeinsam genutzten Modus und im exklusiven Modus aus. Wenn ein Gerät nicht über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Software Volume und stumm Steuerelemente über diese Schnittstelle auf die Volumeebene im freigegebenen Modus, jedoch nicht im exklusiven Modus aus. Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus, wobei die Software Steuerelemente umgangen werden.

Als allgemeine Regel sollten Anwendungen die Verwendung der [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle vermeiden, um die volumeebenen von Datenströmen im freigegebenen Modus zu steuern. Stattdessen sollten Anwendungen die Schnittstelle [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)oder [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zu diesem Zweck verwenden.

Wenn eine Anwendung ein Volume-Steuerelement anzeigt, das die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle verwendet, um die Volumeebene eines audioendpunktgeräts zu steuern, sollte dieses volumesteuerelement das von dem System Volume-Control-Programm (sndvol) angezeigte Endpunkt-volumesteuerelement Wie bereits erläutert, wird das Steuerelement für das Endpunkt Volume auf der linken Seite des sndvol-Fensters im Gruppenfeld mit der Bezeichnung **Gerät** angezeigt. Wenn der Benutzer das Endpunkt Volume eines Geräts über das volumesteuerelement in sndvol ändert, sollte das entsprechende Endpunkt-volumensteuerelement in der Anwendung in gemeinsamen mit dem-Steuerelement in sndvol verschoben werden. Wenn der Benutzer die Volumeebene über das Steuerelement "Endpunkt Volume" im Anwendungsfenster ändert, sollte das entsprechende volumensteuerelement in sndvol in gemeinsamen mit der volumesteuerung der Anwendung verschoben werden.

Um sicherzustellen, dass das Endpoint Volume-Steuerelement in einem Anwendungsfenster das Endpoint Volume-Steuerelement in sndvol widerspiegelt, sollte die Anwendung eine [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle implementieren und diese Schnittstelle für den Empfang von Benachrichtigungen registrieren. Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Endpunkt Volume-Ebene in sndvol ändert, einen Benachrichtigungs Aufruf über die [**iaudioendpointvolumecallback:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode. Während dieses Aufrufes kann die **OnNotify** -Methode das Endpoint Volume-Steuerelement im Anwendungsfenster aktualisieren, sodass es der in sndvol gezeigten Steuerelement Einstellung entspricht. Ebenso erhält sndvol jedes Mal, wenn der Benutzer die Ebene des endpunktvolumes durch die volumesteuerung im Anwendungsfenster ändert, eine Benachrichtigung und aktualisiert sofort das Steuerelement für den Endpunkt Volume, um die neue Volumeebene anzuzeigen.

Das folgende Codebeispiel ist eine Header Datei, die eine mögliche Implementierung der [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle anzeigt:


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



Die caudioendpointvolumecallback-Klasse im vorangehenden Codebeispiel ist eine Implementierung der [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle. Da **iaudioendpointvolumecallback** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der Klassendefinition wird jedes Mal aufgerufen, wenn eine der folgenden Methoden die Ebene des Endpunkt Volumens ändert:

-   [**Iaudioendpointvolume:: setchannelvolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**Iaudioendpointvolume:: setchannelvolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**Iaudioendpointvolume:: setmastervolumelevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**Iaudioendpointvolume:: setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**Iaudioendpointvolume:: setstumm**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**Iaudioendpointvolume:: volumestepdown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**Iaudioendpointvolume:: volumestepup**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

Die Implementierung der [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode im vorangehenden Codebeispiel sendet Nachrichten an das volumesteuerelement im Anwendungsfenster, um die angezeigte Volumeebene zu aktualisieren.

Eine Anwendung ruft die [**iaudioendpointvolume:: registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) -Methode auf, um die [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle für den Empfang von Benachrichtigungen zu registrieren. Wenn für die Anwendung keine Benachrichtigungen mehr erforderlich sind, wird die [**iaudioendpointvolume:: unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) -Methode aufgerufen, um die Registrierung zu löschen.

Das folgende Codebeispiel ist eine Windows-Anwendung, die die Methoden [**registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) und [**unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) aufruft, um die caudioendpointvolumecallback-Klasse im vorangehenden Codebeispiel zu registrieren und die Registrierung aufzuheben:


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
    if (pEnumerator != NULL)
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



Im vorangehenden Codebeispiel ruft die [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um eine Instanz der [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle zu erstellen, und ruft die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode auf, um die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des standardrenderinggeräts abzurufen. **WinMain** Ruft die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode auf, um die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle des Geräts abzurufen, und ruft [**registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die Anwendung für den Empfang von Benachrichtigungen über Änderungen am Endpunkt Volume zu registrieren. Als nächstes öffnet **WinMain** ein Dialogfeld, in dem ein Endpunkt-volumesteuerelement für das Gerät angezeigt wird. Im Dialogfeld wird auch ein Kontrollkästchen angezeigt, das angibt, ob das Gerät stumm geschaltet wird. Mithilfe des Kontrollkästchens Steuerung und stumm Schaltung des Endpunkts im Dialogfeld werden die Einstellungen des Kontrollkästchens Endpunkt-volumesteuerung und stumm Schaltung von sndvol angezeigt. Weitere Informationen zu **WinMain** und **cokreateinstance** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zu " **immdeviceenumerator** " und " **immdevice**" finden Sie unter Auflisten von [Audiogeräten](enumerating-audio-devices.md).

Mit der Dialogfeld Prozedur DlgProc im vorangehenden Codebeispiel werden die Änderungen behandelt, die der Benutzer am Volume vornimmt, und Einstellungen über die Steuerelemente im Dialogfeld stumm schalten. Wenn DlgProc [**setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) oder [**setstumm**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)aufruft, empfängt sndvol eine Benachrichtigung über die Änderung und aktualisiert das entsprechende Steuerelement in seinem Fenster, um die neue Lautstärke-oder stumm Einstellung widerzuspiegeln. Wenn der Benutzer anstelle des Dialog Felds das Volume aktualisiert und Einstellungen über die Steuerelemente im sndvol-Fenster stumm schalten, aktualisiert die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der caudioendpointvolumecallback-Klasse die Steuerelemente im Dialogfeld, um die neuen Einstellungen anzuzeigen.

Wenn der Benutzer das Volume über die Steuerelemente im Dialogfeld ändert, sendet die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der caudioendpointvolumecallback-Klasse keine Nachrichten, um die Steuerelemente im Dialogfeld zu aktualisieren. Dies wäre redundant. **OnNotify** aktualisiert die Steuerelemente im Dialogfeld nur dann, wenn die volumeänderung in sndvol oder einer anderen Anwendung entstanden ist. Der zweite Parameter in den [**setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) -und [**setstumm**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) -Methoden aufrufen in der DlgProc-Funktion ist ein Zeiger auf eine Ereignis Kontext-GUID, die von einer der beiden Methoden an **OnNotify** übergeben wird. **OnNotify** überprüft den Wert der Ereignis Kontext-GUID, um zu bestimmen, ob das Dialogfeld die Quelle der volumeänderung ist. Weitere Informationen zu Ereignis Kontext-GUIDs finden Sie unter **iaudioendpointvolumecallback:: OnNotify**.

Wenn der Benutzer das Dialogfeld verlässt, löscht der [**unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) -Befehl im vorangehenden Codebeispiel die Registrierung der caudioendpointvolumecallback-Klasse, bevor das Programm beendet wird.

Sie können das vorangehende Codebeispiel leicht ändern, um die Volume-und stumm Steuerelemente für das Standard Erfassungsgerät anzuzeigen. Ändern Sie in der [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion den Wert des ersten Parameters im-Befehl in die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode von "-" in "ecapture".

Das folgende Codebeispiel ist das Ressourcen Skript, das das Volume und die stumm Steuerelemente definiert, die im vorangehenden Codebeispiel angezeigt werden:


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



Das folgende Codebeispiel zeigt die Ressourcen Header Datei, die die Steuerelement Bezeichner definiert, die in den vorangehenden Codebeispielen angezeigt werden:


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Die vorangehenden Codebeispiele bilden eine einfache Anwendung zum Steuern und Überwachen des endpunktvolumes des standardrenderinggeräts. Eine nützlichere Anwendung kann den Benutzer darüber hinaus Benachrichtigen, wenn sich der Status des Geräts ändert. Beispielsweise kann das Gerät deaktiviert, getrennt oder entfernt werden. Weitere Informationen zum Überwachen dieser Ereignis Typen finden Sie unter [Geräte Ereignisse](device-events.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lautstärkeregler](volume-controls.md)
</dt> </dl>

 

 
