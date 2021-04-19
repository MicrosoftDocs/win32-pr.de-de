---
description: Der streamingaudiorenderer (SAR) ist eine Medien Senke, die Audiodaten rendert.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Streamingaudiorenderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356843"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="7e238-103">Streamingaudiorenderer</span><span class="sxs-lookup"><span data-stu-id="7e238-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="7e238-104">Der streamingaudiorenderer (SAR) ist eine Medien Senke, die Audiodaten rendert.</span><span class="sxs-lookup"><span data-stu-id="7e238-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="7e238-105">Jede Instanz der SAR rendert einen einzelnen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="7e238-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="7e238-106">Zum Rendering mehrerer Streams verwenden Sie mehrere Instanzen von SAR.</span><span class="sxs-lookup"><span data-stu-id="7e238-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="7e238-107">Um den SAR zu erstellen, rufen Sie eine der folgenden Funktionen auf:</span><span class="sxs-lookup"><span data-stu-id="7e238-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="7e238-108">[**Mskreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="7e238-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="7e238-109">Gibt einen Zeiger auf den SAR zurück.</span><span class="sxs-lookup"><span data-stu-id="7e238-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="7e238-110">[**MF | ateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="7e238-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="7e238-111">Gibt einen Zeiger auf ein Aktivierungs Objekt zurück, das zum Erstellen der SAR verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e238-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="7e238-112">Die zweite Funktion, die ein Aktivierungs Objekt zurückgibt, ist erforderlich, wenn geschützter Inhalt wiedergegeben wird, da das Aktivierungs Objekt in den geschützten Prozess serialisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7e238-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="7e238-113">Wenn Sie den Inhalt löschen möchten, können Sie beide Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e238-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="7e238-114">Der SAR kann unkomprimierte Audiodaten im PCM-oder IEEE-Gleit Komma Format empfangen.</span><span class="sxs-lookup"><span data-stu-id="7e238-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="7e238-115">Wenn die Wiedergabe Rate schneller oder langsamer als 1 × ist, passt der SAR automatisch die Tonhöhe an.</span><span class="sxs-lookup"><span data-stu-id="7e238-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="7e238-116">Konfigurieren des audiorenderers</span><span class="sxs-lookup"><span data-stu-id="7e238-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="7e238-117">Der SAR unterstützt mehrere Konfigurations Attribute.</span><span class="sxs-lookup"><span data-stu-id="7e238-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="7e238-118">Der Mechanismus zum Festlegen dieser Attribute hängt von der Funktion ab, die Sie zum Erstellen der SAR-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="7e238-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="7e238-119">Gehen Sie wie folgt vor, wenn Sie die [**msup**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion verwenden:</span><span class="sxs-lookup"><span data-stu-id="7e238-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="7e238-120">Erstellen Sie einen neuen Attribut Speicher, indem Sie [**mfcreateattribute**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e238-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="7e238-121">Fügen Sie dem Attribut Speicher die Attribute hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e238-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="7e238-122">Übergeben Sie den Attribut Speicher an die [**mfkreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion im *paudioattributparameter* .</span><span class="sxs-lookup"><span data-stu-id="7e238-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="7e238-123">Wenn Sie die [**mfkreateaudiorendereraktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) -Funktion verwenden, gibt die Funktion einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle im *ppaktivierungs* -Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="7e238-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="7e238-124">Verwenden Sie diesen Zeiger, um die Attribute hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7e238-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="7e238-125">Eine Liste der Konfigurations Attribute finden Sie unter [Attribute für audiorenderer](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7e238-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="7e238-126">Auswählen des audioendpunktgeräts</span><span class="sxs-lookup"><span data-stu-id="7e238-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="7e238-127">Ein *audioendpunktgerät* ist ein Hardware Gerät, das Audiodaten rendert oder aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7e238-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="7e238-128">Beispiele hierfür sind Sprecher, Kopfhörer, Mikrofon und CD-Player.</span><span class="sxs-lookup"><span data-stu-id="7e238-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="7e238-129">Der SAR verwendet immer ein audiorenderinggerät.</span><span class="sxs-lookup"><span data-stu-id="7e238-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="7e238-130">Es gibt zwei Möglichkeiten, das Gerät auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7e238-130">There are two ways to select the device.</span></span>

<span data-ttu-id="7e238-131">Der erste Ansatz besteht darin, die audiorenderinggeräte im System mithilfe der [**immdeviceenumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="7e238-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="7e238-132">Diese Schnittstelle ist in der Dokumentation zur kernton-API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="7e238-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="7e238-133">Erstellen Sie das Geräte Enumeratorobjekt.</span><span class="sxs-lookup"><span data-stu-id="7e238-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="7e238-134">Verwenden Sie den Geräte Enumerator, um audiorenderinggeräte aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="7e238-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="7e238-135">Jedes Gerät wird durch einen Zeiger auf die [**immdevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7e238-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="7e238-136">Wählen Sie ein Gerät basierend auf den Geräteeigenschaften oder der Auswahl des Benutzers aus.</span><span class="sxs-lookup"><span data-stu-id="7e238-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="7e238-137">Bitten Sie [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , um den Geräte Bezeichner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e238-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="7e238-138">Legen Sie den Geräte Bezeichner als Wert für das Attribut [**\_ Endpunkt-ID für das MF- \_ audiorenderer \_ \_ \_**](mf-audio-renderer-attribute-endpoint-id-attribute.md) fest.</span><span class="sxs-lookup"><span data-stu-id="7e238-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="7e238-139">Anstatt Geräte aufzuzählen, können Sie das Audiogerät anhand seiner *Rolle* angeben.</span><span class="sxs-lookup"><span data-stu-id="7e238-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="7e238-140">Eine audiorolle identifiziert eine allgemeine Kategorie der Verwendung.</span><span class="sxs-lookup"><span data-stu-id="7e238-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="7e238-141">Beispielsweise ist die *Konsolen* Rolle für Spiele und System Benachrichtigungen definiert, während die *Multimedia* -Rolle für Musik und Filme definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7e238-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="7e238-142">Jeder Rolle ist ein audiorenderinggerät zugewiesen, und der Benutzer kann diese Zuweisungen ändern.</span><span class="sxs-lookup"><span data-stu-id="7e238-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="7e238-143">Wenn Sie eine Geräte Rolle angeben, verwendet SAR das beliebige Audiogerät, das für diese Rolle zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="7e238-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="7e238-144">Um die Geräte Rolle anzugeben, legen Sie das Attribut für das [**MF \_ - \_ audiorendererattribut \_ \_ EndPoint \_ Role**](mf-audio-renderer-attribute-endpoint-role-attribute.md) fest.</span><span class="sxs-lookup"><span data-stu-id="7e238-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="7e238-145">Die beiden in diesem Abschnitt aufgeführten Attribute schließen sich gegenseitig aus.</span><span class="sxs-lookup"><span data-stu-id="7e238-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="7e238-146">Wenn Sie keinen der beiden Optionen festlegen, verwendet der SAR das Audiogerät, das der Rolle " **econsole** " zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7e238-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="7e238-147">Der folgende Code listet die audiorenderinggeräte auf und weist dem SAR das erste Gerät in der Liste zu.</span><span class="sxs-lookup"><span data-stu-id="7e238-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="7e238-148">In diesem Beispiel wird die [**mfkreateaudiorenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) -Funktion verwendet, um den SAR zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7e238-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="7e238-149">Um das Aktivierungs Objekt für den SAR zu erstellen, ändern Sie den Code, der nach dem Aufrufen von " [**immdevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) " angezeigt wird, in Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7e238-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="7e238-150">Auswählen der Audiositzung</span><span class="sxs-lookup"><span data-stu-id="7e238-150">Selecting the Audio Session</span></span>

<span data-ttu-id="7e238-151">Eine Audiositzung ist eine Gruppe verwandter Audiodatenströme, die von einer Anwendung gemeinsam verwaltet werden können.</span><span class="sxs-lookup"><span data-stu-id="7e238-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="7e238-152">Die Anwendung kann die Volumeebene und den stumm Zustand jeder Sitzung steuern.</span><span class="sxs-lookup"><span data-stu-id="7e238-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="7e238-153">Sitzungen werden durch die GUID identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7e238-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="7e238-154">Um die Audiositzung für den SAR anzugeben, verwenden Sie das-Attribut für das [MF \_ - \_ audiorendererattribut \_ \_ Session \_ ID](mf-audio-renderer-attribute-session-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7e238-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="7e238-155">Wenn Sie dieses Attribut nicht festlegen, fügt der SAR die Standard Sitzung für diesen Prozess an, der durch **GUID \_ null** identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="7e238-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="7e238-156">Standardmäßig ist eine Audiositzung Prozess spezifisch, d. h., Sie enthält nur Datenströme aus dem aufrufenden Prozess.</span><span class="sxs-lookup"><span data-stu-id="7e238-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="7e238-157">Um einer prozessübergreifenden Sitzung beizutreten, legen Sie das Attribut Flags für das [MF \_ - \_ audiorenderer \_ Attribut \_](mf-audio-renderer-attribute-flags-attribute.md) mit dem Wert **MF \_ - \_ audiorendererattributflags \_ \_ \_ CrossProcess** fest.</span><span class="sxs-lookup"><span data-stu-id="7e238-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="7e238-158">Nachdem Sie den SAR erstellt haben, verwenden Sie die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle, um die Sitzung mit einer Gruppe von Sitzungen zu verknüpfen, die in der Systemsteuerung von der gleichen volumesteuerung gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="7e238-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="7e238-159">Sie können diese Schnittstelle auch verwenden, um den anzeigen Amen und das Symbol festzulegen, die im volumesteuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7e238-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="7e238-160">Steuern der volumeebenen</span><span class="sxs-lookup"><span data-stu-id="7e238-160">Controlling Volume Levels</span></span>

<span data-ttu-id="7e238-161">Verwenden Sie die [**imfsimpleaudiovolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) -Schnittstelle, um die Master Volume-Ebene aller Streams in der-Audiositzung von SAR zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7e238-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="7e238-162">Um das Volume eines einzelnen Streams zu steuern oder die Menge einzelner Kanäle innerhalb eines Streams zu steuern, verwenden Sie die [**imfaudiostreamvolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7e238-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="7e238-163">Beide Schnittstellen werden abgerufen, indem [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7e238-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="7e238-164">Sie können **GetService** direkt auf dem SAR aufrufen oder es für die Medien Sitzung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7e238-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="7e238-165">Volumeebenen werden als Dämpfungswerte ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="7e238-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="7e238-166">Für jeden Kanal ist die Ebene der Dämpfung das Produkt des Master Volumes und des channelvolumes.</span><span class="sxs-lookup"><span data-stu-id="7e238-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e238-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e238-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e238-168">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="7e238-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
