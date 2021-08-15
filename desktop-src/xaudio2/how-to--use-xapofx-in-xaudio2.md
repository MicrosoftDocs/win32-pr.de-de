---
description: In diesem Thema erfahren Sie, wie Sie einen der in XAPOFX enthaltenen Effekte in einer XAudio2-Effektkette verwenden.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: "So wird's gemacht: Verwenden von XAPOFX in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618e508d5e023c29c373193aa38da9d0e7f9f76c94a57f63e50df0c346426b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696151"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>So wird's gemacht: Verwenden von XAPOFX in XAudio2

In diesem Thema erfahren Sie, wie Sie einen der in XAPOFX enthaltenen Effekte in einer XAudio2-Effektkette verwenden.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>So verwenden Sie einen Effekt von XAPOFX in einer XAudio2-Effektkette

1.  Erstellen Sie den Effekt, indem Sie die CLSID eines XAPOFX-Effekts an die [**CreateFX-Funktion**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) übergeben.

    In diesem Fall wird der vereinfachte Halleffekt FXReverb erstellt.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Füllen Sie eine [**XAUDIO2 \_ EFFECT \_ DESCRIPTOR-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Füllen Sie eine [**XAUDIO2 \_ EFFECT \_ CHAIN-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) mit Daten auf.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Wenden Sie die Effektkette mit der [**SetEffectChain-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) auf eine XAudio2-Stimme an.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Sie können eine Effektkette auch auf eine Stimme anwenden, wenn Sie die Stimme erstellen, indem Sie die Kette als Parameter an [**IXAudio2::CreateSourceVoice,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)oder [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergeben.

     

5.  Geben Sie den Effekt mit IUnknown::Release frei. Wenn Sie eine XAPO erstellen, hat sie den Verweiszähler 1. Wenn der XAPO-Wert mit [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)an XAudio2 übergeben wird, erhöht XAudio2 die Verweisanzahl für den XAPO-Wert. Durch die Freigabe des Clientverweises auf die XAPO kann XAudio2 den Besitz des XAPO übernehmen. Wenn XAudio2 den einzigen Verweis auf die XAPO hat, wird dieser Verweis verworfen, wenn er nicht mehr von XAudio2 verwendet wird. Wenn der Clientcode einen Verweis auf die XAPO verwalten muss , z. B. zur späteren Wiederverwendung, können Sie diesen Schritt überspringen.

    ```
    pXAPO->Release();
    ```

    

6.  Füllen Sie die Dem Effekt zugeordnete Parameterstruktur auf, sofern diese noch nicht angegeben ist.

    In diesem Fall wird die [**FXREVERB \_ PARAMETERS-Struktur**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) verwendet, um die Größe des Halleffekts und der Raumgröße zu bestimmen.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Übergeben Sie die Effect-Parameterstruktur an den Effekt, indem Sie die [**Funktion SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) für die Stimme aufrufen, an die der Effekt angefügt ist.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
