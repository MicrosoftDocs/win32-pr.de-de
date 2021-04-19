---
description: 'Es gibt drei Arten von XAudio2 Voice-Objekten: Quelle, teilmischung und Mastering Stimmen.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: XAudio2-Stimmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364227"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="fa6a3-103">XAudio2-Stimmen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-103">XAudio2 Voices</span></span>

<span data-ttu-id="fa6a3-104">Es gibt drei Arten von XAudio2 Voice-Objekten: *Quelle*, *teilmischung* und *Mastering* Stimmen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="fa6a3-105">Quellstimmen verarbeiten die vom Client bereitgestellten Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="fa6a3-106">Quell- und Submixstimmen senden ihre Ausgabe an mindestens eine Submix- oder Masterstimme.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="fa6a3-107">Submix- und Masterstimmen mischen die Audiodaten aller Stimmen, von denen sie Daten erhalten, und verarbeiten das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="fa6a3-108">Masterstimmen schreiben Audiodaten auf ein Audiogerät.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="fa6a3-109">Von allen Stimmen ausgeführte Aktionen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="fa6a3-110">Alle Stimmen führen die folgenden Aktionen für die Audiodatei aus, die Sie übertragen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="fa6a3-111">Gesamte volumeanpassung, die sich auf alle Audiokanäle auswirkt.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="fa6a3-112">Weitere Informationen finden Sie unter [**IXAudio2Voice:: SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="fa6a3-113">Eine optionale, vom Client angegebene Kette von einem oder mehreren DSP-Effekten, z. b. der integrierte oder der von der [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo) -Schnittstelle definierte Benutzer Effekt.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="fa6a3-114">Siehe [XAudio2-Audioeffekte](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="fa6a3-115">Anpassung des pro-Kanal-Ausgabe Volumens.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="fa6a3-116">Weitere Informationen finden Sie unter [**IXAudio2Voice:: setchannelvolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="fa6a3-117">Trennen Sie die Matrix Mischung mit den einzelnen Ziel Stimmen oder dem Audioausgabegerät für das beherrschen von Stimmen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="fa6a3-118">Diese Mischung ändert die Anzahl der Kanäle im Audioformat, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="fa6a3-119">Quellen Stimmen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-119">Source Voices</span></span>

<span data-ttu-id="fa6a3-120">Verwenden Sie Quell Stimmen, um Audiodaten an die XAudio2-Verarbeitungs Pipeline zu senden.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="fa6a3-121">Sie sind die Einstiegspunkte in das [XAudio2-audiodiagramm](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="fa6a3-122">Sie müssen Sprach Daten an eine Mastering-Stimme senden, damit Sie entweder direkt oder über zwischenteilmix-Stimmen gehört.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="fa6a3-123">Zusätzlich zu den Aktionen, die von allen Stimmen durchgeführt werden, führen Quell Stimmen die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="fa6a3-124">Bei Bedarf wird ein Decoder zuerst ausgeführt, um codierte Quelldaten in Pulse Code Modulation (PCM) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="fa6a3-125">Eine Stichprobenrate Konvertierung (src) für Variablen Raten konvertiert die Quell Audiodaten der Stimme in die von den Ziel Stimmen erwartete Samplingrate, falls erforderlich, und unterstützt auch dynamische Änderungen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="fa6a3-126">Ein optionaler Zustandsvariablen Filter kann verwendet werden, um den Sound auf verschiedene Weise zu färben.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="fa6a3-127">Weitere Informationen finden Sie unter [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="fa6a3-128">Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="fa6a3-129">Weitere Informationen finden Sie unter [**IXAudio2Voice:: setoutputfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="fa6a3-130">Teilmengen von Stimmen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-130">Submix Voices</span></span>

<span data-ttu-id="fa6a3-131">Eine teilmix-Stimme wird hauptsächlich für Leistungsverbesserungen und Auswirkungen der Verarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="fa6a3-132">Sie können keine Datenpuffer direkt an submischungs Stimmen senden.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="fa6a3-133">Es ist nicht hörbar, es sei denn, Sie senden es an eine Mastering Voice.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="fa6a3-134">Sie können eine unter Mischungs Stimme verwenden, um sicherzustellen, dass ein bestimmter Satz von Sprach Daten in das gleiche Format konvertiert wird und eine bestimmte Wirkungskette für das Ergebnis des gemeinsamen Ergebnisses verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="fa6a3-135">Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen teilmischungs Stimmen die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="fa6a3-136">Ein src mit fester Rate wird bei Bedarf in der Ausgabe der Stimme ausgeführt, um die Audiodaten in die von den Ziel Stimmen erwartete Stichprobenrate zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="fa6a3-137">Ein optionaler Zustandsvariablen Filter kann verwendet werden, um den Sound auf verschiedene Weise zu färben.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="fa6a3-138">Weitere Informationen finden Sie unter [**IXAudio2Voice:: setfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="fa6a3-139">Ein optionaler Filter kann auf die Ausgaben der Stimme angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="fa6a3-140">Weitere Informationen finden Sie unter [**IXAudio2Voice:: setoutputfilterparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="fa6a3-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="fa6a3-141">Meistern von Stimmen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-141">Mastering Voices</span></span>

<span data-ttu-id="fa6a3-142">Verwenden Sie eine Mastering Voice, um das Audioausgabegerät darzustellen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="fa6a3-143">Datenpuffer können nicht direkt an die Mastering-Stimmen übermittelt werden, aber Daten, die an andere Arten von Stimmen übermittelt werden, müssen zu einer zu hörenden Stimme gelangen.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="fa6a3-144">Zusätzlich zu den Aktionen, die von allen Stimmen ausgeführt werden, führen Mastering-Stimmen die folgenden Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="fa6a3-145">Wenn Sie die Mastering Voice mit einem expliziten *inputsamplerate* -Wert erstellen, der vom Audiogerät nicht unterstützt wird, wird ein src mit fester Rate verwendet, um die nächstgelegene, vom Gerät unterstützte Stichprobenrate zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="fa6a3-146">Schneiden Sie die endgültige Ausgabe Audiodatei ab, wenn Sie vom Ausgabegerät benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa6a3-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa6a3-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa6a3-148">Stimmen</span><span class="sxs-lookup"><span data-stu-id="fa6a3-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="fa6a3-149">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="fa6a3-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="fa6a3-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="fa6a3-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="fa6a3-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="fa6a3-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
