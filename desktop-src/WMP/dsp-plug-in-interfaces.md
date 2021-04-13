---
title: DSP-Plug-in-Schnittstellen
description: DSP-Plug-in-Schnittstellen
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player-Plug-ins, DSP-Schnittstellen
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, DSP-Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, ispecifypropertypage-Schnittstelle
- DSP-Plug-ins, Schnittstellen
- DSP-Plug-ins, ispecifypropertypage-Schnittstelle
- Schnittstellen, DSP-Plug-ins
- Ispecifypropertypage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390038"
---
# <a name="dsp-plug-in-interfaces"></a><span data-ttu-id="63ef7-113">DSP-Plug-in-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="63ef7-113">DSP Plug-in Interfaces</span></span>

<span data-ttu-id="63ef7-114">Die Plug-in-Schnittstellen (Digital Signal Processing, DSP) werden verwendet, um die Datenübertragung zwischen Windows Media Player und dem-Plug-in zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="63ef7-114">The digital signal processing (DSP) plug-in interfaces are used to manage data transfer between Windows Media Player and the plug-in.</span></span> <span data-ttu-id="63ef7-115">Alle DSP-Plug-Ins können optional die **ispecifypropertypage** -Schnittstelle implementieren, um eine Implementierung der Eigenschaften Seite bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="63ef7-115">All DSP plug-ins may optionally implement the **ISpecifyPropertyPage** interface to provide a property page implementation.</span></span>

<span data-ttu-id="63ef7-116">Zum Erstellen von DSP-Plug-ins sind die folgenden Schnittstellen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63ef7-116">The following interfaces are required for creating DSP plug-ins.</span></span>



| <span data-ttu-id="63ef7-117">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="63ef7-117">Interface</span></span>                                                | <span data-ttu-id="63ef7-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63ef7-118">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ef7-119">**Imediaobject**</span><span class="sxs-lookup"><span data-stu-id="63ef7-119">**IMediaObject**</span></span>                                         | <span data-ttu-id="63ef7-120">Verwaltet den Datenaustausch mit Windows Media Player und führt digitale Signalverarbeitungsaufgaben aus.</span><span class="sxs-lookup"><span data-stu-id="63ef7-120">Manages data exchange with Windows Media Player and performs digital signal processing tasks.</span></span> <span data-ttu-id="63ef7-121">Im DirectX SDK ist eine ausführliche Dokumentation enthalten.</span><span class="sxs-lookup"><span data-stu-id="63ef7-121">Detailed documentation is included with the DirectX SDK.</span></span> |
| [<span data-ttu-id="63ef7-122">Iwmpmediapluginregistrar</span><span class="sxs-lookup"><span data-stu-id="63ef7-122">IWMPMediaPluginRegistrar</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | <span data-ttu-id="63ef7-123">Verwaltet die Plug-in-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="63ef7-123">Manages plug-in registration.</span></span>                                                                                                                          |
| [<span data-ttu-id="63ef7-124">Iwmpplug-in</span><span class="sxs-lookup"><span data-stu-id="63ef7-124">IWMPPlugin</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | <span data-ttu-id="63ef7-125">Verwaltet die Verbindung mit Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="63ef7-125">Manages the connection to Windows Media Player.</span></span>                                                                                                        |
| [<span data-ttu-id="63ef7-126">Iwmppluginenable</span><span class="sxs-lookup"><span data-stu-id="63ef7-126">IWMPPluginEnable</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | <span data-ttu-id="63ef7-127">Speichert, ob das Plug-in derzeit von Windows Media Player aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="63ef7-127">Stores whether the plug-in is currently enabled by Windows Media Player.</span></span>                                                                               |
| [<span data-ttu-id="63ef7-128">Iwmpservices</span><span class="sxs-lookup"><span data-stu-id="63ef7-128">IWMPServices</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | <span data-ttu-id="63ef7-129">Ruft Informationen über die aktuelle streamzeit und den streamzustand vom Player ab.</span><span class="sxs-lookup"><span data-stu-id="63ef7-129">Retrieves information from the Player about the current stream time and stream state.</span></span>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="63ef7-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63ef7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63ef7-131">**Programmier Referenz für DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="63ef7-131">**DSP Plug-ins Programming Reference**</span></span>](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




