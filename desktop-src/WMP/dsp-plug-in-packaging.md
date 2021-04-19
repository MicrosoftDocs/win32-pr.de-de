---
title: Plug-in-Paket für DSP
description: Plug-in-Paket für DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player-Plug-ins, Media Foundation Pipeline
- Plug-ins, Media Foundation Pipeline
- Plug-Ins für die digitale Signalverarbeitung, Media Foundation Pipeline
- DSP-Plug-ins, Media Foundation Pipeline
- Media Foundation Pipeline
- Windows Media Player-Plug-ins, DirectShow-Pipeline
- Plug-ins, DirectShow-Pipeline
- Plug-Ins für die digitale Signalverarbeitung, DirectShow-Pipeline
- DSP-Plug-ins, DirectShow-Pipeline
- DirectShow-Pipeline
- Plug-Ins für die digitale Signalverarbeitung, Basic
- DSP-Plug-ins, Basic
- Windows Media Player-Plug-ins, Basic DSP
- Plug-ins, Basic DSP
- grundlegende DSP-Plug-ins
- Windows Media Player-Plug-ins, Dual-Modus-DSP
- Plug-ins, im Dual-Modus-DSP
- Plug-Ins für die digitale Signalverarbeitung, Dual-Mode
- DSP-Plug-ins, Dual-Mode
- Dual-Modus-DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339079"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="82bde-123">Plug-in-Paket für DSP</span><span class="sxs-lookup"><span data-stu-id="82bde-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="82bde-124">Windows Media Player rendert Audiodaten und Videos mithilfe einer der folgenden Pipelines.</span><span class="sxs-lookup"><span data-stu-id="82bde-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="82bde-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="82bde-125">DirectShow</span></span>
-   <span data-ttu-id="82bde-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82bde-126">Media Foundation</span></span>

<span data-ttu-id="82bde-127">In Microsoft Windows XP und früheren Versionen verwendet der Player DirectShow.</span><span class="sxs-lookup"><span data-stu-id="82bde-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="82bde-128">In Windows Vista verwendet der Player manchmal DirectShow und verwendet manchmal Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="82bde-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="82bde-129">Ein DSP-Plug-in, das in der DirectShow-Pipeline ausgeführt werden soll, wird als *einfaches DSP-Plug-in* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="82bde-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="82bde-130">Grundlegende DSP-Plug-ins fungieren als DirectX-Medienobjekt (DMO).</span><span class="sxs-lookup"><span data-stu-id="82bde-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="82bde-131">Ein einfaches DSP-Plug-in kann nativ in der DirectShow-Pipeline ausgeführt werden und kann auch in der Media Foundation Pipeline innerhalb eines von Media Foundation bereitgestellten Wrappers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="82bde-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="82bde-132">Ein DSP-Plug-in, das für die systemeigene (kein Wrapper erforderlich) in den DirectShow-und Media Foundation-Pipelines entwickelt wurde, wird als *Plug-in für das Dual-Modus-DSP* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="82bde-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="82bde-133">Ein bidirektionales DSP-Plug-in kann als DMO oder als Media Foundation Transformation (MFT) fungieren.</span><span class="sxs-lookup"><span data-stu-id="82bde-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="82bde-134">Ein DSP-Plug-in ist ein COM-Objekt, das als selbst registrierte DLL-Datei verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="82bde-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="82bde-135">Die Schnittstellen, die das Plug-in implementiert, hängen davon ab, ob das Plug-in als einfaches DSP-Plug-in oder als ein bidirektionales DSP-Plug-in entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="82bde-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="82bde-136">Ausführliche Informationen zu den Schnittstellen, die von DSP-Plug-Ins implementiert werden müssen, finden Sie unter [erforderliche Schnittstellen](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="82bde-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="82bde-137">Ein DSP-Plug-in, das in der Media Foundation Pipeline (System intern oder umschließt) ausgeführt wird, muss sein Threading Modell als "beides" registrieren.</span><span class="sxs-lookup"><span data-stu-id="82bde-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="82bde-138">Ausführliche Informationen zu Registrierungs unter Schlüsseln und Einträgen, die DSP-Plug-ins zugeordnet sind, finden Sie unter [Registrieren von DSP-Plug-ins](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="82bde-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="82bde-139">Ein DSP-Plug-in, das benutzerdefinierte Schnittstellen implementiert und in der Media Foundation Pipeline (nativ oder umschließt) ausgeführt wird, muss mit einer Proxy-Stub. dll-Datei gekoppelt werden, die die benutzerdefinierten Schnittstellen über Prozess Grenzen hinweg Mars Hallen kann.</span><span class="sxs-lookup"><span data-stu-id="82bde-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="82bde-140">Weitere Informationen zur Proxy-Stub-Komponente finden Sie unter [Aktualisieren vorhandener DSP-Plug-ins](updating-existing-dsp-plug-ins.md) und [Updates des DSP-Plug-in-Assistenten für Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="82bde-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="82bde-141">DSP-Plug-in-Objekte dürfen nicht als Singletons erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="82bde-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="82bde-142">Windows Media Player muss mehrere separate Instanzen eines bestimmten DSP-Plug-ins erstellen können.</span><span class="sxs-lookup"><span data-stu-id="82bde-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="82bde-143">DSP-Plug-ins, die im Windows Vista-PMP (geschützter Medien Pfad) ausgeführt werden, müssen signiert sein.</span><span class="sxs-lookup"><span data-stu-id="82bde-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="82bde-144">Weitere Informationen finden Sie unter [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="82bde-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82bde-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82bde-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82bde-146">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="82bde-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 