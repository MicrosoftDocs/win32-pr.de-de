---
description: In diesem Thema werden die Schritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: "So wird's gemacht: Wiedergeben von Ton mit XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526882"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="6615d-103">So wird's gemacht: Wiedergeben von Ton mit XAudio2</span><span class="sxs-lookup"><span data-stu-id="6615d-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="6615d-104">In diesem Thema werden die Schritte beschrieben, die für die Wiedergabe zuvor geladener Audiodaten in XAudio2 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6615d-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="6615d-105">Nach dem Initialisieren von XAudio2 (siehe Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)) und Laden der Audiodaten (siehe Gewusst wie: Gewusst [wie: Laden von audiodatendateien in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)) können Sie einen Sound wiedergeben, indem Sie eine Quell Stimme erstellen und Audiodaten an diese übergeben.</span><span class="sxs-lookup"><span data-stu-id="6615d-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="6615d-106">So spielen Sie einen Sound wieder</span><span class="sxs-lookup"><span data-stu-id="6615d-106">To play a sound</span></span>

1.  <span data-ttu-id="6615d-107">Initialisieren Sie die XAudio2-Engine, indem Sie die unter Gewusst [wie: Initialisieren von XAudio2](how-to--initialize-xaudio2.md)beschriebenen Schritte befolgen.</span><span class="sxs-lookup"><span data-stu-id="6615d-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="6615d-108">Füllen Sie eine [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -und [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) Struktur aus, indem Sie die Schritte befolgen, die unter Gewusst [wie: Laden von audiodatendateien in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md)beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="6615d-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="6615d-109">Abhängig vom Format der Audiodaten müssen Sie möglicherweise eine größere Datenstruktur verwenden, die eine [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -Struktur anstelle eines **WaveFormatEx**-Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="6615d-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="6615d-110">Weitere Informationen finden Sie auf der Referenzseite zu **WaveFormatEx** .</span><span class="sxs-lookup"><span data-stu-id="6615d-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="6615d-111">Erstellen Sie eine Quell Stimme, indem Sie die [**IXAudio2:: createsourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) -Methode für eine Instanz der XAudio2-Engine aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6615d-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="6615d-112">Das Format der Stimme wird durch die Werte angegeben, die in einer [**WaveFormatEx**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) -Struktur festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="6615d-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="6615d-113">Senden Sie mithilfe der Funktion " [**submitsourcebuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)" einen [**XAUDIO2- \_ Puffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) an die Quell Stimme.</span><span class="sxs-lookup"><span data-stu-id="6615d-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="6615d-114">Die audiobeispieldaten, an die *Puffer* Punkte immer noch im Besitz von der APP sind und die zugewiesen und zugänglich bleiben müssen, bis der Sound angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="6615d-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="6615d-115">Verwenden Sie die [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) -Funktion, um die Quell Stimme zu starten.</span><span class="sxs-lookup"><span data-stu-id="6615d-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="6615d-116">Da alle XAudio2 stimmen ihre Ausgabe standardmäßig an die Mastering-Stimme senden, wird das Audiogerät, das bei der Initialisierung ausgewählt wird, automatisch von Audiodaten aus der Quellsprache entfernt.</span><span class="sxs-lookup"><span data-stu-id="6615d-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="6615d-117">In einem komplizierteren audiodiagramm müsste die Quell Stimme die Stimme angeben, an die die Ausgabe gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6615d-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="6615d-118">Hinweise für Windows Store-Apps</span><span class="sxs-lookup"><span data-stu-id="6615d-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="6615d-119">Es wird empfohlen, einen [intelligenten Zeiger](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) zu verwenden, um die Lebensdauer von XAUDIO2-Objekten auf sichere Weise zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6615d-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="6615d-120">Für Windows Store-Apps können Sie die Vorlage " [**comptr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) -intelligenter Zeiger" aus der Windows-Runtime C++ Template Library (WRL) verwenden.</span><span class="sxs-lookup"><span data-stu-id="6615d-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="6615d-121">Stellen Sie sicher, dass alle intelligenten Zeiger auf XAUDIO2 Objekte vollständig freigegeben werden, bevor Sie das [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="6615d-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6615d-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6615d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6615d-123">XAudio2</span><span class="sxs-lookup"><span data-stu-id="6615d-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="6615d-124">So wird's gemacht: Initialisieren von XAudio2</span><span class="sxs-lookup"><span data-stu-id="6615d-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="6615d-125">So wird's gemacht: Laden von Datendateien in XAudio2</span><span class="sxs-lookup"><span data-stu-id="6615d-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
