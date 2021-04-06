---
title: Informationen zu iwmppluginenable
description: Informationen zu iwmppluginenable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, iwmppluginenable-Schnittstelle
- Plug-ins, iwmppluginenable-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, iwmppluginenable-Schnittstelle
- DSP-Plug-ins, iwmppluginenable-Schnittstelle
- Iwmppluginenable-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947441"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="1a0f1-113">Informationen zu iwmppluginenable</span><span class="sxs-lookup"><span data-stu-id="1a0f1-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="1a0f1-114">Die **iwmppluginenable** -Schnittstelle ist für Windows Media Player DSP-Plug-Ins erforderlich. **Iwmppluginenable** enthält zwei Methoden, mit denen gespeichert wird, ob Windows Media Player das DSP-Plug-in aktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="1a0f1-115">Windows Media Player ruft **iwmppluginenable:: abtenable** auf, wenn eine Instanz des DSP-Plug-Ins erstellt wird. dabei wird der Wert **true** übergeben, wenn das Plug-in aktiviert wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1a0f1-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="1a0f1-116">DSP-Plug-ins bleiben möglicherweise auch dann geladen, wenn der Benutzer Sie deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="1a0f1-117">Wenn diese Option deaktiviert ist, muss ein Plug-in Daten aus dem Eingabepuffer in den Ausgabepuffer kopieren und damit nur die Formatierung der Formatierungs Verarbeitung durchführen.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="1a0f1-118">Außerdem ruft Windows Media Player diese Methode auf, bevor Sie eine Instanz des DSP-Plug-ins freigibt.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="1a0f1-119">Dies ist hilfreich, damit Clients des Plug-ins überprüfen können, ob das Plug-in derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="1a0f1-120">Beispielsweise kann ein Benutzeroberflächen-Plug-in die Darstellung der Steuerelemente ändern, um den Benutzer darüber zu benachrichtigen, dass das DSP-Plug-in nicht verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1a0f1-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a0f1-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a0f1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a0f1-122">**Erforderliche Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="1a0f1-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




