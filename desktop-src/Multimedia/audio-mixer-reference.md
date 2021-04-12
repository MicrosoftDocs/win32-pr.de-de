---
title: Audiomischreferenz
description: Audiomischreferenz
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- Multimedia-Audiodaten, Audiomixer
- Audiodaten, Audiomixer
- Multimedia-Audiodatei, Mixer-Referenz
- Audiodatei, Mixer-Referenz
- Audiomixer, Referenz
- Mixer, Referenz
- Referenz für Audiomixer, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104209186"
---
# <a name="audio-mixer-reference"></a><span data-ttu-id="1a928-110">Audiomischreferenz</span><span class="sxs-lookup"><span data-stu-id="1a928-110">Audio Mixer Reference</span></span>

<span data-ttu-id="1a928-111">In diesem Abschnitt werden die Funktionen, Strukturen und Meldungen beschrieben, die audiomixern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="1a928-111">This section describes the functions, structures, and messages associated with audio mixers.</span></span> <span data-ttu-id="1a928-112">Diese Elemente werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="1a928-112">These elements are grouped as follows.</span></span>

## <a name="querying-devices"></a><span data-ttu-id="1a928-113">Abfragen von Geräten</span><span class="sxs-lookup"><span data-stu-id="1a928-113">Querying Devices</span></span>

-   [<span data-ttu-id="1a928-114">**Mixercaps**</span><span class="sxs-lookup"><span data-stu-id="1a928-114">**MIXERCAPS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [<span data-ttu-id="1a928-115">**mixergetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="1a928-115">**mixerGetDevCaps**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [<span data-ttu-id="1a928-116">**mixergetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="1a928-116">**mixerGetNumDevs**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a><span data-ttu-id="1a928-117">Öffnen und schließen</span><span class="sxs-lookup"><span data-stu-id="1a928-117">Opening and Closing</span></span>

-   [<span data-ttu-id="1a928-118">**mixerclose**</span><span class="sxs-lookup"><span data-stu-id="1a928-118">**mixerClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [<span data-ttu-id="1a928-119">**mixeropen**</span><span class="sxs-lookup"><span data-stu-id="1a928-119">**mixerOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a><span data-ttu-id="1a928-120">Abrufen von Mixer-bezeichlern</span><span class="sxs-lookup"><span data-stu-id="1a928-120">Retrieving Mixer Identifiers</span></span>

-   [<span data-ttu-id="1a928-121">**mixergetid**</span><span class="sxs-lookup"><span data-stu-id="1a928-121">**mixerGetID**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a><span data-ttu-id="1a928-122">Abrufen von Linien Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="1a928-122">Retrieving Line Controls</span></span>

-   [<span data-ttu-id="1a928-123">**Mixercontrol**</span><span class="sxs-lookup"><span data-stu-id="1a928-123">**MIXERCONTROL**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [<span data-ttu-id="1a928-124">**mixergetlinecontrols**</span><span class="sxs-lookup"><span data-stu-id="1a928-124">**mixerGetLineControls**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [<span data-ttu-id="1a928-125">**Mixerlinecontrols**</span><span class="sxs-lookup"><span data-stu-id="1a928-125">**MIXERLINECONTROLS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a><span data-ttu-id="1a928-126">Ändern von Steuerelement Attributen</span><span class="sxs-lookup"><span data-stu-id="1a928-126">Changing Control Attributes</span></span>

-   [<span data-ttu-id="1a928-127">**Mixercontroldetails**</span><span class="sxs-lookup"><span data-stu-id="1a928-127">**MIXERCONTROLDETAILS**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   <span data-ttu-id="1a928-128">[**mixercontroldetails \_ boolescher Wert**](/previous-versions//dd757295(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a928-128">[**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85))</span></span>
-   <span data-ttu-id="1a928-129">[**mixercontroldetails- \_ listtext**](/previous-versions//dd757296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a928-129">[**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85))</span></span>
-   <span data-ttu-id="1a928-130">[**mixercontroldetails \_ signiert**](/previous-versions//dd757297(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a928-130">[**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85))</span></span>
-   <span data-ttu-id="1a928-131">[**mixercontroldetails \_ ohne Vorzeichen**](/previous-versions//dd757298(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a928-131">[**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85))</span></span>
-   [<span data-ttu-id="1a928-132">**mixergetcontroldetails**</span><span class="sxs-lookup"><span data-stu-id="1a928-132">**mixerGetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [<span data-ttu-id="1a928-133">**mixersetcontroldetails**</span><span class="sxs-lookup"><span data-stu-id="1a928-133">**mixerSetControlDetails**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a><span data-ttu-id="1a928-134">Abrufen von Zeilen Informationen</span><span class="sxs-lookup"><span data-stu-id="1a928-134">Retrieving Line Information</span></span>

-   [<span data-ttu-id="1a928-135">**mixergetlineingefo**</span><span class="sxs-lookup"><span data-stu-id="1a928-135">**mixerGetLineInfo**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [<span data-ttu-id="1a928-136">**Mixerline**</span><span class="sxs-lookup"><span data-stu-id="1a928-136">**MIXERLINE**</span></span>](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [<span data-ttu-id="1a928-137">**Änderung des mm \_ mixm- \_ Steuer Elements \_**</span><span class="sxs-lookup"><span data-stu-id="1a928-137">**MM\_MIXM\_CONTROL\_CHANGE**</span></span>](mm-mixm-control-change.md)
-   [<span data-ttu-id="1a928-138">**MM- \_ mixm- \_ Zeilen \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="1a928-138">**MM\_MIXM\_LINE\_CHANGE**</span></span>](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a><span data-ttu-id="1a928-139">Senden von User-Defined Nachrichten</span><span class="sxs-lookup"><span data-stu-id="1a928-139">Sending User-Defined Messages</span></span>

-   [<span data-ttu-id="1a928-140">**mixermessage**</span><span class="sxs-lookup"><span data-stu-id="1a928-140">**mixerMessage**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a><span data-ttu-id="1a928-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a928-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a928-142">Audiomischreferenz</span><span class="sxs-lookup"><span data-stu-id="1a928-142">Audio Mixer Reference</span></span>](audio-mixer-reference.md)
</dt> </dl>

 

 