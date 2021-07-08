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
# <a name="endpoint-volume-controls"></a><span data-ttu-id="e56ba-103">Steuerelemente für Endpunktvolumen</span><span class="sxs-lookup"><span data-stu-id="e56ba-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="e56ba-104">Mit den [**Schnittstellen ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)und [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) können Clients die Lautstärkeebenen von Audiositzungen [steuern,](audio-sessions.md)bei denen es sich um Sammlungen von Audiostreams im freigegebenen Modus handelt.</span><span class="sxs-lookup"><span data-stu-id="e56ba-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="e56ba-105">Diese Schnittstellen funktionieren nicht mit Audiostreams im exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="e56ba-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="e56ba-106">Anwendungen, die Streams im exklusiven Modus verwalten, können die Volumeebenen dieser Streams über die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) steuern.</span><span class="sxs-lookup"><span data-stu-id="e56ba-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="e56ba-107">Diese Schnittstelle steuert die Lautstärke des [Audioendpunktgeräts.](audio-endpoint-devices.md)</span><span class="sxs-lookup"><span data-stu-id="e56ba-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="e56ba-108">Sie verwendet die Hardware-Volumesteuerung für das Endpunktgerät, wenn die Audiohardware ein solches Steuerelement implementiert.</span><span class="sxs-lookup"><span data-stu-id="e56ba-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="e56ba-109">Andernfalls implementiert **die IAudioEndpointVolume-Schnittstelle** die Volumesteuerung in der Software.</span><span class="sxs-lookup"><span data-stu-id="e56ba-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="e56ba-110">Wenn ein Gerät über ein Hardwarevolume-Steuerelement verfügt, wirken sich Änderungen, die über die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) am Steuerelement vorgenommen werden, sowohl im gemeinsam genutzten als auch im exklusiven Modus auf die Volumeebene aus.</span><span class="sxs-lookup"><span data-stu-id="e56ba-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="e56ba-111">Wenn auf einem Gerät kein Hardwarevolumen und stummgeschaltete Steuerelemente verfügbar sind, wirken sich Änderungen am Softwarevolumen und stummgeschalteten Steuerelementen über diese Schnittstelle auf die Volumeebene im gemeinsam genutzten Modus aus, jedoch nicht im exklusiven Modus.</span><span class="sxs-lookup"><span data-stu-id="e56ba-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="e56ba-112">Im exklusiven Modus tauschen die Anwendung und die Audiohardware Audiodaten direkt aus und umgehen dabei die Softwaresteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e56ba-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="e56ba-113">Im Allgemeinen sollten Anwendungen vermeiden, die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) zu verwenden, um die Volumeebenen von Streams im freigegebenen Modus zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e56ba-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="e56ba-114">Stattdessen sollten Anwendungen zu diesem Zweck die [**Schnittstelle ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)oder [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e56ba-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="e56ba-115">Wenn eine Anwendung ein Volumesteuerprogramm anzeigt, das die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) verwendet, um die Lautstärke eines Audioendpunktgeräts zu steuern, sollte dieses Volumesteuerprogramm das vom Systemvolumesteuerungsprogramm Sndvol angezeigte Steuerelement des Endpunktvolumes spiegeln.</span><span class="sxs-lookup"><span data-stu-id="e56ba-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="e56ba-116">Wie bereits erläutert, wird das Steuerelement für das Endpunktvolume auf der linken Seite des Fensters Sndvol im Gruppenfeld Mit der Bezeichnung **Gerät angezeigt.**</span><span class="sxs-lookup"><span data-stu-id="e56ba-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="e56ba-117">Wenn der Benutzer das Endpunktvolume eines Geräts über die Volumesteuerung in Sndvol ändert, sollte die entsprechende Steuerung des Endpunktvolumes in der Anwendung zusammen mit dem Steuerelement in Sndvol übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="e56ba-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="e56ba-118">Wenn der Benutzer die Volumeebene über das Endpunktvolume-Steuerelement im Anwendungsfenster ändert, sollte die entsprechende Volumesteuerung in Sndvol zusammen mit der Volumesteuerung der Anwendung bewegt werden.</span><span class="sxs-lookup"><span data-stu-id="e56ba-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="e56ba-119">Um sicherzustellen, dass das Endpunktvolume-Steuerelement in einem Anwendungsfenster das Endpunktvolume-Steuerelement in Sndvol spiegelt, muss die Anwendung eine [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) implementieren und diese Schnittstelle für den Empfang von Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="e56ba-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="e56ba-120">Danach empfängt die Anwendung jedes Mal, wenn der Benutzer die Endpunktvolumeebene in Sndvol ändert, einen Benachrichtigungsaufruf über die [**IAudioEndpointVolumeCallback::OnNotify-Methode.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify)</span><span class="sxs-lookup"><span data-stu-id="e56ba-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="e56ba-121">Während dieses Aufrufs kann die **OnNotify-Methode** das Endpunktvolume-Steuerelement im Anwendungsfenster aktualisieren, damit es mit der in Sndvol angezeigten Steuerelementeinstellung übereinstimmen kann.</span><span class="sxs-lookup"><span data-stu-id="e56ba-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="e56ba-122">Ebenso empfängt Sndvol jedes Mal, wenn der Benutzer die Endpunktvolumeebene über die Volumesteuerung im Anwendungsfenster ändert, eine Benachrichtigung und aktualisiert sofort das Endpunktvolume-Steuerelement, um die neue Volumeebene anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e56ba-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="e56ba-123">Das folgende Codebeispiel ist eine Headerdatei, die eine mögliche Implementierung der [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) zeigt:</span><span class="sxs-lookup"><span data-stu-id="e56ba-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


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



