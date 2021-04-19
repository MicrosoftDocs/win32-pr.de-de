---
description: In diesem Thema wird gezeigt, wie Sie einen mit der xapo-API erstellten Effekt in einer XAudio2 Effect-Kette verwenden.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: "So wird's gemacht: Verwenden eines XAPOs in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353119"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a>So wird's gemacht: Verwenden eines XAPOs in XAudio2

In diesem Thema wird gezeigt, wie Sie einen mit der xapo-API erstellten Effekt in einer XAudio2 Effect-Kette verwenden.

1.  Erstellen Sie den xapo wie unter Gewusst [wie: Erstellen eines xapo](how-to--create-an-xapo.md)beschrieben.

    Sie können auch Lauf Zeitparameter Funktionen implementieren, wie unter Gewusst [wie: Hinzufügen von Lauf Zeitparameter Unterstützung zu xapo](how-to--add-run-time-parameter-support-to-an-xapo.md)beschrieben.

2.  Erstellen Sie eine Instanz von xapo.

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf.

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  Wenden Sie die Effekt Kette auf eine XAudio2-Stimme mit der Funktion " [**setteffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > Eine Wirkungskette kann auch auf eine Stimme angewendet werden, wenn die Stimme erstellt wird, indem Sie die Kette als Parameter an [**IXAudio2:: anatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: anatesubmixvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)oder [**IXAudio2:: smatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergibt.

     

6.  Geben Sie den Effekt mit IUnknown:: Release frei.

    Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet. Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen. Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird er verworfen, wenn er nicht mehr von XAudio2 verwendet wird. Wenn der Client Code z. b. einen Verweis auf das xapo zur späteren Wiederverwendung beibehalten muss, sollten Sie diesen Schritt überspringen.

    ```
    pXAPO->Release();
    ```

    

7.  Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf. In diesem Fall der Prozentsatz der vollständigen Stärke, bei der der Effekt angewendet werden soll.

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioeffekte](audio-effects.md)
</dt> <dt>

[Übersicht über xapo](xapo-overview.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> </dl>

 

 
