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
# <a name="endpoint-volume-controls"></a><span data-ttu-id="4fbed-103">Steuerelemente für Endpunkt-</span><span class="sxs-lookup"><span data-stu-id="4fbed-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="4fbed-104">Mit den Schnittstellen [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) können Clients die volumeebenen von [audiositzungen](audio-sessions.md)steuern, bei denen es sich um Sammlungen von Audiodatenströmen im freigegebenen Modus handelt.</span><span class="sxs-lookup"><span data-stu-id="4fbed-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="4fbed-105">Diese Schnittstellen können nicht mit exklusiven Audiodatenströmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="4fbed-106">Anwendungen, die Streams im exklusiven Modus verwalten, können die volumeebenen dieser Streams über die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle steuern.</span><span class="sxs-lookup"><span data-stu-id="4fbed-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="4fbed-107">Diese Schnittstelle steuert die Volumeebene des [audioendpunktgeräts](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="4fbed-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="4fbed-108">Er verwendet das Hardware Volume-Steuerelement für das Endpunkt Gerät, wenn die Audiohardware ein solches Steuerelement implementiert.</span><span class="sxs-lookup"><span data-stu-id="4fbed-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="4fbed-109">Andernfalls implementiert die **iaudioendpointvolume** -Schnittstelle das Volume-Steuerelement in Software.</span><span class="sxs-lookup"><span data-stu-id="4fbed-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="4fbed-110">Wenn ein Gerät über ein Hardware Volume-Steuerelement verfügt, wirken sich die Änderungen am Steuerelement über die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle auf die Volumeebene im gemeinsam genutzten Modus und im exklusiven Modus aus.</span><span class="sxs-lookup"><span data-stu-id="4fbed-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="4fbed-111">Wenn ein Gerät nicht über Hardware Volume und stumm Steuerelemente verfügt, wirken sich Änderungen am Software Volume und stumm Steuerelemente über diese Schnittstelle auf die Volumeebene im freigegebenen Modus, jedoch nicht im exklusiven Modus aus.</span><span class="sxs-lookup"><span data-stu-id="4fbed-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="4fbed-112">Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus, wobei die Software Steuerelemente umgangen werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="4fbed-113">Als allgemeine Regel sollten Anwendungen die Verwendung der [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle vermeiden, um die volumeebenen von Datenströmen im freigegebenen Modus zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4fbed-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="4fbed-114">Stattdessen sollten Anwendungen die Schnittstelle [**isimpleaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**ichannelaudiovolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)oder [**iaudiostreamvolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) zu diesem Zweck verwenden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="4fbed-115">Wenn eine Anwendung ein Volume-Steuerelement anzeigt, das die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle verwendet, um die Volumeebene eines audioendpunktgeräts zu steuern, sollte dieses volumesteuerelement das von dem System Volume-Control-Programm (sndvol) angezeigte Endpunkt-volumesteuerelement</span><span class="sxs-lookup"><span data-stu-id="4fbed-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="4fbed-116">Wie bereits erläutert, wird das Steuerelement für das Endpunkt Volume auf der linken Seite des sndvol-Fensters im Gruppenfeld mit der Bezeichnung **Gerät** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fbed-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="4fbed-117">Wenn der Benutzer das Endpunkt Volume eines Geräts über das volumesteuerelement in sndvol ändert, sollte das entsprechende Endpunkt-volumensteuerelement in der Anwendung in gemeinsamen mit dem-Steuerelement in sndvol verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="4fbed-118">Wenn der Benutzer die Volumeebene über das Steuerelement "Endpunkt Volume" im Anwendungsfenster ändert, sollte das entsprechende volumensteuerelement in sndvol in gemeinsamen mit der volumesteuerung der Anwendung verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="4fbed-119">Um sicherzustellen, dass das Endpoint Volume-Steuerelement in einem Anwendungsfenster das Endpoint Volume-Steuerelement in sndvol widerspiegelt, sollte die Anwendung eine [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle implementieren und diese Schnittstelle für den Empfang von Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="4fbed-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="4fbed-120">Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Endpunkt Volume-Ebene in sndvol ändert, einen Benachrichtigungs Aufruf über die [**iaudioendpointvolumecallback:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4fbed-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="4fbed-121">Während dieses Aufrufes kann die **OnNotify** -Methode das Endpoint Volume-Steuerelement im Anwendungsfenster aktualisieren, sodass es der in sndvol gezeigten Steuerelement Einstellung entspricht.</span><span class="sxs-lookup"><span data-stu-id="4fbed-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="4fbed-122">Ebenso erhält sndvol jedes Mal, wenn der Benutzer die Ebene des endpunktvolumes durch die volumesteuerung im Anwendungsfenster ändert, eine Benachrichtigung und aktualisiert sofort das Steuerelement für den Endpunkt Volume, um die neue Volumeebene anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="4fbed-123">Das folgende Codebeispiel ist eine Header Datei, die eine mögliche Implementierung der [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle anzeigt:</span><span class="sxs-lookup"><span data-stu-id="4fbed-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


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



