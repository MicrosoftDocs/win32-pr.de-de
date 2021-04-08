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
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="49cee-103">Vorgehensweise: Ändern des sprach Volumens</span><span class="sxs-lookup"><span data-stu-id="49cee-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="49cee-104">In diesem Thema erfahren Sie, wie Sie das Volume einer Stimme auf der Gesamtebene, in jedem Ausgabekanal oder zwischen den einzelnen Kanälen einer Stimme und einer anderen Stimme in der [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)ändern können.</span><span class="sxs-lookup"><span data-stu-id="49cee-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="49cee-105">So legen Sie eine Gesamt Volume-Ebene für die Eingabe der Stimme fest</span><span class="sxs-lookup"><span data-stu-id="49cee-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="49cee-106">Verwenden Sie die [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="49cee-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="49cee-107">So legen Sie das Volumen der Ausgabekanäle der Stimme fest</span><span class="sxs-lookup"><span data-stu-id="49cee-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="49cee-108">Erstellen Sie ein Array von Gleit Komma Zahlen, die die gewünschten Volumes aller Ausgabekanäle in der Stimme enthalten.</span><span class="sxs-lookup"><span data-stu-id="49cee-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="49cee-109">Das Array erhält einen Eintrag für jeden Kanal in der Stimme.</span><span class="sxs-lookup"><span data-stu-id="49cee-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="49cee-110">Verwenden Sie die Funktion [**setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) , um das Volume der Ausgabekanäle festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49cee-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="49cee-111">So legen Sie die Anzahl der Verbindungen fest</span><span class="sxs-lookup"><span data-stu-id="49cee-111">To set the volume of connections</span></span>

<span data-ttu-id="49cee-112">Legen Sie das Verbindungs Volume zwischen der Stimme und einer Stimme in der [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)fest.</span><span class="sxs-lookup"><span data-stu-id="49cee-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="49cee-113">Erstellen Sie ein Array von Gleit Komma Zahlen, das eine Ausgabe Matrix definiert, wenn die Stimme an eine andere Sprache sendet.</span><span class="sxs-lookup"><span data-stu-id="49cee-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="49cee-114">Das Array muss über eine Anzahl von Einträgen verfügen, die gleich den Sprachkanälen der Quell Spracheingabe Kanäle × Destination sind.</span><span class="sxs-lookup"><span data-stu-id="49cee-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="49cee-115">In diesem Beispiel erfolgt die Zuordnung von einer Stimme mit einem Kanal zu einer Stimme mit zwei Kanälen.</span><span class="sxs-lookup"><span data-stu-id="49cee-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="49cee-116">Verwenden Sie die [**setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) -Funktion, um die Ausgabe Matrix festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49cee-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="49cee-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="49cee-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49cee-118">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="49cee-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="49cee-119">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="49cee-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="49cee-120">XAudio2 Volume und Tonhöhe-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="49cee-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
