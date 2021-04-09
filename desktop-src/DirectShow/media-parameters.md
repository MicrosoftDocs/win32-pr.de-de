---
description: Medien Parameter
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Medien Parameter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869472"
---
# <a name="media-parameters"></a><span data-ttu-id="1ad4a-103">Medien Parameter</span><span class="sxs-lookup"><span data-stu-id="1ad4a-103">Media Parameters</span></span>

<span data-ttu-id="1ad4a-104">Mithilfe von Medien Parametern kann eine Anwendung die Eigenschaften eines Objekts so konfigurieren, dass Sie sich im Laufe der Zeit auf mathematisch deterministische Weise ändern.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-104">Media parameters enable an application to configure an object's properties so that they change over time in a mathematically deterministic way.</span></span>

<span data-ttu-id="1ad4a-105">Nehmen wir beispielsweise an, dass ein Sound Techniker ein digitales Master Band vermischt und eine geringfügige Verzögerung auf einen Vokal Abschnitt anwenden möchte, um den Sound auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-105">For example, suppose that a sound engineer is mixing a digital master tape and wants to apply a slight delay to a vocal section, to fill out the sound.</span></span> <span data-ttu-id="1ad4a-106">Der Effekt wird als jarringvorgang verwendet, wenn die Verzögerung plötzlich reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-106">The effect will be jarring if the delay cuts in abruptly.</span></span> <span data-ttu-id="1ad4a-107">Stattdessen sollte der Effekt 100 Prozent trocken (keine Verzögerung) beginnen, und die nasse/trockene Mischung sollte allmählich erhöht werden, bis die gewünschte Ebene erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-107">Instead, the effect should begin 100 percent dry (no delay), and the wet/dry mix should increase gradually until it reaches the desired level.</span></span> <span data-ttu-id="1ad4a-108">Außerdem sollte dieser Übergang eine glatte Kurve oder eine lineare Fortsetzung nach sich ziehen.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-108">Moreover, this transition should follow a smooth curve or linear progression.</span></span> <span data-ttu-id="1ad4a-109">Zur Unterstützung dieses Szenarios kann ein DMO die folgenden Schnittstellen verfügbar machen:</span><span class="sxs-lookup"><span data-stu-id="1ad4a-109">To support this scenario, a DMO can expose the following interfaces:</span></span>

-   <span data-ttu-id="1ad4a-110">[**Imediaparaminfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) enthält Methoden zum Ermitteln von Informationen zu den unterstützten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-110">[**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contains methods for discovering information about the supported properties.</span></span> <span data-ttu-id="1ad4a-111">In der Regel ruft der Client diese Methoden auf, bevor er mit dem Streamen von Daten beginnt.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-111">Typically, the client will call these methods before it begins to stream data.</span></span>
-   <span data-ttu-id="1ad4a-112">[**Imediaparams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) enthalten Methoden zum Festlegen der Kurven, die ein Parameter beim Streaming befolgt.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-112">[**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contain methods for setting the curves that a parameter will follow during streaming.</span></span>

<span data-ttu-id="1ad4a-113">Diese Schnittstellen sind hauptsächlich für DMOS konzipiert, aber jedes Objekt kann Sie unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-113">These interfaces are designed primarily for DMOs, but any object can support them.</span></span> <span data-ttu-id="1ad4a-114">In diesem Abschnitt bezieht sich der Begriffs *Parameter* auf eine beliebige Eigenschaft, die diese beiden Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ad4a-114">Within this section, the term *parameter* refers to any property that supports these two interfaces.</span></span>

<span data-ttu-id="1ad4a-115">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="1ad4a-115">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1ad4a-116">Parameter Kurven</span><span class="sxs-lookup"><span data-stu-id="1ad4a-116">Parameter Curves</span></span>](parameter-curves.md)
-   [<span data-ttu-id="1ad4a-117">Parameter Informationen</span><span class="sxs-lookup"><span data-stu-id="1ad4a-117">Parameter Information</span></span>](parameter-information.md)
-   [<span data-ttu-id="1ad4a-118">Umschlag Segmente</span><span class="sxs-lookup"><span data-stu-id="1ad4a-118">Envelope Segments</span></span>](envelope-segments.md)
-   [<span data-ttu-id="1ad4a-119">Berechnen von Parameter Werten</span><span class="sxs-lookup"><span data-stu-id="1ad4a-119">Calculating Parameter Values</span></span>](calculating-parameter-values.md)

## <a name="related-topics"></a><span data-ttu-id="1ad4a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ad4a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ad4a-121">DirectX-Medienobjekte</span><span class="sxs-lookup"><span data-stu-id="1ad4a-121">DirectX Media Objects</span></span>](directx-media-objects.md)
</dt> </dl>

 

 