<span data-ttu-id="e56ba-124">Die CAudioEndpointVolumeCallback-Klasse im vorherigen Codebeispiel ist eine Implementierung der [**IAudioEndpointVolumeCallback-Schnittstelle.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)</span><span class="sxs-lookup"><span data-stu-id="e56ba-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="e56ba-125">Da **IAudioEndpointVolumeCallback** von [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)erbt, enthält die Klassendefinition Implementierungen der **IUnknown-Methoden** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)und [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="e56ba-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="e56ba-126">Die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der Klassendefinition wird jedes Mal aufgerufen, wenn eine der folgenden Methoden die Endpunktvolumenebene ändert:</span><span class="sxs-lookup"><span data-stu-id="e56ba-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="e56ba-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="e56ba-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="e56ba-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="e56ba-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="e56ba-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="e56ba-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="e56ba-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="e56ba-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="e56ba-131">**IAudioEndpointVolume::SetMute**</span><span class="sxs-lookup"><span data-stu-id="e56ba-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="e56ba-132">**IAudioEndpointVolume::VolumeStepDown**</span><span class="sxs-lookup"><span data-stu-id="e56ba-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="e56ba-133">**IAudioEndpointVolume::VolumeStepUp**</span><span class="sxs-lookup"><span data-stu-id="e56ba-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="e56ba-134">Die Implementierung der [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) im vorherigen Codebeispiel sendet Nachrichten an das Volumesteuersystem im Anwendungsfenster, um die angezeigte Volumeebene zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e56ba-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="e56ba-135">Eine Anwendung ruft die [**IAudioEndpointVolume::RegisterControlChangeNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die [**IAudioEndpointVolumeCallback-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) für den Empfang von Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e56ba-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="e56ba-136">Wenn die Anwendung keine Benachrichtigungen mehr benötigt, ruft sie die [**IAudioEndpointVolume::UnregisterControlChangeNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) auf, um die Registrierung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="e56ba-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="e56ba-137">Das folgende Codebeispiel ist eine Windows-Anwendung, die die [**Methoden RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) und [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) aufruft, um die CAudioEndpointVolumeCallback-Klasse im vorherigen Codebeispiel zu registrieren und deren Registrierung zu aufheben:</span><span class="sxs-lookup"><span data-stu-id="e56ba-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


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



<span data-ttu-id="e56ba-138">Im vorherigen Codebeispiel ruft die [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) die [**CoCreateInstance-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um eine Instanz der [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) zu erstellen, und ruft die [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) des Standardrenderinggeräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e56ba-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="e56ba-139">**WinMain** ruft die [**IMMDevice::Activate-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) auf, um die [**IAudioEndpointVolume-Schnittstelle**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) des Geräts zu erhalten, und [**ruft RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) auf, um die Anwendung zum Empfangen von Benachrichtigungen über Änderungen des Endpunktvolumes zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="e56ba-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="e56ba-140">Als Nächstes **öffnet WinMain** ein Dialogfeld, in dem ein Endpunkt-Volumesteuerfeld für das Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e56ba-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="e56ba-141">Im Dialogfeld wird auch ein Kontrollkästchen angezeigt, das angibt, ob das Gerät stummgeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="e56ba-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="e56ba-142">Das Kontrollkästchen Steuerelement für Endpunktvolume und Stummschaltung im Dialogfeld spiegelt die Einstellungen des Endpunktvolume-Steuerelements und des Kontrollkästchens Stummschalten wieder, das von Sndvol angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e56ba-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="e56ba-143">Weitere Informationen zu **WinMain** und **CoCreateInstance** finden Sie in der Windows SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="e56ba-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="e56ba-144">Weitere Informationen zu **IMMDeviceEnumerator** und **IMMDevice finden** Sie unter [Aufzählen von Audiogeräten.](enumerating-audio-devices.md)</span><span class="sxs-lookup"><span data-stu-id="e56ba-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="e56ba-145">Die Dialogfeldprozedur DlgProc im vorherigen Codebeispiel verarbeitet die Änderungen, die der Benutzer am Volume vorn vorgenommen hat, und stummschalten die Einstellungen über die Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e56ba-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="e56ba-146">Wenn DlgProc [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) oder [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)aufruft, empfängt Sndvol eine Benachrichtigung über die Änderung und aktualisiert das entsprechende Steuerelement in seinem Fenster, um das neue Volume oder die Stummschaltungseinstellung widerzuanzeigen.</span><span class="sxs-lookup"><span data-stu-id="e56ba-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="e56ba-147">Wenn der Benutzer anstelle des Dialogfelds das Volume aktualisiert und die Einstellungen über die Steuerelemente im Sndvol-Fenster stummschaltt, aktualisiert die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der CAudioEndpointVolumeCallback-Klasse die Steuerelemente im Dialogfeld, um die neuen Einstellungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e56ba-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="e56ba-148">Wenn der Benutzer das Volume über die Steuerelemente im Dialogfeld ändert, sendet die [**OnNotify-Methode**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) in der CAudioEndpointVolumeCallback-Klasse keine Meldungen zum Aktualisieren der Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="e56ba-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="e56ba-149">Dies wäre redundant.</span><span class="sxs-lookup"><span data-stu-id="e56ba-149">To do so would be redundant.</span></span> <span data-ttu-id="e56ba-150">**OnNotify** aktualisiert die Steuerelemente im Dialogfeld nur, wenn die Volumeänderung aus Sndvol oder einer anderen Anwendung stammt.</span><span class="sxs-lookup"><span data-stu-id="e56ba-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="e56ba-151">Der zweite Parameter in den [**Methodenaufrufen SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) und [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) in der DlgProc-Funktion ist ein Zeiger auf eine Ereigniskontext-GUID, die beide Methoden an **OnNotify** übergeben.</span><span class="sxs-lookup"><span data-stu-id="e56ba-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="e56ba-152">**OnNotify überprüft** den Wert der Ereigniskontext-GUID, um zu bestimmen, ob das Dialogfeld die Quelle der Volumeänderung ist.</span><span class="sxs-lookup"><span data-stu-id="e56ba-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="e56ba-153">Weitere Informationen zu Ereigniskontext-GUIDs finden Sie unter **IAudioEndpointVolumeCallback::OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="e56ba-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="e56ba-154">Wenn der Benutzer das Dialogfeld beendet, löscht der [**UnregisterControlChangeNotify-Aufruf**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) im vorherigen Codebeispiel die Registrierung der CAudioEndpointVolumeCallback-Klasse, bevor das Programm beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e56ba-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="e56ba-155">Sie können das vorherige Codebeispiel problemlos ändern, um Lautstärke- und Stummschaltelemente für das Standarderfassungsgerät anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e56ba-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="e56ba-156">Ändern Sie in der [**WinMain-Funktion**](/windows/desktop/api/winbase/nf-winbase-winmain) den Wert des ersten Parameters im Aufruf der [**IMMDeviceEnumerator::GetDefaultAudioEndpoint-Methode**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) von eRender in eCapture.</span><span class="sxs-lookup"><span data-stu-id="e56ba-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="e56ba-157">Das folgende Codebeispiel ist das Ressourcenskript, das das Volume und stummgeschaltete Steuerelemente definiert, die im vorherigen Codebeispiel angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="e56ba-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="e56ba-158">Das folgende Codebeispiel ist die Ressourcenheaderdatei, die die Steuerelementbezeichner definiert, die in den obigen Codebeispielen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="e56ba-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="e56ba-159">Die obigen Codebeispiele bilden eine einfache Anwendung zum Steuern und Überwachen des Endpunktvolumens des Standardrenderinggeräts.</span><span class="sxs-lookup"><span data-stu-id="e56ba-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="e56ba-160">Eine nützlichere Anwendung kann den Benutzer darüber hinaus benachrichtigen, wenn sich der Status des Geräts ändert.</span><span class="sxs-lookup"><span data-stu-id="e56ba-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="e56ba-161">Beispielsweise kann das Gerät deaktiviert, nicht angeschlossen oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e56ba-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="e56ba-162">Weitere Informationen zum Überwachen dieser Ereignistypen finden Sie unter [Geräteereignisse.](device-events.md)</span><span class="sxs-lookup"><span data-stu-id="e56ba-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e56ba-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e56ba-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e56ba-164">Lautstärkeregler</span><span class="sxs-lookup"><span data-stu-id="e56ba-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
