---
title: Ändern der Eigenschaften Seite Echo Sample
description: Ändern der Eigenschaften Seite Echo Sample
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388185"
---
# <a name="modifying-the-echo-sample-property-page"></a><span data-ttu-id="71bd5-108">Ändern der Eigenschaften Seite Echo Sample</span><span class="sxs-lookup"><span data-stu-id="71bd5-108">Modifying the Echo Sample Property Page</span></span>

<span data-ttu-id="71bd5-109">Die Standard Implementierung der Eigenschaften Seite, die vom Windows Media Player Plug-in-Assistenten DSP-Plug-in-Beispiel bereitgestellt wird, enthält ein einzelnes Bearbeitungsfeld-Steuerelement, das den Skalierungsfaktor des Benutzers empfängt.</span><span class="sxs-lookup"><span data-stu-id="71bd5-109">The default property page implementation provided by the Windows Media Player Plug-in Wizard DSP plug-in sample contains a single edit box control that receives the scale factor from the user.</span></span> <span data-ttu-id="71bd5-110">Sie müssen die Eigenschaften Seite ändern, damit die beiden vom Echo-Beispiel verwendeten Eigenschaftswerte empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="71bd5-110">You need to modify the property page to receive the two property values used by the Echo sample.</span></span>

<span data-ttu-id="71bd5-111">Eine Übersicht über die Eigenschaften Seiten des DSP-Plug-Ins finden Sie unter [Implementieren eines audiodsp-Plug-ins](implementing-an-audio-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="71bd5-111">For an overview of DSP plug-in property pages, see [Implementing an Audio DSP Plug-in](implementing-an-audio-dsp-plug-in.md).</span></span>

<span data-ttu-id="71bd5-112">In den folgenden Abschnitten wird Schritt für Schritt erläutert, wie Sie die Beispiel Eigenschaften Seite ändern:</span><span class="sxs-lookup"><span data-stu-id="71bd5-112">The following sections step you through the process of modifying the sample property page:</span></span>

-   [<span data-ttu-id="71bd5-113">Ändern der Echo Dialog-Ressource</span><span class="sxs-lookup"><span data-stu-id="71bd5-113">Modifying the Echo Dialog Resource</span></span>](modifying-the-echo-dialog-resource.md)
-   [<span data-ttu-id="71bd5-114">Hinzufügen und Ändern der Ereignisse</span><span class="sxs-lookup"><span data-stu-id="71bd5-114">Adding and Modifying the Events</span></span>](adding-and-modifying-the-events.md)
-   [<span data-ttu-id="71bd5-115">So speichert das Echo Beispiel Daten</span><span class="sxs-lookup"><span data-stu-id="71bd5-115">How the Echo Sample Persists Data</span></span>](how-the-echo-sample-persists-data.md)
-   [<span data-ttu-id="71bd5-116">Implementieren von cechoproppage:: OnInitDialog</span><span class="sxs-lookup"><span data-stu-id="71bd5-116">Implementing CEchoPropPage::OnInitDialog</span></span>](implementing-cechoproppage--oninitdialog.md)
-   [<span data-ttu-id="71bd5-117">Implementieren von cechoproppage:: apply</span><span class="sxs-lookup"><span data-stu-id="71bd5-117">Implementing CEchoPropPage::Apply</span></span>](implementing-cechoproppage--apply.md)
-   [<span data-ttu-id="71bd5-118">Implementieren von Cecho:: FinalConstruct</span><span class="sxs-lookup"><span data-stu-id="71bd5-118">Implementing CEcho::FinalConstruct</span></span>](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a><span data-ttu-id="71bd5-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71bd5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71bd5-120">**Das Echo-Beispiel**</span><span class="sxs-lookup"><span data-stu-id="71bd5-120">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




