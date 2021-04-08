---
description: In diesem Thema erfahren Sie, wie Sie das Volume einer Stimme auf der Gesamtebene, in jedem Ausgabekanal oder zwischen den einzelnen Kanälen einer Stimme und einer anderen Stimme in der sendlist ändern können.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Vorgehensweise: Ändern des sprach Volumens'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757693"
---
# <a name="how-to-change-voice-volume"></a>Vorgehensweise: Ändern des sprach Volumens

In diesem Thema erfahren Sie, wie Sie das Volume einer Stimme auf der Gesamtebene, in jedem Ausgabekanal oder zwischen den einzelnen Kanälen einer Stimme und einer anderen Stimme in der [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)ändern können.

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a>So legen Sie eine Gesamt Volume-Ebene für die Eingabe der Stimme fest

-   Verwenden Sie die [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) -Funktion.

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a>So legen Sie das Volumen der Ausgabekanäle der Stimme fest

1.  Erstellen Sie ein Array von Gleit Komma Zahlen, die die gewünschten Volumes aller Ausgabekanäle in der Stimme enthalten.

    Das Array erhält einen Eintrag für jeden Kanal in der Stimme.

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  Verwenden Sie die Funktion [**setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) , um das Volume der Ausgabekanäle festzulegen.

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a>So legen Sie die Anzahl der Verbindungen fest

Legen Sie das Verbindungs Volume zwischen der Stimme und einer Stimme in der [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)fest.

1.  Erstellen Sie ein Array von Gleit Komma Zahlen, das eine Ausgabe Matrix definiert, wenn die Stimme an eine andere Sprache sendet.

    > [!Note]  
    > Das Array muss über eine Anzahl von Einträgen verfügen, die gleich den Sprachkanälen der Quell Spracheingabe Kanäle × Destination sind. In diesem Beispiel erfolgt die Zuordnung von einer Stimme mit einem Kanal zu einer Stimme mit zwei Kanälen.

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  Verwenden Sie die [**setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) -Funktion, um die Ausgabe Matrix festzulegen.

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 Volume und Tonhöhe-Steuerelement](volume-and-pitch-control.md)
</dt> </dl>

 

 
