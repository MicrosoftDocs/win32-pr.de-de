---
description: In diesem Thema wird gezeigt, wie Sie eine der in xapofx enthaltenen Effekte in einer XAudio2 Effect-Kette verwenden können.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: "So wird's gemacht: Verwenden von XAPOFX in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357379"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a>So wird's gemacht: Verwenden von XAPOFX in XAudio2

In diesem Thema wird gezeigt, wie Sie eine der in xapofx enthaltenen Effekte in einer XAudio2 Effect-Kette verwenden können.

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a>So verwenden Sie einen Effekt von xapofx in einer XAudio2 Effect-Kette

1.  Erstellen Sie den Effekt, indem Sie die CLSID eines xapofx-Effekts an die Funktion " [**kreatefx**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) " übergeben.

    In diesem Fall wird der vereinfachte einhall Effekt fxreverb erstellt.

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  Wenden Sie die Effekt Kette auf eine XAudio2-Stimme mit der Funktion " [**setteffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Sie können auch eine Wirkungskette auf eine Stimme anwenden, wenn Sie die Stimme erstellen, indem Sie die Kette als Parameter an [**IXAudio2:::: anatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: anatesubmixvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)oder [**IXAudio2:: kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergeben.

     

5.  Geben Sie den Effekt mit IUnknown:: Release frei. Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet. Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen. Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird dieser Verweis verworfen, wenn er nicht mehr von XAudio2 verwendet wird. Wenn der Client Code einen Verweis auf die xapo beibehalten muss – z. b. zur späteren Wiederverwendung –, können Sie diesen Schritt überspringen.

    ```
    pXAPO->Release();
    ```

    

6.  Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf.

    In diesem Fall wird die Struktur von [**fxreverb- \_ Parametern**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) verwendet, um die Verbreitung und die Raum Größe festzulegen, die vom-mappeneffekt verwendet werden sollen.

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
