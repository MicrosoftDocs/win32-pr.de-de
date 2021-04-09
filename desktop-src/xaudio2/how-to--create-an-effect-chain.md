---
description: In diesem Thema wird gezeigt, wie Sie eine Wirkungskette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen. In diesem Thema wird beschrieben, wie Sie den Reverb-Effekt verwenden, bei dem es sich um einen der integrierten XAudio2-Effekte handelt.
ms.assetid: 4c33bd83-2654-cd6f-ea6c-bbc0d5872638
title: "So wird's gemacht: Erstellen einer Effektkette"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d58186b623dca04da99001a29e54cf3ecc39fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129769"
---
# <a name="how-to-create-an-effect-chain"></a><span data-ttu-id="86048-104">So wird's gemacht: Erstellen einer Effektkette</span><span class="sxs-lookup"><span data-stu-id="86048-104">How to: Create an Effect Chain</span></span>

<span data-ttu-id="86048-105">In diesem Thema wird gezeigt, wie Sie eine Wirkungskette auf eine Stimme anwenden können, um die benutzerdefinierte Verarbeitung der Audiodaten für diese Stimme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="86048-105">This topic shows you how you can apply an effect chain to a voice to allow custom processing of the audio data for that voice.</span></span> <span data-ttu-id="86048-106">In diesem Thema wird beschrieben, wie Sie den Reverb-Effekt verwenden, bei dem es sich um einen der integrierten XAudio2-Effekte handelt.</span><span class="sxs-lookup"><span data-stu-id="86048-106">This topic describes how to use the reverb effect, which is one of the built-in XAudio2 effects.</span></span>

## <a name="to-create-a-basic-effect-chain-that-applies-an-effect-to-a-voice"></a><span data-ttu-id="86048-107">So erstellen Sie eine grundlegende Wirkungskette, die einen Effekt auf eine Stimme anwendet</span><span class="sxs-lookup"><span data-stu-id="86048-107">To create a basic effect chain that applies an effect to a voice</span></span>

1.  <span data-ttu-id="86048-108">Erstellen Sie den Effekt.</span><span class="sxs-lookup"><span data-stu-id="86048-108">Create the effect.</span></span>

    <span data-ttu-id="86048-109">In diesem Beispiel erstellt die [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) -Funktion einen Hall Effekt.</span><span class="sxs-lookup"><span data-stu-id="86048-109">In this example, the [**XAudio2CreateReverb**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) function creates a reverb effect.</span></span> <span data-ttu-id="86048-110">Eine Liste möglicher Quellen mit Effekten für die Verwendung mit XAudio2 finden Sie unter [XAudio2-Audioeffekte](xaudio2-audio-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="86048-110">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) for a list of possible sources of effects for use with XAudio2.</span></span>

    ```
    IUnknown * pXAPO;
    hr = XAudio2CreateReverb(&pXAPO);
    ```

    

