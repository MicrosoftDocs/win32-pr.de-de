---
description: In diesem Thema wird gezeigt, wie Sie einen mit der xapo-API erstellten Effekt in einer XAudio2 Effect-Kette verwenden.
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: "So wird's gemacht: Verwenden eines XAPOs in XAudio2"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353119"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="9fba7-103">So wird's gemacht: Verwenden eines XAPOs in XAudio2</span><span class="sxs-lookup"><span data-stu-id="9fba7-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="9fba7-104">In diesem Thema wird gezeigt, wie Sie einen mit der xapo-API erstellten Effekt in einer XAudio2 Effect-Kette verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fba7-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="9fba7-105">Erstellen Sie den xapo wie unter Gewusst [wie: Erstellen eines xapo](how-to--create-an-xapo.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9fba7-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="9fba7-106">Sie können auch Lauf Zeitparameter Funktionen implementieren, wie unter Gewusst [wie: Hinzufügen von Lauf Zeitparameter Unterstützung zu xapo](how-to--add-run-time-parameter-support-to-an-xapo.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9fba7-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="9fba7-107">Erstellen Sie eine Instanz von xapo.</span><span class="sxs-lookup"><span data-stu-id="9fba7-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="9fba7-108">Füllt eine [**XAUDIO2 \_ Effect- \_ deskriptorstruktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="9fba7-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="9fba7-109">Füllt eine [**XAUDIO2- \_ Effekt \_ Ketten**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) Struktur mit Daten auf.</span><span class="sxs-lookup"><span data-stu-id="9fba7-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="9fba7-110">Wenden Sie die Effekt Kette auf eine XAudio2-Stimme mit der Funktion " [**setteffectchain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) " an.</span><span class="sxs-lookup"><span data-stu-id="9fba7-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="9fba7-111">Eine Wirkungskette kann auch auf eine Stimme angewendet werden, wenn die Stimme erstellt wird, indem Sie die Kette als Parameter an [**IXAudio2:: anatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2:: anatesubmixvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)oder [**IXAudio2:: smatemasteringvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)übergibt.</span><span class="sxs-lookup"><span data-stu-id="9fba7-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="9fba7-112">Geben Sie den Effekt mit IUnknown:: Release frei.</span><span class="sxs-lookup"><span data-stu-id="9fba7-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="9fba7-113">Wenn Sie ein xapo erstellen, wird ein Verweis Zähler von 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fba7-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="9fba7-114">Wenn das xapo-Element mit der [**Datei**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)"XAudio2" mit dem Wert "" an weitergeleitet wird, Inkrementieren Sie den Verweis Zähler für den xapo</span><span class="sxs-lookup"><span data-stu-id="9fba7-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="9fba7-115">Das Freigeben des Client Verweises auf das xapo ermöglicht XAudio2, den Besitz von xapo zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="9fba7-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="9fba7-116">Wenn XAudio2 über den einzigen Verweis auf den xapo verfügt, wird er verworfen, wenn er nicht mehr von XAudio2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fba7-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="9fba7-117">Wenn der Client Code z. b. einen Verweis auf das xapo zur späteren Wiederverwendung beibehalten muss, sollten Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="9fba7-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="9fba7-118">Füllt die der Auswirkung zugeordnete Parameter Struktur, sofern vorhanden, auf.</span><span class="sxs-lookup"><span data-stu-id="9fba7-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="9fba7-119">In diesem Fall der Prozentsatz der vollständigen Stärke, bei der der Effekt angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fba7-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="9fba7-120">Übergeben Sie die Effektparameter Struktur an den Effekt, indem Sie die Funktion " [**setteffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) " auf der Stimme aufrufen, an die der Effekt angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9fba7-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9fba7-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9fba7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fba7-122">Audioeffekte</span><span class="sxs-lookup"><span data-stu-id="9fba7-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="9fba7-123">Übersicht über xapo</span><span class="sxs-lookup"><span data-stu-id="9fba7-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="9fba7-124">XAudio2-Programmieranleitung</span><span class="sxs-lookup"><span data-stu-id="9fba7-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
