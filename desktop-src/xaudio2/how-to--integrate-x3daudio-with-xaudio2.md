---
description: In diesem Thema wird gezeigt, wie X3DAudio in XAudio2 integriert wird.
ms.assetid: a8f41f0d-b284-aefa-923b-471b13b4a3ec
title: "So wird's gemacht: Integrieren von X3DAudio in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c940acbe78e8d4ca4247f77500adeeca7c9619057a3008dea50fc8b55a9f364e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962689"
---
# <a name="how-to-integrate-x3daudio-with-xaudio2"></a>So wird's gemacht: Integrieren von X3DAudio in XAudio2

In diesem Thema wird gezeigt, wie X3DAudio in XAudio2 integriert wird. Sie können X3DAudio verwenden, um die Lautstärke- und Tonhöhenwerte für XAudio2-Stimmen und die Parameter für den integrierten Halleffekt XAudio2 zur Verfügung zu stellen. In diesem Thema wird davon ausgegangen, dass Sie ein Audiodiagramm erstellt haben, wie unter [How to: Build a Basic Audio Processing Graph .](how-to--build-a-basic-audio-processing-graph.md) Wenn Sie noch kein Audiodiagramm erstellt haben, erzeugt [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) einen Fehler.

**So initialisieren Sie X3DAudio**

