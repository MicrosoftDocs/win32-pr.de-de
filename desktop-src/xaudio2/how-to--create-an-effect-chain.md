---
description: In diesem Thema wird gezeigt, wie Sie eine Wirkungskette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen. In diesem Thema wird beschrieben, wie Sie den Reverb-Effekt verwenden, bei dem es sich um einen der integrierten XAudio2-Effekte handelt.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: "So wird's gemacht: Erstellen einer Effektkette"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129769"
---
# <a name="how-to-create-an-effect-chain"></a>So wird's gemacht: Erstellen einer Effektkette

In diesem Thema wird gezeigt, wie Sie eine Wirkungskette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen. In diesem Thema wird beschrieben, wie Sie den Reverb-Effekt verwenden, bei dem es sich um einen der integrierten XAudio2-Effekte handelt.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>So erstellen Sie eine grundlegende Wirkungskette, die einen Effekt auf eine Stimme anwendet

1.  Erstellen Sie den Effekt.

    In diesem Beispiel erstellt die [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) -Funktion einen Hall Effekt. Eine Liste möglicher Quellen mit Effekten für die Verwendung mit XAudio2 finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md) .

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.

    Wenn sich mehrere Effekte in der Kette befinden, wird für jeden Effekt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) benötigt.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf. In diesem Fall hat die Kette nur einen Effekt. Wenn die Kette mehr als einen Effekt hat, enthält das Element effectcount die Anzahl der Effekte, und das peffectdescriptors-Element verweist auf ein Array von XAUDIO2 \_ Effect- \_ deskriptorstrukturen.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Wenden Sie die Effekt Kette auf eine Stimme mit der Funktion " [**sffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.

    Sie können Effektketten auf Haupt Stimmen, Quell Stimmen und Teil Mischungs Stimmen anwenden.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Geben Sie den Effekt mit IUnknown:: Release frei.

    Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet. Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen. Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird er verworfen, wenn er nicht mehr von XAudio2 verwendet wird. Wenn der Client Code einen Verweis auf die xapo-– beibehalten muss, z. b. zur späteren Wiederverwendung –, sollten Sie diesen Schritt überspringen.

    ```
    pXAPO->Release();
    ```

    

6.  Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf. Der Hall Effekt verwendet eine [**XAUDIO2FX- \_ Hall- \_ Parameter**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) Struktur.

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Deaktivieren oder aktivieren Sie den Effekt, wenn dies angemessen ist.

    Sie können [**disableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) jederzeit verwenden, um einen Effekt zu deaktivieren.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Sie können einen Effekt mit [**enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)erneut aktivieren.

    ```
    pVoice->EnableEffect(0);
    ```

    

    Mit den Parametern für [**disableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) und [**enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) wird angegeben, welche Auswirkung in der Kette aktiviert oder deaktiviert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Übersicht über xapo](xapo-overview.md)
</dt> <dt>

[Gewusst wie: Verwenden von xaopfx in XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[Gewusst wie: Verwenden eines xaop in XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
