---
description: In diesem Thema wird gezeigt, wie Sie eine der in xapofx enthaltenen Effekte in einer XAudio2 Effect-Kette verwenden können.
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: "So wird's gemacht: Verwenden von XAPOFX in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357379"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="b4534-103">So wird's gemacht: Verwenden von XAPOFX in XAudio2</span><span class="sxs-lookup"><span data-stu-id="b4534-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="b4534-104">In diesem Thema wird gezeigt, wie Sie eine der in xapofx enthaltenen Effekte in einer XAudio2 Effect-Kette verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b4534-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="b4534-105">So verwenden Sie einen Effekt von xapofx in einer XAudio2 Effect-Kette</span><span class="sxs-lookup"><span data-stu-id="b4534-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="b4534-106">Erstellen Sie den Effekt, indem Sie die CLSID eines xapofx-Effekts an die Funktion " [**kreatefx**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) " übergeben.</span><span class="sxs-lookup"><span data-stu-id="b4534-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="b4534-107">In diesem Fall wird der vereinfachte einhall Effekt fxreverb erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4534-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="b4534-108">Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="b4534-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="b4534-109">Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="b4534-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="b4534-110">Wenden Sie die Effekt Kette auf eine XAudio2-Stimme mit der Funktion " [**setteffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.</span><span class="sxs-lookup"><span data-stu-id="b4534-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="b4534-111">Sie können auch eine Wirkungskette auf eine Stimme anwenden, wenn Sie die Stimme erstellen, indem Sie die Kette als Parameter an [**IXAudio2:::: anatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: anatesubmixvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)oder [**IXAudio2:: kreatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergeben.</span><span class="sxs-lookup"><span data-stu-id="b4534-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="b4534-112">Geben Sie den Effekt mit IUnknown:: Release frei.</span><span class="sxs-lookup"><span data-stu-id="b4534-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="b4534-113">Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4534-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="b4534-114">Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo</span><span class="sxs-lookup"><span data-stu-id="b4534-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="b4534-115">Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="b4534-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="b4534-116">Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird dieser Verweis verworfen, wenn er nicht mehr von XAudio2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b4534-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="b4534-117">Wenn der Client Code einen Verweis auf die xapo beibehalten muss – z. b. zur späteren Wiederverwendung –, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="b4534-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="b4534-118">Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf.</span><span class="sxs-lookup"><span data-stu-id="b4534-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="b4534-119">In diesem Fall wird die Struktur von [**fxreverb- \_ Parametern**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) verwendet, um die Verbreitung und die Raum Größe festzulegen, die vom-mappeneffekt verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b4534-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="b4534-120">Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="b4534-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b4534-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4534-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4534-122">Audioeffekte</span><span class="sxs-lookup"><span data-stu-id="b4534-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="b4534-123">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="b4534-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
