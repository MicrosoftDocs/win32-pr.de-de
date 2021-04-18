---
title: Joystick Benachrichtigungs Meldungen
description: Joystick Benachrichtigungs Meldungen
ms.assetid: 9e8ccc1b-85a9-44bf-b561-6ad4c10cddd1
keywords:
- Joysticks, Benachrichtigungen
- Joysticks, Meldungen
- Joysticks, Position
- Joysticks, Schaltflächen
- MM_JOY1 Meldungen
- MM_JOY2 Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698f999dab49ea6684e9184f6ed5c46286518b97
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338173"
---
# <a name="joystick-notification-messages"></a><span data-ttu-id="fce72-109">Joystick Benachrichtigungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="fce72-109">Joystick Notification Messages</span></span>

<span data-ttu-id="fce72-110">Joystick Nachrichten benachrichtigen Ihre Anwendung, dass sich die Position eines Joysticks geändert hat oder eine der Schaltflächen den Status geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fce72-110">Joystick messages notify your application that a joystick has changed position or that one of its buttons has changed states.</span></span> <span data-ttu-id="fce72-111">Nachrichten, die mit mm \_ JOY1 beginnen, werden an die Funktion gesendet, wenn Ihre Anwendung mithilfe des Bezeichners JOYSTICKID1 Eingaben aus dem Joystick anfordert, und mm \_ JOY2-Nachrichten werden gesendet, wenn Ihre Anwendung Eingaben vom Joystick mithilfe des Bezeichners JOYSTICKID2 anfordert.</span><span class="sxs-lookup"><span data-stu-id="fce72-111">Messages beginning with MM\_JOY1 are sent to the function if your application requests input from the joystick using the identifier JOYSTICKID1, and MM\_JOY2 messages are sent if your application requests input from the joystick using the identifier JOYSTICKID2.</span></span>

<span data-ttu-id="fce72-112">In den Nachrichten in der folgenden Tabelle wird der Status der Joystick Schaltflächen identifiziert:</span><span class="sxs-lookup"><span data-stu-id="fce72-112">The messages in the following table identify the status of the joystick buttons:</span></span>



| <span data-ttu-id="fce72-113">`Message`</span><span class="sxs-lookup"><span data-stu-id="fce72-113">Message</span></span>                                         | <span data-ttu-id="fce72-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fce72-114">Description</span></span>                                                     |
|-------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="fce72-115">**MM \_ JOY1BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="fce72-115">**MM\_JOY1BUTTONDOWN**</span></span>](mm-joy1buttondown.md) | <span data-ttu-id="fce72-116">Eine Schaltfläche auf dem Joystick JOYSTICKID1 wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="fce72-116">A button on joystick JOYSTICKID1 has been pressed.</span></span>              |
| [<span data-ttu-id="fce72-117">**MM \_ JOY1BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="fce72-117">**MM\_JOY1BUTTONUP**</span></span>](mm-joy1buttonup.md)     | <span data-ttu-id="fce72-118">Eine Schaltfläche auf dem Joystick JOYSTICKID1 wurde freigegeben.</span><span class="sxs-lookup"><span data-stu-id="fce72-118">A button on joystick JOYSTICKID1 has been released.</span></span>             |
| [<span data-ttu-id="fce72-119">**MM \_ JOY1MOVE**</span><span class="sxs-lookup"><span data-stu-id="fce72-119">**MM\_JOY1MOVE**</span></span>](mm-joy1move.md)             | <span data-ttu-id="fce72-120">Joystick JOYSTICKID1 geänderte Position in der x-oder y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="fce72-120">Joystick JOYSTICKID1 changed position in the x- or y-direction.</span></span> |
| [<span data-ttu-id="fce72-121">**MM \_ JOY1ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="fce72-121">**MM\_JOY1ZMOVE**</span></span>](mm-joy1zmove.md)           | <span data-ttu-id="fce72-122">Joystick JOYSTICKID1 geänderte Position in z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="fce72-122">Joystick JOYSTICKID1 changed position in the z-direction.</span></span>       |
| [<span data-ttu-id="fce72-123">**MM \_ JOY2BUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="fce72-123">**MM\_JOY2BUTTONDOWN**</span></span>](mm-joy2buttondown.md) | <span data-ttu-id="fce72-124">Eine Schaltfläche auf dem Joystick JOYSTICKID2 wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="fce72-124">A button on joystick JOYSTICKID2 has been pressed.</span></span>              |
| [<span data-ttu-id="fce72-125">**MM \_ JOY2BUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="fce72-125">**MM\_JOY2BUTTONUP**</span></span>](mm-joy2buttonup.md)     | <span data-ttu-id="fce72-126">Eine Schaltfläche auf dem Joystick JOYSTICKID2 wurde freigegeben.</span><span class="sxs-lookup"><span data-stu-id="fce72-126">A button on joystick JOYSTICKID2 has been released.</span></span>             |
| [<span data-ttu-id="fce72-127">**MM \_ JOY2MOVE**</span><span class="sxs-lookup"><span data-stu-id="fce72-127">**MM\_JOY2MOVE**</span></span>](mm-joy2move.md)             | <span data-ttu-id="fce72-128">Joystick JOYSTICKID2 geänderte Position in der x-oder y-Richtung</span><span class="sxs-lookup"><span data-stu-id="fce72-128">Joystick JOYSTICKID2 changed position in the x- or y-direction</span></span>  |
| [<span data-ttu-id="fce72-129">**MM \_ JOY2ZMOVE**</span><span class="sxs-lookup"><span data-stu-id="fce72-129">**MM\_JOY2ZMOVE**</span></span>](mm-joy2zmove.md)           | <span data-ttu-id="fce72-130">Joystick JOYSTICKID2 geänderte Position in z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="fce72-130">Joystick JOYSTICKID2 changed position in the z-direction.</span></span>       |



 

<span data-ttu-id="fce72-131">Alle Nachrichten melden nicht vorhandene Schaltflächen als freigegeben.</span><span class="sxs-lookup"><span data-stu-id="fce72-131">All messages report nonexistent buttons as released.</span></span>

 

 




