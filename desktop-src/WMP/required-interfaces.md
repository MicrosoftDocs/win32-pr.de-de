---
title: Erforderliche Schnittstellen (Windows Media Player SDK)
description: Erfahren Sie mehr über die erforderlichen Schnittstellen, Windows Media Player directshow oder Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player-Plug-Ins,Schnittstellen
- Plug-Ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-Ins, Schnittstellen
- Schnittstellen,DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406093"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="8145d-108">Erforderliche Schnittstellen (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="8145d-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="8145d-109">Windows Media Player rendert Audio- und Videodaten mithilfe einer der folgenden Pipelines.</span><span class="sxs-lookup"><span data-stu-id="8145d-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="8145d-110">Directshow</span><span class="sxs-lookup"><span data-stu-id="8145d-110">DirectShow</span></span>
-   <span data-ttu-id="8145d-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8145d-111">Media Foundation</span></span>

<span data-ttu-id="8145d-112">In Microsoft Windows XP und früher verwendet der Player DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8145d-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="8145d-113">In Windows Vista verwendet der Player manchmal DirectShow und manchmal Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8145d-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="8145d-114">Ein DSP-Plug-In implementiert einige oder alle der folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="8145d-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="8145d-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="8145d-115">**IMediaObject**</span></span>
-   <span data-ttu-id="8145d-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="8145d-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="8145d-117">**VORÜBERSETZUNGTransform**</span><span class="sxs-lookup"><span data-stu-id="8145d-117">**IMFTransform**</span></span>
-   <span data-ttu-id="8145d-118">**GEGETService**</span><span class="sxs-lookup"><span data-stu-id="8145d-118">**IMFGetService**</span></span>
-   <span data-ttu-id="8145d-119">**Ispecifypropertypages**</span><span class="sxs-lookup"><span data-stu-id="8145d-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="8145d-120">Ein Plug-In, das **IMediaObject** und **IWMPPluginEnable** implementiert, kann in der DirectShow-Pipeline ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8145d-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="8145d-121">Sie kann auch in der Media Foundation Pipeline in einem wrapper ausgeführt werden, der von Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8145d-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="8145d-122">Ein Plug-In dieses Typs wird als Microsoft DirectX Media Object (DMO) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8145d-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="8145d-123">Es ist üblich, einen DMO als analog zu einem Filterobjekt in DirectShow zu sehen.</span><span class="sxs-lookup"><span data-stu-id="8145d-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="8145d-124">Die DMO-Dokumentation befindet sich im Abschnitt DirectShow des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8145d-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="8145d-125">Ein Plug-In, das **DIEBTRANSFORM** und **DEN -DIENST** implementiert, kann nativ (kein Wrapper erforderlich) in der Media Foundation ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8145d-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="8145d-126">Ein Plug-In dieses Typs wird als Media Foundation Transform (MFT) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8145d-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="8145d-127">Die MFT-Dokumentation befindet sich im Media Foundation Abschnitt der Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8145d-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="8145d-128">Ein Plug-In, das **IMediaObject,** **IWMPPluginEnable,** **CISTransform** **undGEGETService** implementiert, kann in der DirectShow-Pipeline ausgeführt werden und kann auch nativ in der Media Foundation ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8145d-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="8145d-129">Dieser Plug-In-Typ, der als *DSP-Plug-In* im dualen Modus bezeichnet wird, kann die Rolle eines DMO- oder MFT-Plug-Ins spielen.</span><span class="sxs-lookup"><span data-stu-id="8145d-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="8145d-130">Wenn Windows Media Player ein DSP-Plug-In im dualen Modus in der pipeline Media Foundation verwendet, fragt es zuerst die **BERTRANSFORM-Schnittstelle** ab.</span><span class="sxs-lookup"><span data-stu-id="8145d-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="8145d-131">Wenn diese Abfrage fehlschlägt, Windows Media Player Abfragen für die **IMediaObject-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="8145d-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="8145d-132">Wenn die **IMediaObject-Abfrage** erfolgreich ist, wird das Plug-In umschlossen und der Media Foundation hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8145d-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="8145d-133">Unabhängig von der Pipeline muss jedes DSP-Plug-In, das dem Benutzer das Festlegen von Eigenschaften ermöglicht, **ISpecifyPropertyPages implementieren.**</span><span class="sxs-lookup"><span data-stu-id="8145d-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8145d-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8145d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8145d-135">**Übersicht über DSP-Plug-In-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="8145d-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="8145d-136">**DSP-Plug-In-Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="8145d-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8145d-137">**DSP-Plug-In-Paketierung**</span><span class="sxs-lookup"><span data-stu-id="8145d-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




