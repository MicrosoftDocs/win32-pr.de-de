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
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Rendering von räumlichem Sound mithilfe räumlicher Audioobjekte

In diesem Artikel werden einige einfache Beispiele vorgestellt, die veranschaulichen, wie räumlicher Sound mit statischen räumlichen Audioobjekten, dynamischen räumlichen Audioobjekten und räumlichen Audioobjekten implementiert werden, die die Head relative Transfer Function (HRTF) von Microsoft verwenden. Die Implementierungs Schritte für alle drei dieser Techniken sind sehr ähnlich, und dieser Artikel enthält ein ähnlich strukturiertes Codebeispiel für jede Technik. Vollständige End-to-End-Beispiele für reale räumliche audioimplementierungen finden Sie unter [Microsoft Spatial Sound Samples GitHub Repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio). Eine Übersicht über Windows Sonic, die Plattform auf Platt Form Ebene von Microsoft für räumliche Audiounterstützung auf Xbox und Windows, finden Sie unter [räumlicher Sound](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Audiodarstellung mit statischen räumlichen Audioobjekten

Ein statisches Audioobjekt wird verwendet, um Sound in einem von 18 statischen Audiokanälen zu erzeugen, die in der [**audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) -Enumeration definiert sind. Jeder dieser Kanäle stellt einen echten oder virtualisierten Referenten an einem festgelegten Raum dar, der sich nicht im Laufe der Zeit bewegt. Die statischen Kanäle, die auf einem bestimmten Gerät verfügbar sind, hängen vom verwendeten räumlichen Audioformat ab. Eine Liste der unterstützten Formate und deren Anzahl von Kanälen finden Sie unter [räumlicher Sound](spatial-sound.md).

Wenn Sie einen räumlichen Audiostream initialisieren, müssen Sie angeben, welche der verfügbaren statischen Kanäle der Stream verwenden soll. Die folgenden Beispiel Konstanten Definitionen können verwendet werden, um allgemeine Sprecher Konfigurationen anzugeben und die Anzahl der verfügbaren Kanäle für jede zu erhalten.


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



Der erste Schritt beim Rendern räumlicher Audiodaten besteht darin, den audioendpunkt zu erhalten, an den Audiodaten gesendet werden. Erstellen Sie eine Instanz von [**mmdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) , und rufen Sie [**getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) auf, um das standardaudiorendering-Gerät abzurufen.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Wenn Sie einen räumlichen Audiodatenstrom erstellen, müssen Sie das Audioformat angeben, das der Stream verwenden soll, indem Sie eine [WaveFormatEx](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) -Struktur bereitstellen. Wenn Sie Audiodaten aus einer Datei wiedergeben, wird das Format normalerweise durch das Audiodateiformat bestimmt. In diesem Beispiel wird ein Mono-, 32-Bit-, 48 Hz-Format verwendet.


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



Der nächste Schritt beim Rendern von räumlichem audiovorgang besteht darin, einen räumlichen Audiodatenstrom zu initialisieren. Rufen Sie zuerst eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab. Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.

Füllt eine [**spatialaudioobjectrenderstreamactivationparameams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) -Struktur auf, die zum Initialisieren des räumlichen Audiostreams verwendet wird. In diesem Beispiel wird das Feld **staticobjecttypemask** auf die zuvor in diesem Artikel definierte typkonstante **channelmask \_** festgelegt, was bedeutet, dass nur der Front-Right-und der linke Kanal vom Audiodatenstrom verwendet werden können. Da in diesem Beispiel nur statische Audioobjekte und keine dynamischen Objekte verwendet werden, wird das Feld **maxdynamicobjectcount** auf 0 festgelegt. Das **Kategoriefeld** ist auf einen Member der [**Audiodaten \_ Strom- \_ kategorienumeration**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) festgelegt, der definiert, wie das System den Sound aus diesem Stream mit anderen Audioquellen vermischt.

Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.


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
> Wenn Sie die [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) -Schnittstellen für einen Xbox One Development Kit (XDK)-Titel verwenden, müssen Sie zuerst **enablespatialaudio** aufrufen, bevor Sie [**immdeviceenumerator:: enumaudioendpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) oder [**immdeviceenumerator:: getdefaultaudioendpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint)aufrufen. Wenn dies nicht der Fall ist, wird ein E \_ nointerface-Fehler vom aufzurufenden Aktivierungsbefehl zurückgegeben. **Enablespatialaudioist** nur für XDK-Titel verfügbar und muss nicht für universelle Windows-Plattform apps, die auf Xbox One ausgeführt werden, oder für nicht-Xbox one-Geräte aufgerufen werden.

 

Deklarieren Sie einen Zeiger für ein [**ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) , das zum Schreiben von Audiodaten in einen statischen Kanal verwendet wird. Typische Apps verwenden ein-Objekt für jeden Kanal, der im Feld **staticobjecttypemask** angegeben wird. Der Einfachheit halber wird in diesem Beispiel nur ein einzelnes statisches Audioobjekt verwendet.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen. In diesem Beispiel wird ein-Counter verwendet, um das Rendering von Audiodaten nach fünf Sekunden zu unterbinden.

Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das bereitgestellt wurde, als der räumliche Audiostream initialisiert wurde, signalisiert werden soll. Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird. In diesem Fall kann [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufgerufen werden, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.

Nennen Sie als nächstes [**ispatialaudioobjectrenderstream:: beginupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frame Anzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.

Wenn noch kein statisches räumliches Audioobjekt erstellt wurde, erstellen Sie ein oder mehrere, indem Sie [**ispatialaudioobjectrenderstream:: activatespatialaudioobject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject)aufrufen, und übergeben Sie einen Wert aus der [**audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) -Enumeration, die den statischen Kanal angibt, in dem die Audioobjekt-Audiodatei gerendert wird.

Anschließend wird [**ispatialaudioobject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) aufgerufen, um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. In diesem Beispiel wird eine Hilfsmethode, " **Write tedeaudioobjectbuffer**", verwendet, um den Puffer mit Audiodaten zu füllen. Diese Methode wird weiter unten in diesem Artikel gezeigt. Nach dem Schreiben in den Puffer überprüft das Beispiel, ob die 5-Sekunden-Lebensdauer des-Objekts erreicht wurde. wenn dies der Fall ist, wird [**ispatialaudioobject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden und das-Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.

Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, nennen Sie [**ispatialaudioobjectrenderstream:: endupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , damit das System weiß, dass die Daten für das Rendering bereit sind. Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.


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



Wenn Sie mit dem Rendern räumlicher Audiodaten abgeschlossen sind, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudioobjectrenderstream:: beenden**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)aufrufen. Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)freigeben.


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



Die hilfsprogrammmethode " **Write-deaudioobjectbuffer** " schreibt entweder einen vollständigen Puffer von Beispielen oder die Anzahl der verbleibenden Stichproben, die durch das von der APP definierte Zeit Limit angegeben werden. Dies kann z. b. auch durch die Anzahl der in einer Quellaudiodatei verbleibenden Beispiele bestimmt werden. Eine einfache Sin-Wave wird generiert und in den Puffer geschrieben, um die Häufigkeit zu skalieren, die durch den *Frequency* -Eingabeparameter skaliert wird.


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Audiodarstellung mit dynamischen räumlichen Audioobjekten

Dynamische Objekte ermöglichen es Ihnen, Audiodaten von einer beliebigen Position im Raum relativ zum Benutzer zu übernehmen. Die Position und das Volume eines dynamischen audioobjekts können im Laufe der Zeit geändert werden. Spiele verwenden normalerweise die Position eines 3D-Objekts in der Spiel Welt, um die Position des ihm zugeordneten dynamischen audioobjekts anzugeben. Im folgenden Beispiel wird eine einfache Struktur, **My3dObject**, verwendet, um den minimalen Satz von Daten zu speichern, die für die Darstellung eines Objekts erforderlich sind. Diese Daten umfassen einen Zeiger auf ein [**ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), die Position, die Geschwindigkeit, das Volume und die Tonfrequenz für das Objekt sowie einen Wert, der die Gesamtzahl der Frames speichert, für die das Objekt Sound gerenden Sound erzeugen soll.


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



Die Implementierungs Schritte für dynamische Audioobjekte sind größtenteils mit den Schritten für statische Audioobjekte identisch, die oben beschrieben werden. Zuerst sollten Sie einen audioendpunkt erhalten.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Initialisieren Sie als nächstes den räumlichen Audiodatenstrom. Rufen Sie eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab. Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.

Rufen Sie [**ispatialaudioclient:: getmaxdynamicobjectcount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl von dynamischen Objekten abzurufen, die vom System unterstützt werden. Wenn dieser Rückruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert. Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl der dynamischen Audioobjekte, die für unterschiedliche räumliche Audioformate verfügbar sind, finden Sie unter [Spatial Sound](spatial-sound.md).

Legen Sie beim Auffüllen der [**spatialaudioobjectrenderstreamactivationparser**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) -Struktur das Feld **maxdynamicobjectcount** auf die maximale Anzahl dynamischer Objekte fest, die von Ihrer APP verwendet werden.

Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.


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



Im folgenden finden Sie eine Reihe von Anwendungs spezifischem Code, der die Unterstützung dieses Beispiels benötigt, mit dem zufällig positionierte Audioobjekte dynamisch erzeugt und in einem Vektor gespeichert werden.


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



Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen.

Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das wir bereitgestellt haben, als der räumliche Audiostream initialisiert wurde, um signalisiert zu werden. Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird. In diesem Fall kann [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) aufgerufen werden, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.

Nennen Sie als nächstes [**ispatialaudioobjectrenderstream:: beginupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte und die Frame Anzahl des Puffers für Audioobjekte zurück, die von diesem Stream gerendert werden.

Wenn der "Spawn"-Leistungswert den angegebenen Wert erreicht, wird ein neues dynamisches Audioobjekt durch Aufrufen von [**ispatialaudioobjectrenderstream:: activatespatialaudioobject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) mit [**\_ dynamischem audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)-Objekt aktiviert. Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **splaudclnt \_ E \_ keine \_ weiteren \_ Objekte** zurück. In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer APP-spezifischen Priorisierung freigeben. Nachdem das dynamische Audioobjekt erstellt wurde, wird es zu einer neuen **My3dObject** -Struktur hinzugefügt, wobei zufällige Positions-, Geschwindigkeits-, Volume-und Häufigkeits Werte erstellt werden, die dann der Liste der aktiven-Objekte hinzugefügt werden.

Anschließend durchlaufen Sie alle aktiven-Objekte, die in diesem Beispiel mit der von der APP definierten **My3dObject** -Struktur dargestellt werden. Aufrufen Sie für jedes Audioobjekt [**ispatialaudioobject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) , um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. Die Hilfsmethode, " **Write tedeaudioobjectbuffer**", um den Puffer mit Audiodaten zu füllen. Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position des dynamischen audioobjekts durch Aufrufen von [**ispatialaudioobject:: SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). Das Volume des audioobjekts kann auch durch Aufrufen von [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume)geändert werden. Wenn Sie die Position oder das Volume des Objekts nicht aktualisieren, werden die Position und das Volume von der letzten Festlegung beibehalten. Wenn die von der APP definierte Lebensdauer des Objekts erreicht wurde, wird [**ispatialaudioobject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden, und das Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.

Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, nennen Sie [**ispatialaudioobjectrenderstream:: endupdatingaudioobjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) , damit das System weiß, dass die Daten für das Rendering bereit sind. Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.


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



Wenn Sie mit dem Rendern räumlicher Audiodaten abgeschlossen sind, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudioobjectrenderstream:: beenden**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop)aufrufen. Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudioobjectrenderstream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset)freigeben.


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Audiodarstellung mit dynamischen räumlichen Audioobjekten für HRTF

Ein weiterer Satz von APIs, [**ispatialaudiorenderstreamforhrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) und [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), ermöglicht das räumliche Audio, das die Head-relative Transfer Function (HRTF) von Microsoft zum Simulieren von Sounds verwendet, um die Position des Emitters im Raum relativ zu dem Benutzer zu simulieren, der im Laufe der Zeit geändert werden kann. Neben der Position können Sie mithilfe von HRTF-Audioobjekten eine Ausrichtung im Bereich angeben, eine directivität, in der ein Sound ausgegeben wird, z. b. eine Kegel-oder eine karoid-Form, und ein Zerfalls Modell, wenn sich das Objekt näher und weiter vom virtuellen Listener bewegt. Beachten Sie, dass diese HRTF-Schnittstellen nur verfügbar sind, wenn der Benutzer Windows Sonic for-Kopfhörer als räumliche Audioengine für das Gerät ausgewählt hat. Informationen zum Konfigurieren eines Geräts für die Verwendung von Windows Sonic für Kopfhörer finden Sie unter [räumlicher Sound](spatial-sound.md).

Mit den [**ispatialaudiorenderstreamforhrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) -und [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) -APIs kann eine Anwendung explizit den Windows-Sound für den Kopfhörer-Rendering-Pfad direkt verwenden. Diese APIs unterstützen keine räumlichen Audioformate, wie z. b. Dolby Atmos für das Heim Theater oder Dolby Atmos für Kopfhörer, und weder das Consumer-gesteuerte Ausgabeformat auch **über die** Audiosteuerelement-Systemsteuerung. Diese Schnittstellen sind für die Verwendung in Windows Mixed Reality-Anwendungen gedacht, bei denen Windows Sonic für Kopf fachspezifische Funktionen verwendet werden soll (z. b. Umgebungseinstellungen und Entfernungs basierte Rolloff, die außerhalb der typischen Inhalts Erstellungs Pipelines Programm gesteuert angegeben sind). Die meisten Spiele-und Virtual Reality-Szenarien bevorzugen stattdessen die Verwendung von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) . Die Implementierungs Schritte für beide API-Sätze sind fast identisch, sodass beide Technologien implementiert und zur Laufzeit gewechselt werden können, je nachdem, welche Funktion auf dem aktuellen Gerät verfügbar ist.

Mixed-Reality-Apps verwenden normalerweise die Position eines 3D-Objekts in der virtuellen Welt, um die Position des zugeordneten dynamischen audioobjekts anzugeben. Im folgenden Beispiel wird eine einfache Struktur, **My3dObjectForHrtf**, verwendet, um den minimalen Satz von Daten zu speichern, die für die Darstellung eines Objekts erforderlich sind. Diese Daten umfassen einen Zeiger auf ein [**ispatialaudioobjectforhrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), die Position, die Ausrichtung, die Geschwindigkeit und die Tonfrequenz für das Objekt sowie einen Wert, der die Gesamtzahl der Frames speichert, für die das Objekt Sound gerenden Sound erzeugen soll.


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



Die Implementierungs Schritte für dynamische HRTF-Audioobjekte sind größtenteils mit den Schritten für dynamische Audioobjekte identisch, die im vorherigen Abschnitt beschrieben wurden. Zuerst sollten Sie einen audioendpunkt erhalten.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Initialisieren Sie als nächstes den räumlichen Audiodatenstrom. Rufen Sie eine Instanz von [**ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) durch Aufrufen von [**immdevice:: Aktivierung**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)ab. Rufen Sie [**ispatialaudioclient:: isaudioobjectformatsupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) auf, um sicherzustellen, dass das von Ihnen verwendete Audioformat unterstützt wird. Erstellen Sie ein Ereignis, das von der audiopipeline verwendet wird, um die APP zu benachrichtigen, dass Sie für weitere Audiodaten bereit ist.

Rufen Sie [**ispatialaudioclient:: getmaxdynamicobjectcount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) auf, um die Anzahl von dynamischen Objekten abzurufen, die vom System unterstützt werden. Wenn dieser Rückruf 0 zurückgibt, werden dynamische räumliche Audioobjekte auf dem aktuellen Gerät nicht unterstützt oder aktiviert. Informationen zum Aktivieren räumlicher Audiodaten und Details zur Anzahl der dynamischen Audioobjekte, die für unterschiedliche räumliche Audioformate verfügbar sind, finden Sie unter [Spatial Sound](spatial-sound.md).

Legen Sie beim Auffüllen der [**spatialaudiohrtfactivationparameams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) -Struktur das Feld **maxdynamicobjectcount** auf die maximale Anzahl dynamischer Objekte fest, die von Ihrer APP verwendet werden. Die Aktivierungs Parameter für HRTF unterstützen einige zusätzliche Parameter, z. b. " [**spatialaudiohrtfdistancedecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay)", " [**spatialaudiohrtfdirectivityunion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion)", " [**spatialaudiohrtfumgebungstyp**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)" und " [**spatialaudiohrtforientation**](spatialaudiohrtforientation.md)", die die Standardwerte dieser Einstellungen für neue Objekte angeben, die aus dem Stream erstellt werden. Diese Parameter sind optional. Legen Sie die Felder auf **nullptr** fest, um keine Standardwerte bereitzustellen.

Nennen Sie [**ispatialaudioclient:: activatespatialaudiostream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) , um den Stream zu aktivieren.


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



Im folgenden finden Sie eine Reihe von Anwendungs spezifischem Code, der die Unterstützung dieses Beispiels benötigt, mit dem zufällig positionierte Audioobjekte dynamisch erzeugt und in einem Vektor gespeichert werden.


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



Bevor Sie die audiorenderschleife eingeben, müssen Sie [**ispatialaudioobjectrenderstreamforhrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) aufrufen, um die Medien Pipeline anzuweisen, mit der Anforderung von Audiodaten zu beginnen.

Warten Sie innerhalb der Renderschleife auf das Puffer Abschluss Ereignis, das wir bereitgestellt haben, als der räumliche Audiostream initialisiert wurde, um signalisiert zu werden. Beim Warten auf das Ereignis sollten Sie ein angemessenes Timeout Limit wie 100 MS festlegen, da jede Änderung an rendertyp oder Endpunkt bewirkt, dass dieses Ereignis nie signalisiert wird. In diesem Fall können Sie [**ispatialaudiorenderstreamforhrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) aufrufen, um zu versuchen, den räumlichen Audiodatenstrom zurückzusetzen.

Nennen Sie als nächstes [**ispatialaudiorenderstreamforhrtf:: beginupdatingaudioobjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) , damit das System weiß, dass Sie die Puffer der Audioobjekte mit Daten füllen. Diese Methode gibt die Anzahl der verfügbaren dynamischen Audioobjekte zurück, die in diesem Beispiel nicht verwendet werden, und die Frame Anzahl des Puffers für Audioobjekte, die von diesem Stream gerendert werden.

Wenn der fektionsindikator den angegebenen Wert erreicht, wird ein neues dynamisches Audioobjekt durch Aufrufen von [**ispatialaudiorenderstreamforhrtf:: activatespatialaudioobjectforhrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) mit [**\_ dynamischem audioobjecttype**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype)-Objekt aktiviert. Wenn alle verfügbaren dynamischen Audioobjekte bereits zugeordnet wurden, gibt diese Methode **splaudclnt \_ E \_ keine \_ weiteren \_ Objekte** zurück. In diesem Fall können Sie ein oder mehrere zuvor aktivierte Audioobjekte basierend auf Ihrer APP-spezifischen Priorisierung freigeben. Nachdem das dynamische Audioobjekt erstellt wurde, wird es einer neuen **My3dObjectForHrtf** -Struktur mit zufälligen Positions-, Drehungs-, Geschwindigkeits-, Volume-und Häufigkeits Werten hinzugefügt, die dann der Liste der aktiven-Objekte hinzugefügt werden.

Anschließend durchlaufen Sie alle aktiven-Objekte, die in diesem Beispiel mit der von der APP definierten **My3dObjectForHrtf** -Struktur dargestellt werden. Aufrufen Sie für jedes Audioobjekt [**ispatialaudioobjectforhrtf:: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) , um einen Zeiger auf den Audiopuffer des räumlichen audioobjekts zu erhalten. Diese Methode gibt auch die Größe des Puffers in Bytes zurück. Die zuvor in diesem Artikel aufgeführte Hilfsmethode " **Write tedeaudioobjectbuffer**", um den Puffer mit Audiodaten zu füllen. Nach dem Schreiben in den Puffer aktualisiert das Beispiel die Position und Ausrichtung des HRTF-audioobjekts durch Aufrufen von [**ispatialaudioobjectforhrtf:: SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) und [**ispatialaudioobjectforhrtf:: setOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). In diesem Beispiel wird eine **Hilfsmethode calculateemitterkoneorientationmatrix** verwendet, um die Orientierungs Matrix anhand der Richtung zu berechnen, auf die das 3D-Objekt zeigt. Die Implementierung dieser Methode wird unten dargestellt. Das Volume des audioobjekts kann auch durch Aufrufen von [**ispatialaudioobjectforhrtf:: setgewinn**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain)geändert werden. Wenn Sie die Position, die Ausrichtung oder das Volume des Objekts nicht aktualisieren, werden die Position, die Ausrichtung und das Volume vom Zeitpunkt der letzten Festlegung beibehalten. Wenn die von der APP definierte Lebensdauer des Objekts erreicht ist, wird [**ispatialaudioobjectforhrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) aufgerufen, damit die audiopipeline weiß, dass mit diesem Objekt keine weiteren Audiodaten geschrieben werden, und das Objekt auf **nullptr** festgelegt wird, um die Ressourcen freizugeben.

Nachdem Sie Daten in alle Ihre Audioobjekte geschrieben haben, müssen Sie [**ispatialaudiorenderstreamforhrtf:: endupdatingaudioobjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) aufrufen, um dem System mitzuteilen, dass die Daten für das Rendering bereit sind. Sie können **GetBuffer** nur zwischen einem Aufrufen von **beginupdatingaudioobjects** und **endupdatingaudioobjects** aufrufen.


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



Wenn Sie das Rendering räumlicher Audiodaten abgeschlossen haben, beenden Sie den räumlichen Audiostream, indem Sie [**ispatialaudiorenderstreamforhrtf:: beenden**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85))aufrufen. Wenn Sie den Stream nicht mehr verwenden möchten, können Sie die Ressourcen durch Aufrufen von [**ispatialaudiorenderstreamforhrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85))freigeben.


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



Das folgende Codebeispiel zeigt die Implementierung der **Hilfsmethode calculateemitterkoneorientationmatrix** , die im obigen Beispiel verwendet wurde, um die Orientierungs Matrix anhand der Richtung zu berechnen, auf die das 3D-Objekt zeigt.


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

[**Ispatialaudioclient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**Ispatialaudioobject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
