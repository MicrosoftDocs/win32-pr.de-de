---
title: Joystick Referenz
description: Joystick Referenz
ms.assetid: c2ad092f-a0c5-4e28-ada7-227dc52c3c83
keywords:
- Windows Multimedia, Joystick Referenz
- Multimedia, Joystick Referenz
- Multimedia-Eingabe, Joystick Referenz
- Joysticks, Referenz
- Verweis für Joysticks, Informationen zu
- Joystick Referenz, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242f3fb21f9da9b1853ae8e9e7f694b9ad3bf711
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858179"
---
# <a name="joystick-reference"></a><span data-ttu-id="eea02-109">Joystick Referenz</span><span class="sxs-lookup"><span data-stu-id="eea02-109">Joystick Reference</span></span>

<span data-ttu-id="eea02-110">In diesem Abschnitt werden die Funktionen, Strukturen und Meldungen beschrieben, die mit Joysticks verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="eea02-110">This section describes the functions, structures, and messages associated with joysticks.</span></span> <span data-ttu-id="eea02-111">Die Elemente werden wie folgt gruppiert:</span><span class="sxs-lookup"><span data-stu-id="eea02-111">The elements are grouped as follows:</span></span>

## <a name="device-capabilities"></a><span data-ttu-id="eea02-112">Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="eea02-112">Device Capabilities</span></span>

-   [<span data-ttu-id="eea02-113">**joygetdevcaps**</span><span class="sxs-lookup"><span data-stu-id="eea02-113">**joyGetDevCaps**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps)
-   [<span data-ttu-id="eea02-114">**joygetnumentvs**</span><span class="sxs-lookup"><span data-stu-id="eea02-114">**joyGetNumDevs**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs)
-   [<span data-ttu-id="eea02-115">**JOYCAPS**</span><span class="sxs-lookup"><span data-stu-id="eea02-115">**JOYCAPS**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joycaps)

## <a name="querying-a-joystick"></a><span data-ttu-id="eea02-116">Abfragen eines Joysticks</span><span class="sxs-lookup"><span data-stu-id="eea02-116">Querying a Joystick</span></span>

-   [<span data-ttu-id="eea02-117">**joyconfigchanged**</span><span class="sxs-lookup"><span data-stu-id="eea02-117">**joyConfigChanged**</span></span>](/windows/desktop/api/joystickapi/nf-joystickapi-joyconfigchanged)
-   [<span data-ttu-id="eea02-118">**joygetpos**</span><span class="sxs-lookup"><span data-stu-id="eea02-118">**joyGetPos**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos)
-   [<span data-ttu-id="eea02-119">**"joygetposex"**</span><span class="sxs-lookup"><span data-stu-id="eea02-119">**joyGetPosEx**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetposex)
-   [<span data-ttu-id="eea02-120">**Joyinfo**</span><span class="sxs-lookup"><span data-stu-id="eea02-120">**JOYINFO**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfo)
-   [<span data-ttu-id="eea02-121">**Joyinfoex**</span><span class="sxs-lookup"><span data-stu-id="eea02-121">**JOYINFOEX**</span></span>](/windows/win32/api/joystickapi/ns-joystickapi-joyinfoex)

## <a name="capturing-a-joystick"></a><span data-ttu-id="eea02-122">Erfassen eines Joysticks</span><span class="sxs-lookup"><span data-stu-id="eea02-122">Capturing a Joystick</span></span>

-   [<span data-ttu-id="eea02-123">**joygetthreshold**</span><span class="sxs-lookup"><span data-stu-id="eea02-123">**joyGetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joygetthreshold)
-   [<span data-ttu-id="eea02-124">**joyreleasecapture**</span><span class="sxs-lookup"><span data-stu-id="eea02-124">**joyReleaseCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joyreleasecapture)
-   [<span data-ttu-id="eea02-125">**joysetcapture**</span><span class="sxs-lookup"><span data-stu-id="eea02-125">**joySetCapture**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture)
-   [<span data-ttu-id="eea02-126">**joysetthreshold**</span><span class="sxs-lookup"><span data-stu-id="eea02-126">**joySetThreshold**</span></span>](/windows/win32/api/joystickapi/nf-joystickapi-joysetthreshold)
-   [<span data-ttu-id="eea02-127">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="eea02-127">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md)
-   [<span data-ttu-id="eea02-128">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="eea02-128">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)
-   [<span data-ttu-id="eea02-129">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="eea02-129">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)
-   [<span data-ttu-id="eea02-130">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="eea02-130">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)
-   [<span data-ttu-id="eea02-131">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="eea02-131">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md)
-   [<span data-ttu-id="eea02-132">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="eea02-132">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)
-   [<span data-ttu-id="eea02-133">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="eea02-133">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)
-   [<span data-ttu-id="eea02-134">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="eea02-134">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)

## <a name="related-topics"></a><span data-ttu-id="eea02-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eea02-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eea02-136">Joystick</span><span class="sxs-lookup"><span data-stu-id="eea02-136">Joysticks</span></span>](joysticks.md)
</dt> </dl>

 

 