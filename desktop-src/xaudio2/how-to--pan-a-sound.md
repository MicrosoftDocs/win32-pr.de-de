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
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="588a3-103">Gewusst wie: Schwenken eines Sounds</span><span class="sxs-lookup"><span data-stu-id="588a3-103">How to: Pan a Sound</span></span>

<span data-ttu-id="588a3-104">In diesem Thema wird erläutert, wie Sie die Ausgabe Matrix einer Mono-Quellsprache festlegen können, die in eine Stereo-Mastering-Stimme ausgibt, um das Schwenken zwischen der linken und der rechten sprechenden Seite zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="588a3-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="588a3-105">Einrichten von schwenken</span><span class="sxs-lookup"><span data-stu-id="588a3-105">To setup panning</span></span>

1.  <span data-ttu-id="588a3-106">Rufen Sie die Sprecher Konfiguration mit [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)ab.</span><span class="sxs-lookup"><span data-stu-id="588a3-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="588a3-107">Erstellen Sie ein Array, das die Ausgabe Matrix enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="588a3-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="588a3-108">Die minimale Größe der Ausgabe Matrix ist die Anzahl der Kanäle in der Quellsprache und die Anzahl der Kanäle in der Ausgabesprache.</span><span class="sxs-lookup"><span data-stu-id="588a3-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="588a3-109">In diesem Fall behandelt ein 8-Element-Array eine Mono-Sprachausgabe in einem beliebigen Ausgabeformat bis zu 7,1-Umschließungs Sound.</span><span class="sxs-lookup"><span data-stu-id="588a3-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="588a3-110">Berechnen Sie die Sende Stufen basierend auf dem gewünschten schwenken zwischen der linken und der rechten sprechenden Seite.</span><span class="sxs-lookup"><span data-stu-id="588a3-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="588a3-111">In diesem Beispiel reichen die Pan-Werte von-1 bis 1, wobei-1 den gesamten Sound des linken Lautsprechers angibt, und 1, der den gesamten Sound für den rechten Redner angibt.</span><span class="sxs-lookup"><span data-stu-id="588a3-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="588a3-112">Legen Sie die Ausgabe Matrix Indizes entsprechend dem linken und rechten Sprecher mit den Werten fest, die im vorherigen Schritt berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="588a3-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="588a3-113">Der linke und der Rechte Sprecher werden anhand der von [**IXAudio2MasteringVoice:: getchannelmask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask)zurückgegebenen Kanalmaske bestimmt.</span><span class="sxs-lookup"><span data-stu-id="588a3-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="588a3-114">Da die Kanäle immer in der auf der [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) -Referenzseite angegebenen Reihenfolge codiert werden müssen, ist es möglich, den Array Index zu bestimmen, der einem einzelnen Redner entspricht.</span><span class="sxs-lookup"><span data-stu-id="588a3-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

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

    

5.  <span data-ttu-id="588a3-115">Wenden Sie die Ausgabe Matrix mithilfe von [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)auf die ursprüngliche Stimme an.</span><span class="sxs-lookup"><span data-stu-id="588a3-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="588a3-116">Die ursprüngliche Stimme ist entweder eine Quell Stimme oder eine teilmischungs-Stimme, die entweder an eine Teil Mischungs Stimme oder eine Stimme der Stimme sendet.</span><span class="sxs-lookup"><span data-stu-id="588a3-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="588a3-117">Mit [**IXAudio2Voice:: getvoicedetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails)können Sie Informationen über die Ausgangs-und Ziel Stimmen wie die Anzahl der Kanäle erhalten.</span><span class="sxs-lookup"><span data-stu-id="588a3-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="588a3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="588a3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="588a3-119">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="588a3-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="588a3-120">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="588a3-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="588a3-121">XAudio2 Volume und Tonhöhe-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="588a3-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
