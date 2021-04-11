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
# <a name="how-to-change-voice-pitch"></a><span data-ttu-id="504e7-103">Vorgehensweise: Ändern der Stimm Schrift</span><span class="sxs-lookup"><span data-stu-id="504e7-103">How to: Change Voice Pitch</span></span>

<span data-ttu-id="504e7-104">In diesem Thema wird gezeigt, wie Sie die Menge der Audiodaten erhöhen oder verringern können, indem Sie die Funktion [**setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) in einer Quellsprache ändern.</span><span class="sxs-lookup"><span data-stu-id="504e7-104">This topic shows you how you can raise or lower the pitch of audio data by changing its rate of playback using the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function on a source voice.</span></span>

## <a name="to-change-the-pitch-of-a-source-voice"></a><span data-ttu-id="504e7-105">So ändern Sie die Tonhöhe einer Quell Stimme</span><span class="sxs-lookup"><span data-stu-id="504e7-105">To change the pitch of a source voice</span></span>

1.  <span data-ttu-id="504e7-106">Legen Sie das gewünschte Häufigkeits Verhältnis für die [**Quell Stimme**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)fest.</span><span class="sxs-lookup"><span data-stu-id="504e7-106">Determine the desired frequency ratio for the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice).</span></span>

    <span data-ttu-id="504e7-107">Weitere Informationen zum Berechnen des Häufigkeits Verhältnisses finden Sie unter [XAudio2 Volume und Pitch Control](xaudio2-volume-and-pitch-control.md) .</span><span class="sxs-lookup"><span data-stu-id="504e7-107">See [XAudio2 Volume and Pitch Control](xaudio2-volume-and-pitch-control.md) for more information about calculating the frequency ratio.</span></span>

    ```
    float frequencyRatio = sourceRate / targetRate;
    ```

    

2.  <span data-ttu-id="504e7-108">Verwenden Sie die Funktion [**setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) , um das Häufigkeits Verhältnis der Quell Stimme festzulegen.</span><span class="sxs-lookup"><span data-stu-id="504e7-108">Use the [**SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) function to set the frequency ratio of the source voice.</span></span>

    ```
    pSourceVoice->SetFrequencyRatio(frequencyRatio);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="504e7-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="504e7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="504e7-110">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="504e7-110">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="504e7-111">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="504e7-111">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="504e7-112">XAudio2 Volume und Tonhöhe-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="504e7-112">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
