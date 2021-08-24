---
description: Dieser Artikel enthält einige einfache Beispiele, die veranschaulichen, wie räumlicher Sound mithilfe von statischen räumlichen Audioobjekten, dynamischen räumlichen Audioobjekten und räumlichen Audioobjekten implementiert wird, die die Head Relative Transfer Function (HRTF) von Microsoft verwenden.
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Rendern von räumlichem Sound mit räumlichen Audioobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9498b1792ed884624afef859f3f8c70d6001d91be5dff15211717651dc4767
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642500"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Rendern von räumlichem Sound mit räumlichen Audioobjekten

Dieser Artikel enthält einige einfache Beispiele, die veranschaulichen, wie räumlicher Sound mithilfe von statischen räumlichen Audioobjekten, dynamischen räumlichen Audioobjekten und räumlichen Audioobjekten implementiert wird, die die Head Relative Transfer Function (HRTF) von Microsoft verwenden. Die Implementierungsschritte für alle drei dieser Techniken sind sehr ähnlich, und dieser Artikel enthält ein ähnlich strukturiertes Codebeispiel für jede Technik. Vollständige End-to-End-Beispiele für reale Räumliche Audioimplementierungen finden Sie im [GitHub-Repository microsoft spatial sound samples (Microsoft Spatial Sound-Beispiele).](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio) Eine Übersicht über Windows Sonic, die Lösung von Microsoft auf Plattformebene für die Unterstützung räumlicher Sounds auf Xbox und Windows, finden Sie unter [Spatial Sound](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Rendern von Audiodaten mit statischen räumlichen Audioobjekten

Ein statisches Audioobjekt wird verwendet, um Sound in einem von 18 statischen Audiokanälen zu rendern, die in der [**AudioObjectType-Enumeration definiert**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) sind. Jeder dieser Kanäle stellt einen echten oder virtualisierten Lautsprecher an einem festen Punkt im Raum dar, der sich nicht im Laufe der Zeit bewegt. Die statischen Kanäle, die auf einem bestimmten Gerät verfügbar sind, hängen vom verwendeten Raumklangformat ab. Eine Liste der unterstützten Formate und deren Kanalanzahl finden Sie unter [Spatial Sound](spatial-sound.md).

Wenn Sie einen räumlichen Audiostream initialisieren, müssen Sie angeben, welche der verfügbaren statischen Kanäle der Stream verwenden soll. Die folgenden Konstantendefinitionen können verwendet werden, um allgemeine Sprecherkonfigurationen anzugeben und die Anzahl der für jeden Kanal verfügbaren Kanäle zu erhalten.


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



Der erste Schritt beim Rendern räumlicher Audiodaten besteht im Erhalten des Audioendpunkts, an den Audiodaten gesendet werden. Erstellen Sie eine Instanz von [**MMDeviceEnumerator,**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) und rufen Sie [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um das Standardaudiorendergerät zu erhalten.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Wenn Sie einen räumlichen Audiodatenstrom erstellen, müssen Sie das Audioformat angeben, das der Stream verwenden soll, indem Sie eine [WAVEFORMATEX-Struktur](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) bereitstellen. Wenn Sie Audiodaten aus einer Datei wieder geben, wird das Format in der Regel durch das Audiodateiformat bestimmt. In diesem Beispiel wird ein Monoformat mit 32 Bit und 48Hz verwendet.


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



Der nächste Schritt beim Rendern räumlicher Audiodaten besteht im Initialisieren eines räumlichen Audiostreams. Rufen Sie zunächst eine Instanz von [**ISpatialAudioClient ab,**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) indem [**Sie IMMDevice::Activate aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Rufen [**Sie ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das von der Audiopipeline verwendet wird, um die App zu benachrichtigen, dass sie für weitere Audiodaten bereit ist.

Füllen Sie [**eine SpatialAudioObjectRenderStreamActivationParams-Struktur**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) auf, die zum Initialisieren des räumlichen Audiostreams verwendet wird. In diesem Beispiel wird das **Feld StaticObjectTypeMask** auf die **stereo-Konstante ChannelMask \_** festgelegt, die zuvor in diesem Artikel definiert wurde. Dies bedeutet, dass nur der linke und rechte Vorderkanal vom Audiostream verwendet werden kann. Da in diesem Beispiel nur statische Audioobjekte und keine dynamischen Objekte verwendet werden, wird das **MaxDynamicObjectCount-Feld** auf 0 festgelegt. Das **Feld Category** wird auf einen Member der AUDIO STREAM [**\_ \_ CATEGORY-Enumeration**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) festgelegt, der definiert, wie das System den Sound aus diesem Stream mit anderen Audioquellen gemischt.

Rufen [**Sie ISpatialAudioClient::ActivateSpatialAudioStream auf,**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) um den Stream zu aktivieren.


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
> Wenn Sie die [**ISpatialAudioClient-Schnittstellen**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) für einen Titel des Xbox One Development Kit (XDK) verwenden, müssen Sie zunächst **EnableSpatialAudio** aufrufen, bevor Sie [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) oder [**IMMDeviceEnumerator::GetDefaultAudioEndpoint aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) Wenn dies nicht der Ergebnis ist, wird vom Aufruf von Activate ein E \_ NOINTERFACE-Fehler zurückgegeben. **EnableSpatialAudio** ist nur für XDK-Titel verfügbar und muss weder für Apps der universellen Windows-Plattform aufgerufen werden, die auf Xbox One ausgeführt werden, noch für nicht Xbox One Geräte.

 

Deklarieren Sie einen Zeiger für ein [**ISpatialAudioObject,**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) das zum Schreiben von Audiodaten in einen statischen Kanal verwendet wird. Typische Apps verwenden ein -Objekt für jeden Kanal, der im **Feld StaticObjectTypeMask angegeben** ist. Der Einfachheit halber wird in diesem Beispiel nur ein einzelnes statisches Audioobjekt verwendet.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Rufen Sie vor dem Eingeben der Audiorenderschleife [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) auf, um die Medienpipeline anweisen, mit dem Anfordern von Audiodaten zu beginnen. In diesem Beispiel wird ein Zähler verwendet, um das Rendern von Audiodaten nach 5 Sekunden zu beenden.

Warten Sie innerhalb der Renderschleife, bis das Pufferabschlussereignis, das beim Initialisieren des räumlichen Audiostreams bereitgestellt wurde, signalisiert wird. Sie sollten ein angemessenes Timeoutlimit festlegen, z. B. 100 ms, wenn Sie auf das Ereignis warten, da jede Änderung des Rendertyps oder Endpunkts dazu führen wird, dass dieses Ereignis nie signalisiert wird. In diesem Fall können Sie [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufrufen, um zu versuchen, den räumlichen Audiostream zurückzusetzen.

Rufen Sie als Nächstes [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) auf, um das System darüber zu informieren, dass Sie die Puffer der Audioobjekte mit Daten füllen möchten. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frameanzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.

Wenn noch kein statisches räumliches Audioobjekt erstellt wurde, erstellen Sie mindestens ein Objekt, indem Sie [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject)aufrufen und einen Wert aus der [**AudioObjectType-Enumeration**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) übergeben, der den statischen Kanal angibt, in den das Audio des Objekts gerendert wird.

Rufen Sie als Nächstes [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) auf, um einen Zeiger auf den Audiopuffer des räumlichen Audioobjekts zu erhalten. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. In diesem Beispiel wird die Hilfsmethode **WriteToAudioObjectBuffer** verwendet, um den Puffer mit Audiodaten zu füllen. Diese Methode wird weiter unten in diesem Artikel gezeigt. Nach dem Schreiben in den Puffer überprüft das Beispiel, ob die 5-Sekunden-Lebensdauer des Objekts erreicht wurde. Wenn dies der Fall ist, wird [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, um die Audiopipeline darüber zu informieren, dass mit diesem Objekt keine Audiodaten mehr geschrieben werden und das Objekt auf **nullptr** festgelegt ist, um seine Ressourcen frei zu machen.

Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, rufen Sie [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) auf, um dem System mitzuteilen, dass die Daten für das Rendering bereit sind. Sie können **GetBuffer nur** zwischen einem Aufruf von **BeginUpdatingAudioObjects** und **EndUpdatingAudioObjects aufrufen.**


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



Wenn Sie mit dem Rendern räumlicher Audiodaten fertig sind, beenden Sie den räumlichen Audiostream, indem Sie [**ISpatialAudioObjectRenderStream::Stop aufrufen.**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop) Wenn Sie den Stream nicht erneut verwenden möchten, geben Sie seine Ressourcen frei, indem Sie [**ISpatialAudioObjectRenderStream::Reset aufrufen.**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



Die **WriteToAudioObjectBuffer-Hilfsmethode** schreibt entweder einen vollständigen Puffer von Stichproben oder die Anzahl der verbleibenden Stichproben, die von unserem app-definierten Zeitlimit angegeben werden. Dies kann beispielsweise auch durch die Anzahl der in einer Quellaudiodatei verbleibenden Stichproben bestimmt werden. Eine einfache Sin-Welle, deren Häufigkeit  durch den frequency-Eingabeparameter skaliert wird, wird generiert und in den Puffer geschrieben.


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Rendern von Audiodaten mit dynamischen räumlichen Audioobjekten

Mit dynamischen Objekten können Sie Audiodaten von einer beliebigen Position im Raum relativ zum Benutzer rendern. Position und Lautstärke eines dynamischen Audioobjekts können im Laufe der Zeit geändert werden. Spiele verwenden in der Regel die Position eines 3D-Objekts in der Spielwelt, um die Position des dynamischen Audioobjekts anzugeben, das ihm zugeordnet ist. Im folgenden Beispiel wird die einfache Struktur **My3dObject** verwendet, um den minimalen Satz von Daten zu speichern, der für die Darstellung eines Objekts erforderlich ist. Diese Daten enthalten einen Zeiger auf ein [**ISpatialAudioObject,**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)die Position, Geschwindigkeit, Lautstärke und Tonfrequenz für das Objekt sowie einen Wert, der die Gesamtzahl der Frames speichert, für die das Objekt Sound rendern soll.


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



Die Implementierungsschritte für dynamische Audioobjekte sind größtenteils identisch mit den Schritten für statische Audioobjekte, die oben beschrieben wurden. Zunächst erhalten Sie einen Audioendpunkt.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Initialisieren Sie als Nächstes den räumlichen Audiostream. Rufen Sie eine Instanz von [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) ab, indem Sie [**IMMDevice::Activate aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Rufen [**Sie ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das von der Audiopipeline verwendet wird, um die App zu benachrichtigen, dass sie für weitere Audiodaten bereit ist.

Rufen [**Sie ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl der vom System unterstützten dynamischen Objekte abzurufen. Wenn dieser Aufruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert. Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl von dynamischen Audioobjekten, die für verschiedene räumliche Audioformate verfügbar sind, finden Sie unter [Spatial Sound](spatial-sound.md).

Legen Sie beim Auflisten der [**SpatialAudioObjectRenderStreamActivationParams-Struktur**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) das **Feld MaxDynamicObjectCount** auf die maximale Anzahl von dynamischen Objekten fest, die Ihre App verwendet.

Rufen [**Sie ISpatialAudioClient::ActivateSpatialAudioStream auf,**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) um den Stream zu aktivieren.


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



Im Folgenden finden Sie app-spezifischen Code für die benötigte Unterstützung dieses Beispiels, der dynamisch zufällig positionierte Audioobjekte erzeugt und in einem Vektor speichern kann.


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



Rufen Sie vor dem Eingeben der Audiorenderschleife [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) auf, um die Medienpipeline anweisen, mit dem Anfordern von Audiodaten zu beginnen.

Warten Sie innerhalb der Renderschleife auf das Pufferabschlussereignis, das wir bereitgestellt haben, als der räumliche Audiostream initialisiert wurde, um signalisiert zu werden. Sie sollten ein angemessenes Timeoutlimit festlegen, z. B. 100 ms, wenn Sie auf das Ereignis warten, da jede Änderung des Rendertyps oder Endpunkts dazu führen wird, dass dieses Ereignis nie signalisiert wird. In diesem Fall können Sie [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufrufen, um zu versuchen, den räumlichen Audiostream zurückzusetzen.

Rufen Sie als Nächstes [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) auf, um das System darüber zu informieren, dass Sie die Puffer der Audioobjekte mit Daten füllen möchten. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte und die Frameanzahl des Puffers für Audioobjekte zurück, die von diesem Stream gerendert werden.

Wenn der Spawn-Indikator den angegebenen Wert erreicht, aktivieren wir ein neues dynamisches Audioobjekt, indem [**wir ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) aufrufen und [**AudioObjectType \_ Dynamic angeben.**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **SPLAUDCLNT \_ E NO MORE OBJECTS \_ \_ \_ zurück.** In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer app-spezifischen Priorisierung veröffentlichen. Nachdem das dynamische Audioobjekt erstellt wurde, wird es einer neuen **My3dObject-Struktur** mit zufälligen Werten für Position, Geschwindigkeit, Lautstärke und Häufigkeit hinzugefügt, die dann der Liste der aktiven Objekte hinzugefügt werden.

Als Nächstes iterieren Sie alle aktiven Objekte, die in diesem Beispiel mit der von der App definierten **My3dObject-Struktur dargestellt** werden. Rufen Sie für jedes Audioobjekt [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) auf, um einen Zeiger auf den Audiopuffer des räumlichen Audioobjekts zu erhalten. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. Die Hilfsmethode **WriteToAudioObjectBuffer,** um den Puffer mit Audiodaten zu füllen. Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position des dynamischen Audioobjekts durch Aufrufen von [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). Die Lautstärke des Audioobjekts kann auch durch Aufrufen von [**SetVolume geändert werden.**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume) Wenn Sie die Position oder das Volume des Objekts nicht aktualisieren, behält es die Position und das Volume des letzten Festlegens bei. Wenn die von der App definierte Lebensdauer des Objekts erreicht wurde, wird [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, um die Audiopipeline darüber zu informieren, dass mit diesem Objekt keine weitere Audiodatei geschrieben wird und das Objekt auf **nullptr** festgelegt ist, um seine Ressourcen frei zu machen.

Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, rufen Sie [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) auf, um dem System mitzuteilen, dass die Daten für das Rendering bereit sind. Sie können **GetBuffer nur** zwischen einem Aufruf von **BeginUpdatingAudioObjects** und **EndUpdatingAudioObjects aufrufen.**


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



Wenn Sie mit dem Rendern räumlicher Audiodaten fertig sind, beenden Sie den räumlichen Audiostream, indem Sie [**ISpatialAudioObjectRenderStream::Stop aufrufen.**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop) Wenn Sie den Stream nicht erneut verwenden möchten, geben Sie seine Ressourcen frei, indem Sie [**ISpatialAudioObjectRenderStream::Reset aufrufen.**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Rendern von Audio mit dynamischen räumlichen Audioobjekten für HRTF

Ein weiterer Satz von APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) und [**ISpatialAudioObjectForHrtf,**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)ermöglicht räumliche Audiodaten, die die head-relative Transfer Function (HRTF) von Microsoft verwenden, um Sounds zu dämpfen, um die Position des Emitters im Raum relativ zum Benutzer zu simulieren, die im Laufe der Zeit geändert werden kann. Zusätzlich zur Position können Sie mit HRTF-Audioobjekten eine Ausrichtung im Raum, eine Direktivität, in der Sound ausgegeben wird, wie z. B. eine Kegel- oder Tropenform, und ein Verfallsmodell angeben, wenn sich das Objekt dem virtuellen Listener näher und weiter nähert. Beachten Sie, dass diese HRTF-Schnittstellen nur verfügbar sind, wenn der Benutzer Windows Sonic für Kopfhörer als raumbezogene Audio-Engine für das Gerät ausgewählt hat. Informationen zum Konfigurieren eines Geräts für die Windows Sonic für Kopfhörer finden Sie unter [Spatial Sound](spatial-sound.md).

Mit [**den APIs ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) und [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) kann eine Anwendung den Windows Sonic für Kopfhörer rendern. Diese APIs unterstützen weder räumliche Soundformate wie Dolby Atmos for Home Theater oder Dolby Atmos for Headphones noch den Wechsel des Ausgabeformats über die Sound-Systemsteuerung, noch die Wiedergabe über Lautsprecher.  Diese Schnittstellen sind für die Verwendung in Windows Mixed Reality Anwendungen vorgesehen, die Windows Sonic für Kopfhörer spezifische Funktionen verwenden möchten (z. B. Umgebungsvoreinstellungen und entfernungsbasiertes Rolloff, die programmgesteuert außerhalb typischer Inhaltserstellungspipelines angegeben werden). Die meisten Spiele und Virtual Reality-Szenarien verwenden stattdessen [**ISpatialAudioClient.**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) Die Implementierungsschritte für beide API-Sätze sind fast identisch, sodass es möglich ist, beide Technologien zu implementieren und zur Laufzeit zu wechseln, je nachdem, welches Feature auf dem aktuellen Gerät verfügbar ist.

Mixed Reality-Apps verwenden in der Regel die Position eines 3D-Objekts in der virtuellen Welt, um die Position des dynamischen Audioobjekts anzugeben, das ihm zugeordnet ist. Im folgenden Beispiel wird die einfache Struktur **My3dObjectForHrtf** verwendet, um den Minimaldatensatz zu speichern, der für die Darstellung eines Objekts erforderlich ist. Diese Daten enthalten einen Zeiger auf ein [**ISpatialAudioObjectForHrtf,**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf)die Position, Ausrichtung, Geschwindigkeit und Tonfrequenz für das Objekt und einen Wert, der die Gesamtanzahl von Frames speichert, für die das Objekt Sound rendern soll.


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



Die Implementierungsschritte für dynamische HRTF-Audioobjekte sind größtenteils mit den Schritten für dynamische Audioobjekte identisch, die im vorherigen Abschnitt beschrieben wurden. Zunächst erhalten Sie einen Audioendpunkt.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Initialisieren Sie als Nächstes den räumlichen Audiostream. Rufen Sie eine Instanz von [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) ab, indem [**Sie IMMDevice::Activate aufrufen.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) Rufen Sie [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das die Audiopipeline verwendet, um die App darüber zu informieren, dass sie für weitere Audiodaten bereit ist.

Rufen Sie [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl der vom System unterstützten dynamischen Objekte abzurufen. Wenn dieser Aufruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert. Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl dynamischer Audioobjekte, die für verschiedene räumliche Audioformate verfügbar sind, finden Sie unter [Räumlicher Sound.](spatial-sound.md)

Legen Sie beim Auffüllen der [**SpatialAudioHrtfActivationParams-Struktur**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) das Feld **MaxDynamicObjectCount** auf die maximale Anzahl dynamischer Objekte fest, die Ihre App verwenden wird. Die Aktivierungsparameter für HRTF unterstützen einige zusätzliche Parameter, z. B. [**SpatialAudioHrtfDistanceDecay,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay) [**SpatialAudioHrtfDirectivityUnion,**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion) [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)und [**SpatialAudioHrtfOrientation,**](spatialaudiohrtforientation.md)die die Standardwerte dieser Einstellungen für neue Objekte angeben, die aus dem Stream erstellt werden. Diese Parameter sind optional. Legen Sie die Felder auf **nullptr** fest, um keine Standardwerte anzugeben.

Rufen Sie [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) auf, um den Stream zu aktivieren.


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



Im Folgenden finden Sie einen app-spezifischen Code zur Unterstützung dieses Beispiels, der dynamisch zufällig positionierte Audioobjekte erzeugt und in einem Vektor speichert.


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



Rufen Sie vor dem Eingeben der Audiorenderschleife [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) auf, um die Medienpipeline anzuweisen, mit dem Anfordern von Audiodaten zu beginnen.

Warten Sie innerhalb der Renderschleife auf das Pufferabschlussereignis, das beim Initialisieren des räumlichen Audiodatenstroms angegeben wurde. Sie sollten ein angemessenes Timeoutlimit festlegen, z. B. 100 ms, wenn Sie auf das Ereignis warten, da jede Änderung am Rendertyp oder Endpunkt dazu führt, dass dieses Ereignis nie signalisiert wird. In diesem Fall können Sie [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) aufrufen, um zu versuchen, den räumlichen Audiostream zurückzusetzen.

Rufen Sie als [**Nächstes ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) auf, um das System darüber zu informieren, dass Sie die Puffer der Audioobjekte mit Daten füllen möchten. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frameanzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.

Wenn der Spawn-Indikator den angegebenen Wert erreicht, aktivieren wir ein neues dynamisches Audioobjekt, indem wir [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) aufrufen und [**audioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)angeben. Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **SPLAUDCLNT \_ E NO MORE \_ \_ \_ OBJECTS** zurück. In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer app-spezifischen Priorisierung freigeben. Nachdem das dynamische Audioobjekt erstellt wurde, wird es einer neuen **My3dObjectForHrtf-Struktur** mit zufälligen Werten für Position, Drehung, Geschwindigkeit, Lautstärke und Häufigkeit hinzugefügt, die dann der Liste der aktiven Objekte hinzugefügt wird.

Als Nächstes iterieren Sie alle aktiven Objekte, die in diesem Beispiel mit der von der App definierten **My3dObjectForHrtf-Struktur** dargestellt werden. Rufen Sie für jedes Audioobjekt [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) auf, um einen Zeiger auf den Audiopuffer des räumlichen Audioobjekts abzurufen. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. Die zuvor in diesem Artikel aufgeführte Hilfsmethode **WriteToAudioObjectBuffer,** um den Puffer mit Audiodaten zu füllen. Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position und Ausrichtung des HRTF-Audioobjekts, indem [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) und [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation)aufgerufen werden. In diesem Beispiel wird die Hilfsmethode **CalculateEmitterConeOrientationMatrix** verwendet, um die Ausrichtungsmatrix anhand der Richtung zu berechnen, auf die das 3D-Objekt verweist. Die Implementierung dieser Methode ist unten dargestellt. Die Lautstärke des Audioobjekts kann auch durch Aufrufen von [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain)geändert werden. Wenn Sie position, orientation oder volume des Objekts nicht aktualisieren, behält es position, orientation und volume ab dem zeitpunkt der letzten Festlegung bei. Wenn die von der App definierte Lebensdauer des Objekts erreicht wurde, wird [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) aufgerufen, um die Audiopipeline darüber zu informieren, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden, und das Objekt wird auf **nullptr** festgelegt, um seine Ressourcen freizusetzen.

Nachdem Sie Daten in alle Audioobjekte geschrieben haben, rufen [**Sie ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) auf, um dem System mitzuteilen, dass die Daten zum Rendern bereit sind. Sie können **GetBuffer** nur zwischen einem Aufruf von **BeginUpdatingAudioObjects** und **EndUpdatingAudioObjects** aufrufen.


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



Wenn Sie das Rendern räumlicher Audiodaten abgeschlossen haben, beenden Sie den räumlichen Audiostream, indem Sie [**ISpatialAudioRenderStreamForHrtf::Stop aufrufen.**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)) Wenn Sie den Stream nicht erneut verwenden möchten, können Sie seine Ressourcen freigeben, indem Sie [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85))aufrufen.


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



Das folgende Codebeispiel zeigt die Implementierung der **CalculateEmitterConeOrientationMatrix-Hilfsmethode,** die im obigen Beispiel verwendet wurde, um die Ausrichtungsmatrix anhand der Richtung zu berechnen, in der das 3D-Objekt zeigt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Raumklang](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
