---
description: In diesem Thema wird gezeigt, wie X3DAudio mit XAudio2 integriert wird.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: "So wird's gemacht: Integrieren von X3DAudio in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc54fa5f673e319712808ca6d2b587b8ad2d0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757692"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a><span data-ttu-id="f9a73-103">So wird's gemacht: Integrieren von X3DAudio in XAudio2</span><span class="sxs-lookup"><span data-stu-id="f9a73-103">How to: Integrate X3DAudio with XAudio2</span></span>

<span data-ttu-id="f9a73-104">In diesem Thema wird gezeigt, wie X3DAudio mit XAudio2 integriert wird.</span><span class="sxs-lookup"><span data-stu-id="f9a73-104">This topic shows how to integrate X3DAudio with XAudio2.</span></span> <span data-ttu-id="f9a73-105">Sie können X3DAudio verwenden, um die Werte für das Volume und den Wert für XAudio2 Stimmen und die Parameter für den XAudio2, der in den Reverb-Effekt integriert ist</span><span class="sxs-lookup"><span data-stu-id="f9a73-105">You can use X3DAudio to provide the volume and pitch values for XAudio2 voices and the parameters for the XAudio2 built in reverb effect.</span></span> <span data-ttu-id="f9a73-106">In diesem Thema wird davon ausgegangen, dass Sie ein audiodiagramm erstellt haben, wie unter Gewusst [wie: Erstellen eines einfachen audioverarbeitungdiagramms](how-to--build-a-basic-audio-processing-graph.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f9a73-106">This topic assumes that you have created an audio graph as described in [How to: Build a Basic Audio Processing Graph](how-to--build-a-basic-audio-processing-graph.md).</span></span> <span data-ttu-id="f9a73-107">Wenn Sie noch kein audiodiagramm erstellt haben, schlägt [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) fehl.</span><span class="sxs-lookup"><span data-stu-id="f9a73-107">If you have not already created an audio graph, [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) will fail.</span></span>

<span data-ttu-id="f9a73-108">**So initialisieren Sie X3DAudio**</span><span class="sxs-lookup"><span data-stu-id="f9a73-108">**To initialize X3DAudio**</span></span>

1.  <span data-ttu-id="f9a73-109">Initialisieren Sie X3DAudio durch Aufrufen von [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span><span class="sxs-lookup"><span data-stu-id="f9a73-109">Initialize X3DAudio by calling [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).</span></span>

    <span data-ttu-id="f9a73-110">Die [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) -Funktion übernimmt Flags, die die Lautsprecher Einrichtung angeben, die Geschwindigkeit des Sounds in benutzerdefinierten Welteinheiten pro Sekunde und ein Handle, um eine Instanz der X3DAudio-Engine zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="f9a73-110">The [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) function takes flags indicating the speaker setup, the speed of sound in user-defined world units per second, and a handle to return an instance of the X3DAudio engine.</span></span> <span data-ttu-id="f9a73-111">Aufrufen von [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) zum Abrufen der Kanalmaske des Ausgabeformats.</span><span class="sxs-lookup"><span data-stu-id="f9a73-111">Call [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) to get the output format's channel mask.</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  <span data-ttu-id="f9a73-112">Erstellen Sie Instanzen der [**X3DAUDIO- \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) -und [**X3DAUDIO- \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="f9a73-112">Create instances of the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span>

    <span data-ttu-id="f9a73-113">Die [**X3DAUDIO- \_ listenerstruktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) stellt die Position dar, an der der Ton gehört.</span><span class="sxs-lookup"><span data-stu-id="f9a73-113">The [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) structure represents the position of whatever is hearing the sound.</span></span> <span data-ttu-id="f9a73-114">Im Allgemeinen ist dies die Position der Kamera oder eine Position in der Nähe.</span><span class="sxs-lookup"><span data-stu-id="f9a73-114">Generally, this is the position of the camera or a position close to it.</span></span> <span data-ttu-id="f9a73-115">Die [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) -Struktur stellt die Position der Sache dar, die den Sound macht.</span><span class="sxs-lookup"><span data-stu-id="f9a73-115">The [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structure represents the position of the thing making the sound.</span></span> <span data-ttu-id="f9a73-116">Es gibt eine **X3DAUDIO- \_ Emitter** -Struktur für jeden Sound, der nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f9a73-116">There will be one **X3DAUDIO\_EMITTER** structure for each sound that is being tracked.</span></span>

    <span data-ttu-id="f9a73-117">Member der Strukturen, die in einer Spiel Schleife nicht aktualisiert werden, sollten hier initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-117">Members of the structures that will not be updated in a game loop should be initialized here.</span></span> <span data-ttu-id="f9a73-118">Die meisten Member der Strukturen können einfach mit 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-118">Most members of the structures can simply be initialized to zero.</span></span> <span data-ttu-id="f9a73-119">Einige Member von [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) müssen jedoch so festgelegt werden, dass Sie mit Werten ungleich 0 (null) initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-119">However, some members of [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) need to be set to be initialized to non-zero values.</span></span> <span data-ttu-id="f9a73-120">Das ChannelCount-Element des **X3DAUDIO- \_ emitters** muss mit der Anzahl der Kanäle in der vom EMITTER dargestellten Sprache initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-120">The ChannelCount member of the **X3DAUDIO\_EMITTER** needs to be initialized to the number of channels in the voice the emitter represents.</span></span> <span data-ttu-id="f9a73-121">Außerdem muss der Member "Cursor" von " **X3DAUDIO \_ Emitter** " im Bereich "FLT \_ min bis FLT Max" liegen \_ .</span><span class="sxs-lookup"><span data-stu-id="f9a73-121">Also, the CurveDistanceScaler member of **X3DAUDIO\_EMITTER** must be in the range FLT\_MIN to FLT\_MAX.</span></span>

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  <span data-ttu-id="f9a73-122">Erstellen Sie eine Instanz der [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur.</span><span class="sxs-lookup"><span data-stu-id="f9a73-122">Create an instance of the [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure.</span></span>

    <span data-ttu-id="f9a73-123">Die [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur wird verwendet, um Ergebnisse zurückzugeben, die von [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-123">The [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure is used to return results calculated by [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate).</span></span> <span data-ttu-id="f9a73-124">Die **X3DAudioCalculate** -Funktion weist keinen Arbeitsspeicher für einen ihrer Parameter zu.</span><span class="sxs-lookup"><span data-stu-id="f9a73-124">The **X3DAudioCalculate** function does not allocate memory for any of its parameters.</span></span> <span data-ttu-id="f9a73-125">Dies bedeutet, dass Sie Arrays für die pmatrixkoefficients-und pdelta Time-Member der **X3DAUDIO \_ DSP- \_ Einstellungs** Struktur zuordnen müssen, wenn Sie beabsichtigen, Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-125">This means that you need to allocate arrays for the **X3DAUDIO\_DSP\_SETTINGS** structure's pMatrixCoefficients and pDelayTimes members if you intend to use them.</span></span> <span data-ttu-id="f9a73-126">Außerdem müssen Sie die Elemente srcchannelcount und dstchannelcount auf die Anzahl der Kanäle in den Quell-und Ziel Stimmen des Emitters festlegen.</span><span class="sxs-lookup"><span data-stu-id="f9a73-126">In addition, you need to set the SrcChannelCount and DstChannelCount members to the number of channels in the emitter's source and destination voices.</span></span>

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > <span data-ttu-id="f9a73-127">Verwenden Sie [**IXAudio2Voice:: getvoicedetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) auf der Mastering-Stimme, um die Anzahl der Input Channels für **nchannels** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9a73-127">Use [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) on the mastering voice to obtain the number of InputChannels for **nChannels**.</span></span> <span data-ttu-id="f9a73-128">Verwenden Sie für DirectX SDK-Versionen von XAUDIO2 vor Windows 8 IXAudio2:: getdevicedetails.</span><span class="sxs-lookup"><span data-stu-id="f9a73-128">For DirectX SDK versions of XAUDIO2 prior to Windows 8, use IXAudio2::GetDeviceDetails.</span></span>

     

<span data-ttu-id="f9a73-129">Führen Sie diese Schritte einmal alle zwei bis drei Rahmen aus, um neue Einstellungen zu berechnen und anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-129">Perform these steps once every two to three frames to calculate new settings and apply them.</span></span> <span data-ttu-id="f9a73-130">In diesem Beispiel sendet eine Quell Stimme direkt an die Stimme der Stimme und an eine teilmischungs-Stimme, auf die Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f9a73-130">In this example, a source voice is sending directly to the mastering voice and to a submix voice with a reverb effect applied to it.</span></span>

<span data-ttu-id="f9a73-131">**So verwenden Sie X3DAudio zum Berechnen und Anwenden neuer 3D-Audioeinstellungen**</span><span class="sxs-lookup"><span data-stu-id="f9a73-131">**To use X3DAudio to calculate and apply new 3D audio settings**</span></span>

1.  <span data-ttu-id="f9a73-132">Aktualisieren Sie die Strukturen [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) mit Ihrer aktuellen Position, Geschwindigkeit und Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="f9a73-132">Update the [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures with their current position, velocity, and orientation.</span></span>

    ```
    Emitter.OrientFront = EmitterOrientFront;
    Emitter.OrientTop = EmitterOrientTop;
    Emitter.Position = EmitterPosition;
    Emitter.Velocity = EmitterVelocity;
    Listener.OrientFront = ListenerOrientFront;
    Listener.OrientTop = ListenerOrientTop;
    Listener.Position = ListenerPosition;
    Listener.Velocity = ListenerVelocity;
    ```

    

2.  <span data-ttu-id="f9a73-133">[**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) , um neue Einstellungen für die Stimmen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="f9a73-133">Call [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) to calculate new settings for the voices.</span></span>

    <span data-ttu-id="f9a73-134">Bei den Parametern für [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) handelt es sich um die aktualisierten Strukturen [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) .</span><span class="sxs-lookup"><span data-stu-id="f9a73-134">The parameters for [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) will be the updated [**X3DAUDIO\_LISTENER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) and [**X3DAUDIO\_EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) structures.</span></span> <span data-ttu-id="f9a73-135">Die Flags geben an, welche Werte **X3DAudioCalculate** berechnen soll und welche [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur die Ergebnisse der durchgeführten Berechnungen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="f9a73-135">The flags will indicate what values **X3DAudioCalculate** should calculate, and which [**X3DAUDIO\_DSP\_SETTINGS**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) structure will hold the results of the calculations performed.</span></span>

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  <span data-ttu-id="f9a73-136">Verwenden Sie [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice:: setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , um das Volume und die Tonwerte auf die Quell Stimme anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-136">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) and [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) to apply the volume and pitch values to the source voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  <span data-ttu-id="f9a73-137">Verwenden Sie [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) , um die berechnete Hall Ebene auf die unter Mischungs Stimme anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-137">Use [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) to apply the calculated reverb level to the submix voice.</span></span>

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  <span data-ttu-id="f9a73-138">Verwenden Sie [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) , um den direkten Koeffizienten für den direkten Pass-Filter-Filter auf die Quell Stimme anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a73-138">Use [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) to apply the calculated low pass filter direct coefficient to the source voice.</span></span>

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f9a73-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9a73-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a73-140">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="f9a73-140">X3DAudio</span></span>](x3daudio.md)
</dt> <dt>

[<span data-ttu-id="f9a73-141">X3DAudio Übersicht</span><span class="sxs-lookup"><span data-stu-id="f9a73-141">X3DAudio Overview</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="f9a73-142">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="f9a73-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="f9a73-143">XAudio2 Volume und Tonhöhe-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f9a73-143">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
