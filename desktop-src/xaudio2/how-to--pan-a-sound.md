---
description: In diesem Thema wird erläutert, wie Sie die Ausgabe Matrix einer Mono-Quellsprache festlegen können, die in eine Stereo-Mastering-Stimme ausgibt, um das Schwenken zwischen der linken und der rechten sprechenden Seite zu erreichen.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Gewusst wie: Schwenken eines Sounds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866483"
---
# <a name="how-to-pan-a-sound"></a>Gewusst wie: Schwenken eines Sounds

In diesem Thema wird erläutert, wie Sie die Ausgabe Matrix einer Mono-Quellsprache festlegen können, die in eine Stereo-Mastering-Stimme ausgibt, um das Schwenken zwischen der linken und der rechten sprechenden Seite zu erreichen.

## <a name="to-setup-panning"></a>Einrichten von schwenken

1.  Rufen Sie die Sprecher Konfiguration mit [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)ab.

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Erstellen Sie ein Array, das die Ausgabe Matrix enthalten soll. Die minimale Größe der Ausgabe Matrix ist die Anzahl der Kanäle in der Quellsprache und die Anzahl der Kanäle in der Ausgabesprache. In diesem Fall behandelt ein 8-Element-Array eine Mono-Sprachausgabe in einem beliebigen Ausgabeformat bis zu 7,1-Umschließungs Sound.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Berechnen Sie die Sende Stufen basierend auf dem gewünschten schwenken zwischen der linken und der rechten sprechenden Seite. In diesem Beispiel reichen die Pan-Werte von-1 bis 1, wobei-1 den gesamten Sound des linken Lautsprechers angibt, und 1, der den gesamten Sound für den rechten Redner angibt.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Legen Sie die Ausgabe Matrix Indizes entsprechend dem linken und rechten Sprecher mit den Werten fest, die im vorherigen Schritt berechnet wurden. Der linke und der Rechte Sprecher werden anhand der von [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)zurückgegebenen Kanalmaske bestimmt. Da die Kanäle immer in der auf der [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) -Referenzseite angegebenen Reihenfolge codiert werden müssen, ist es möglich, den Array Index zu bestimmen, der einem einzelnen Redner entspricht.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Wenden Sie die Ausgabe Matrix mithilfe von [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)auf die ursprüngliche Stimme an. Die ursprüngliche Stimme ist entweder eine Quell Stimme oder eine teilmischungs-Stimme, die entweder an eine Teil Mischungs Stimme oder eine Stimme der Stimme sendet. Mit [**IXAudio2Voice:: getvoicedetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails)können Sie Informationen über die Ausgangs-und Ziel Stimmen wie die Anzahl der Kanäle erhalten.

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 Volume und Tonhöhe-Steuerelement](volume-and-pitch-control.md)
</dt> </dl>

 

 
