---
title: Updates des DSP-Plug-in-Assistenten für Windows Media Player 11
description: Updates des DSP-Plug-in-Assistenten für Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Plug-ins, Plug-in-Assistent
- Plug-Ins für die digitale Signalverarbeitung, Plug-in-Assistent
- DSP-Plug-ins, Plug-in-Assistent
- Plug-in-Assistent
- Visual Studio, DSP-Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389879"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="c52ce-109">Updates des DSP-Plug-in-Assistenten für Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="c52ce-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="c52ce-110">Das Windows Media Player 11 SDK führt die folgenden Änderungen am DSP-Plug-in-Assistenten ein:</span><span class="sxs-lookup"><span data-stu-id="c52ce-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="c52ce-111">Plug-Ins registrieren das Threading Modell als "both".</span><span class="sxs-lookup"><span data-stu-id="c52ce-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="c52ce-112">Dadurch kann das Plug-in in der Media Foundation Pipeline unter Windows Vista ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c52ce-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="c52ce-113">Weitere Informationen finden Sie in der Datei *ProjectName*. rgs.</span><span class="sxs-lookup"><span data-stu-id="c52ce-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="c52ce-114">Audiodsp-Plug-ins haben Unterstützung für die folgenden zwei zusätzlichen Formate:</span><span class="sxs-lookup"><span data-stu-id="c52ce-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="c52ce-115">"Wave \_ Format \_ IEEE \_ float"</span><span class="sxs-lookup"><span data-stu-id="c52ce-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="c52ce-116">Das Wave- \_ Format ist \_ erweiterbar mit dem unter Format "ksdataformat"- \_ Untertyp \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="c52ce-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="c52ce-117">Weitere Informationen finden Sie in der Datei *ProjectName*. cpp.</span><span class="sxs-lookup"><span data-stu-id="c52ce-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="c52ce-118">Video DSP-Plug-ins haben Unterstützung für das Videoformat NV12.</span><span class="sxs-lookup"><span data-stu-id="c52ce-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="c52ce-119">Plug-ins führen zusätzliche Aufrufe an [iwmpmediapluginregistrar:: wmpregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) und [iwmpmediapluginregistrar:: wmpunregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) durch einen neuen Plug-in-Typ aus: WMP \_ PlugInType \_ DSP \_ oudefproc.</span><span class="sxs-lookup"><span data-stu-id="c52ce-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="c52ce-120">Weitere Informationen finden Sie in der Projektdatei *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="c52ce-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="c52ce-121">Ein zusätzliches Projekt in jeder Projekt Mappe erstellt eine Proxy-/Stub-DLL für die benutzerdefinierte Schnittstelle der Eigenschaften Seiteneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="c52ce-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="c52ce-122">Weitere Informationen finden Sie Unterprojekt *Name* .</span><span class="sxs-lookup"><span data-stu-id="c52ce-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="c52ce-123">Aufrufe von veralteten Methoden wurden geändert, um die neuesten Versionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c52ce-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="c52ce-124">Der Assistent kann ein Dual-Mode-Plug-in generieren, das sowohl als DMO als auch durch Implementieren von **imediaobject** und als MFT durch Implementieren von **imftransform** funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c52ce-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c52ce-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c52ce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c52ce-126">**DSP-Plug-in-Assistent**</span><span class="sxs-lookup"><span data-stu-id="c52ce-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