1.  Initialisieren Sie X3DAudio, indem Sie [**X3DAudioInitialize aufrufen.**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Die [**X3DAudioInitialize-Funktion**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) verwendet Flags, die die Einrichtung des Lautsprechers, die Geschwindigkeit des Sounds in benutzerdefinierten Welteinheiten pro Sekunde und ein Handle zum Zurückgeben einer Instanz der X3DAudio-Engine angeben. Rufen [**Sie IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) auf, um die Kanalmaske des Ausgabeformats zu erhalten.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       

    X3DAUDIO_HANDLE X3DInstance;
    X3DAudioInitialize( dwChannelMask, X3DAUDIO_SPEED_OF_SOUND, X3DInstance );
    ```

    

2.  Erstellen Sie Instanzen der [**X3DAUDIO \_ LISTENER- und**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) [**X3DAUDIO \_ EMITTER-Strukturen.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

    Die [**X3DAUDIO \_ LISTENER-Struktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) stellt die Position des Sounds dar. Im Allgemeinen ist dies die Position der Kamera oder eine Position in der Nähe. Die [**X3DAUDIO \_ EMITTER-Struktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) stellt die Position des Sounds dar. Es gibt eine **X3DAUDIO \_ EMITTER-Struktur** für jeden Sound, der nachverfolgt wird.

    Member der Strukturen, die nicht in einer Spielschleife aktualisiert werden, sollten hier initialisiert werden. Die meisten Member der Strukturen können einfach mit 0 initialisiert werden. Einige Member von [**X3DAUDIO \_ EMITTER**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) müssen jedoch so festgelegt werden, dass sie auf Werte ohne Null initialisiert werden. Das ChannelCount-Member des **X3DAUDIO-EMITTER \_** muss mit der Anzahl der Kanäle in der Stimme initialisiert werden, die der Emitter darstellt. Außerdem muss das CurveDistanceScaler-Mitglied von **X3DAUDIO \_ EMITTER** im Bereich FLT \_ MIN bis FLT \_ MAX liegen.

    ```
    X3DAUDIO_LISTENER Listener = {0};
    X3DAUDIO_EMITTER Emitter = {0};
    Emitter.ChannelCount = 1;
    Emitter.CurveDistanceScaler = FLT_MIN;
    ```

    

3.  Erstellen Sie eine Instanz der [**X3DAUDIO \_ DSP \_ SETTINGS-Struktur.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)

    Die [**X3DAUDIO \_ DSP \_ SETTINGS-Struktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) wird verwendet, um von [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)berechnete Ergebnisse zurück zu geben. Die **X3DAudioCalculate-Funktion** weist keinen Arbeitsspeicher für einen ihrer Parameter zu. Dies bedeutet, dass Sie Arrays für die pMatrixCoefficients- und pDelayTimes-Member der **X3DAUDIO \_ DSP \_ SETTINGS-Struktur** zuordnen müssen, wenn Sie diese verwenden möchten. Darüber hinaus müssen Sie die Elemente SrcChannelCount und DstChannelCount auf die Anzahl der Kanäle in den Quell- und Zielstimmen des Emitters festlegen.

    ```
    X3DAUDIO_DSP_SETTINGS DSPSettings = {0};
    FLOAT32 * matrix = new FLOAT32[deviceDetails.OutputFormat.Format.nChannels];
    DSPSettings.SrcChannelCount = 1;
    DSPSettings.DstChannelCount = deviceDetails.OutputFormat.Format.nChannels;
    DSPSettings.pMatrixCoefficients = matrix;
    ```

    

    > [!Note]  
    > Verwenden [**Sie IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails) auf der Masterstimme, um die Anzahl der InputChannels für **nChannels zu erhalten.** Verwenden Sie für DirectX SDK-Versionen von XAUDIO2 vor Windows 8 IXAudio2::GetDeviceDetails.

     

Führen Sie diese Schritte alle zwei bis drei Frames aus, um neue Einstellungen zu berechnen und anzuwenden. In diesem Beispiel sendet eine Quellstimme direkt an die Masterstimme und an eine Untermischungsstimme, auf die ein Halleffekt angewendet wird.

**So verwenden Sie X3DAudio zum Berechnen und Anwenden neuer 3D-Audioeinstellungen**

1.  Aktualisieren Sie [**die X3DAUDIO \_ LISTENER-**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ EMITTER-Strukturen**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) mit ihrer aktuellen Position, Geschwindigkeit und Ausrichtung.

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

    

2.  Rufen [**Sie X3DAudioCalculate auf,**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) um neue Einstellungen für die Stimmen zu berechnen.

    Die Parameter für [**X3DAudioCalculate sind**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) die aktualisierten [**X3DAUDIO \_ LISTENER-**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ EMITTER-Strukturen.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) Die Flags geben an, welche **Werte X3DAudioCalculate** berechnen soll und welche [**X3DAUDIO \_ DSP \_ SETTINGS-Struktur**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings) die Ergebnisse der durchgeführten Berechnungen enthält.

    ```
    X3DAudioCalculate(X3DInstance, &Listener, &Emitter,
        X3DAUDIO_CALCULATE_MATRIX | X3DAUDIO_CALCULATE_DOPPLER | X3DAUDIO_CALCULATE_LPF_DIRECT | X3DAUDIO_CALCULATE_REVERB,
        &DSPSettings );
    ```

    

3.  Verwenden [**Sie IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice::SetFrequencyRatio,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) um die Lautstärke- und Tonhöhenwerte auf die Quellstimme anzuwenden.

    ```
    pSFXSourceVoice->SetOutputMatrix( pMasterVoice, 1, deviceDetails.OutputFormat.Format.nChannels, DSPSettings.pMatrixCoefficients ) ;
    pSFXSourceVoice->SetFrequencyRatio(DSPSettings.DopplerFactor);
    ```

    

4.  Verwenden [**Sie IXAudio2Voice::SetOutputMatrix,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) um die berechnete Hallebene auf die Untermischungsstimme anzuwenden.

    ```
    pSFXSourceVoice->SetOutputMatrix(pSubmixVoice, 1, 1, &DSPSettings.ReverbLevel);
    ```

    

5.  Verwenden [**Sie IXAudio2Voice::SetFilterParameters,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) um den berechneten direkten Filterkoeffizienten für den niedrigen Durchgang auf die Quellstimme anzuwenden.

    ```
    XAUDIO2_FILTER_PARAMETERS FilterParameters = { LowPassFilter, 2.0f * sinf(X3DAUDIO_PI/6.0f * DSPSettings.LPFDirectCoefficient), 1.0f };
    pSFXSourceVoice->SetFilterParameters(&FilterParameters);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> <dt>

[Übersicht über X3DAudio](x3daudio-overview.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[XAudio2-Steuerelement für Lautstärke und Tonhöhe](volume-and-pitch-control.md)
</dt> </dl>

 

 
