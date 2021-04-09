---
title: Erforderliche Schnittstellen (Windows Media Player SDK)
description: Erforderliche Schnittstellen
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858602"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="9fd82-108">Erforderliche Schnittstellen (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="9fd82-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="9fd82-109">Windows Media Player rendert Audiodaten und Videos mithilfe einer der folgenden Pipelines.</span><span class="sxs-lookup"><span data-stu-id="9fd82-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="9fd82-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="9fd82-110">DirectShow</span></span>
-   <span data-ttu-id="9fd82-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9fd82-111">Media Foundation</span></span>

<span data-ttu-id="9fd82-112">In Microsoft Windows XP und früheren Versionen verwendet der Player DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9fd82-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="9fd82-113">In Windows Vista verwendet der Player manchmal DirectShow und verwendet manchmal Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9fd82-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="9fd82-114">Ein DSP-Plug-in implementiert einige oder alle der folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="9fd82-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="9fd82-115">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="9fd82-115">**IMediaObject**</span></span>
-   <span data-ttu-id="9fd82-116">**Iwmppluginenable**</span><span class="sxs-lookup"><span data-stu-id="9fd82-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="9fd82-117">**IMF-Transformation**</span><span class="sxs-lookup"><span data-stu-id="9fd82-117">**IMFTransform**</span></span>
-   <span data-ttu-id="9fd82-118">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="9fd82-118">**IMFGetService**</span></span>
-   <span data-ttu-id="9fd82-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="9fd82-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="9fd82-120">Ein Plug-in, das **imediaobject** und **iwmppluginenable** implementiert, kann in der DirectShow-Pipeline ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9fd82-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="9fd82-121">Sie kann auch in der Media Foundation Pipeline in einem von Media Foundation bereitgestellten Wrapper ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9fd82-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="9fd82-122">Ein Plug-in dieses Typs wird als Microsoft DirectX Media Object (DMO) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9fd82-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="9fd82-123">Es ist üblich, ein DMO als analog zu einem Filter Objekt in DirectShow zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="9fd82-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="9fd82-124">Die DMO-Dokumentation befindet sich im Abschnitt DirectShow des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9fd82-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="9fd82-125">Ein Plug-in, das **IMF Transform** und **IMF-Service** implementiert, kann nativ (kein Wrapper erforderlich) in der Media Foundation Pipeline ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9fd82-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="9fd82-126">Ein Plug-in dieses Typs wird als "Media Foundation Transform (MFT)" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9fd82-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="9fd82-127">Die MFT-Dokumentation befindet sich im Abschnitt Media Foundation des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9fd82-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="9fd82-128">Ein Plug-in, das " **imediaobject**", " **iwmppluginenable**", " **IMF Transform**" und " **IMF GetService** " implementiert, kann in der Pipeline "DirectShow" ausgeführt werden und kann auch nativ in der Media Foundation Pipeline ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9fd82-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="9fd82-129">Diese Art von Plug-in, das als *Plug-in für den Dual-Mode-DSP* bezeichnet wird, kann die Rolle eines DMO oder einer MFT wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="9fd82-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="9fd82-130">Wenn Windows Media Player ein bidirektionales DSP-Plug-in in der Media Foundation Pipeline verwendet, fragt es zuerst die **IMF Transform** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="9fd82-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="9fd82-131">Wenn diese Abfrage fehlschlägt, führt Windows Media Player Abfragen für die **imediaobject** -Schnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="9fd82-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="9fd82-132">Wenn die **imediaobject** -Abfrage erfolgreich ist, wird das Plug-in umschließt und der Media Foundation Pipeline hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9fd82-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="9fd82-133">Unabhängig von der Pipeline muss jedes DSP-Plug-in, das es dem Benutzer ermöglicht, Eigenschaften festzulegen, **ISpecifyPropertyPages** implementieren.</span><span class="sxs-lookup"><span data-stu-id="9fd82-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fd82-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9fd82-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9fd82-135">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="9fd82-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="9fd82-136">**DSP-Plug-in-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="9fd82-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9fd82-137">**Plug-in-Paket für DSP**</span><span class="sxs-lookup"><span data-stu-id="9fd82-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




