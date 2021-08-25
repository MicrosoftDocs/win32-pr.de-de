---
description: In diesem Thema erfahren Sie, wie Sie die Tonhöhe von Audiodaten erhöhen oder verringern können, indem Sie die Wiedergaberate mithilfe der SetFrequencyRatio-Funktion für eine Quellstimme ändern.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'How to: Change Voice Pitch'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc44fe757c563e3556f760ead594bb619da9f62fb2c3eafc774e15d7b9e5bc85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926470"
---
# <a name="how-to-change-voice-pitch"></a>How to: Change Voice Pitch

In diesem Thema erfahren Sie, wie Sie die Tonhöhe von Audiodaten erhöhen oder verringern können, indem Sie die Wiedergaberate mithilfe der [**SetFrequencyRatio-Funktion**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) für eine Quellstimme ändern.

## <a name="to-change-the-pitch-of-a-source-voice"></a>So ändern Sie die Tonhöhe einer Quellstimme

1.  Bestimmen Sie das gewünschte Häufigkeitsverhältnis für die [**Quellstimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).

    Weitere Informationen zum Berechnen des Häufigkeitsverhältnisses finden Sie unter [XAudio2 Volume and Pitch Control (XAudio2-Lautstärke- und Tonhöhensteuerung).](xaudio2-volume-and-pitch-control.md)

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Verwenden Sie die [**SetFrequencyRatio-Funktion,**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) um das Häufigkeitsverhältnis der Quellstimme festzulegen.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2-Lautstärke- und Tonhöhen-Steuerelement](volume-and-pitch-control.md)
</dt> </dl>

 

 