<span data-ttu-id="4fbed-124">Die caudioendpointvolumecallback-Klasse im vorangehenden Codebeispiel ist eine Implementierung der [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4fbed-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="4fbed-125">Da **iaudioendpointvolumecallback** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown** -Methoden [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="4fbed-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="4fbed-126">Die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der Klassendefinition wird jedes Mal aufgerufen, wenn eine der folgenden Methoden die Ebene des Endpunkt Volumens ändert:</span><span class="sxs-lookup"><span data-stu-id="4fbed-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="4fbed-127">**Iaudioendpointvolume:: setchannelvolumelevel**</span><span class="sxs-lookup"><span data-stu-id="4fbed-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="4fbed-128">**Iaudioendpointvolume:: setchannelvolumelevelscalar**</span><span class="sxs-lookup"><span data-stu-id="4fbed-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="4fbed-129">**Iaudioendpointvolume:: setmastervolumelevel**</span><span class="sxs-lookup"><span data-stu-id="4fbed-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="4fbed-130">**Iaudioendpointvolume:: setmastervolumelevelscalar**</span><span class="sxs-lookup"><span data-stu-id="4fbed-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="4fbed-131">**Iaudioendpointvolume:: setstumm**</span><span class="sxs-lookup"><span data-stu-id="4fbed-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="4fbed-132">**Iaudioendpointvolume:: volumestepdown**</span><span class="sxs-lookup"><span data-stu-id="4fbed-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="4fbed-133">**Iaudioendpointvolume:: volumestepup**</span><span class="sxs-lookup"><span data-stu-id="4fbed-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="4fbed-134">Die Implementierung der [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode im vorangehenden Codebeispiel sendet Nachrichten an das volumesteuerelement im Anwendungsfenster, um die angezeigte Volumeebene zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4fbed-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="4fbed-135">Eine Anwendung ruft die [**iaudioendpointvolume:: registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) -Methode auf, um die [**iaudioendpointvolumecallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) -Schnittstelle für den Empfang von Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4fbed-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="4fbed-136">Wenn für die Anwendung keine Benachrichtigungen mehr erforderlich sind, wird die [**iaudioendpointvolume:: unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) -Methode aufgerufen, um die Registrierung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="4fbed-137">Das folgende Codebeispiel ist eine Windows-Anwendung, die die Methoden [**registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) und [**unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) aufruft, um die caudioendpointvolumecallback-Klasse im vorangehenden Codebeispiel zu registrieren und die Registrierung aufzuheben:</span><span class="sxs-lookup"><span data-stu-id="4fbed-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


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



<span data-ttu-id="4fbed-138">Im vorangehenden Codebeispiel ruft die [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion auf, um eine Instanz der [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle zu erstellen, und ruft die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode auf, um die [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle des standardrenderinggeräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="4fbed-139">**WinMain** Ruft die [**immdevice:: Aktivierungs**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) -Methode auf, um die [**iaudioendpointvolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) -Schnittstelle des Geräts abzurufen, und ruft [**registercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die Anwendung für den Empfang von Benachrichtigungen über Änderungen am Endpunkt Volume zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="4fbed-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="4fbed-140">Als nächstes öffnet **WinMain** ein Dialogfeld, in dem ein Endpunkt-volumesteuerelement für das Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fbed-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="4fbed-141">Im Dialogfeld wird auch ein Kontrollkästchen angezeigt, das angibt, ob das Gerät stumm geschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4fbed-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="4fbed-142">Mithilfe des Kontrollkästchens Steuerung und stumm Schaltung des Endpunkts im Dialogfeld werden die Einstellungen des Kontrollkästchens Endpunkt-volumesteuerung und stumm Schaltung von sndvol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fbed-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="4fbed-143">Weitere Informationen zu **WinMain** und **cokreateinstance** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="4fbed-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="4fbed-144">Weitere Informationen zu " **immdeviceenumerator** " und " **immdevice**" finden Sie unter Auflisten von [Audiogeräten](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="4fbed-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="4fbed-145">Mit der Dialogfeld Prozedur DlgProc im vorangehenden Codebeispiel werden die Änderungen behandelt, die der Benutzer am Volume vornimmt, und Einstellungen über die Steuerelemente im Dialogfeld stumm schalten.</span><span class="sxs-lookup"><span data-stu-id="4fbed-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="4fbed-146">Wenn DlgProc [**setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) oder [**setstumm**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)aufruft, empfängt sndvol eine Benachrichtigung über die Änderung und aktualisiert das entsprechende Steuerelement in seinem Fenster, um die neue Lautstärke-oder stumm Einstellung widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4fbed-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="4fbed-147">Wenn der Benutzer anstelle des Dialog Felds das Volume aktualisiert und Einstellungen über die Steuerelemente im sndvol-Fenster stumm schalten, aktualisiert die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der caudioendpointvolumecallback-Klasse die Steuerelemente im Dialogfeld, um die neuen Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="4fbed-148">Wenn der Benutzer das Volume über die Steuerelemente im Dialogfeld ändert, sendet die [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) -Methode in der caudioendpointvolumecallback-Klasse keine Nachrichten, um die Steuerelemente im Dialogfeld zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4fbed-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="4fbed-149">Dies wäre redundant.</span><span class="sxs-lookup"><span data-stu-id="4fbed-149">To do so would be redundant.</span></span> <span data-ttu-id="4fbed-150">**OnNotify** aktualisiert die Steuerelemente im Dialogfeld nur dann, wenn die volumeänderung in sndvol oder einer anderen Anwendung entstanden ist.</span><span class="sxs-lookup"><span data-stu-id="4fbed-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="4fbed-151">Der zweite Parameter in den [**setmastervolumelevelscalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) -und [**setstumm**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) -Methoden aufrufen in der DlgProc-Funktion ist ein Zeiger auf eine Ereignis Kontext-GUID, die von einer der beiden Methoden an **OnNotify** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fbed-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="4fbed-152">**OnNotify** überprüft den Wert der Ereignis Kontext-GUID, um zu bestimmen, ob das Dialogfeld die Quelle der volumeänderung ist.</span><span class="sxs-lookup"><span data-stu-id="4fbed-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="4fbed-153">Weitere Informationen zu Ereignis Kontext-GUIDs finden Sie unter **iaudioendpointvolumecallback:: OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="4fbed-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="4fbed-154">Wenn der Benutzer das Dialogfeld verlässt, löscht der [**unregistercontrolchangenotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) -Befehl im vorangehenden Codebeispiel die Registrierung der caudioendpointvolumecallback-Klasse, bevor das Programm beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fbed-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="4fbed-155">Sie können das vorangehende Codebeispiel leicht ändern, um die Volume-und stumm Steuerelemente für das Standard Erfassungsgerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4fbed-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="4fbed-156">Ändern Sie in der [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) -Funktion den Wert des ersten Parameters im-Befehl in die [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) -Methode von "-" in "ecapture".</span><span class="sxs-lookup"><span data-stu-id="4fbed-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="4fbed-157">Das folgende Codebeispiel ist das Ressourcen Skript, das das Volume und die stumm Steuerelemente definiert, die im vorangehenden Codebeispiel angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="4fbed-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="4fbed-158">Das folgende Codebeispiel zeigt die Ressourcen Header Datei, die die Steuerelement Bezeichner definiert, die in den vorangehenden Codebeispielen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="4fbed-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="4fbed-159">Die vorangehenden Codebeispiele bilden eine einfache Anwendung zum Steuern und Überwachen des endpunktvolumes des standardrenderinggeräts.</span><span class="sxs-lookup"><span data-stu-id="4fbed-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="4fbed-160">Eine nützlichere Anwendung kann den Benutzer darüber hinaus Benachrichtigen, wenn sich der Status des Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="4fbed-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="4fbed-161">Beispielsweise kann das Gerät deaktiviert, getrennt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="4fbed-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="4fbed-162">Weitere Informationen zum Überwachen dieser Ereignis Typen finden Sie unter [Geräte Ereignisse](device-events.md).</span><span class="sxs-lookup"><span data-stu-id="4fbed-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fbed-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fbed-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fbed-164">Lautstärkeregler</span><span class="sxs-lookup"><span data-stu-id="4fbed-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
