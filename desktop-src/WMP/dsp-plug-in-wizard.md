---
title: DSP-Plug-in-Assistent
description: DSP-Plug-in-Assistent
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Plug-ins, Plug-in-Assistent
- Plug-Ins für die digitale Signalverarbeitung, Plug-in-Assistent
- DSP-Plug-ins, Plug-in-Assistent
- Plug-in-Assistent
- Visual Studio, DSP-Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515693"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="f7585-109">DSP-Plug-in-Assistent</span><span class="sxs-lookup"><span data-stu-id="f7585-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="f7585-110">Das Windows Media Player SDK bietet einen Plug-in-Assistenten, den Sie Visual Studio hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="f7585-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="f7585-111">Der Assistent kann Beispielcode für eine Vielzahl von Plug-ins generieren, einschließlich der folgenden Typen von DSP-Plug-ins:</span><span class="sxs-lookup"><span data-stu-id="f7585-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="f7585-112">Audiodsp-Plug-in</span><span class="sxs-lookup"><span data-stu-id="f7585-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="f7585-113">Audiodsp-Plug-in (Dual-Modus)</span><span class="sxs-lookup"><span data-stu-id="f7585-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="f7585-114">Video DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="f7585-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="f7585-115">Video DSP-Plug-in (Dual-Modus)</span><span class="sxs-lookup"><span data-stu-id="f7585-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="f7585-116">Jedes der beiden grundlegenden Beispiel-Plug-ins, audiodsp und Video DSP, fungiert als DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="f7585-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="f7585-117">Das heißt, dass jedes Plug-in-Beispiel die **imediaobject** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f7585-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="f7585-118">Jede der beiden Sample-Plug-ins im Dual-Modus kann entweder als DMO oder als Media Foundation Transformation (MFT) fungieren.</span><span class="sxs-lookup"><span data-stu-id="f7585-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="f7585-119">Das heißt, dass die Plug-Ins für das Dual-Mode-Beispiel sowohl die **imediaobject** -Schnittstelle als auch die **IMF Transform** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="f7585-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="f7585-120">Sie können den Beispiel-Plug-in-Code kompilieren, verknüpfen, registrieren und testen.</span><span class="sxs-lookup"><span data-stu-id="f7585-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="f7585-121">Anschließend können Sie den generierten Beispielcode ändern, um ein eigenes DSP-Plug-in zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7585-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7585-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7585-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7585-123">**Aufbau eines DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="f7585-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="f7585-124">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="f7585-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="f7585-125">**Updates des DSP-Plug-in-Assistenten für Windows Media Player 11**</span><span class="sxs-lookup"><span data-stu-id="f7585-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




