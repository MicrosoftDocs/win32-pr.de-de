---
title: Mixarchitektur
description: Mixarchitektur
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- Multimedia-Audiodatei, Mixer-Architektur
- Audioarchitektur, Mixer-Architektur
- Audiomixer, Architektur
- Audiomixer, audiolinien
- audiolinien
- Audiomischungen, Steuerelemente
- Multimedia-Audiosteuer Elemente
- Audiodaten, Mixer-Steuerelemente
- Mixer, audiolinien
- Mixer, Architektur
- Mischungen, Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309932"
---
# <a name="mixer-architecture"></a><span data-ttu-id="bbd71-114">Mixarchitektur</span><span class="sxs-lookup"><span data-stu-id="bbd71-114">Mixer Architecture</span></span>

<span data-ttu-id="bbd71-115">Das grundlegende Element der mixerarchitektur ist eine *Audiolinie*.</span><span class="sxs-lookup"><span data-stu-id="bbd71-115">The basic element of the mixer architecture is an *audio line*.</span></span> <span data-ttu-id="bbd71-116">Eine Audiolinie besteht aus einem oder mehreren Kanälen von Daten, die aus einer einzelnen Quelle oder einer System Ressource stammen.</span><span class="sxs-lookup"><span data-stu-id="bbd71-116">An audio line consists of one or more channels of data originating from a single source or a system resource.</span></span> <span data-ttu-id="bbd71-117">Beispielsweise verfügt eine Stereo audiozeile über zwei Datenkanäle, aber Sie wird als einzelne Audiolinie betrachtet, da Sie aus einer einzelnen Quelle stammt.</span><span class="sxs-lookup"><span data-stu-id="bbd71-117">For example, a stereo audio line has two data channels, but it is considered a single audio line because it originates from a single source.</span></span>

<span data-ttu-id="bbd71-118">Die mixerarchitektur bietet Routing Dienste zum Verwalten von audiolinien auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="bbd71-118">The mixer architecture provides routing services to manage audio lines on a computer.</span></span> <span data-ttu-id="bbd71-119">Sie können die Routing Dienste verwenden, wenn Sie über ausreichend Hardware Geräte und Software Treiber verfügen.</span><span class="sxs-lookup"><span data-stu-id="bbd71-119">You can use the routing services if you have adequate hardware devices and software drivers installed.</span></span> <span data-ttu-id="bbd71-120">Die Mixer-Architektur ermöglicht es, dass mehrere audioquellzeilen einer einzelnen zielaudiozeile zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="bbd71-120">The mixer architecture allows several audio source lines to map to a single destination audio line.</span></span>

<span data-ttu-id="bbd71-121">Jeder Audiolinie können Mixer-Steuerelemente zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="bbd71-121">Each audio line can have mixer controls associated with it.</span></span> <span data-ttu-id="bbd71-122">Ein Mixer-Steuerelement kann je nach den Merkmalen der zugeordneten Audiolinie eine beliebige Anzahl von Funktionen (z. b. das Steuerelement Volume) ausführen.</span><span class="sxs-lookup"><span data-stu-id="bbd71-122">A mixer control can perform any number of functions (such as control volume), depending on the characteristics of the associated audio line.</span></span>

 

 




