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
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>So wird's gemacht: Integrieren von X3DAudio in XAudio2

In diesem Thema wird gezeigt, wie X3DAudio mit XAudio2 integriert wird. Sie können X3DAudio verwenden, um die Werte für das Volume und den Wert für XAudio2 Stimmen und die Parameter für den XAudio2, der in den Reverb-Effekt integriert ist In diesem Thema wird davon ausgegangen, dass Sie ein audiodiagramm erstellt haben, wie unter Gewusst [wie: Erstellen eines einfachen audioverarbeitungdiagramms](how-to--build-a-basic-audio-processing-graph.md)beschrieben. Wenn Sie noch kein audiodiagramm erstellt haben, schlägt [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) fehl.

**So initialisieren Sie X3DAudio**

1.  Initialisieren Sie X3DAudio durch Aufrufen von [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize).

    Die [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) -Funktion übernimmt Flags, die die Lautsprecher Einrichtung angeben, die Geschwindigkeit des Sounds in benutzerdefinierten Welteinheiten pro Sekunde und ein Handle, um eine Instanz der X3DAudio-Engine zurückzugeben. Aufrufen von [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) zum Abrufen der Kanalmaske des Ausgabeformats.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Erstellen Sie Instanzen der [**X3DAUDIO- \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) -und [**X3DAUDIO- \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) -Strukturen.

    Die [**X3DAUDIO- \_ listenerstruktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) stellt die Position dar, an der der Ton gehört. Im Allgemeinen ist dies die Position der Kamera oder eine Position in der Nähe. Die [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) -Struktur stellt die Position der Sache dar, die den Sound macht. Es gibt eine **X3DAUDIO- \_ Emitter** -Struktur für jeden Sound, der nachverfolgt wird.

    Member der Strukturen, die in einer Spiel Schleife nicht aktualisiert werden, sollten hier initialisiert werden. Die meisten Member der Strukturen können einfach mit 0 (null) initialisiert werden. Einige Member von [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) müssen jedoch so festgelegt werden, dass Sie mit Werten ungleich 0 (null) initialisiert werden. Das ChannelCount-Element des **X3DAUDIO- \_ emitters** muss mit der Anzahl der Kanäle in der vom EMITTER dargestellten Sprache initialisiert werden. Außerdem muss der Member "Cursor" von " **X3DAUDIO \_ Emitter** " im Bereich "FLT \_ min bis FLT Max" liegen \_ .

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Erstellen Sie eine Instanz der [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur.

    Die [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur wird verwendet, um Ergebnisse zurückzugeben, die von [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)berechnet werden. Die **X3DAudioCalculate** -Funktion weist keinen Arbeitsspeicher für einen ihrer Parameter zu. Dies bedeutet, dass Sie Arrays für die pmatrixkoefficients-und pdelta Time-Member der **X3DAUDIO \_ DSP- \_ Einstellungs** Struktur zuordnen müssen, wenn Sie beabsichtigen, Sie zu verwenden. Außerdem müssen Sie die Elemente srcchannelcount und dstchannelcount auf die Anzahl der Kanäle in den Quell-und Ziel Stimmen des Emitters festlegen.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Verwenden Sie [**IXAudio2Voice:: getvoicedetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) auf der Mastering-Stimme, um die Anzahl der Input Channels für **nchannels** abzurufen. Verwenden Sie für DirectX SDK-Versionen von XAUDIO2 vor Windows 8 IXAudio2:: getdevicedetails.

     

Führen Sie diese Schritte einmal alle zwei bis drei Rahmen aus, um neue Einstellungen zu berechnen und anzuwenden. In diesem Beispiel sendet eine Quell Stimme direkt an die Stimme der Stimme und an eine teilmischungs-Stimme, auf die Sie angewendet wird.

**So verwenden Sie X3DAudio zum Berechnen und Anwenden neuer 3D-Audioeinstellungen**

1.  Aktualisieren Sie die Strukturen [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) mit Ihrer aktuellen Position, Geschwindigkeit und Ausrichtung.

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

    

2.  [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) , um neue Einstellungen für die Stimmen zu berechnen.

    Bei den Parametern für [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) handelt es sich um die aktualisierten Strukturen [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) . Die Flags geben an, welche Werte **X3DAudioCalculate** berechnen soll und welche [**X3DAUDIO \_ DSP- \_ Einstellungs**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) Struktur die Ergebnisse der durchgeführten Berechnungen enthalten soll.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Verwenden Sie [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice:: setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , um das Volume und die Tonwerte auf die Quell Stimme anzuwenden.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Verwenden Sie [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) , um die berechnete Hall Ebene auf die unter Mischungs Stimme anzuwenden.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Verwenden Sie [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) , um den direkten Koeffizienten für den direkten Pass-Filter-Filter auf die Quell Stimme anzuwenden.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[X3DAudio Übersicht](x3daudio-overview.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[XAudio2 Volume und Tonhöhe-Steuerelement](volume-and-pitch-control.md)
</dt> </dl>

 

 
