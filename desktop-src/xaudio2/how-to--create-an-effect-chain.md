---
description: In diesem Thema erfahren Sie, wie Sie eine Effektkette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen. In diesem Thema wird beschrieben, wie der Halleffekt verwendet wird, einer der integrierten XAudio2-Effekte.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: "So wird's gemacht: Erstellen einer Effektkette"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abd6372fe07f71d75a4963f6617cdeda15ecf8390e3142fcf110029bd8f6dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838412"
---
# <a name="how-to-create-an-effect-chain"></a>So wird's gemacht: Erstellen einer Effektkette

In diesem Thema erfahren Sie, wie Sie eine Effektkette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen. In diesem Thema wird beschrieben, wie der Halleffekt verwendet wird, einer der integrierten XAudio2-Effekte.

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a>So erstellen Sie eine grundlegende Effektkette, die einen Effekt auf eine Stimme angewendet

1.  Erstellen Sie den Effekt.

    In diesem Beispiel erstellt die [**XAudio2CreateReverb-Funktion**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) einen Halleffekt. Unter [XAudio2 Audio Effects (XAudio2-Audioeffekte)](xaudio2-audio-effects.md) finden Sie eine Liste der möglichen Quellen von Effekten für die Verwendung mit XAudio2.

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  Füllen Sie eine [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.

    Wenn die Kette mehrere Effekte auftrat, benötigt jeder Effekt eine [**XAUDIO2 \_ \_ EFFECT-DESCRIPTOR-Struktur.**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Füllen Sie eine [**XAUDIO2 \_ EFFECT \_ CHAIN-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) mit Daten auf. In diesem Fall hat die Kette nur einen Effekt. Wenn die Kette mehr als einen Effekt hat, enthält das EffectCount-Member die Anzahl der Effekte, und das pEffectDescriptors-Member wird auf ein Array von XAUDIO2 \_ EFFECT \_ DESCRIPTOR-Strukturen verweisen.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Wenden Sie die Effektkette mit der [**SetEffectChain-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) auf eine Stimme an.

    Sie können Effektketten auf Masterstimmen, Quellstimmen und Untermischungsstimmen anwenden.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  Geben Sie den Effekt mit IUnknown::Release frei.

    Wenn Sie eine XAPO erstellen, hat sie den Verweiszähler 1. Wenn der XAPO-Wert mit [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)an XAudio2 übergeben wird, erhöht XAudio2 die Verweisanzahl für den XAPO-Wert. Durch die Freigabe des Clientverweises auf die XAPO kann XAudio2 den Besitz des XAPO übernehmen. Wenn XAudio2 den einzigen Verweis auf die XAPO hat, wird sie verworfen, wenn sie nicht mehr von XAudio2 verwendet wird. Wenn der Clientcode einen Verweis auf die XAPO verwalten muss , z. B. zur späteren Wiederverwendung, sollten Sie diesen Schritt überspringen.

    ```
    pXAPO->Release();
    ```

    

6.  Füllen Sie die Dem Effekt zugeordnete Parameterstruktur auf, sofern diese noch nicht angegeben ist. Der Halleffekt verwendet eine [**XAUDIO2FX \_ REVERB \_ PARAMETERS-Struktur.**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)

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

    

7.  Übergeben Sie die Effect-Parameterstruktur an den Effekt, indem Sie die [**Funktion SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) für die Stimme aufrufen, an die der Effekt angefügt ist.

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  Deaktivieren oder aktivieren Sie den Effekt, wenn dies erforderlich ist.

    Sie können [**DisableEffect jederzeit verwenden,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) um einen Effekt zu deaktivieren.

    ```
    pVoice->DisableEffect(0);
    ```

    

    Sie können einen Effekt mit [**EnableEffect erneut aktivieren.**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)

    ```
    pVoice->EnableEffect(0);
    ```

    

    Die Parameter für [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) und [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) geben an, welche Auswirkung in der Kette aktiviert oder deaktiviert werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Übersicht über XAPO](xapo-overview.md)
</dt> <dt>

[How to: Use XAOPFX in XAudio2](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[How to: Use an XAOP in XAudio2](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
