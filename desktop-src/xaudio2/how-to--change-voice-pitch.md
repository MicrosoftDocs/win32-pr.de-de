---
description: In diesem Thema wird gezeigt, wie Sie die Menge der Audiodaten erhöhen oder verringern können, indem Sie die Funktion setfrequencyratio in einer Quellsprache ändern.
ms.assetid: 93408116-1c1f-307f-7e1f-090f2663ff0b
title: 'Vorgehensweise: Ändern der Stimm Schrift'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7143dda30eae48bd8ed966c4170da2884d2633ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129772"
---
# <a name="how-to-change-voice-pitch"></a>Vorgehensweise: Ändern der Stimm Schrift

In diesem Thema wird gezeigt, wie Sie die Menge der Audiodaten erhöhen oder verringern können, indem Sie die Funktion [**setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) in einer Quellsprache ändern.

## <a name="to-change-the-pitch-of-a-source-voice"></a>So ändern Sie die Tonhöhe einer Quell Stimme

1.  Legen Sie das gewünschte Häufigkeits Verhältnis für die [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)fest.

    Weitere Informationen zum Berechnen des Häufigkeits Verhältnisses finden Sie unter [XAudio2 Volume und Pitch Control](xaudio2-volume-and-pitch-control.md) .

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  Verwenden Sie die Funktion [**setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , um das Häufigkeits Verhältnis der Quell Stimme festzulegen.

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[XAudio2 Volume und Tonhöhe-Steuerelement](volume-and-pitch-control.md)
</dt> </dl>

 

 
