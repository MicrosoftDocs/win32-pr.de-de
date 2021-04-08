---
description: In diesem Artikel werden einige einfache Beispiele vorgestellt, die veranschaulichen, wie räumlicher Sound mit statischen räumlichen Audioobjekten, dynamischen räumlichen Audioobjekten und räumlichen Audioobjekten implementiert werden, die die Head relative Transfer Function (HRTF) von Microsoft verwenden.
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Rendering von räumlichem Sound mithilfe räumlicher Audioobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748545"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="b41a0-103">Rendering von räumlichem Sound mithilfe räumlicher Audioobjekte</span><span class="sxs-lookup"><span data-stu-id="b41a0-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="b41a0-104">In diesem Artikel werden einige einfache Beispiele vorgestellt, die veranschaulichen, wie räumlicher Sound mit statischen räumlichen Audioobjekten, dynamischen räumlichen Audioobjekten und räumlichen Audioobjekten implementiert werden, die die Head relative Transfer Function (HRTF) von Microsoft verwenden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="b41a0-105">Die Implementierungs Schritte für alle drei dieser Techniken sind sehr ähnlich, und dieser Artikel enthält ein ähnlich strukturiertes Codebeispiel für jede Technik.</span><span class="sxs-lookup"><span data-stu-id="b41a0-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="b41a0-106">Vollständige End-to-End-Beispiele für reale räumliche audioimplementierungen finden Sie unter [Microsoft Spatial Sound Samples GitHub Repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span><span class="sxs-lookup"><span data-stu-id="b41a0-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="b41a0-107">Eine Übersicht über Windows Sonic, die Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox und Windows, finden Sie unter [räumlicher Sound](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="b41a0-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="b41a0-108">Audiodarstellung mit statischen räumlichen Audioobjekten</span><span class="sxs-lookup"><span data-stu-id="b41a0-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="b41a0-109">Ein statisches Audioobjekt wird verwendet, um Sound in einem von 18 statischen Audiokanälen zu erzeugen, die in der [**audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) -Enumeration definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="b41a0-110">Jeder dieser Kanäle stellt einen echten oder virtualisierten Referenten an einem festgelegten Raum dar, der sich nicht im Laufe der Zeit bewegt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="b41a0-111">Die statischen Kanäle, die auf einem bestimmten Gerät verfügbar sind, hängen vom verwendeten räumlichen Audioformat ab.</span><span class="sxs-lookup"><span data-stu-id="b41a0-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="b41a0-112">Eine Liste der unterstützten Formate und deren Anzahl von Kanälen finden Sie unter [räumlicher Sound](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="b41a0-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="b41a0-113">Wenn Sie einen räumlichen Audiostream initialisieren, müssen Sie angeben, welche der verfügbaren statischen Kanäle der Stream verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="b41a0-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="b41a0-114">Die folgenden Beispiel Konstanten Definitionen können verwendet werden, um allgemeine Sprecher Konfigurationen anzugeben und die Anzahl der verfügbaren Kanäle für jede zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



<span data-ttu-id="b41a0-115">Der erste Schritt beim Rendern räumlicher Audiodaten besteht darin, den audioendpunkt zu erhalten, an den Audiodaten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="b41a0-116">Erstellen Sie eine Instanz von [**mmdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , und rufen Sie [**getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um das standardaudiorendering-Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="b41a0-117">Wenn Sie einen räumlichen Audiodatenstrom erstellen, müssen Sie das Audioformat angeben, das der Stream verwenden soll, indem Sie eine [WaveFormatEx](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) -Struktur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="b41a0-118">Wenn Sie Audiodaten aus einer Datei wiedergeben, wird das Format normalerweise durch das Audiodateiformat bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="b41a0-119">In diesem Beispiel wird ein Mono-, 32-Bit-, 48 Hz-Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41a0-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



<span data-ttu-id="b41a0-120">Der nächste Schritt beim Rendern von räumlichem audiovorgang besteht darin, einen räumlichen Audiodatenstrom zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b41a0-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="b41a0-121">Rufen Sie zuerst eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab.</span><span class="sxs-lookup"><span data-stu-id="b41a0-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="b41a0-122">Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="b41a0-123">Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b41a0-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="b41a0-124">Füllt eine [**spatialaudioobjectrenderstreamactivationparameams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) -Struktur auf, die zum Initialisieren des räumlichen Audiostreams verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="b41a0-125">In diesem Beispiel wird das Feld **staticobjecttypemask** auf die zuvor in diesem Artikel definierte typkonstante **channelmask \_** festgelegt, was bedeutet, dass nur der Front-Right-und der linke Kanal vom Audiodatenstrom verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b41a0-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="b41a0-126">Da in diesem Beispiel nur statische Audioobjekte und keine dynamischen Objekte verwendet werden, wird das Feld **maxdynamicobjectcount** auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="b41a0-127">Das **Kategoriefeld** ist auf einen Member der [**Audiodaten \_ Strom- \_ kategorienumeration**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) festgelegt, der definiert, wie das System den Sound aus diesem Stream mit anderen Audioquellen vermischt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="b41a0-128">Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b41a0-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> <span data-ttu-id="b41a0-129">Wenn Sie die [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) -Schnittstellen für einen Xbox One Development Kit (XDK)-Titel verwenden, müssen Sie zuerst **enablespatialaudio** aufrufen, bevor Sie [**immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) oder [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="b41a0-130">Wenn dies nicht der Fall ist, wird ein E \_ nointerface-Fehler vom aufzurufenden Aktivierungsbefehl zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="b41a0-131">**Enablespatialaudioist** nur für XDK-Titel verfügbar und muss nicht für universelle Windows-Plattform apps, die auf Xbox One ausgeführt werden, oder für nicht-Xbox one-Geräte aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="b41a0-132">Deklarieren Sie einen Zeiger für ein [**ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) , das zum Schreiben von Audiodaten in einen statischen Kanal verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="b41a0-133">Typische Apps verwenden ein-Objekt für jeden Kanal, der im Feld **staticobjecttypemask** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="b41a0-134">Der Einfachheit halber wird in diesem Beispiel nur ein einzelnes statisches Audioobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="b41a0-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="b41a0-135">Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="b41a0-136">In diesem Beispiel wird ein-Counter verwendet, um das Rendering von Audiodaten nach fünf Sekunden zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="b41a0-137">Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das bereitgestellt wurde, als der räumliche Audiostream initialisiert wurde, signalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b41a0-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="b41a0-138">Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="b41a0-139">In diesem Fall kann [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufgerufen werden, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="b41a0-140">Nennen Sie als nächstes [**ispatialaudioobjectrenderstream:: beginupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="b41a0-141">Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frame Anzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="b41a0-142">Wenn noch kein statisches räumliches Audioobjekt erstellt wurde, erstellen Sie ein oder mehrere, indem Sie [**ispatialaudioobjectrenderstream:: activatespatialaudioobject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject)aufrufen, und übergeben Sie einen Wert aus der [**audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) -Enumeration, die den statischen Kanal angibt, in dem die Audioobjekt-Audiodatei gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="b41a0-143">Anschließend wird [**ispatialaudioobject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) aufgerufen, um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="b41a0-144">Diese Methode gibt auch die Größe des Puffers in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="b41a0-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="b41a0-145">In diesem Beispiel wird eine Hilfsmethode, " **Write tedeaudioobjectbuffer**", verwendet, um den Puffer mit Audiodaten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="b41a0-146">Diese Methode wird weiter unten in diesem Artikel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-146">This method is shown later in this article.</span></span> <span data-ttu-id="b41a0-147">Nach dem Schreiben in den Puffer überprüft das Beispiel, ob die 5-Sekunden-Lebensdauer des-Objekts erreicht wurde. wenn dies der Fall ist, wird [**ispatialaudioobject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden und das-Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="b41a0-148">Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, nennen Sie [**ispatialaudioobjectrenderstream:: endupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , damit das System weiß, dass die Daten für das Rendering bereit sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="b41a0-149">Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



<span data-ttu-id="b41a0-150">Wenn Sie mit dem Rendern räumlicher Audiodaten abgeschlossen sind, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudioobjectrenderstream:: beenden**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="b41a0-151">Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)freigeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="b41a0-152">Die hilfsprogrammmethode " **Write-deaudioobjectbuffer** " schreibt entweder einen vollständigen Puffer von Beispielen oder die Anzahl der verbleibenden Stichproben, die durch das von der APP definierte Zeit Limit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="b41a0-153">Dies kann z. b. auch durch die Anzahl der in einer Quellaudiodatei verbleibenden Beispiele bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="b41a0-154">Eine einfache Sin-Wave wird generiert und in den Puffer geschrieben, um die Häufigkeit zu skalieren, die durch den *Frequency* -Eingabeparameter skaliert wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="b41a0-155">Audiodarstellung mit dynamischen räumlichen Audioobjekten</span><span class="sxs-lookup"><span data-stu-id="b41a0-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="b41a0-156">Dynamische Objekte ermöglichen es Ihnen, Audiodaten von einer beliebigen Position im Raum relativ zum Benutzer zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="b41a0-157">Die Position und das Volume eines dynamischen audioobjekts können im Laufe der Zeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="b41a0-158">Spiele verwenden normalerweise die Position eines 3D-Objekts in der Spiel Welt, um die Position des ihm zugeordneten dynamischen audioobjekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="b41a0-159">Im folgenden Beispiel wird eine einfache Struktur, **My3dObject**, verwendet, um den minimalen Satz von Daten zu speichern, die für die Darstellung eines Objekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="b41a0-160">Diese Daten umfassen einen Zeiger auf ein [**ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), die Position, die Geschwindigkeit, das Volume und die Tonfrequenz für das Objekt sowie einen Wert, der die Gesamtzahl der Frames speichert, für die das Objekt Sound gerenden Sound erzeugen soll.</span><span class="sxs-lookup"><span data-stu-id="b41a0-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="b41a0-161">Die Implementierungs Schritte für dynamische Audioobjekte sind größtenteils mit den Schritten für statische Audioobjekte identisch, die oben beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="b41a0-162">Zuerst sollten Sie einen audioendpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="b41a0-163">Initialisieren Sie als nächstes den räumlichen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="b41a0-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="b41a0-164">Rufen Sie eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab.</span><span class="sxs-lookup"><span data-stu-id="b41a0-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="b41a0-165">Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="b41a0-166">Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b41a0-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="b41a0-167">Rufen Sie [**ispatialaudioclient:: getmaxdynamicobjectcount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl von dynamischen Objekten abzurufen, die vom System unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="b41a0-168">Wenn dieser Rückruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b41a0-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="b41a0-169">Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl der dynamischen Audioobjekte, die für unterschiedliche räumliche Audioformate verfügbar sind, finden Sie unter [Spatial Sound](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="b41a0-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="b41a0-170">Legen Sie beim Auffüllen der [**spatialaudioobjectrenderstreamactivationparser**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) -Struktur das Feld **maxdynamicobjectcount** auf die maximale Anzahl dynamischer Objekte fest, die von Ihrer APP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="b41a0-171">Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b41a0-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



<span data-ttu-id="b41a0-172">Im folgenden finden Sie eine Reihe von Anwendungs spezifischem Code, der die Unterstützung dieses Beispiels benötigt, mit dem zufällig positionierte Audioobjekte dynamisch erzeugt und in einem Vektor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



<span data-ttu-id="b41a0-173">Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="b41a0-174">Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das wir bereitgestellt haben, als der räumliche Audiostream initialisiert wurde, um signalisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="b41a0-175">Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="b41a0-176">In diesem Fall kann [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufgerufen werden, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="b41a0-177">Nennen Sie als nächstes [**ispatialaudioobjectrenderstream:: beginupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="b41a0-178">Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte und die Frame Anzahl des Puffers für Audioobjekte zurück, die von diesem Stream gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="b41a0-179">Wenn der "Spawn"-Leistungswert den angegebenen Wert erreicht, wird ein neues dynamisches Audioobjekt durch Aufrufen von [**ispatialaudioobjectrenderstream:: activatespatialaudioobject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) mit [**\_ dynamischem audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)-Objekt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b41a0-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="b41a0-180">Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **splaudclnt \_ E \_ keine \_ weiteren \_ Objekte** zurück.</span><span class="sxs-lookup"><span data-stu-id="b41a0-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="b41a0-181">In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer APP-spezifischen Priorisierung freigeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="b41a0-182">Nachdem das dynamische Audioobjekt erstellt wurde, wird es zu einer neuen **My3dObject** -Struktur hinzugefügt, wobei zufällige Positions-, Geschwindigkeits-, Volume-und Häufigkeits Werte erstellt werden, die dann der Liste der aktiven-Objekte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="b41a0-183">Anschließend durchlaufen Sie alle aktiven-Objekte, die in diesem Beispiel mit der von der APP definierten **My3dObject** -Struktur dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="b41a0-184">Aufrufen Sie für jedes Audioobjekt [**ispatialaudioobject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) , um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="b41a0-185">Diese Methode gibt auch die Größe des Puffers in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="b41a0-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="b41a0-186">Die Hilfsmethode, " **Write tedeaudioobjectbuffer**", um den Puffer mit Audiodaten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="b41a0-187">Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position des dynamischen audioobjekts durch Aufrufen von [**ispatialaudioobject:: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="b41a0-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="b41a0-188">Das Volume des audioobjekts kann auch durch Aufrufen von [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="b41a0-189">Wenn Sie die Position oder das Volume des Objekts nicht aktualisieren, werden die Position und das Volume von der letzten Festlegung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="b41a0-190">Wenn die von der APP definierte Lebensdauer des Objekts erreicht wurde, wird [**ispatialaudioobject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden, und das Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="b41a0-191">Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, nennen Sie [**ispatialaudioobjectrenderstream:: endupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , damit das System weiß, dass die Daten für das Rendering bereit sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="b41a0-192">Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



<span data-ttu-id="b41a0-193">Wenn Sie mit dem Rendern räumlicher Audiodaten abgeschlossen sind, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudioobjectrenderstream:: beenden**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="b41a0-194">Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)freigeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="b41a0-195">Audiodarstellung mit dynamischen räumlichen Audioobjekten für HRTF</span><span class="sxs-lookup"><span data-stu-id="b41a0-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="b41a0-196">Ein weiterer Satz von APIs, [**ispatialaudiorenderstreamforhrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) und [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), ermöglicht das räumliche Audio, das die Head-relative Transfer Function (HRTF) von Microsoft zum Simulieren von Sounds verwendet, um die Position des Emitters im Raum relativ zu dem Benutzer zu simulieren, der im Laufe der Zeit geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b41a0-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="b41a0-197">Neben der Position können Sie mithilfe von HRTF-Audioobjekten eine Ausrichtung im Bereich angeben, eine directivität, in der ein Sound ausgegeben wird, z. b. eine Kegel-oder eine karoid-Form, und ein Zerfalls Modell, wenn sich das Objekt näher und weiter vom virtuellen Listener bewegt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="b41a0-198">Beachten Sie, dass diese HRTF-Schnittstellen nur verfügbar sind, wenn der Benutzer Windows Sonic for-Kopfhörer als räumliche Audioengine für das Gerät ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="b41a0-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="b41a0-199">Informationen zum Konfigurieren eines Geräts für die Verwendung von Windows Sonic für Kopfhörer finden Sie unter [räumlicher Sound](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="b41a0-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="b41a0-200">Mit den [**ispatialaudiorenderstreamforhrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) -und [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) -APIs kann eine Anwendung explizit den Windows-Sound für den Kopfhörer-Rendering-Pfad direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="b41a0-201">Diese APIs unterstützen keine räumlichen Audioformate, wie z. b. Dolby Atmos für das Heim Theater oder Dolby Atmos für Kopfhörer, und weder das Consumer-gesteuerte Ausgabeformat auch **über die** Audiosteuerelement-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="b41a0-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="b41a0-202">Diese Schnittstellen sind für die Verwendung in Windows Mixed Reality-Anwendungen gedacht, bei denen Windows Sonic für Kopf fachspezifische Funktionen verwendet werden soll (z. b. Umgebungseinstellungen und Entfernungs basierte Rolloff, die außerhalb der typischen Inhalts Erstellungs Pipelines Programm gesteuert angegeben sind).</span><span class="sxs-lookup"><span data-stu-id="b41a0-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="b41a0-203">Die meisten Spiele-und Virtual Reality-Szenarien bevorzugen stattdessen die Verwendung von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) .</span><span class="sxs-lookup"><span data-stu-id="b41a0-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="b41a0-204">Die Implementierungs Schritte für beide API-Sätze sind fast identisch, sodass beide Technologien implementiert und zur Laufzeit gewechselt werden können, je nachdem, welche Funktion auf dem aktuellen Gerät verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b41a0-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="b41a0-205">Mixed-Reality-Apps verwenden normalerweise die Position eines 3D-Objekts in der virtuellen Welt, um die Position des zugeordneten dynamischen audioobjekts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="b41a0-206">Im folgenden Beispiel wird eine einfache Struktur, **My3dObjectForHrtf**, verwendet, um den minimalen Satz von Daten zu speichern, die für die Darstellung eines Objekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="b41a0-207">Diese Daten umfassen einen Zeiger auf ein [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), die Position, die Ausrichtung, die Geschwindigkeit und die Tonfrequenz für das Objekt sowie einen Wert, der die Gesamtzahl der Frames speichert, für die das Objekt Sound gerenden Sound erzeugen soll.</span><span class="sxs-lookup"><span data-stu-id="b41a0-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="b41a0-208">Die Implementierungs Schritte für dynamische HRTF-Audioobjekte sind größtenteils mit den Schritten für dynamische Audioobjekte identisch, die im vorherigen Abschnitt beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="b41a0-209">Zuerst sollten Sie einen audioendpunkt erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="b41a0-210">Initialisieren Sie als nächstes den räumlichen Audiodatenstrom.</span><span class="sxs-lookup"><span data-stu-id="b41a0-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="b41a0-211">Rufen Sie eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab.</span><span class="sxs-lookup"><span data-stu-id="b41a0-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="b41a0-212">Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="b41a0-213">Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b41a0-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="b41a0-214">Rufen Sie [**ispatialaudioclient:: getmaxdynamicobjectcount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl von dynamischen Objekten abzurufen, die vom System unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="b41a0-215">Wenn dieser Rückruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b41a0-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="b41a0-216">Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl der dynamischen Audioobjekte, die für unterschiedliche räumliche Audioformate verfügbar sind, finden Sie unter [Spatial Sound](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="b41a0-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="b41a0-217">Legen Sie beim Auffüllen der [**spatialaudiohrtfactivationparameams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) -Struktur das Feld **maxdynamicobjectcount** auf die maximale Anzahl dynamischer Objekte fest, die von Ihrer APP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="b41a0-218">Die Aktivierungs Parameter für HRTF unterstützen einige zusätzliche Parameter, z. b. " [**spatialaudiohrtfdistancedecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay)", " [**spatialaudiohrtfdirectivityunion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion)", " [**spatialaudiohrtfumgebungstyp**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)" und " [**spatialaudiohrtforientation**](spatialaudiohrtforientation.md)", die die Standardwerte dieser Einstellungen für neue Objekte angeben, die aus dem Stream erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="b41a0-219">Diese Parameter sind optional.</span><span class="sxs-lookup"><span data-stu-id="b41a0-219">These parameters are optional.</span></span> <span data-ttu-id="b41a0-220">Legen Sie die Felder auf **nullptr** fest, um keine Standardwerte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="b41a0-221">Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b41a0-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



<span data-ttu-id="b41a0-222">Im folgenden finden Sie eine Reihe von Anwendungs spezifischem Code, der die Unterstützung dieses Beispiels benötigt, mit dem zufällig positionierte Audioobjekte dynamisch erzeugt und in einem Vektor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



<span data-ttu-id="b41a0-223">Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstreamforhrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="b41a0-224">Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das wir bereitgestellt haben, als der räumliche Audiostream initialisiert wurde, um signalisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="b41a0-225">Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b41a0-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="b41a0-226">In diesem Fall können Sie [**ispatialaudiorenderstreamforhrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) aufrufen, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="b41a0-227">Nennen Sie als nächstes [**ispatialaudiorenderstreamforhrtf:: beginupdatingaudioobjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="b41a0-228">Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frame Anzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="b41a0-229">Wenn der fektionsindikator den angegebenen Wert erreicht, wird ein neues dynamisches Audioobjekt durch Aufrufen von [**ispatialaudiorenderstreamforhrtf:: activatespatialaudioobjectforhrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) mit [**\_ dynamischem audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)-Objekt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b41a0-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="b41a0-230">Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **splaudclnt \_ E \_ keine \_ weiteren \_ Objekte** zurück.</span><span class="sxs-lookup"><span data-stu-id="b41a0-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="b41a0-231">In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer APP-spezifischen Priorisierung freigeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="b41a0-232">Nachdem das dynamische Audioobjekt erstellt wurde, wird es einer neuen **My3dObjectForHrtf** -Struktur mit zufälligen Positions-, Drehungs-, Geschwindigkeits-, Volume-und Häufigkeits Werten hinzugefügt, die dann der Liste der aktiven-Objekte hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="b41a0-233">Anschließend durchlaufen Sie alle aktiven-Objekte, die in diesem Beispiel mit der von der APP definierten **My3dObjectForHrtf** -Struktur dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="b41a0-234">Aufrufen Sie für jedes Audioobjekt [**ispatialaudioobjectforhrtf:: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) , um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="b41a0-235">Diese Methode gibt auch die Größe des Puffers in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="b41a0-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="b41a0-236">Die zuvor in diesem Artikel aufgeführte Hilfsmethode " **Write tedeaudioobjectbuffer**", um den Puffer mit Audiodaten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="b41a0-237">Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position und Ausrichtung des HRTF-audioobjekts durch Aufrufen von [**ispatialaudioobjectforhrtf:: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) und [**ispatialaudioobjectforhrtf:: setOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span><span class="sxs-lookup"><span data-stu-id="b41a0-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="b41a0-238">In diesem Beispiel wird eine **Hilfsmethode calculateemitterkoneorientationmatrix** verwendet, um die Orientierungs Matrix anhand der Richtung zu berechnen, auf die das 3D-Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="b41a0-239">Die Implementierung dieser Methode wird unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="b41a0-240">Das Volume des audioobjekts kann auch durch Aufrufen von [**ispatialaudioobjectforhrtf:: setgewinn**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b41a0-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="b41a0-241">Wenn Sie die Position, die Ausrichtung oder das Volume des Objekts nicht aktualisieren, werden die Position, die Ausrichtung und das Volume vom Zeitpunkt der letzten Festlegung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b41a0-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="b41a0-242">Wenn die von der APP definierte Lebensdauer des Objekts erreicht ist, wird [**ispatialaudioobjectforhrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden, und das Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="b41a0-243">Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, müssen Sie [**ispatialaudiorenderstreamforhrtf:: endupdatingaudioobjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) aufrufen, um dem System mitzuteilen, dass die Daten für das Rendering bereit sind.</span><span class="sxs-lookup"><span data-stu-id="b41a0-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="b41a0-244">Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



<span data-ttu-id="b41a0-245">Wenn Sie das Rendering räumlicher Audiodaten abgeschlossen haben, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudiorenderstreamforhrtf:: beenden**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85))aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b41a0-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="b41a0-246">Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudiorenderstreamforhrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85))freigeben.</span><span class="sxs-lookup"><span data-stu-id="b41a0-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="b41a0-247">Das folgende Codebeispiel zeigt die Implementierung der **Hilfsmethode calculateemitterkoneorientationmatrix** , die im obigen Beispiel verwendet wurde, um die Orientierungs Matrix anhand der Richtung zu berechnen, auf die das 3D-Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="b41a0-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a><span data-ttu-id="b41a0-248">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b41a0-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b41a0-249">Raumklang</span><span class="sxs-lookup"><span data-stu-id="b41a0-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="b41a0-250">**Ispatialaudioclient**</span><span class="sxs-lookup"><span data-stu-id="b41a0-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="b41a0-251">**Ispatialaudioobject**</span><span class="sxs-lookup"><span data-stu-id="b41a0-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