2.  <span data-ttu-id="86048-111">Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="86048-111">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    <span data-ttu-id="86048-112">Wenn sich mehrere Effekte in der Kette befinden, wird für jeden Effekt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) benötigt.</span><span class="sxs-lookup"><span data-stu-id="86048-112">If there are multiple effects in the chain, each effect will need a [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="86048-113">Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="86048-113">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span> <span data-ttu-id="86048-114">In diesem Fall hat die Kette nur einen Effekt.</span><span class="sxs-lookup"><span data-stu-id="86048-114">In this case, the chain only has one effect.</span></span> <span data-ttu-id="86048-115">Wenn die Kette mehr als einen Effekt hat, enthält das Element effectcount die Anzahl der Effekte, und das peffectdescriptors-Element verweist auf ein Array von XAUDIO2 \_ Effect- \_ deskriptorstrukturen.</span><span class="sxs-lookup"><span data-stu-id="86048-115">If the chain has more than one effect, the EffectCount member will contain the count of effects, and the pEffectDescriptors member will point to an array of XAUDIO2\_EFFECT\_DESCRIPTOR structures.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="86048-116">Wenden Sie die Effekt Kette auf eine Stimme mit der Funktion " [**sffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.</span><span class="sxs-lookup"><span data-stu-id="86048-116">Apply the effect chain to a voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    <span data-ttu-id="86048-117">Sie können Effektketten auf Haupt Stimmen, Quell Stimmen und Teil Mischungs Stimmen anwenden.</span><span class="sxs-lookup"><span data-stu-id="86048-117">You can apply effect chains to master voices, source voices, and submix voices.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

5.  <span data-ttu-id="86048-118">Geben Sie den Effekt mit IUnknown:: Release frei.</span><span class="sxs-lookup"><span data-stu-id="86048-118">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="86048-119">Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="86048-119">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="86048-120">Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo</span><span class="sxs-lookup"><span data-stu-id="86048-120">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="86048-121">Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="86048-121">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="86048-122">Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird er verworfen, wenn er nicht mehr von XAudio2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86048-122">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="86048-123">Wenn der Client Code einen Verweis auf die xapo-– beibehalten muss, z. b. zur späteren Wiederverwendung –, sollten Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="86048-123">If the client code needs to maintain a reference to the XAPO—for example for later reuse—you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="86048-124">Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf.</span><span class="sxs-lookup"><span data-stu-id="86048-124">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="86048-125">Der Hall Effekt verwendet eine [**XAUDIO2FX- \_ Hall- \_ Parameter**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) Struktur.</span><span class="sxs-lookup"><span data-stu-id="86048-125">The reverb effect uses an [**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) structure.</span></span>

    ```
    XAUDIO2FX_REVERB_PARAMETERS reverbParameters;
    reverbParameters.ReflectionsDelay = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_DELAY;
    reverbParameters.ReverbDelay = XAUDIO2FX_REVERB_DEFAULT_REVERB_DELAY;
    reverbParameters.RearDelay = XAUDIO2FX_REVERB_DEFAULT_REAR_DELAY;
    reverbParameters.PositionLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionRight = XAUDIO2FX_REVERB_DEFAULT_POSITION;
    reverbParameters.PositionMatrixLeft = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.PositionMatrixRight = XAUDIO2FX_REVERB_DEFAULT_POSITION_MATRIX;
    reverbParameters.EarlyDiffusion = XAUDIO2FX_REVERB_DEFAULT_EARLY_DIFFUSION;
    reverbParameters.LateDiffusion = XAUDIO2FX_REVERB_DEFAULT_LATE_DIFFUSION;
    reverbParameters.LowEQGain = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_GAIN;
    reverbParameters.LowEQCutoff = XAUDIO2FX_REVERB_DEFAULT_LOW_EQ_CUTOFF;
    reverbParameters.HighEQGain = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_GAIN;
    reverbParameters.HighEQCutoff = XAUDIO2FX_REVERB_DEFAULT_HIGH_EQ_CUTOFF;
    reverbParameters.RoomFilterFreq = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_FREQ;
    reverbParameters.RoomFilterMain = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_MAIN;
    reverbParameters.RoomFilterHF = XAUDIO2FX_REVERB_DEFAULT_ROOM_FILTER_HF;
    reverbParameters.ReflectionsGain = XAUDIO2FX_REVERB_DEFAULT_REFLECTIONS_GAIN;
    reverbParameters.ReverbGain = XAUDIO2FX_REVERB_DEFAULT_REVERB_GAIN;
    reverbParameters.DecayTime = XAUDIO2FX_REVERB_DEFAULT_DECAY_TIME;
    reverbParameters.Density = XAUDIO2FX_REVERB_DEFAULT_DENSITY;
    reverbParameters.RoomSize = XAUDIO2FX_REVERB_DEFAULT_ROOM_SIZE;
    reverbParameters.WetDryMix = XAUDIO2FX_REVERB_DEFAULT_WET_DRY_MIX;
    ```

    

7.  <span data-ttu-id="86048-126">Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="86048-126">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &reverbParameters, sizeof( reverbParameters ) );
    ```

    

8.  <span data-ttu-id="86048-127">Deaktivieren oder aktivieren Sie den Effekt, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="86048-127">Disable or enable the effect, whenever appropriate.</span></span>

    <span data-ttu-id="86048-128">Sie können [**disableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) jederzeit verwenden, um einen Effekt zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="86048-128">You can use [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) at any time to turn an effect off.</span></span>

    ```
    pVoice->DisableEffect(0);
    ```

    

    <span data-ttu-id="86048-129">Sie können einen Effekt mit [**enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="86048-129">You can turn on an effect again with [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect).</span></span>

    ```
    pVoice->EnableEffect(0);
    ```

    

    <span data-ttu-id="86048-130">Mit den Parametern für [**disableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) und [**enableeffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) wird angegeben, welche Auswirkung in der Kette aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="86048-130">The parameters for [**DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) and [**EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) specify which effect in the chain to enable or disable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86048-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86048-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86048-132">Audioeffekte</span><span class="sxs-lookup"><span data-stu-id="86048-132">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="86048-133">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="86048-133">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="86048-134">So wird's gemacht: Erstellen eines grundlegenden Audioverarbeitungsdiagramms</span><span class="sxs-lookup"><span data-stu-id="86048-134">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="86048-135">Übersicht über xapo</span><span class="sxs-lookup"><span data-stu-id="86048-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="86048-136">Gewusst wie: Verwenden von xaopfx in XAudio2</span><span class="sxs-lookup"><span data-stu-id="86048-136">How to: Use XAOPFX in XAudio2</span></span>](how-to--use-xapofx-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="86048-137">Gewusst wie: Verwenden eines xaop in XAudio2</span><span class="sxs-lookup"><span data-stu-id="86048-137">How to: Use an XAOP in XAudio2</span></span>](how-to--use-an-xapo-in-xaudio2.md)
</dt> </dl>

 

 
